# Coverage Report

## Covered Source Material

| Source Area | Coverage |
| --- | --- |
| Worksheet `1.กลุ่มการขาย ` | Covered by `by-topic/businesssummary/saleorder-summary.md` |
| Worksheet `4.กลุ่มการเคลมสินค้า` | Covered by `by-topic/businesssummary/product-claim-detail.md` |
| Endpoint overview | Covered by `by-topic/businesssummary/overview.md` |

## Endpoint Coverage

| Endpoint | Covered |
| --- | --- |
| `POST https://stockfb.com/api/BusinessSummary/saleorder-summary` | Yes |
| `POST https://stockfb.com/api/businesssummary/product-claim-detail` | Yes |

## Known Gaps From Source

The supplied workbook does not include documented details for:

- Error response schemas.
- HTTP status codes.
- Rate limits.
- Pagination semantics.
- Authentication flow or token lifecycle.
- Environment/base URL variants.
- Request field validation rules.

## Redaction Coverage

Final references intentionally omit token-like Authorization content and account-like sample values from raw examples.
