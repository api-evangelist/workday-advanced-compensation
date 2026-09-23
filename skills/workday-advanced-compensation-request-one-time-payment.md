---
name: Request a one-time payment for a Workday worker
description: >-
  Find a worker in Workday, choose a valid one-time payment plan, and submit a one-time payment
  request against the compensation REST API — with the authorization, paging, error and
  irreversibility rules that actually apply.
api: openapi/_original/workday-advanced-compensation-compensation-v3-openapi.json
generated: '2026-09-17'
method: generated
source: openapi/_original/workday-advanced-compensation-compensation-v3-openapi.json
operations:
  - GET /workers
  - GET /workers/{ID}
  - GET /values/oneTimePaymentPlanGroup/oneTimePaymentPlan/
  - POST /workers/{ID}/requestOneTimePayment
---

# Request a one-time payment

Workday's published compensation specs declare **no operationIds**, so operations are addressed
here by method and path, exactly as the contract does.

## Before you start

- Base URL is tenant-specific: `https://<tenantHostname>/compensation/v3`. There is no shared
  host — substitute the customer's own Workday tenant hostname.
- Authenticate with OAuth 2.0. For server-to-server, register an API Client in the tenant and use
  Client Credentials bound to an Integration System User.
- The ISU must hold the security domains the operations name. The worker reads are scoped
  **Staffing**; the one-time payment request is scoped **Core Compensation**.
- **There is no sandbox.** Workday's own console marks `POST /workers/{ID}/requestOneTimePayment`
  as not try-enabled. The first time you run this flow it is against a real tenant.

## Steps

1. **Find the worker.** `GET /workers` with `search` to match by name, plus `limit` (default 20,
   max 100) and `offset` for paging. The response envelope is `{ total, data[] }`.
   Use `includeTerminatedWorkers` only when you mean it.
2. **Confirm the worker.** `GET /workers/{ID}` where `{ID}` is the 32-character Workday ID from
   step 1. The literal `me` resolves to the authenticated worker.
3. **Get the valid payment plans.** `GET /values/oneTimePaymentPlanGroup/oneTimePaymentPlan/`
   returns the prompt values. Do not hardcode a plan ID — plans are tenant configuration.
4. **Submit the request.** `POST /workers/{ID}/requestOneTimePayment` with the
   `oneTimePaymentPlanEventInput` body: the position, the one-time payment plan, the amount, the
   payment currency, a reason, and any payroll worktags. A 201 means the request was accepted.

## Rules that will bite you

- **This is not an idempotent call.** Workday publishes no idempotency key on any compensation
  write. If you retry after a timeout you may submit the payment twice. Record the 201 and the
  returned identifier before any retry, and never retry blind.
- **You cannot take it back through this API.** A 201 submits a Workday business process with
  approvals, delegation and an audit trail. There is no REST cancel, rescind or reverse operation.
  The reversal path that exists is `Correct_Compensation_Change` on the SOAP Compensation service,
  and no Workday document states a window for it.
- **429 and 500 are both back-pressure.** Workday throttles under tenant load and documents 429
  for REST. Retry with exponential back-off and cache. There are no `RateLimit-*` headers, so you
  get no warning before the rejection.
- **403 is a configuration problem, not a code problem.** It means the ISU's security groups do
  not carry the domain the operation requires.
- Errors are `application/json` shaped by `VALIDATION_ERROR_MODEL_REFERENCE` (4xx) or
  `ERROR_MODEL_REFERENCE` (default) — **not** RFC 9457 problem+json. Message text is explained at
  <https://community.workday.com/rest/error-messages>.
