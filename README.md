# Intact Financial (intact-financial)

Intact Financial Corporation is the largest provider of property and casualty insurance in Canada, headquartered in Toronto and trading on the TSX as IFC. It underwrites personal auto, personal property, and commercial P&C lines through the Intact Insurance, belairdirect, BrokerLink, Intact Prestige, Intact Public Entities, and On Side Restoration brands in Canada, through Intact Insurance Specialty Solutions in the United States, and through Intact Insurance UK, EU, IE and 123.ie internationally following the 2021 acquisition of RSA. Distribution runs through a network of more than 6,000 independent broker offices plus direct-to-consumer channels.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/intact-financial/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/intact-financial/refs/heads/main/apis.yml)

## Tags

- Insurance
- Canada
- Property and Casualty
- Carrier
- Underwriting
- Claims
- Broker
- Partner Gated
- No Public API
- CSIO

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

None.

Intact Financial publishes **no public, self-serve API surface**. This repository is an honest stub, and that absence is the finding.

- No developer portal. `developer.`, `developers.`, `docs.` and `api.` subdomains on both `intactfc.com` and `intact.ca` fail to resolve; `/developers`, `/developer`, `/api`, `/partners` and `/integrations` all return 404.
- No downloadable API definition. Zero OpenAPI, Swagger, GraphQL SDL, `.proto` or AsyncAPI documents were found, so this repo has no `openapi/` directory.
- The only integration surfaces are login walls — the broker **Intact Portal** at [portal.intactinsurance.com](https://portal.intactinsurance.com/) (`brokers.intact.ca` 301-redirects there), and the customer **Client Centre** behind IBM Security WebSEAL at `apps.intactinsurance.com`.
- `api.intactspecialty.com` resolves to an Azure Front Door endpoint but returns 404 at the root and at every spec path probed — a private partner gateway, not a public API.
- No public GitHub organization, no public Postman workspace, no documented webhooks or event catalog, and no OIDC/OAuth discovery document on any host.
- Auth model is session-based web login only. No API keys, no OAuth2, no mTLS documented publicly.

### Standards posture (the sector signal)

Canada's insurance data-standards body is **CSIO** (Centre for Study of Insurance Operations) rather than ACORD directly; CSIO publishes EDI, XML, eDocs, Commercial Lines and JSON API standards plus API Security Standards, and runs CSIOnet as the broker-carrier transport.

- **No ACORD, AL3, NGDS or IVANS reference** appears anywhere on `intactfc.com`, `intact.ca` or `intactspecialty.com`. A site search for "CSIO" on `intact.ca` returns zero results.
- Intact Insurance **is** listed in the [CSIO member directory](https://csio.com/membership/member-directory), but appears on **none** of CSIO's [certified-member lists](https://csio.com/csio-certification/certified-members) — not API Security Standards, not CL Data Standards, not Compliance (Z-code), not eDocs, not JSON API Standards.
- CSIO's [2026 Standards Certification Ratings](https://csio.com/standards-certification-ratings) record **"Intact Insurance — Not Yet Rated / Not Yet Rated"** on both the personal and commercial tracks, while peers Definity and Gore Mutual hold Platinum.

None of the four insurance API verbs — quote, bind, issue, FNOL — is exposed publicly. Broker rating and claims run inside the gated portal or over legacy CSIO EDI/XML into broker management systems (Applied Epic/TAM, Vertafore SIG, Acturis, Rival TBW).

## Links

- [Corporate site](https://www.intactfc.com/)
- [Intact Insurance (Canada)](https://www.intact.ca/)
- [Intact Insurance Specialty Solutions (US)](https://www.intactspecialty.com/)
- [Intact Portal (broker login)](https://portal.intactinsurance.com/)
- [Blog](https://www.intact.ca/en/blog)
- [Newsroom](https://www.intactfc.com/news)
- [Company overview](https://www.intactfc.com/investors/company-overview)
- [LinkedIn](https://www.linkedin.com/company/intact)

## Review

See [review.yml](review.yml) for the full probe log, HTTP statuses, CSIO standards posture, auth model, and reviewer findings (API Evangelist, 2026-07-25).
