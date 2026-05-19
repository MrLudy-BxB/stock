# StockFB BusinessSummary API Reference Index

This is the skill-facing entry point. Use it to choose the smallest useful reference file before loading detailed docs.

## Scope

This skill covers two StockFB BusinessSummary endpoints extracted from `2026_API version 1.xlsx`.

## What Is Included

- 2 endpoint/API operation records in `data/endpoint-index.json`.
- 2 concept records in `data/concept-index.json`.
- 3 topic reference files under `by-topic/`.
- 1 source record covered by the organized references.

## How To Navigate

1. For endpoint/API operation questions, use `data/endpoint-index.json` first.
2. For field, auth, date-filter, or concept questions, use `data/concept-index.json` first.
3. For topic-level questions, use `data/skill-reference-index.json` or the topic list below.
4. Open only the relevant file under `by-topic/` for full context.
5. For source disputes, use source records in topic files and `data/source-index.json`.

## Directory Map

- `data/source-index.json`: maps references to portable source names.
- `data/topic-index.json`: maps topics to reference files.
- `data/skill-reference-index.json`: machine-readable routing guide.
- `data/endpoint-index.json`: endpoint/API operation lookup.
- `data/concept-index.json`: concept lookup.
- `data/taxonomy.json`: topic taxonomy.
- `by-topic/`: grouped reference docs intended for skill loading.
- `reports/`: validation, coverage, and package reports.

## Topic References

### BusinessSummary

Covers BusinessSummary endpoint overview, sale order summary, and product claim detail.

Files: 3. Source records: 1.

- `by-topic/businesssummary/overview.md`: scope, common date-filter pattern, auth limitations, and source traceability.
- `by-topic/businesssummary/saleorder-summary.md`: `POST /api/BusinessSummary/saleorder-summary` request and response fields.
- `by-topic/businesssummary/product-claim-detail.md`: `POST /api/businesssummary/product-claim-detail` request and response fields.

## Source Traceability

References preserve the portable source name `2026_API version 1.xlsx` and source id `workbook-2026-api-version-1`. No public URL is available because the source is a local workbook supplied by the user.

## Known Limitations

- The workbook does not document error responses, rate limits, status codes, pagination semantics, auth token acquisition, or environments.
- Sensitive token-like and account-like sample values are redacted from final references.
