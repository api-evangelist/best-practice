---
name: Run an async SQL Passthrough query and page results
description: Submit a large SQL Passthrough query against a paired Bp Premier practice, poll for completion, and page through the results via the Halo Cloud Integrator API.
api: openapi/haloconnect-integrator-openapi.json
operations: [createAsyncQuery, getQuery, getQueryStatusBatch, getResultPage, streamResultPage]
---

# Run an async SQL Passthrough query and page results

Immediate queries are capped at 8MB; use the async workflow for large result sets.

## Prerequisites
- `Ocp-Apim-Subscription-Key` header on every request.
- An active pairing with the target `siteId`.

## Steps
1. **Submit** — call `createAsyncQuery` with the SQL command; it returns a `queryId`.
2. **Poll status** — call `getQuery` (single) or `getQueryStatusBatch` (many) until status is complete; the completed status includes pagination details (page count).
3. **Fetch pages** — call `getResultPage` for each `pageNumber`, or `streamResultPage` to stream a large page.

## Rules
- No idempotency key: do not blindly re-submit; reuse the returned `queryId` to check status instead (see conventions/best-practice-conventions.yml).
- A `410 Gone` means the result expired — resubmit the query.
- Query-execution failures return `{ status: "executionFailed", errorDetails: { errorType, errorCode, errorMessage } }` where errorType is one of `http | mssql | fbsql | haloLink`.
- To avoid polling entirely, register a webhook so Halo notifies you on completion (asyncapi/best-practice-webhooks.yml).
