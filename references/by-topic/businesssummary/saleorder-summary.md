# Sale Order Summary Endpoint

Source record: `workbook-2026-api-version-1`, worksheet `1.กลุ่มการขาย `, raw rows 1-46.

## Operation

- Method: `POST`
- URL: `https://stockfb.com/api/BusinessSummary/saleorder-summary`
- Content type: `application/json`

## Request Body

```json
{
  "startDate": null,
  "endDate": null
}
```

The workbook example shows both `startDate` and `endDate` as nullable values. No date format requirements are documented for this endpoint in the workbook.

## Response Shape

```json
{
  "orderProduct": {
    "recordsFiltered": 1,
    "recordsTotal": 1,
    "data": [],
    "sumtotalclaim": "0.00",
    "sumTotalCost": "100.00",
    "sumtotalreturn": "0.00",
    "sumtotalsold": "110.00",
    "sumValueSort": "10.00",
    "sumTotalDiscountPrice": "0.00",
    "sumTotalFinalPrice": "110.00"
  },
  "orderPayment": {
    "data": []
  }
}
```

## `orderProduct` Fields

| Field | Type | Description |
| --- | --- | --- |
| `recordsFiltered` | int | จำนวนรายการหลังจาก filter |
| `recordsTotal` | int | จำนวนรายการทั้งหมด |
| `data` | array | รายการข้อมูลสินค้า |
| `sumtotalclaim` | string (decimal) | ยอดรวม claim |
| `sumTotalCost` | string (decimal) | ต้นทุนรวม |
| `sumtotalreturn` | string (decimal) | ยอดคืนสินค้า |
| `sumtotalsold` | string (decimal) | ยอดขายรวม |
| `sumValueSort` | string (decimal) | กำไรรวม (value) |
| `sumTotalDiscountPrice` | string (decimal) | ส่วนลดรวม |
| `sumTotalFinalPrice` | string (decimal) | ราคาสุทธิรวม |

## `orderProduct.data[]` Fields

| Field | Type | Description |
| --- | --- | --- |
| `productType` | int | รหัสประเภทสินค้า |
| `productTypeName` | string | ชื่อประเภทสินค้า |
| `totalCost` | string (decimal) | ต้นทุนรวม (format string) |
| `totalSold` | string (decimal) | ยอดขายรวม (format string) |
| `totalReturn` | string (decimal) | ยอดคืนสินค้า |
| `totalClaim` | string (decimal) | ยอดเคลม |
| `deliveryDate` | datetime/null | วันที่จัดส่ง |
| `value` | string (decimal) | กำไร (ยอดขาย - ต้นทุน) |
| `totalcost` | decimal | ต้นทุนรวม (ตัวเลขใช้คำนวณ) |
| `totalsold` | decimal | ยอดขายรวม (ตัวเลขใช้คำนวณ) |
| `totalreturn` | decimal | ยอดคืนสินค้า (numeric) |
| `totalclaim` | decimal | ยอดเคลม (numeric) |
| `valueSort` | decimal | กำไร (numeric สำหรับ sort) |

## `orderPayment.data[]` Fields

| Field | Type | Description |
| --- | --- | --- |
| `id` | int | รหัสรายการ order |
| `status` | string | สถานะ (เช่น ชำระเงินแล้ว) |
| `statusInt` | int | รหัสสถานะ (enum) |
| `createDate` | string (datetime) | วันที่สร้างรายการ |
| `customer` | string | รหัสลูกค้า |
| `employee` | string | รหัสพนักงาน |
| `total` | decimal | ยอดรวมคำสั่งซื้อ |
| `orderCode` | string | เลขที่ออเดอร์ |
| `deliveryStatusContent` | string | สถานะการจัดส่งแล้ว (เช่น 2 / 2) |
| `isDeliverOrder` | bool | เป็น order จัดส่งหรือไม่ |
| `isSalesOrderPickUp` | bool | เป็น order รับเองหรือไม่ |

## Known Limitations

- Authentication requirements are not shown for this endpoint in the workbook row.
- Error responses, pagination behavior, and date filtering semantics are not documented in the workbook.
- The worksheet label `OorderProduct` appears to be an original workbook typo and is preserved as `orderProduct` based on the response object name.
