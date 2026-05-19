---
name: stockfb-businesssummary-api
description: Use when answering questions about StockFB BusinessSummary API endpoints documented in the 2026 API workbook, including sale order summaries, product claim details, request bodies, response fields, and source limitations.
metadata:
  short-description: StockFB BusinessSummary API endpoint reference
---

# StockFB BusinessSummary API

Use this skill when the user asks about StockFB BusinessSummary API endpoints, request bodies, response fields, sale summaries, product claim details, or limitations in the workbook-sourced documentation.

## Lookup Workflow

1. Start with `references/INDEX.md` to choose the smallest useful reference file.
2. For endpoint/API operation questions, inspect `references/data/endpoint-index.json` first.
3. For field, auth, or date-filter questions, inspect `references/data/concept-index.json` first.
4. For topic-level questions, use `references/data/skill-reference-index.json` or the topic list in `references/INDEX.md`.
5. Load the matching file under `references/by-topic/` for full context.
6. Cite the portable source name `2026_API version 1.xlsx` and bundled reference path for source-grounded answers.

## Reference Map

- `references/INDEX.md`: human-readable routing guide.
- `references/data/`: compact lookup and routing indexes.
- `references/by-topic/businesssummary/`: endpoint and overview references.
- `references/reports/`: validation, coverage, and package reports.

## Answering Rules

- Do not invent API behavior, parameters, limits, errors, schemas, auth flows, or availability absent from the bundled references.
- If bundled references are incomplete or uncertain, say what is unresolved and cite the closest reference.
- Preserve exact endpoint methods, URLs, field names, and documented Thai descriptions from the references.
- Do not reveal or reconstruct redacted token-like values or account-like sample values from raw workbook evidence.
