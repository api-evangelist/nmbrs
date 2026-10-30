# Nmbrs

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Nmbrs (Visma Nmbrs) is cloud HR and payroll software for the Netherlands and Sweden, widely used by employers, accountants, and payroll service providers. Nmbrs exposes its HRIS and payroll data through a public API in two generations. The current, forward-looking interface is a REST API served from https://api.nmbrsapp.com, authenticated with OAuth 2.0 (Authorization Code flow via identityservice.nmbrs.com) plus a per-product subscription key, with granular scopes over companies, employees, employments, salaries, wage components, payruns, and absences. The older SOAP API (api.nmbrs.nl/soap/v3 - EmployeeService, CompanyService, DebtorService) remains available for existing integrations but is deprecated and scheduled to be retired on 1 March 2027, after which REST is the only supported API.

**Areas:** Human Resources · HRIS · Payroll · Employee Management · Absence Management · Netherlands · Sweden · SOAP · REST

## Nmbrs on APIs.io

Everything profiled for Nmbrs is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/nmbrs/](https://apis.io/providers/nmbrs/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [Nmbrs SOAP EmployeeService (Legacy)](https://apis.io/apis/nmbrs/nmbrs-soap-employee-service/) — Legacy SOAP v3 EmployeeService (300+ operations, e.g. Employee_GetCurrent, Contract_GetAll, Salary_GetCurrent, Absence2_Insert, WageComponentFixed_Insert)…
- [Nmbrs SOAP CompanyService (Legacy)](https://apis.io/apis/nmbrs/nmbrs-soap-company-service/) — Legacy SOAP v3 CompanyService (120+ operations, e.g. Company_GetCurrentPeriod, Run_GetList, RunRequest_Insert,…
- [Nmbrs SOAP DebtorService (Legacy)](https://apis.io/apis/nmbrs/nmbrs-soap-debtor-service/) — Legacy SOAP v3 DebtorService for the accountant/debtor tier that owns companies (e.g. AccountantContact_GetList, Debtor_GetList). Deprecated - retiring 1…
- [Nmbrs Absences API](https://apis.io/apis/nmbrs/nmbrs-absences-api/) — Employee absence, leave, and sickness registrations.
- [Nmbrs Companies API](https://apis.io/apis/nmbrs/nmbrs-companies-api/) — Company (employer) records within a Nmbrs environment.
- [Nmbrs Employees API](https://apis.io/apis/nmbrs/nmbrs-employees-api/) — Employee records and their personal / HR information.
- [Nmbrs Employments API](https://apis.io/apis/nmbrs/nmbrs-employments-api/) — Employment contracts and employment history for an employee.
- [Nmbrs Salaries API](https://apis.io/apis/nmbrs/nmbrs-salaries-api/) — Salary and wage information for an employee.
- [Nmbrs Wage Components API](https://apis.io/apis/nmbrs/nmbrs-wage-components-api/) — Fixed and variable wage components used in payroll.
- [Nmbrs Pay Runs API](https://apis.io/apis/nmbrs/nmbrs-pay-runs-api/) — Payroll runs (payruns) and their results for a company.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Nmbrs Agentic Access](https://apis.io/agentic-access/nmbrs/nmbrs-agentic-access/)

#### Collections (8)

Postman and Open Collection request collections.

- [Nmbrs Public REST API (HR & Payroll)](https://apis.io/collections/nmbrs/open-nmbrs/)
- [Nmbrs Public REST API (HR & Payroll) Absences API](https://apis.io/collections/nmbrs/open-nmbrs-absences-api/)
- [Nmbrs Public REST API (HR & Payroll) Absences Companies API](https://apis.io/collections/nmbrs/open-nmbrs-companies-api/)
- [Nmbrs Public REST API (HR & Payroll) Absences Employees API](https://apis.io/collections/nmbrs/open-nmbrs-employees-api/)
- [Nmbrs Public REST API (HR & Payroll) Absences Employments API](https://apis.io/collections/nmbrs/open-nmbrs-employments-api/)
- [Nmbrs Public REST API (HR & Payroll) Absences Payruns API](https://apis.io/collections/nmbrs/open-nmbrs-payruns-api/)
- [Nmbrs Public REST API (HR & Payroll) Absences Salaries API](https://apis.io/collections/nmbrs/open-nmbrs-salaries-api/)
- [Nmbrs Public REST API (HR & Payroll) Absences Wage Components API](https://apis.io/collections/nmbrs/open-nmbrs-wage-components-api/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Nmbrs Authentication](https://apis.io/security/nmbrs/nmbrs-authentication/)
- [Nmbrs Domain Security](https://apis.io/security/nmbrs/nmbrs-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Nmbrs Plans Pricing](https://apis.io/plans/nmbrs/nmbrs-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Nmbrs Rate Limits](https://apis.io/rate-limits/nmbrs/nmbrs-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Nmbrs Finops](https://apis.io/finops/nmbrs/nmbrs-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.nmbrs.com)
- [Documentation](https://developer.nmbrs.com/docs)
- [API reference](https://nmbrs.stoplight.io/docs/nmbrs-restapi)
- [Sign up](https://developer.nmbrs.com)
- [Blog](https://www.nmbrs.com/blog)

## API Evangelist rating

**Kin Score 28.7** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 50.2 |
| Contract governance | 0.0 |
| Operational transparency | 5.3 |
| Developer ergonomics | 32.1 |
| Access clarity | 21.1 |

**Agent readiness 22.9** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | negotiable (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 11.8** — Employment & Payroll

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/nmbrs/](https://apis.io/providers/nmbrs/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Nmbrs: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/nmbrs/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
