# Intact Financial (intact-financial)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
