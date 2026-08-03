# Best Practice Software (best-practice)

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

Best Practice Software is an Australian clinical and practice-management software company, headquartered in Bundaberg, Queensland, and one half of the Australian GP-software duopoly (alongside MedicalDirector). Its flagship products - Bp Premier (general practice), Bp VIP.net (specialist and allied), and Bp Allied - run in thousands of Australian medical practices. Best Practice's programmatic surface is delivered through Halo Connect (Halo Cloud / Halo Link), a FHIR-based integration platform for approved partners. The FHIR API for Bp Premier is built to AU Base 4.1.0 (falling back to HL7 FHIR R4 4.0.1). Access is partner-gated - a Halo Cloud subscription plus per-practice pairing - not a self-serve public API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/best-practice/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/best-practice/refs/heads/main/apis.yml)

## Tags

- Healthcare
- Australia
- EHR / EMR
- FHIR / HL7 / AU Base
- Interoperability
- Practice Management / General Practice
- Appointments / Scheduling

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

### Halo Cloud API for Integrators

The integrator-facing Halo Cloud API from Best Practice's Halo Connect platform. Covers Sites (site metadata and onboarding), SQL Passthrough (SQL against the practice database), FHIR (search practice data as HL7 FHIR R4 resources), and Registered Queries (recurring SQL). OpenAPI 3.1.1, authenticated with an Azure API Management subscription key (`Ocp-Apim-Subscription-Key`); every call requires an active site pairing.

- **Human URL:** [https://docs.haloconnect.io/api-reference/integrator-openapi.html](https://docs.haloconnect.io/api-reference/integrator-openapi.html)
- **Base URL:** `https://api.haloconnect.io`

#### Properties

- [OpenAPI](openapi/haloconnect-integrator-openapi.json) - [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [API Reference](https://docs.haloconnect.io/api-reference/integrator-openapi.html)
- [Documentation](https://docs.haloconnect.io/halo-cloud/overview/)
- [Getting Started](https://docs.haloconnect.io/halo-cloud/getting-started/)

### Halo Cloud API for Desktop Applications

The desktop-application-facing Halo Cloud API from Halo Connect. Provides a token endpoint plus SQL Passthrough and FHIR query access for locally installed applications integrating with Bp Premier. OpenAPI 3.1.1, authenticated with a subscription key together with a bearer JWT and a `DeviceId` header.

- **Human URL:** [https://docs.haloconnect.io/api-reference/desktop-openapi.html](https://docs.haloconnect.io/api-reference/desktop-openapi.html)
- **Base URL:** `https://api.haloconnect.io`

#### Properties

- [OpenAPI](openapi/haloconnect-desktop-openapi.json) - [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [API Reference](https://docs.haloconnect.io/api-reference/desktop-openapi.html)
- [Documentation](https://docs.haloconnect.io/halo-cloud/overview/)
- [Getting Started](https://docs.haloconnect.io/halo-cloud/getting-started/)

### FHIR API for Bp Premier

The HL7 FHIR API for Best Practice Bp Premier, delivered through Halo Connect. Built to the AU Base 4.1.0 implementation guide, falling back to FHIR R4 (4.0.1). Resources are served under `https://api.haloconnect.io/integrator/sites/{siteId}/fhir/R4/` with a CapabilityStatement at `{baseUrl}/metadata`; documented resources and operations include Patient, Appointment, Slot (Find Free Slots) and a Patient `$summary` document. Partner-gated.

- **Human URL:** [https://docs.haloconnect.io/halo-cloud/fhir-api/overview/](https://docs.haloconnect.io/halo-cloud/fhir-api/overview/)
- **Base URL:** `https://api.haloconnect.io/integrator/sites/{siteId}/fhir/R4`

#### Properties

- [OpenAPI](openapi/haloconnect-integrator-openapi.json) - [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://docs.haloconnect.io/halo-cloud/fhir-api/overview/)
- [Documentation](https://docs.haloconnect.io/halo-cloud/fhir-api/capabilities/)
- [Implementation Guide](https://kb.bpsoftware.net/au/bppremier/devportal/Content/Halo/HaloResources.htm) (login required)

## Common Properties

- [Website](https://bpsoftware.net/)
- [Developer Portal](https://docs.haloconnect.io/)
- [Documentation](https://docs.haloconnect.io/halo-cloud/overview/)
- [API Reference](https://docs.haloconnect.io/api-reference/integrator-openapi.html)
- [Getting Started](https://docs.haloconnect.io/halo-cloud/getting-started/)
- [Blog](https://haloconnect.io/blog)
- [Status Page](https://status.haloconnect.io/)
- [Support](https://bpsoftware.net/contact/)
- [Terms of Service](https://bpsoftware.net/terms-of-use/)
- [Privacy Policy](https://bpsoftware.net/privacy-policy/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
