# Nmbrs (nmbrs)

Nmbrs (Visma Nmbrs) is cloud **HR and payroll software** for the **Netherlands and Sweden**, used by employers, accountants, and payroll service providers. Nmbrs exposes its **HRIS and payroll** data through a public API in two generations:

- **REST API (current, recommended)** — served from `https://api.nmbrsapp.com`, authenticated with the **OAuth 2.0 Authorization Code** flow (`identityservice.nmbrs.com`) plus a **per-product subscription key** sent on every request. Granular OAuth scopes (e.g. `employee.info`, `employee.employment`, `employee.payment`) cover companies, employees, employments, salaries, wage components, payruns, and absences.
- **SOAP API (legacy, deprecated)** — served from `https://api.nmbrs.nl/soap/v3` as `EmployeeService`, `CompanyService`, and `DebtorService` with several hundred operations, authenticated with a **username + API token**. The SOAP API is **scheduled to be retired on 1 March 2027**; new integrations should use REST and existing SOAP integrations should migrate.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/nmbrs/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/nmbrs/refs/heads/main/apis.yml)

## Access & Honesty Note

The Nmbrs REST API is **gated**: you must register on the [developer portal](https://developer.nmbrs.com), subscribe to a product to get a subscription key, and complete OAuth 2.0 authentication at the company/debtor level. A live unauthenticated probe of `GET https://api.nmbrsapp.com/api/companies` returns **HTTP 401**, confirming the base URL and auth model.

The full REST reference is published as an **interactive Stoplight project** rather than a downloadable OpenAPI file. The OpenAPI and collections in this repository are therefore **modeled** (`endpointsModeled`) from the documented resource groups around a **confirmed base URL and auth model** — they are a faithful representation for discovery, not a byte-for-byte copy of the vendor spec. The legacy SOAP services publish live `.asmx` operation listings and WSDLs at `https://api.nmbrs.nl/soap/v3`.

## Tags

- Human Resources
- HRIS
- Payroll
- Employee Management
- Absence Management
- Netherlands
- Sweden
- SOAP
- REST

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### Nmbrs Companies API (REST)

Companies (employers) inside a Nmbrs environment — the parent scope for employees and payroll. `GET https://api.nmbrsapp.com/api/companies` is a confirmed live endpoint.

- **Base URL:** `https://api.nmbrsapp.com`
- [Documentation](https://developer.nmbrs.com/docs) · [API Reference](https://nmbrs.stoplight.io/docs/nmbrs-restapi) · [OpenAPI](openapi/nmbrs-openapi.yml)

### Nmbrs Employees API (REST)

Core HRIS surface — list a company's employees and read individual records including personal information. Guarded by `employee.info` scopes.

- **Base URL:** `https://api.nmbrsapp.com`
- [Get employee list](https://nmbrs.stoplight.io/docs/nmbrs-restapi/a31578b069764-get-employee-list) · [OpenAPI](openapi/nmbrs-openapi.yml)

### Nmbrs Employments API (REST)

Employment contracts and history (start/end dates, contract type) under the `employee.employment` scope. Modeled endpoints.

### Nmbrs Payroll & Payruns API (REST)

Company payruns (per period/year) and employee salaries — the engine behind per-payslip billing. Salary access uses the `employee.payment` scope. Modeled endpoints.

### Nmbrs Wage Components API (REST)

Fixed and variable wage components applied in payroll — list and add per period/year. Modeled endpoints.

### Nmbrs Absences API (REST)

Employee absence, leave, and sickness registrations — list and register. Modeled endpoints.

### Nmbrs SOAP EmployeeService (Legacy)

SOAP v3 `EmployeeService` (300+ operations: `Employee_GetCurrent`, `Contract_GetAll`, `Salary_GetCurrent`, `Absence2_Insert`, `WageComponentFixed_Insert`, …). Username + API token. **Retiring 2027-03-01.**

- **Base URL:** `https://api.nmbrs.nl/soap/v3` · [WSDL](https://api.nmbrs.nl/soap/v3/EmployeeService.asmx?WSDL)

### Nmbrs SOAP CompanyService (Legacy)

SOAP v3 `CompanyService` (120+ operations: `Company_GetCurrentPeriod`, `Run_GetList`, `RunRequest_Insert`, `SalaryDocuments_GetAllPayslipsPDFByRunCompany`, `Journals_GetByRunCompany`, `WageTax_GetList`, …). **Retiring 2027-03-01.**

- **Base URL:** `https://api.nmbrs.nl/soap/v3` · [WSDL](https://api.nmbrs.nl/soap/v3/CompanyService.asmx?WSDL)

### Nmbrs SOAP DebtorService (Legacy)

SOAP v3 `DebtorService` for the accountant/debtor tier (`Debtor_GetList`, `AccountantContact_GetList`, …). **Retiring 2027-03-01.**

- **Base URL:** `https://api.nmbrs.nl/soap/v3` · [WSDL](https://api.nmbrs.nl/soap/v3/DebtorService.asmx?WSDL)

## Common Properties

- [Authentication](authentication/nmbrs-authentication.yml)
- [Domain Security](security/nmbrs-domain-security.yml)
- [LinkedIn](https://www.linkedin.com/company/nmbrs)
- [Website](https://www.nmbrs.com)
- [Documentation](https://developer.nmbrs.com/docs)
- [API Reference](https://nmbrs.stoplight.io/docs/nmbrs-restapi)
- [Sign Up](https://developer.nmbrs.com)
- [Plans](plans/nmbrs-plans-pricing.yml)
- [Rate Limits](rate-limits/nmbrs-rate-limits.yml)
- [Fin Ops](finops/nmbrs-finops.yml)

## Pricing

Nmbrs bills **per payslip** — you pay only for employees who actually receive a payslip in a given month, with no charge for inactive employees and no per-login/per-user fees. Business packages are **Essential, Advanced, Advanced Pro**; there is a separate track for accountants / payroll service providers. Country pricing differs (NL business from ~€69/mo for up to 10 employees; SE from ~99 kr/mo). See [plans](plans/nmbrs-plans-pricing.yml).

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
