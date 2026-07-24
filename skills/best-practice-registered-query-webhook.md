---
name: Register a recurring query and receive webhook notifications
description: Create a registered (recurring) SQL query against a paired Bp Premier practice and consume HMAC-signed webhook notifications instead of polling.
api: openapi/haloconnect-integrator-openapi.json
operations: [createRegisteredQuery, getRegisteredQueries, getRegisteredQuery, getRegisteredQueryResult, cancelRegisteredQuery]
---

# Register a recurring query and receive webhook notifications

Registered queries run on a set frequency; combined with webhooks they let you process practice data changes without polling.

## Prerequisites
- `Ocp-Apim-Subscription-Key` header and an active pairing with `siteId`.
- A webhook URL registered with Halo support (linked to your Halo Cloud subscription).

## Steps
1. **Register** — call `createRegisteredQuery` with the SQL and frequency; it returns a `queryId`.
2. **Confirm** — call `getRegisteredQueries` / `getRegisteredQuery` to verify registration.
3. **Receive webhook** — on each run that detects data, Halo POSTs a notification containing `siteId`, `queryId`, and `webhookSource: registered`.
4. **Verify the signature** — validate the `X-Halo-Signature-256` header (HMAC-SHA256 over `<message_body>.<timestamp_iso8601>` using your per-integrator secret); reject stale `X-Halo-Timestamp` values to prevent replay.
5. **Fetch results** — call `getRegisteredQueryResult` (paged) for the actual data — the webhook payload never contains practice data.
6. **Stop** — call `cancelRegisteredQuery` when done.

## Rules
- Webhook payloads are metadata only; always fetch results over the API.
- Errors use the custom envelope `{ error: { status, statusText, message } }` (errors/best-practice-problem-types.yml).
