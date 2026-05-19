# StockFB BusinessSummary API Overview

This reference covers the BusinessSummary endpoints extracted from the user-provided workbook `2026_API version 1.xlsx`.

## Endpoint Groups

| Group | Endpoint | Purpose |
| --- | --- | --- |
| Sales | `POST https://stockfb.com/api/BusinessSummary/saleorder-summary` | Sale order summary with product totals and order payment rows |
| Claims | `POST https://stockfb.com/api/businesssummary/product-claim-detail` | Product claim detail rows |

## Common Request Pattern

Both documented endpoints use a JSON request body with date range fields:

```json
{
  "startDate": "<date-or-null>",
  "endDate": "<date-or-null>"
}
```

The workbook examples show nullable dates for sale order summary and ISO-like UTC dates for product claim detail. The workbook does not define validation rules or timezone semantics.

## Authentication

The workbook shows an Authorization header for `product-claim-detail`. The sensitive token-like value is intentionally omitted. The workbook does not document token acquisition, refresh, scopes, roles, or expiration.

## Source Traceability

| Source ID | Portable Source | Worksheets |
| --- | --- | --- |
| `workbook-2026-api-version-1` | `2026_API version 1.xlsx` | `1.กลุ่มการขาย `, `4.กลุ่มการเคลมสินค้า` |

## Known Limitations

- Only two endpoints are documented in the supplied workbook.
- Error responses, rate limits, status codes, pagination, auth flow, and environment configuration are not documented.
- Final references redact token-like and account-like sample values from the raw workbook extraction.
