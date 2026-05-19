# StockFB BusinessSummary API Skill

Source-grounded AI-agent skill for StockFB BusinessSummary API endpoints extracted from a user-provided 2026 API workbook.

## What This Skill Covers

- `POST https://stockfb.com/api/BusinessSummary/saleorder-summary`.
- `POST https://stockfb.com/api/businesssummary/product-claim-detail`.
- Request body fields, response shapes, and response field tables documented in the workbook.
- Source limitations, redactions, and unresolved behavior documented in bundled reports.

## Install

Install this skill from its standalone GitHub repository:

```sh
npx skills add https://github.com/<owner>/<skill-repo>
```

If installing from a local clone of this standalone skill repository, run from the repository root:

```sh
npx skills add .
```

If installing from a repo-local published skills collection, run from the collection repository root after the skill has been explicitly exported there:

```sh
npx skills add ./published-skills --skill stockfb-businesssummary-api
```

## Use

Ask questions such as:

- What request body does `saleorder-summary` accept?
- What fields are returned in `orderProduct.data[]`?
- Does `product-claim-detail` require an Authorization header?
- What source limitations exist for the BusinessSummary endpoints?

## Package Structure

```text
stockfb-businesssummary-api/
├── README.md
├── SKILL.md
├── metadata.json
└── references/
    ├── INDEX.md
    ├── by-topic/
    ├── data/
    └── reports/
```

## Source And Safety Notes

- Source: `2026_API version 1.xlsx`.
- No absolute local machine paths are included in this skill.
- Secrets, private tokens, raw credentials, and workflow-only artifacts are not included.
- Token-like and account-like sample values found in raw evidence are redacted from final references.
- Known limitations are recorded in `references/reports/validation-report.md`.

## Start Reading

For manual review, start with:

- `SKILL.md`
- `references/INDEX.md`
- `references/reports/validation-report.md`
