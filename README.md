# Best Practice Software

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

Best Practice Software is an Australian clinical and practice-management software company, headquartered in Bundaberg, Queensland, and one half of the Australian GP-software duopoly (alongside MedicalDirector). Its flagship products - Bp Premier (general practice), Bp VIP.net (specialist and allied), and Bp Allied - run in thousands of Australian medical practices. Best Practice's programmatic surface is delivered through Halo Connect (Halo Cloud / Halo Link), a FHIR-based integration platform that lets approved partners query practice data over a modern API instead of the legacy SQL database. The FHIR API for Bp Premier is built to the AU Base 4.1.0 implementation guide, falling back to HL7 FHIR R4 (4.0.1), and exposes resources such as Patient, Appointment, Slot (Find Free Slots) and a Patient $summary document. Halo Cloud also offers SQL Passthrough and Registered Queries for structured practice data. Access is gated - integrators require a Halo Cloud subscription plus per-practice pairing and PMS-managed database credentials, authenticated with an Azure API Management subscription key (desktop apps additionally use a bearer JWT and device id). This is not a self-serve public API; it is a partner-onboarded, standards-aligned interoperability layer for the Australian primary-care market.

**Areas:** Healthcare · Australia · Electronic Health Records · FHIR · HL7 · Interoperability · AU Base · Practice Management · General Practice · Appointments · Scheduling

## Best Practice Software on APIs.io

Everything profiled for Best Practice Software is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/best-practice/](https://apis.io/providers/best-practice/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [Best Practice Software FHIR API](https://apis.io/apis/best-practice/best-practice-fhir-api/) — Query practice data using FHIR resources.
- [Best Practice Software Registered Queries API](https://apis.io/apis/best-practice/best-practice-registered-queries-api/) — The Registered Queries API from Best Practice Software — 6 operation(s) for registered queries.
- [Best Practice Software Sites API](https://apis.io/apis/best-practice/best-practice-sites-api/) — Endpoints for practice onboarding and site metadata.
- [Best Practice Software SQL Passthrough API](https://apis.io/apis/best-practice/best-practice-sql-passthrough-api/) — Send SQL queries to practices as immediate, async or registered queries. **Immediate queries** are small, time-sensitive queries that return a result in…
- [Best Practice Software Tokens API](https://apis.io/apis/best-practice/best-practice-tokens-api/) — Obtain authorization tokens for desktop applications to authenticate API requests.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Best Practice Webhooks](https://apis.io/asyncapis/best-practice/best-practice-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [halo-cloud-integrator](https://apis.io/servers/best-practice/halo-cloud-integrator/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Best Practice Agentic Access](https://apis.io/agentic-access/best-practice/best-practice-agentic-access/)

#### Collections (2)

Postman and Open Collection request collections.

- [Halo Cloud API for Desktop Applications](https://apis.io/collections/best-practice/open-haloconnect-desktop/)
- [Halo Cloud API for Integrators](https://apis.io/collections/best-practice/open-haloconnect-integrator/)

#### Overlays (2)

OpenAPI overlays, including conversational phrasing for each operation.

- [Best Practice Desktop Overlay](https://apis.io/overlays/best-practice/best-practice-desktop-overlay/)
- [Best Practice Integrator Overlay](https://apis.io/overlays/best-practice/best-practice-integrator-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Best Practice Authentication](https://apis.io/security/best-practice/best-practice-authentication/)
- [Best Practice Domain Security](https://apis.io/security/best-practice/best-practice-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://bpsoftware.net/)
- [Documentation](https://docs.haloconnect.io/halo-cloud/overview/)
- [Getting started](https://docs.haloconnect.io/halo-cloud/getting-started/)
- [API reference](https://docs.haloconnect.io/api-reference/integrator-openapi.html)
- [Support](https://bpsoftware.net/contact/)
- [Blog](https://haloconnect.io/blog)
- [Terms of service](https://bpsoftware.net/terms-of-use/)
- [Privacy policy](https://bpsoftware.net/privacy-policy/)
- [Status](https://status.haloconnect.io/)

## API Evangelist rating

**Kin Score 48.0** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 59.2 |
| Contract governance | 18.2 |
| Operational transparency | 39.5 |
| Developer ergonomics | 66.1 |
| Access clarity | 21.1 |

**Agent readiness 26.9** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | partial |
| Rate Limit Signal | — |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | — |

**Regulatory alignment 24.2** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/best-practice/](https://apis.io/providers/best-practice/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Best Practice Software: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/best-practice/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
