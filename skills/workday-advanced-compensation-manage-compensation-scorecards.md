---
name: Build and score a Workday compensation scorecard
description: >-
  Create a compensation scorecard with profiles, goals and eligibility rules, create a scorecard
  result, and patch scores onto it — the Advanced Compensation merit-and-bonus flow on Workday's
  compensation REST API.
api: openapi/_original/workday-advanced-compensation-compensation-v3-openapi.json
generated: '2026-09-17'
method: generated
source: openapi/_original/workday-advanced-compensation-compensation-v3-openapi.json
operations:
  - GET /scorecards
  - POST /scorecards
  - GET /scorecards/{ID}
  - PUT /scorecards/{ID}
  - DELETE /scorecards/{ID}
  - GET /scorecardResults
  - POST /scorecardResults
  - GET /scorecardResults/{ID}
  - PATCH /scorecardResults/{ID}/scores/{subresourceID}
  - DELETE /scorecardResults/{ID}
---

# Build and score a compensation scorecard

Every operation in this skill is scoped **Advanced Compensation** and secured by the Workday
domain **Set Up: Merit and Bonus**. If the calling Integration System User does not hold that
domain you get 403 on all ten.

## Steps

1. **See what exists.** `GET /scorecards` — `{ total, data[] }`, paged with `limit` (max 100) and
   `offset`.
2. **Create the scorecard.** `POST /scorecards` with the `createScorecard` body. A scorecard
   carries `scorecardProfiles[]`; each profile carries `profileScorecardGoals[]` and one
   `eligibilityRule`. Build the whole tree in one request — there is no sub-resource create for
   profiles or goals.
3. **Read it back.** `GET /scorecards/{ID}` with the 32-character Workday ID returned in step 2.
4. **Amend it.** `PUT /scorecards/{ID}` with `editScorecards`. This is a replace, not a merge —
   send the full object.
5. **Create the result.** `POST /scorecardResults` with `createScorecardResults`, referencing the
   scorecard by its Workday ID. The result holds a `scoreset` of scores against the goals.
6. **Score it.** `PATCH /scorecardResults/{ID}/scores/{subresourceID}` with `scoreInput`, where
   `{subresourceID}` is the score's own Workday ID from the result. One score per call.
7. **Review.** `GET /scorecardResults` and `GET /scorecardResults/{ID}`.

## Rules that will bite you

- **Deletes are real deletes.** `DELETE /scorecards/{ID}` and `DELETE /scorecardResults/{ID}`
  have no undo and no restore window in any published document. Read the object first and keep
  the payload if you might need it back.
- **No idempotency key.** Retrying `POST /scorecards` or `POST /scorecardResults` after a timeout
  creates a second object. Check with a `GET` before you retry.
- **Workday spells one schema two ways.** Both `eligibilityRule` and `eligibiltyRule` appear in
  Workday's own published component schemas. Match the spelling the specific request body uses.
- **IDs are opaque.** A Workday ID is 32 hex characters with no type prefix; you cannot tell a
  scorecard ID from a worker ID by looking at it. Carry the type alongside it.
- **Only reads are try-enabled.** Workday's console will not let you rehearse any of the five
  writes in this flow.
- Errors: 400/401/403/404 return `VALIDATION_ERROR_MODEL_REFERENCE`; the catalogue is at
  <https://community.workday.com/rest/error-messages>.
