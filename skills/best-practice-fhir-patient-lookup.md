---
name: FHIR patient lookup and summary (Bp Premier)
description: Search a paired Bp Premier practice for a patient and retrieve a Patient Summary via the Halo Cloud FHIR API.
api: openapi/haloconnect-integrator-openapi.json
operations: [getSites, Integrator_PairSite, getFhirQuery, postFhirSearch]
---

# FHIR patient lookup and summary (Bp Premier)

Use the Halo Cloud Integrator FHIR surface to find a patient and pull an IPS Patient Summary. FHIR is served under `/integrator/sites/{siteId}/fhir/R4/` and conforms to HL7 FHIR R4 (4.0.1) / AU Base 4.1.0.

## Prerequisites
- An `Ocp-Apim-Subscription-Key` (Azure API Management subscription key) on every request.
- An active pairing with the target site. If unpaired, resolve the site with `getSites` (by PMS ID) then pair with `Integrator_PairSite`.

## Steps
1. **Resolve the site** — call `getSites` to find the `siteId` (Halo GUID) for the practice by PMS ID.
2. **Ensure pairing** — call `Integrator_PairSite` if no active pairing exists for the site.
3. **Search the patient** — call `getFhirQuery` (GET) or `postFhirSearch` (POST `_search`) against the `Patient` resource, filtering by identifier (e.g. Medicare number) or name/DOB search params.
4. **Retrieve the summary** — invoke the `$summary` operation on the matched Patient to obtain the International Patient Summary document.

## Rules
- Every call is site-scoped: a `403` means the subscription is valid but there is no active pairing with `siteId`.
- Errors use the custom envelope `{ error: { status, statusText, message } }` (see errors/best-practice-problem-types.yml).
- The resource set varies per PMS; confirm supported resources via the CapabilityStatement at `{baseUrl}/metadata`.
