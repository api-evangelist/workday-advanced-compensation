# Workday Advanced Compensation (workday-advanced-compensation)
API for managing compensation plans, budgets, allocations, and related processes in Workday.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/workday-advanced-compensation/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags:

 - Advanced Compensation, Bonuses, Compensation, Enterprise, HCM, HR, Merit, Payroll, Salary Planning, Stock Awards, Workday

## Timestamps

- **Created:** 2024-01-15
- **Modified:** 2026-05-03

## APIs

### Workday Advanced Compensation API
RESTful APIs for managing compensation plans, merit increases, bonuses, stock awards, compensation grades, budgets, and review processes in Workday. Enables organizations to programmatically manage their total compensation strategy, administer compensation cycles, and integrate compensation data with other systems.

**Human URL:** [https://community.workday.com/sites/default/files/file-hosting/productionapi/Compensation/v41.1/index.html](https://community.workday.com/sites/default/files/file-hosting/productionapi/Compensation/v41.1/index.html)


#### Tags:

 - Bonuses, Compensation, HR, Merit, Payroll, Salary Planning, Stock Awards

#### Properties

- [Documentation](https://community.workday.com/sites/default/files/file-hosting/productionapi/Compensation/v41.1/index.html)
- [OpenAPI](https://community.workday.com/sites/default/files/file-hosting/productionapi/Compensation/v41.1/Compensation.yaml)
- [Authentication](https://doc.workday.com/admin-guide/en-us/integration-security/securing-workday-web-services/authentication-types.html)
- [Versioning](https://doc.workday.com/r/Workday_Web_Services/Workday_Web_Services_Directory/About_Workday_Web_Services_Versioning)
- [OpenAPI](openapi/workday-advanced-compensation-openapi.yml)
- [JSONSchema](json-schema/workday-advanced-compensation-compensation-plan-schema.json)
- [JSONSchema](json-schema/workday-advanced-compensation-compensation-grade-schema.json)
- [JSONSchema](json-schema/workday-advanced-compensation-merit-plan-schema.json)
- [JSONSchema](json-schema/workday-advanced-compensation-bonus-plan-schema.json)
- [JSONSchema](json-schema/workday-advanced-compensation-stock-plan-schema.json)
- [JSONSchema](json-schema/workday-advanced-compensation-compensation-budget-schema.json)
- [JSONSchema](json-schema/workday-advanced-compensation-compensation-review-schema.json)
- [JSONSchema](json-schema/workday-advanced-compensation-employee-compensation-schema.json)
- [JSONSchema](json-schema/workday-advanced-compensation-compensation-change-request-schema.json)
- [NaftikoCapability - Compensation Management](capabilities/compensation-management.yaml)
- [NaftikoCapability - Advanced Compensation (Shared)](capabilities/shared/advanced-compensation.yaml)

## Common Properties

- [Developer Portal](https://developer.workday.com/)
- [API Status](https://status.workday.com/)
- [Terms of Service](https://www.workday.com/en-us/legal.html)
- [Privacy Policy](https://www.workday.com/en-us/privacy.html)
- [Security](https://www.workday.com/en-us/why-workday/security-trust.html)
- [Rate Limits](https://doc.workday.com/r/Workday_Web_Services/Workday_Web_Services_Directory/Web_Service_Rate_Limiting)
- [Sandbox Environment](https://doc.workday.com/r/en-us/workday-studio/workday-studio-user-guide/sandboxes)
- [SDKs](https://github.com/Workday)
- [JSON-LD](json-ld/workday-advanced-compensation-context.jsonld)
- [SpectralRules](rules/workday-advanced-compensation-spectral-rules.yml)
- [NaftikoCapability - Compensation Management](capabilities/compensation-management.yaml)
- [NaftikoCapability - Advanced Compensation (Shared)](capabilities/shared/advanced-compensation.yaml)
- [Vocabulary](vocabulary/workday-advanced-compensation-vocabulary.yml)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Workday Advanced Compensation API](openapi/workday-advanced-compensation-openapi.yml)

### JSON Schema

- [Compensation Plan](json-schema/workday-advanced-compensation-compensation-plan-schema.json)
- [Compensation Grade](json-schema/workday-advanced-compensation-compensation-grade-schema.json)
- [Merit Plan](json-schema/workday-advanced-compensation-merit-plan-schema.json)
- [Bonus Plan](json-schema/workday-advanced-compensation-bonus-plan-schema.json)
- [Stock Plan](json-schema/workday-advanced-compensation-stock-plan-schema.json)
- [Compensation Budget](json-schema/workday-advanced-compensation-compensation-budget-schema.json)
- [Compensation Review](json-schema/workday-advanced-compensation-compensation-review-schema.json)
- [Employee Compensation](json-schema/workday-advanced-compensation-employee-compensation-schema.json)
- [Compensation Change Request](json-schema/workday-advanced-compensation-compensation-change-request-schema.json)

### JSON Structure

- [Compensation Plan](json-structure/workday-advanced-compensation-compensation-plan-structure.json)
- [Compensation Grade](json-structure/workday-advanced-compensation-compensation-grade-structure.json)
- [Merit Plan](json-structure/workday-advanced-compensation-merit-plan-structure.json)
- [Bonus Plan](json-structure/workday-advanced-compensation-bonus-plan-structure.json)
- [Stock Plan](json-structure/workday-advanced-compensation-stock-plan-structure.json)
- [Compensation Budget](json-structure/workday-advanced-compensation-compensation-budget-structure.json)
- [Compensation Review](json-structure/workday-advanced-compensation-compensation-review-structure.json)
- [Employee Compensation](json-structure/workday-advanced-compensation-employee-compensation-structure.json)
- [Compensation Change Request](json-structure/workday-advanced-compensation-compensation-change-request-structure.json)

### JSON-LD

- [Workday Advanced Compensation Context](json-ld/workday-advanced-compensation-context.jsonld)

## Capabilities

Naftiko capabilities organized as shared per-API definitions composed into customer-facing workflows.

### Shared Per-API Definitions

- [Advanced Compensation](capabilities/shared/advanced-compensation.yaml) — 10 operations for compensation plan, grade, and employee compensation management

### Workflow Capabilities

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Compensation Management](capabilities/compensation-management.yaml) | Workday Advanced Compensation API | 12 | Compensation Analyst, HR Manager, Total Rewards Manager |

## Vocabulary

- [Workday Advanced Compensation Vocabulary](vocabulary/workday-advanced-compensation-vocabulary.yml) — Unified taxonomy mapping 8 resources, 4 actions, 1 workflow, and 4 personas across operational (OpenAPI) and capability (Naftiko) dimensions

## Rules

- [Workday Advanced Compensation Spectral Rules](rules/workday-advanced-compensation-spectral-rules.yml) — 40 rules across 14 categories enforcing Workday Advanced Compensation API conventions

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
