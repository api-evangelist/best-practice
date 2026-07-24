# Best Practice Software (best-practice)

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
