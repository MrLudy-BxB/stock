# Product Claim Detail Endpoint

Source record: `workbook-2026-api-version-1`, worksheet `4.กลุ่มการเคลมสินค้า`, raw rows 1-22.

## Operation

- Method: `POST`
- URL: `https://stockfb.com/api/businesssummary/product-claim-detail`
- Content type: `application/json`
- Authorization: the workbook example includes an `Authorization` header value. The value is omitted from cleaned and final references because it appears to be a sensitive token-like credential.

## Request Body

```json
{
  "startDate": "2024-05-01T17:00:00.00Z",
  "endDate": "2024-05-07T16:59:59.59Z"
}
```

## Response Shape

```json
{
  "recordsTotal": 248,
  "data": [
    {
      "uid": "<redacted-sample-uid>",
      "fullFormat": "<redacted-sample-composite-value>",
      "claimType": "คืนเงิน",
      "productType": "เฟส เพื่อน2500คน",
      "employee": "CNX StaffManager",
      "supplierName": "จาง วอนยอง",
      "supplierCode": "S000006",
      "claimCode": "CM24050213350781",
      "salesOrderCode": "240502-133527",
      "createDateStr": "02/05/2024 13:35",
      "salePrice": "2,500.00",
      "createDate": "2024-05-02T06:35:27.7997847",
      "reason": "สินค้าหมด",
      "id": 11498
    }
  ]
}
```

## Fields

| Field | Type | Description |
| --- | --- | --- |
| `recordsTotal` | integer | จำนวนข้อมูลทั้งหมด |
| `data` | array | รายการข้อมูล Claim |
| `data[].uid` | string | รหัส UID สินค้า |
| `data[].fullFormat` | string | ข้อมูลรวมทั้งหมดในรูปแบบ String เดียว โดยคั่นด้วย |
| `data[].claimType` | string | ประเภทการเคลม |
| `data[].productType` | string | ประเภทสินค้า |
| `data[].employee` | string | ชื่อพนักงานผู้ดำเนินการ |
| `data[].supplierName` | string | ชื่อ Supplier หรือผู้ให้บริการ |
| `data[].supplierCode` | string | รหัส Supplier |
| `data[].claimCode` | string | รหัส ClaimOrder |
| `data[].salesOrderCode` | string | รหัสคำสั่งซื้อ (Sales Order) |
| `data[].createDateStr` | string | วันที่อนุมัติรายการในรูปแบบแสดงผล UI |
| `data[].salePrice` | decimal/string | ราคาขายของสินค้า |
| `data[].createDate` | datetime | วันที่อนุมัติรายการในรูปแบบ ISO DateTime |
| `data[].reason` | string | เหตุผลของการ Claim |
| `data[].id` | integer | Primary Key ของข้อมูลรายการสินค้าที่ claim ในระบบ |

## Known Limitations

- The workbook documents that an Authorization header is used, but does not describe how to obtain or refresh it.
- Error responses, pagination behavior, and date filtering semantics are not documented in the workbook.
- The exact delimiter for `data[].fullFormat` is unclear in the field table because the description appears truncated; the raw example uses pipe-delimited content.
