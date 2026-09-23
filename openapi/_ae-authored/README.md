# Written by API Evangelist, not harvested from the provider

These documents were in `openapi/_original/`, which is the verbatim record of what the PROVIDER
published. They are not that. Each carries an explicit authorship marker — `x-derived-from`,
`x-generated-from: documentation`, or an AE-authored `x-method` — saying we built it.

The Kin Score credits the presence of `_original/` as evidence the provider published a contract,
and grades a marked document as `derived` separately. Leaving these where they were meant the same
file was discounted once and credited once.

Moved, not deleted: they describe real APIs and the pipeline reads them. The only thing wrong was
the claim their location made about who wrote them.

Moved 2026-08-29, roadmap#2 item 4 / roadmap#48.

---

**Update 2026-09-17.** The eight per-tag documents `refine-openapis` split out of the root
AE-authored spec were still sitting in `openapi/` proper and were still the only `type: OpenAPI`
pointers in `apis.yml`, so a document we wrote was standing in for the provider's contract. It
was also wrong on the facts: those files describe `/bonusPlans`, `/meritPlans`, `/stockPlans`,
`/compensationBudgets` and friends at `https://{tenant}.workday.com/api/compensation/v1`, and
Workday publishes no such REST endpoints.

The same enrichment pass found Workday's REAL first-party contracts, all served anonymously from
Workday's own hosts, and they are now in `openapi/_original/` and `wsdl/`:

- `compensation` v1/v2/v3, OpenAPI 3.0.1, from developer.workday.com — 14 operations on v3 over
  scorecards, scorecard results, workers and one-time payments. Twenty of the twenty-six
  operations across the three versions say `Scope: Advanced Compensation` in their own
  descriptions.
- `Compensation` and `Compensation_Review` Workday Web Services WSDLs (v47.0) from
  community.workday.com — 68 and 21 operations. This is where the Advanced Compensation
  capability set actually lives.

The eight split documents were moved here for the reason this directory exists: they are marked
`x-generated-from: documentation`, and their location was making a claim about authorship that
was not true.
