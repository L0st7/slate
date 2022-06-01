---
title: OpenAPI definition v0
language_tabs:
  - "'ruby": Ruby'
  - "'python": Python'
language_clients:
  - "'ruby": ""
  - "'python": ""
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="openapi-definition">OpenAPI definition v0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="http://dev.api.yody.io:8000/unicorn/purchase-order-service/">http://dev.api.yody.io:8000/unicorn/purchase-order-service/</a>

<h1 id="openapi-definition-procurement-controller">procurement-controller</h1>

## updateStatus

<a id="opIdupdateStatus"></a>

> Code samples

`PUT /purchase-orders/{purchase_order_id}/receive-status/finish`

<h3 id="updatestatus-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|purchase_order_id|path|integer(int64)|true|none|

> Example responses

> 200 Response

<h3 id="updatestatus-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## getDetailProcurement

<a id="opIdgetDetailProcurement"></a>

> Code samples

`GET /purchase-orders/{purchase_order_id}/procurements/{procurement_id}`

<h3 id="getdetailprocurement-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|purchase_order_id|path|integer(int64)|true|none|
|procurement_id|path|integer(int64)|true|none|

> Example responses

> 200 Response

<h3 id="getdetailprocurement-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## updateProcurement

<a id="opIdupdateProcurement"></a>

> Code samples

`PUT /purchase-orders/{purchase_order_id}/procurements/{procurement_id}`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "reference": "string",
  "store_id": 0,
  "store": "string",
  "expect_receipt_date": "2019-08-24T14:15:22Z",
  "note": "string",
  "status": "string",
  "status_name": "string",
  "activated_date": "2019-08-24T14:15:22Z",
  "activated_by": "string",
  "stock_in_date": "2019-08-24T14:15:22Z",
  "stock_in_by": "string",
  "procurement_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "line_item_id": 0,
      "sku": "string",
      "barcode": "string",
      "variant": "string",
      "variant_image": "string",
      "variant_id": 0,
      "retail_price": 0,
      "ordered_quantity": 0,
      "accepted_quantity": 0,
      "planned_quantity": 0,
      "quantity": 0,
      "real_quantity": 0,
      "note": "string",
      "procurement_id": 0
    }
  ],
  "refer_ids": [
    0
  ]
}
```

<h3 id="updateprocurement-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|purchase_order_id|path|integer(int64)|true|none|
|procurement_id|path|integer(int64)|true|none|
|body|body|[ProcurementRequest](#schemaprocurementrequest)|true|none|

> Example responses

> 200 Response

<h3 id="updateprocurement-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## delete_1

<a id="opIddelete_1"></a>

> Code samples

`DELETE /purchase-orders/{purchase_order_id}/procurements/{procurement_id}`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string"
}
```

<h3 id="delete_1-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|purchase_order_id|path|integer(int64)|true|none|
|procurement_id|path|integer(int64)|true|none|
|body|body|[BasicRequest](#schemabasicrequest)|true|none|

> Example responses

> 200 Response

<h3 id="delete_1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultString](#schemaresultstring)|

<aside class="success">
This operation does not require authentication
</aside>

## updateNoteProcurement

<a id="opIdupdateNoteProcurement"></a>

> Code samples

`PUT /purchase-orders/{purchase_order_id}/procurements/{procurement_id}/update-note`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "note": "string"
}
```

<h3 id="updatenoteprocurement-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|purchase_order_id|path|integer(int64)|true|none|
|procurement_id|path|integer(int64)|true|none|
|body|body|[ProcurementUpdateNoteRequest](#schemaprocurementupdatenoterequest)|true|none|

> Example responses

> 200 Response

<h3 id="updatenoteprocurement-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultString](#schemaresultstring)|

<aside class="success">
This operation does not require authentication
</aside>

## confirmProcurement

<a id="opIdconfirmProcurement"></a>

> Code samples

`PUT /purchase-orders/{purchase_order_id}/procurements/{procurement_id}/confirm`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "reference": "string",
  "store_id": 0,
  "store": "string",
  "expect_receipt_date": "2019-08-24T14:15:22Z",
  "note": "string",
  "status": "string",
  "status_name": "string",
  "activated_date": "2019-08-24T14:15:22Z",
  "activated_by": "string",
  "stock_in_date": "2019-08-24T14:15:22Z",
  "stock_in_by": "string",
  "procurement_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "line_item_id": 0,
      "sku": "string",
      "barcode": "string",
      "variant": "string",
      "variant_image": "string",
      "variant_id": 0,
      "retail_price": 0,
      "ordered_quantity": 0,
      "accepted_quantity": 0,
      "planned_quantity": 0,
      "quantity": 0,
      "real_quantity": 0,
      "note": "string",
      "procurement_id": 0
    }
  ],
  "refer_ids": [
    0
  ]
}
```

<h3 id="confirmprocurement-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|purchase_order_id|path|integer(int64)|true|none|
|procurement_id|path|integer(int64)|true|none|
|body|body|[ProcurementRequest](#schemaprocurementrequest)|true|none|

> Example responses

> 200 Response

<h3 id="confirmprocurement-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## approveProcurement

<a id="opIdapproveProcurement"></a>

> Code samples

`PUT /purchase-orders/{purchase_order_id}/procurements/{procurement_id}/approve`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "reference": "string",
  "store_id": 0,
  "store": "string",
  "expect_receipt_date": "2019-08-24T14:15:22Z",
  "note": "string",
  "status": "string",
  "status_name": "string",
  "activated_date": "2019-08-24T14:15:22Z",
  "activated_by": "string",
  "stock_in_date": "2019-08-24T14:15:22Z",
  "stock_in_by": "string",
  "procurement_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "line_item_id": 0,
      "sku": "string",
      "barcode": "string",
      "variant": "string",
      "variant_image": "string",
      "variant_id": 0,
      "retail_price": 0,
      "ordered_quantity": 0,
      "accepted_quantity": 0,
      "planned_quantity": 0,
      "quantity": 0,
      "real_quantity": 0,
      "note": "string",
      "procurement_id": 0
    }
  ],
  "refer_ids": [
    0
  ]
}
```

<h3 id="approveprocurement-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|purchase_order_id|path|integer(int64)|true|none|
|procurement_id|path|integer(int64)|true|none|
|body|body|[ProcurementRequest](#schemaprocurementrequest)|true|none|

> Example responses

> 200 Response

<h3 id="approveprocurement-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## confirmProcurementMerge

<a id="opIdconfirmProcurementMerge"></a>

> Code samples

`PUT /purchase-orders/procurements/merge/confirm`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "reference": "string",
  "store_id": 0,
  "store": "string",
  "expect_receipt_date": "2019-08-24T14:15:22Z",
  "note": "string",
  "status": "string",
  "status_name": "string",
  "activated_date": "2019-08-24T14:15:22Z",
  "activated_by": "string",
  "stock_in_date": "2019-08-24T14:15:22Z",
  "stock_in_by": "string",
  "procurement_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "line_item_id": 0,
      "sku": "string",
      "barcode": "string",
      "variant": "string",
      "variant_image": "string",
      "variant_id": 0,
      "retail_price": 0,
      "ordered_quantity": 0,
      "accepted_quantity": 0,
      "planned_quantity": 0,
      "quantity": 0,
      "real_quantity": 0,
      "note": "string",
      "procurement_id": 0
    }
  ],
  "refer_ids": [
    0
  ]
}
```

<h3 id="confirmprocurementmerge-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ProcurementRequest](#schemaprocurementrequest)|true|none|

> Example responses

> 200 Response

<h3 id="confirmprocurementmerge-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|

<aside class="success">
This operation does not require authentication
</aside>

## createProcurement

<a id="opIdcreateProcurement"></a>

> Code samples

`POST /purchase-orders/{purchase_order_id}/procurements`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "reference": "string",
  "store_id": 0,
  "store": "string",
  "expect_receipt_date": "2019-08-24T14:15:22Z",
  "note": "string",
  "status": "string",
  "status_name": "string",
  "activated_date": "2019-08-24T14:15:22Z",
  "activated_by": "string",
  "stock_in_date": "2019-08-24T14:15:22Z",
  "stock_in_by": "string",
  "procurement_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "line_item_id": 0,
      "sku": "string",
      "barcode": "string",
      "variant": "string",
      "variant_image": "string",
      "variant_id": 0,
      "retail_price": 0,
      "ordered_quantity": 0,
      "accepted_quantity": 0,
      "planned_quantity": 0,
      "quantity": 0,
      "real_quantity": 0,
      "note": "string",
      "procurement_id": 0
    }
  ],
  "refer_ids": [
    0
  ]
}
```

<h3 id="createprocurement-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|purchase_order_id|path|integer(int64)|true|none|
|body|body|[ProcurementRequest](#schemaprocurementrequest)|true|none|

> Example responses

> 200 Response

<h3 id="createprocurement-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## mergeProcurement

<a id="opIdmergeProcurement"></a>

> Code samples

`POST /purchase-orders/{purchase_order_id}/procurements/merge`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "reference": "string",
  "store_id": 0,
  "store": "string",
  "expect_receipt_date": "2019-08-24T14:15:22Z",
  "note": "string",
  "status": "string",
  "status_name": "string",
  "activated_date": "2019-08-24T14:15:22Z",
  "activated_by": "string",
  "stock_in_date": "2019-08-24T14:15:22Z",
  "stock_in_by": "string",
  "procurement_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "line_item_id": 0,
      "sku": "string",
      "barcode": "string",
      "variant": "string",
      "variant_image": "string",
      "variant_id": 0,
      "retail_price": 0,
      "ordered_quantity": 0,
      "accepted_quantity": 0,
      "planned_quantity": 0,
      "quantity": 0,
      "real_quantity": 0,
      "note": "string",
      "procurement_id": 0
    }
  ],
  "refer_ids": [
    0
  ]
}
```

<h3 id="mergeprocurement-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|purchase_order_id|path|integer(int64)|true|none|
|body|body|[ProcurementRequest](#schemaprocurementrequest)|true|none|

> Example responses

> 200 Response

<h3 id="mergeprocurement-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## createManualProcurement

<a id="opIdcreateManualProcurement"></a>

> Code samples

`POST /purchase-orders/{purchase_order_id}/procurements/create-manual`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "reference": "string",
  "store_id": 0,
  "store": "string",
  "expect_receipt_date": "2019-08-24T14:15:22Z",
  "note": "string",
  "status": "string",
  "status_name": "string",
  "activated_date": "2019-08-24T14:15:22Z",
  "activated_by": "string",
  "stock_in_date": "2019-08-24T14:15:22Z",
  "stock_in_by": "string",
  "procurement_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "line_item_id": 0,
      "sku": "string",
      "barcode": "string",
      "variant": "string",
      "variant_image": "string",
      "variant_id": 0,
      "retail_price": 0,
      "ordered_quantity": 0,
      "accepted_quantity": 0,
      "planned_quantity": 0,
      "quantity": 0,
      "real_quantity": 0,
      "note": "string",
      "procurement_id": 0
    }
  ],
  "refer_ids": [
    0
  ]
}
```

<h3 id="createmanualprocurement-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|purchase_order_id|path|integer(int64)|true|none|
|body|body|[ProcurementRequest](#schemaprocurementrequest)|true|none|

> Example responses

> 200 Response

<h3 id="createmanualprocurement-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## searchProcurement

<a id="opIdsearchProcurement"></a>

> Code samples

`GET /purchase-orders/procurements`

<h3 id="searchprocurement-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|none|
|limit|query|integer(int32)|false|none|
|sort_type|query|string|false|none|
|sort_column|query|string|false|none|
|content|query|string|false|none|
|active_from|query|string(date-time)|false|none|
|active_to|query|string(date-time)|false|none|
|active_by|query|string|false|none|
|stock_in_from|query|string(date-time)|false|none|
|stock_in_to|query|string(date-time)|false|none|
|stock_in_by|query|string|false|none|
|merchandisers|query|array[string]|false|none|
|status|query|array[string]|false|none|
|stores|query|array[integer]|false|none|
|is_cancel|query|boolean|false|none|
|suppliers|query|array[integer]|false|none|
|expect_receipt_from|query|string(date-time)|false|none|
|expect_receipt_to|query|string(date-time)|false|none|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|

> Example responses

> 200 Response

<h3 id="searchprocurement-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPageableDtoProcurementDto](#schemaresultpageabledtoprocurementdto)|

<aside class="success">
This operation does not require authentication
</aside>

## searchProcurementMerge

<a id="opIdsearchProcurementMerge"></a>

> Code samples

`GET /purchase-orders/procurements/merge`

<h3 id="searchprocurementmerge-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|ids|query|array[integer]|true|none|

> Example responses

> 200 Response

<h3 id="searchprocurementmerge-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultProcurementDto](#schemaresultprocurementdto)|

<aside class="success">
This operation does not require authentication
</aside>

## searchProcurement_1

<a id="opIdsearchProcurement_1"></a>

> Code samples

`GET /purchase-orders/procurements/items`

<h3 id="searchprocurement_1-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|none|
|limit|query|integer(int32)|false|none|
|sort_type|query|string|false|none|
|sort_column|query|string|false|none|
|content|query|string|false|none|
|stores|query|array[integer]|false|none|
|stock_in_date_from|query|string(date-time)|false|none|
|stock_in_date_to|query|string(date-time)|false|none|
|stock_in_by|query|string|false|none|
|note|query|string|false|none|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|

> Example responses

> 200 Response

<h3 id="searchprocurement_1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPageableDtoProcurementItemCustomDto](#schemaresultpageabledtoprocurementitemcustomdto)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="openapi-definition-payment-controller">payment-controller</h1>

## update

<a id="opIdupdate"></a>

> Code samples

`PUT /purchase-orders/{purchase_order_id}/payments/{payment_id}`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "amount": 0,
  "reference": "string",
  "payment_method_code": "string",
  "status": "string",
  "status_name": "string",
  "transaction_date": "2019-08-24T14:15:22Z",
  "is_refund": true,
  "purchase_order_id": 0,
  "note": "string"
}
```

<h3 id="update-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|purchase_order_id|path|integer(int64)|true|none|
|payment_id|path|integer(int64)|true|none|
|body|body|[PaymentRequest](#schemapaymentrequest)|true|none|

> Example responses

> 200 Response

<h3 id="update-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## delete_2

<a id="opIddelete_2"></a>

> Code samples

`DELETE /purchase-orders/{purchase_order_id}/payments/{payment_id}`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string"
}
```

<h3 id="delete_2-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|purchase_order_id|path|integer(int64)|true|none|
|payment_id|path|integer(int64)|true|none|
|body|body|[BasicRequest](#schemabasicrequest)|true|none|

> Example responses

> 200 Response

<h3 id="delete_2-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultString](#schemaresultstring)|

<aside class="success">
This operation does not require authentication
</aside>

## updateStatus_1

<a id="opIdupdateStatus_1"></a>

> Code samples

`PUT /purchase-orders/{purchase_order_id}/financial-status/finish`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string"
}
```

<h3 id="updatestatus_1-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|purchase_order_id|path|integer(int64)|true|none|
|body|body|[BasicRequest](#schemabasicrequest)|true|none|

> Example responses

> 200 Response

<h3 id="updatestatus_1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## createPayment

<a id="opIdcreatePayment"></a>

> Code samples

`POST /purchase-orders/{purchase_order_id}/payments`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "amount": 0,
  "reference": "string",
  "payment_method_code": "string",
  "status": "string",
  "status_name": "string",
  "transaction_date": "2019-08-24T14:15:22Z",
  "is_refund": true,
  "purchase_order_id": 0,
  "note": "string"
}
```

<h3 id="createpayment-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|purchase_order_id|path|integer(int64)|true|none|
|body|body|[PaymentRequest](#schemapaymentrequest)|true|none|

> Example responses

> 200 Response

<h3 id="createpayment-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="openapi-definition-purchase-order-controller">purchase-order-controller</h1>

## getPurchaseOrder

<a id="opIdgetPurchaseOrder"></a>

> Code samples

`GET /purchase-orders/{id}`

<h3 id="getpurchaseorder-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|none|

> Example responses

> 200 Response

<h3 id="getpurchaseorder-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## update_1

<a id="opIdupdate_1"></a>

> Code samples

`PUT /purchase-orders/{id}`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "company_id": 0,
  "merchandiser_code": "string",
  "merchandiser": "string",
  "designer_code": "string",
  "designer": "string",
  "qc_code": "string",
  "qc": "string",
  "reference": "string",
  "type": "string",
  "supplier_id": 0,
  "supplier_code": "string",
  "supplier": "string",
  "phone": "string",
  "supplier_note": "string",
  "billing_address": {
    "created_by": "string",
    "created_name": "string",
    "updated_by": "string",
    "updated_name": "string",
    "request_id": "string",
    "operator_kc_id": "string",
    "id": 0,
    "name": "string",
    "email": "string",
    "phone": "string",
    "tax_code": "string",
    "country_id": 0,
    "country": "string",
    "city_id": 0,
    "city": "string",
    "district_id": 0,
    "district": "string",
    "ward_id": 0,
    "ward": "string",
    "zip_code": "string",
    "full_address": "string",
    "bank_number": "string",
    "bank_name": "string",
    "beneficiary": "string",
    "position": "string"
  },
  "supplier_address": {
    "created_by": "string",
    "created_name": "string",
    "updated_by": "string",
    "updated_name": "string",
    "request_id": "string",
    "operator_kc_id": "string",
    "id": 0,
    "name": "string",
    "email": "string",
    "phone": "string",
    "tax_code": "string",
    "country_id": 0,
    "country": "string",
    "city_id": 0,
    "city": "string",
    "district_id": 0,
    "district": "string",
    "ward_id": 0,
    "ward": "string",
    "zip_code": "string",
    "full_address": "string",
    "bank_number": "string",
    "bank_name": "string",
    "beneficiary": "string",
    "position": "string"
  },
  "line_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "code": "string",
      "sku": "string",
      "variant_id": 0,
      "barcode": "string",
      "product_id": 0,
      "product": "string",
      "variant": "string",
      "retail_price": 0,
      "product_type": "string",
      "quantity": 0,
      "receipt_quantity": 0,
      "planned_quantity": 0,
      "price": 0,
      "amount": 0,
      "note": "string",
      "type": "string",
      "variant_image": "string",
      "unit": "string",
      "tax": 0,
      "tax_rate": 0,
      "line_amount_after_line_discount": 0,
      "discount_rate": 0,
      "discount_value": 0,
      "discount_amount": 0,
      "position": 0,
      "purchase_order_id": 0
    }
  ],
  "expect_import_date": "2019-08-24T14:15:22Z",
  "expect_store_id": 0,
  "expect_store": "string",
  "payment_condition_id": 0,
  "payment_condition_name": "string",
  "payment_note": "string",
  "note": "string",
  "tags": "string",
  "policy_price_code": "string",
  "tax_included": true,
  "payments": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "amount": 0,
      "reference": "string",
      "payment_method_code": "string",
      "status": "string",
      "status_name": "string",
      "transaction_date": "2019-08-24T14:15:22Z",
      "is_refund": true,
      "purchase_order_id": 0,
      "note": "string"
    }
  ],
  "procurements": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "code": "string",
      "reference": "string",
      "store_id": 0,
      "store": "string",
      "expect_receipt_date": "2019-08-24T14:15:22Z",
      "note": "string",
      "status": "string",
      "status_name": "string",
      "activated_date": "2019-08-24T14:15:22Z",
      "activated_by": "string",
      "stock_in_date": "2019-08-24T14:15:22Z",
      "stock_in_by": "string",
      "procurement_items": [
        {
          "created_by": "string",
          "created_name": "string",
          "updated_by": "string",
          "updated_name": "string",
          "request_id": "string",
          "operator_kc_id": "string",
          "id": 0,
          "line_item_id": 0,
          "sku": "string",
          "barcode": "string",
          "variant": "string",
          "variant_image": "string",
          "variant_id": 0,
          "retail_price": 0,
          "ordered_quantity": 0,
          "accepted_quantity": 0,
          "planned_quantity": 0,
          "quantity": 0,
          "real_quantity": 0,
          "note": "string",
          "procurement_id": 0
        }
      ],
      "refer_ids": [
        0
      ]
    }
  ],
  "payment_discount_rate": 0,
  "payment_discount_value": 0,
  "payment_discount_amount": 0,
  "trade_discount_rate": 0,
  "trade_discount_value": 0,
  "trade_discount_amount": 0,
  "cost_lines": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "title": "string",
      "amount": 0
    }
  ],
  "untaxed_amount": 0,
  "tax": 0,
  "total": 0,
  "total_paid": 0,
  "total_refunds": 0,
  "receipt_quantity": 0,
  "planned_quantity": 0,
  "status": "string",
  "financial_status": "string",
  "receive_status": "string",
  "cancel_reason": "string",
  "is_grid_mode": true,
  "is_grid_mode_supplement": true,
  "version": 0
}
```

<h3 id="update_1-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|id|path|integer(int64)|true|none|
|body|body|[UpdatePurchaseOrderRequest](#schemaupdatepurchaseorderrequest)|true|none|

> Example responses

> 200 Response

<h3 id="update_1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## updateNotes

<a id="opIdupdateNotes"></a>

> Code samples

`PUT /purchase-orders/{id}/notes`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "note": "string",
  "supplier_note": "string"
}
```

<h3 id="updatenotes-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|id|path|integer(int64)|true|none|
|body|body|[UpdateNotesRequest](#schemaupdatenotesrequest)|true|none|

> Example responses

> 200 Response

<h3 id="updatenotes-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## cancel

<a id="opIdcancel"></a>

> Code samples

`PUT /purchase-orders/{id}/cancel`

<h3 id="cancel-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|id|path|integer(int64)|true|none|

> Example responses

> 200 Response

<h3 id="cancel-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## search

<a id="opIdsearch"></a>

> Code samples

`GET /purchase-orders`

<h3 id="search-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|none|
|limit|query|integer(int32)|false|none|
|sort_type|query|string|false|none|
|sort_column|query|string|false|none|
|info|query|string|false|none|
|from_order_date|query|string(date-time)|false|none|
|to_order_date|query|string(date-time)|false|none|
|from_cancelled_date|query|string(date-time)|false|none|
|to_cancelled_date|query|string(date-time)|false|none|
|from_activated_date|query|string(date-time)|false|none|
|to_activated_date|query|string(date-time)|false|none|
|from_completed_date|query|string(date-time)|false|none|
|to_completed_date|query|string(date-time)|false|none|
|from_expect_import_date|query|string(date-time)|false|none|
|to_expect_import_date|query|string(date-time)|false|none|
|expect_store|query|string|false|none|
|status|query|string|false|none|
|financial_status|query|string|false|none|
|receive_status|query|string|false|none|
|merchandiser|query|string|false|none|
|qc|query|string|false|none|
|cost_included|query|boolean|false|none|
|tax_included|query|boolean|false|none|
|is_have_returned|query|boolean|false|none|
|note|query|string|false|none|
|supplier_note|query|string|false|none|
|tags|query|string|false|none|
|reference|query|string|false|none|
|ids|query|string|false|none|

> Example responses

> 200 Response

<h3 id="search-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPageableDtoSimplePurchaseOrderDto](#schemaresultpageabledtosimplepurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## create

<a id="opIdcreate"></a>

> Code samples

`POST /purchase-orders`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "company_id": 0,
  "merchandiser_code": "string",
  "merchandiser": "string",
  "designer_code": "string",
  "designer": "string",
  "qc_code": "string",
  "qc": "string",
  "reference": "string",
  "type": "string",
  "supplier_id": 0,
  "supplier_code": "string",
  "supplier": "string",
  "phone": "string",
  "supplier_note": "string",
  "billing_address": {
    "created_by": "string",
    "created_name": "string",
    "updated_by": "string",
    "updated_name": "string",
    "request_id": "string",
    "operator_kc_id": "string",
    "id": 0,
    "name": "string",
    "email": "string",
    "phone": "string",
    "tax_code": "string",
    "country_id": 0,
    "country": "string",
    "city_id": 0,
    "city": "string",
    "district_id": 0,
    "district": "string",
    "ward_id": 0,
    "ward": "string",
    "zip_code": "string",
    "full_address": "string",
    "bank_number": "string",
    "bank_name": "string",
    "beneficiary": "string",
    "position": "string"
  },
  "supplier_address": {
    "created_by": "string",
    "created_name": "string",
    "updated_by": "string",
    "updated_name": "string",
    "request_id": "string",
    "operator_kc_id": "string",
    "id": 0,
    "name": "string",
    "email": "string",
    "phone": "string",
    "tax_code": "string",
    "country_id": 0,
    "country": "string",
    "city_id": 0,
    "city": "string",
    "district_id": 0,
    "district": "string",
    "ward_id": 0,
    "ward": "string",
    "zip_code": "string",
    "full_address": "string",
    "bank_number": "string",
    "bank_name": "string",
    "beneficiary": "string",
    "position": "string"
  },
  "line_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "code": "string",
      "sku": "string",
      "variant_id": 0,
      "barcode": "string",
      "product_id": 0,
      "product": "string",
      "variant": "string",
      "retail_price": 0,
      "product_type": "string",
      "quantity": 0,
      "receipt_quantity": 0,
      "planned_quantity": 0,
      "price": 0,
      "amount": 0,
      "note": "string",
      "type": "string",
      "variant_image": "string",
      "unit": "string",
      "tax": 0,
      "tax_rate": 0,
      "line_amount_after_line_discount": 0,
      "discount_rate": 0,
      "discount_value": 0,
      "discount_amount": 0,
      "position": 0,
      "purchase_order_id": 0
    }
  ],
  "expect_import_date": "2019-08-24T14:15:22Z",
  "expect_store_id": 0,
  "expect_store": "string",
  "payment_condition_id": 0,
  "payment_condition_name": "string",
  "payment_note": "string",
  "note": "string",
  "tags": "string",
  "policy_price_code": "string",
  "tax_included": true,
  "payments": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "amount": 0,
      "reference": "string",
      "payment_method_code": "string",
      "status": "string",
      "status_name": "string",
      "transaction_date": "2019-08-24T14:15:22Z",
      "is_refund": true,
      "purchase_order_id": 0,
      "note": "string"
    }
  ],
  "procurements": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "code": "string",
      "reference": "string",
      "store_id": 0,
      "store": "string",
      "expect_receipt_date": "2019-08-24T14:15:22Z",
      "note": "string",
      "status": "string",
      "status_name": "string",
      "activated_date": "2019-08-24T14:15:22Z",
      "activated_by": "string",
      "stock_in_date": "2019-08-24T14:15:22Z",
      "stock_in_by": "string",
      "procurement_items": [
        {
          "created_by": "string",
          "created_name": "string",
          "updated_by": "string",
          "updated_name": "string",
          "request_id": "string",
          "operator_kc_id": "string",
          "id": 0,
          "line_item_id": 0,
          "sku": "string",
          "barcode": "string",
          "variant": "string",
          "variant_image": "string",
          "variant_id": 0,
          "retail_price": 0,
          "ordered_quantity": 0,
          "accepted_quantity": 0,
          "planned_quantity": 0,
          "quantity": 0,
          "real_quantity": 0,
          "note": "string",
          "procurement_id": 0
        }
      ],
      "refer_ids": [
        0
      ]
    }
  ],
  "payment_discount_rate": 0,
  "payment_discount_value": 0,
  "payment_discount_amount": 0,
  "trade_discount_rate": 0,
  "trade_discount_value": 0,
  "trade_discount_amount": 0,
  "cost_lines": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "title": "string",
      "amount": 0
    }
  ],
  "untaxed_amount": 0,
  "tax": 0,
  "total": 0,
  "total_paid": 0,
  "total_refunds": 0,
  "receipt_quantity": 0,
  "planned_quantity": 0,
  "status": "string",
  "financial_status": "string",
  "receive_status": "string",
  "cancel_reason": "string",
  "is_grid_mode": true,
  "is_grid_mode_supplement": true
}
```

<h3 id="create-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|body|body|[CreatePurchaseOrderRequest](#schemacreatepurchaseorderrequest)|true|none|

> Example responses

> 200 Response

<h3 id="create-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## delete

<a id="opIddelete"></a>

> Code samples

`DELETE /purchase-orders`

<h3 id="delete-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|ids|query|array[integer]|true|none|

> Example responses

> 200 Response

<h3 id="delete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultString](#schemaresultstring)|

<aside class="success">
This operation does not require authentication
</aside>

## updateVariantPurchaseOrderLines

<a id="opIdupdateVariantPurchaseOrderLines"></a>

> Code samples

`POST /purchase-orders/migration-variant-po-lines`

> Example responses

> 200 Response

<h3 id="updatevariantpurchaseorderlines-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultString](#schemaresultstring)|

<aside class="success">
This operation does not require authentication
</aside>

## migrateUpdateStatusProcurementForCutOff

<a id="opIdmigrateUpdateStatusProcurementForCutOff"></a>

> Code samples

`POST /purchase-orders/migration-status-procurement-cutoff`

> Body parameter

```json
{
  "file_upload": "string"
}
```

<h3 id="migrateupdatestatusprocurementforcutoff-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» file_upload|body|string(binary)|false|none|

> Example responses

> 200 Response

<h3 id="migrateupdatestatusprocurementforcutoff-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultListString](#schemaresultliststring)|

<aside class="success">
This operation does not require authentication
</aside>

## migrateDataPoFromNhanh

<a id="opIdmigrateDataPoFromNhanh"></a>

> Code samples

`POST /purchase-orders/migration-po`

> Body parameter

```json
{
  "file_upload": "string"
}
```

<h3 id="migratedatapofromnhanh-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» file_upload|body|string(binary)|false|none|

> Example responses

> 200 Response

<h3 id="migratedatapofromnhanh-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultListString](#schemaresultliststring)|

<aside class="success">
This operation does not require authentication
</aside>

## printProcurement

<a id="opIdprintProcurement"></a>

> Code samples

`GET /purchase-orders/print-procurement`

<h3 id="printprocurement-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|query|integer(int64)|true|none|
|poId|query|integer(int64)|true|none|
|storeId|query|integer(int64)|false|none|
|print_type|query|string|false|none|

> Example responses

> 200 Response

<h3 id="printprocurement-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ProcurementPrintForm](#schemaprocurementprintform)|

<aside class="success">
This operation does not require authentication
</aside>

## printFrom

<a id="opIdprintFrom"></a>

> Code samples

`GET /purchase-orders/print-forms`

<h3 id="printfrom-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|ids|query|array[integer]|true|none|
|storeId|query|integer(int64)|false|none|
|print_type|query|string|false|none|

> Example responses

> 200 Response

<h3 id="printfrom-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|Inline|

<h3 id="printfrom-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[[PurchaseOrderPrintForm](#schemapurchaseorderprintform)]|false|none|none|
|» purchaseOrderId|integer(int64)|false|none|none|
|» htmlContent|string|false|none|none|
|» size|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## getPurchaseOrder_1

<a id="opIdgetPurchaseOrder_1"></a>

> Code samples

`GET /purchase-orders/list`

<h3 id="getpurchaseorder_1-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|ids|query|array[integer]|true|none|

> Example responses

> 200 Response

<h3 id="getpurchaseorder_1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultListPurchaseOrderDto](#schemaresultlistpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## findAllPoBySupplierIdToCreateProcurementManual

<a id="opIdfindAllPoBySupplierIdToCreateProcurementManual"></a>

> Code samples

`GET /purchase-orders/list-by-supplier/{id}`

<h3 id="findallpobysupplieridtocreateprocurementmanual-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|none|
|condition|query|string|false|none|

> Example responses

> 200 Response

<h3 id="findallpobysupplieridtocreateprocurementmanual-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultListPurchaseOrderDto](#schemaresultlistpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## findPurchaseOrderAlmostRight

<a id="opIdfindPurchaseOrderAlmostRight"></a>

> Code samples

`GET /purchase-orders/almost-right`

<h3 id="findpurchaseorderalmostright-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|sku|query|string|true|none|
|supplier_id|query|integer(int64)|true|none|

> Example responses

> 200 Response

<h3 id="findpurchaseorderalmostright-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultListPurchaseOrderDto](#schemaresultlistpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="openapi-definition-payment-condition-controller">payment-condition-controller</h1>

## getPaymentCondition

<a id="opIdgetPaymentCondition"></a>

> Code samples

`GET /payment-conditions/{id}`

<h3 id="getpaymentcondition-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|none|

> Example responses

> 200 Response

<h3 id="getpaymentcondition-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPaymentConditionDto](#schemaresultpaymentconditiondto)|

<aside class="success">
This operation does not require authentication
</aside>

## update_2

<a id="opIdupdate_2"></a>

> Code samples

`PUT /payment-conditions/{id}`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "code": "string",
  "timeout": 0,
  "note": "string",
  "default": true
}
```

<h3 id="update_2-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|none|
|body|body|[PaymentConditionRequest](#schemapaymentconditionrequest)|true|none|

> Example responses

> 200 Response

<h3 id="update_2-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

## delete_3

<a id="opIddelete_3"></a>

> Code samples

`DELETE /payment-conditions/{id}`

<h3 id="delete_3-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|none|

> Example responses

> 200 Response

<h3 id="delete_3-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultString](#schemaresultstring)|

<aside class="success">
This operation does not require authentication
</aside>

## search_1

<a id="opIdsearch_1"></a>

> Code samples

`GET /payment-conditions`

> Example responses

> 200 Response

<h3 id="search_1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultListPaymentConditionDto](#schemaresultlistpaymentconditiondto)|

<aside class="success">
This operation does not require authentication
</aside>

## create_1

<a id="opIdcreate_1"></a>

> Code samples

`POST /payment-conditions`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "code": "string",
  "timeout": 0,
  "note": "string",
  "default": true
}
```

<h3 id="create_1-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[PaymentConditionRequest](#schemapaymentconditionrequest)|true|none|

> Example responses

> 200 Response

<h3 id="create_1-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPaymentConditionDto](#schemaresultpaymentconditiondto)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="openapi-definition-purchase-order-return-controller">purchase-order-return-controller</h1>

## createPurchaseOrderReturn

<a id="opIdcreatePurchaseOrderReturn"></a>

> Code samples

`POST /purchase-orders/{purchaseOrderId}/return`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "store_id": 0,
  "line_return_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "code": "string",
      "sku": "string",
      "barcode": "string",
      "variant_id": 0,
      "product_id": 0,
      "product": "string",
      "variant": "string",
      "retail_price": 0,
      "product_type": "string",
      "quantity": 0,
      "quantity_return": 0,
      "receipt_quantity": 0,
      "planned_quantity": 0,
      "price": 0,
      "amount": 0,
      "note": "string",
      "type": "string",
      "variant_image": "string",
      "unit": "string",
      "tax": 0,
      "tax_rate": 0,
      "line_amount_after_line_discount": 0,
      "discount_rate": 0,
      "discount_value": 0,
      "discount_amount": 0,
      "position": 0,
      "purchase_order_id": 0
    }
  ],
  "expect_return_date": "2019-08-24T14:15:22Z",
  "untaxed_amount_refunds": 0,
  "amount_tax_refunds": 0,
  "total_refunds": 0,
  "return_reason": "string",
  "payment_return_note": "string",
  "payments": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "amount": 0,
      "reference": "string",
      "payment_method_code": "string",
      "status": "string",
      "status_name": "string",
      "transaction_date": "2019-08-24T14:15:22Z",
      "is_refund": true,
      "purchase_order_id": 0,
      "note": "string"
    }
  ]
}
```

<h3 id="createpurchaseorderreturn-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|purchaseOrderId|path|integer(int64)|true|none|
|body|body|[PurchaseOrderReturnRequest](#schemapurchaseorderreturnrequest)|true|none|

> Example responses

> 200 Response

<h3 id="createpurchaseorderreturn-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDto](#schemaresultpurchaseorderdto)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="openapi-definition-purchase-order-draft-controller">purchase-order-draft-controller</h1>

## createOrUpdateDraft

<a id="opIdcreateOrUpdateDraft"></a>

> Code samples

`POST /purchase-orders-draft`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "data": "string"
}
```

<h3 id="createorupdatedraft-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|body|body|[CreatePurchaseOrderDraftRequest](#schemacreatepurchaseorderdraftrequest)|true|none|

> Example responses

> 200 Response

<h3 id="createorupdatedraft-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDraftDto](#schemaresultpurchaseorderdraftdto)|

<aside class="success">
This operation does not require authentication
</aside>

## getPurchaseOrderDraftByUsername

<a id="opIdgetPurchaseOrderDraftByUsername"></a>

> Code samples

`GET /purchase-orders-draft/created-by/{username}`

<h3 id="getpurchaseorderdraftbyusername-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|username|path|string|true|none|

> Example responses

> 200 Response

<h3 id="getpurchaseorderdraftbyusername-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderDraftDto](#schemaresultpurchaseorderdraftdto)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="openapi-definition-job-engine-controller">job-engine-controller</h1>

## createJobImport

<a id="opIdcreateJobImport"></a>

> Code samples

`POST /excel/job/import`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "conditions": "string",
  "type": "string",
  "hidden_fields": "string",
  "url": "string",
  "note": "string"
}
```

<h3 id="createjobimport-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|body|body|[CreateImportJobRequest](#schemacreateimportjobrequest)|true|none|

> Example responses

> 200 Response

<h3 id="createjobimport-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultJobDto](#schemaresultjobdto)|

<aside class="success">
This operation does not require authentication
</aside>

## createJobExport

<a id="opIdcreateJobExport"></a>

> Code samples

`POST /excel/job/export`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "conditions": "string",
  "type": "string",
  "hidden_fields": "string",
  "url": "string",
  "url_template": "string"
}
```

<h3 id="createjobexport-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateExportJobRequest](#schemacreateexportjobrequest)|true|none|

> Example responses

> 200 Response

<h3 id="createjobexport-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultJobDto](#schemaresultjobdto)|

<aside class="success">
This operation does not require authentication
</aside>

## get

<a id="opIdget"></a>

> Code samples

`GET /excel/job/{code}`

<h3 id="get-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|code|path|string|true|none|

> Example responses

> 200 Response

<h3 id="get-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultJobDto](#schemaresultjobdto)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="openapi-definition-purchase-order-config-controller">purchase-order-config-controller</h1>

## createConfigFilter

<a id="opIdcreateConfigFilter"></a>

> Code samples

`POST /config`

> Body parameter

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "json_content": "string",
  "name": "string",
  "type": "string"
}
```

<h3 id="createconfigfilter-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|
|body|body|[PurchaseOrderConfigRequest](#schemapurchaseorderconfigrequest)|true|none|

> Example responses

> 200 Response

<h3 id="createconfigfilter-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderConfigDto](#schemaresultpurchaseorderconfigdto)|

<aside class="success">
This operation does not require authentication
</aside>

## getConfigs

<a id="opIdgetConfigs"></a>

> Code samples

`GET /config/{userCode}`

<h3 id="getconfigs-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|userCode|path|string|true|none|

> Example responses

> 200 Response

<h3 id="getconfigs-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultListPurchaseOrderConfigDto](#schemaresultlistpurchaseorderconfigdto)|

<aside class="success">
This operation does not require authentication
</aside>

## deleteConfig

<a id="opIddeleteConfig"></a>

> Code samples

`DELETE /config/{id}`

<h3 id="deleteconfig-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|none|

> Example responses

> 200 Response

<h3 id="deleteconfig-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderConfigDto](#schemaresultpurchaseorderconfigdto)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="openapi-definition-purchase-order-log-controller">purchase-order-log-controller</h1>

## Lấy toàn bộ log đơn nhập hàng qua mã đơn nhập hàng

<a id="opIdfindAllByPurchaseOrderId"></a>

> Code samples

`GET /purchase-orders/{id}/log`

<h3 id="lấy-toàn-bộ-log-đơn-nhập-hàng-qua-mã-đơn-nhập-hàng-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|none|

> Example responses

> 200 Response

<h3 id="lấy-toàn-bộ-log-đơn-nhập-hàng-qua-mã-đơn-nhập-hàng-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultListPurchaseOrderLogDto](#schemaresultlistpurchaseorderlogdto)|

<aside class="success">
This operation does not require authentication
</aside>

## Lấy chi tiết log đơn nhập hàng

<a id="opIdgetPurchaseOrderDetail"></a>

> Code samples

`GET /purchase-orders/log/{id}`

<h3 id="lấy-chi-tiết-log-đơn-nhập-hàng-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|none|

> Example responses

> 200 Response

<h3 id="lấy-chi-tiết-log-đơn-nhập-hàng-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultObject](#schemaresultobject)|

<aside class="success">
This operation does not require authentication
</aside>

## Lấy toàn bộ log phiếu nhập kho theo mã phiếu nhập

<a id="opIdfindAllByProcurementCode"></a>

> Code samples

`GET /procurements/{code}/log`

<h3 id="lấy-toàn-bộ-log-phiếu-nhập-kho-theo-mã-phiếu-nhập-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|code|path|string|true|none|

> Example responses

> 200 Response

<h3 id="lấy-toàn-bộ-log-phiếu-nhập-kho-theo-mã-phiếu-nhập-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultListPurchaseOrderLogDto](#schemaresultlistpurchaseorderlogdto)|

<aside class="success">
This operation does not require authentication
</aside>

## Lấy all phiếu nhập kho

<a id="opIdgetProcurementLogsDetail"></a>

> Code samples

`GET /procurements/logs`

<h3 id="lấy-all-phiếu-nhập-kho-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|none|
|limit|query|integer(int32)|false|none|
|sort_type|query|string|false|none|
|sort_column|query|string|false|none|
|condition|query|string|false|none|
|created_date_from|query|string(date-time)|false|none|
|created_date_to|query|string(date-time)|false|none|
|x-user-name|header|string|false|none|
|x-user-code|header|string|false|none|

> Example responses

> 200 Response

<h3 id="lấy-all-phiếu-nhập-kho-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPageableDtoPurchaseOrderLogDto](#schemaresultpageabledtopurchaseorderlogdto)|

<aside class="success">
This operation does not require authentication
</aside>

## Lấy chi tiết log phiếu nhập kho

<a id="opIdgetProcurementLogsDetail_1"></a>

> Code samples

`GET /procurements/log/{id}`

<h3 id="lấy-chi-tiết-log-phiếu-nhập-kho-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int64)|true|none|

> Example responses

> 200 Response

<h3 id="lấy-chi-tiết-log-phiếu-nhập-kho-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[ResultPurchaseOrderLogDto](#schemaresultpurchaseorderlogdto)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="openapi-definition-health-check-controller">health-check-controller</h1>

## ping

<a id="opIdping"></a>

> Code samples

`GET /ping`

> Example responses

> 200 Response

<h3 id="ping-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|string|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_AddressDto">AddressDto</h2>
<!-- backwards compatibility -->
<a id="schemaaddressdto"></a>
<a id="schema_AddressDto"></a>
<a id="tocSaddressdto"></a>
<a id="tocsaddressdto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "name": "string",
  "email": "string",
  "phone": "string",
  "tax_code": "string",
  "country_id": 0,
  "country": "string",
  "city_id": 0,
  "city": "string",
  "district_id": 0,
  "district": "string",
  "ward_id": 0,
  "ward": "string",
  "zip_code": "string",
  "full_address": "string",
  "bank_number": "string",
  "bank_name": "string",
  "beneficiary": "string",
  "position": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|name|string|false|none|none|
|email|string|false|none|none|
|phone|string|false|none|none|
|tax_code|string|false|none|none|
|country_id|integer(int64)|false|none|none|
|country|string|false|none|none|
|city_id|integer(int64)|false|none|none|
|city|string|false|none|none|
|district_id|integer(int64)|false|none|none|
|district|string|false|none|none|
|ward_id|integer(int64)|false|none|none|
|ward|string|false|none|none|
|zip_code|string|false|none|none|
|full_address|string|false|none|none|
|bank_number|string|false|none|none|
|bank_name|string|false|none|none|
|beneficiary|string|false|none|none|
|position|string|false|none|none|

<h2 id="tocS_CostDto">CostDto</h2>
<!-- backwards compatibility -->
<a id="schemacostdto"></a>
<a id="schema_CostDto"></a>
<a id="tocScostdto"></a>
<a id="tocscostdto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "title": "string",
  "amount": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|title|string|false|none|none|
|amount|number|false|none|none|

<h2 id="tocS_PaymentDto">PaymentDto</h2>
<!-- backwards compatibility -->
<a id="schemapaymentdto"></a>
<a id="schema_PaymentDto"></a>
<a id="tocSpaymentdto"></a>
<a id="tocspaymentdto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "account_code": "string",
  "amount": 0,
  "reference": "string",
  "payment_method_code": "string",
  "payment_method": "string",
  "status": "string",
  "status_name": "string",
  "note": "string",
  "is_refund": true,
  "purchase_order_id": 0,
  "transaction_date": "2019-08-24T14:15:22Z",
  "transaction_date_string": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|account_code|string|false|none|none|
|amount|number|false|none|none|
|reference|string|false|none|none|
|payment_method_code|string|false|none|none|
|payment_method|string|false|none|none|
|status|string|false|none|none|
|status_name|string|false|none|none|
|note|string|false|none|none|
|is_refund|boolean|false|none|none|
|purchase_order_id|integer(int64)|false|none|none|
|transaction_date|string(date-time)|false|none|none|
|transaction_date_string|string|false|none|none|

<h2 id="tocS_PaymentRefundsDto">PaymentRefundsDto</h2>
<!-- backwards compatibility -->
<a id="schemapaymentrefundsdto"></a>
<a id="schema_PaymentRefundsDto"></a>
<a id="tocSpaymentrefundsdto"></a>
<a id="tocspaymentrefundsdto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "account_code": "string",
  "amount": 0,
  "reference": "string",
  "payment_method_code": "string",
  "status": "string",
  "status_name": "string",
  "note": "string",
  "purchase_order_id": 0,
  "transaction_date": "2019-08-24T14:15:22Z"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|account_code|string|false|none|none|
|amount|number|false|none|none|
|reference|string|false|none|none|
|payment_method_code|string|false|none|none|
|status|string|false|none|none|
|status_name|string|false|none|none|
|note|string|false|none|none|
|purchase_order_id|integer(int64)|false|none|none|
|transaction_date|string(date-time)|false|none|none|

<h2 id="tocS_ProcurementDto">ProcurementDto</h2>
<!-- backwards compatibility -->
<a id="schemaprocurementdto"></a>
<a id="schema_ProcurementDto"></a>
<a id="tocSprocurementdto"></a>
<a id="tocsprocurementdto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "reference": "string",
  "store_id": 0,
  "store": "string",
  "expect_receipt_date": "2019-08-24T14:15:22Z",
  "note": "string",
  "status": "string",
  "status_name": "string",
  "activated_date": "2019-08-24T14:15:22Z",
  "activated_by": "string",
  "stock_in_date": "2019-08-24T14:15:22Z",
  "stock_in_by": "string",
  "is_cancelled": true,
  "created_date_str": "string",
  "purchase_order": {
    "id": 0,
    "company_id": 0,
    "merchandiser_code": "string",
    "merchandiser": "string",
    "designer_code": "string",
    "designer": "string",
    "qc_code": "string",
    "qc": "string",
    "reference": "string",
    "type": "string",
    "code": "string",
    "supplier_id": 0,
    "supplier_code": "string",
    "supplier": "string",
    "phone": "string"
  },
  "procurement_items": [
    {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "line_item_id": 0,
      "sku": "string",
      "barcode": "string",
      "variant": "string",
      "variant_image": "string",
      "variant_id": 0,
      "retail_price": 0,
      "ordered_quantity": 0,
      "accepted_quantity": 0,
      "planned_quantity": 0,
      "quantity": 0,
      "real_quantity": 0,
      "note": "string",
      "price": 0,
      "vat": 0,
      "vat_rate": 0,
      "amount": 0
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|reference|string|false|none|none|
|store_id|integer(int64)|false|none|none|
|store|string|false|none|none|
|expect_receipt_date|string(date-time)|false|none|none|
|note|string|false|none|none|
|status|string|false|none|none|
|status_name|string|false|none|none|
|activated_date|string(date-time)|false|none|none|
|activated_by|string|false|none|none|
|stock_in_date|string(date-time)|false|none|none|
|stock_in_by|string|false|none|none|
|is_cancelled|boolean|false|none|none|
|created_date_str|string|false|none|none|
|purchase_order|[PurchaseOrderProcurementDto](#schemapurchaseorderprocurementdto)|false|none|none|
|procurement_items|[[ProcurementItemDto](#schemaprocurementitemdto)]|false|none|none|

<h2 id="tocS_ProcurementItemDto">ProcurementItemDto</h2>
<!-- backwards compatibility -->
<a id="schemaprocurementitemdto"></a>
<a id="schema_ProcurementItemDto"></a>
<a id="tocSprocurementitemdto"></a>
<a id="tocsprocurementitemdto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "line_item_id": 0,
  "sku": "string",
  "barcode": "string",
  "variant": "string",
  "variant_image": "string",
  "variant_id": 0,
  "retail_price": 0,
  "ordered_quantity": 0,
  "accepted_quantity": 0,
  "planned_quantity": 0,
  "quantity": 0,
  "real_quantity": 0,
  "note": "string",
  "price": 0,
  "vat": 0,
  "vat_rate": 0,
  "amount": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|line_item_id|integer(int64)|false|none|none|
|sku|string|false|none|none|
|barcode|string|false|none|none|
|variant|string|false|none|none|
|variant_image|string|false|none|none|
|variant_id|integer(int64)|false|none|none|
|retail_price|number|false|none|none|
|ordered_quantity|number|false|none|none|
|accepted_quantity|number|false|none|none|
|planned_quantity|number|false|none|none|
|quantity|number|false|none|none|
|real_quantity|number|false|none|none|
|note|string|false|none|none|
|price|number|false|none|none|
|vat|number|false|none|none|
|vat_rate|number(float)|false|none|none|
|amount|number|false|none|none|

<h2 id="tocS_ProductCompositeDto">ProductCompositeDto</h2>
<!-- backwards compatibility -->
<a id="schemaproductcompositedto"></a>
<a id="schema_ProductCompositeDto"></a>
<a id="tocSproductcompositedto"></a>
<a id="tocsproductcompositedto"></a>

```json
{
  "id": 0,
  "variant_id": 0,
  "sub_variant_id": 0,
  "quantity": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|variant_id|integer(int64)|false|none|none|
|sub_variant_id|integer(int64)|false|none|none|
|quantity|number|false|none|none|

<h2 id="tocS_ProductVariantDto">ProductVariantDto</h2>
<!-- backwards compatibility -->
<a id="schemaproductvariantdto"></a>
<a id="schema_ProductVariantDto"></a>
<a id="tocSproductvariantdto"></a>
<a id="tocsproductvariantdto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "category_id": 0,
  "category": "string",
  "material_id": 0,
  "goods": "string",
  "material": "string",
  "brand": "string",
  "brand_name": "string",
  "made_in_id": 0,
  "made_in": "string",
  "description": "string",
  "content": "string",
  "merchandiser_code": "string",
  "designer_code": "string",
  "merchandiser": "string",
  "designer": "string",
  "tags": "string",
  "status": "string",
  "status_name": "string",
  "name": "string",
  "care_labels": "string",
  "unit": "string",
  "specifications": "string",
  "product_type": "string",
  "product_collections": [
    "string"
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|category_id|integer(int64)|false|none|none|
|category|string|false|none|none|
|material_id|integer(int64)|false|none|none|
|goods|string|false|none|none|
|material|string|false|none|none|
|brand|string|false|none|none|
|brand_name|string|false|none|none|
|made_in_id|integer(int64)|false|none|none|
|made_in|string|false|none|none|
|description|string|false|none|none|
|content|string|false|none|none|
|merchandiser_code|string|false|none|none|
|designer_code|string|false|none|none|
|merchandiser|string|false|none|none|
|designer|string|false|none|none|
|tags|string|false|none|none|
|status|string|false|none|none|
|status_name|string|false|none|none|
|name|string|false|none|none|
|care_labels|string|false|none|none|
|unit|string|false|none|none|
|specifications|string|false|none|none|
|product_type|string|false|none|none|
|product_collections|[string]|false|none|none|

<h2 id="tocS_PurchaseOrderDto">PurchaseOrderDto</h2>
<!-- backwards compatibility -->
<a id="schemapurchaseorderdto"></a>
<a id="schema_PurchaseOrderDto"></a>
<a id="tocSpurchaseorderdto"></a>
<a id="tocspurchaseorderdto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "company_id": 0,
  "merchandiser_code": "string",
  "merchandiser": "string",
  "designer_code": "string",
  "designer": "string",
  "qc_code": "string",
  "qc": "string",
  "reference": "string",
  "type": "string",
  "supplier_id": 0,
  "supplier_code": "string",
  "supplier": "string",
  "billing_address": {
    "id": 0,
    "code": "string",
    "version": 0,
    "created_by": "string",
    "created_name": "string",
    "created_date": "2019-08-24T14:15:22Z",
    "updated_by": "string",
    "updated_name": "string",
    "updated_date": "2019-08-24T14:15:22Z",
    "name": "string",
    "email": "string",
    "phone": "string",
    "tax_code": "string",
    "country_id": 0,
    "country": "string",
    "city_id": 0,
    "city": "string",
    "district_id": 0,
    "district": "string",
    "ward_id": 0,
    "ward": "string",
    "zip_code": "string",
    "full_address": "string",
    "bank_number": "string",
    "bank_name": "string",
    "beneficiary": "string",
    "position": "string"
  },
  "supplier_address": {
    "id": 0,
    "code": "string",
    "version": 0,
    "created_by": "string",
    "created_name": "string",
    "created_date": "2019-08-24T14:15:22Z",
    "updated_by": "string",
    "updated_name": "string",
    "updated_date": "2019-08-24T14:15:22Z",
    "name": "string",
    "email": "string",
    "phone": "string",
    "tax_code": "string",
    "country_id": 0,
    "country": "string",
    "city_id": 0,
    "city": "string",
    "district_id": 0,
    "district": "string",
    "ward_id": 0,
    "ward": "string",
    "zip_code": "string",
    "full_address": "string",
    "bank_number": "string",
    "bank_name": "string",
    "beneficiary": "string",
    "position": "string"
  },
  "line_items": [
    {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "sku": "string",
      "barcode": "string",
      "variant_id": 0,
      "variant_detail": {
        "id": 0,
        "code": "string",
        "version": 0,
        "created_by": "string",
        "created_name": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "updated_by": "string",
        "updated_name": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "name": "string",
        "on_hand": 0,
        "available": 0,
        "committed": 0,
        "in_coming": 0,
        "on_way": 0,
        "on_hold": 0,
        "defect": 0,
        "transferring": 0,
        "shipping": 0,
        "total_stock": 0,
        "supplier_id": 0,
        "supplier": "string",
        "color_id": 0,
        "color": "string",
        "size_id": 0,
        "size": "string",
        "barcode": "string",
        "reference_id": 0,
        "taxable": true,
        "saleable": true,
        "sku": "string",
        "status": "string",
        "status_name": "string",
        "composite": true,
        "width": 0,
        "length": 0,
        "height": 0,
        "weight": 0,
        "weight_unit": "string",
        "length_unit": "string",
        "product_id": 0,
        "product": {
          "id": 0,
          "code": "string",
          "version": 0,
          "created_by": "string",
          "created_name": "string",
          "created_date": "2019-08-24T14:15:22Z",
          "updated_by": "string",
          "updated_name": "string",
          "updated_date": "2019-08-24T14:15:22Z",
          "category_id": 0,
          "category": "string",
          "material_id": 0,
          "goods": "string",
          "material": "string",
          "brand": "string",
          "brand_name": "string",
          "made_in_id": 0,
          "made_in": "string",
          "description": "string",
          "content": "string",
          "merchandiser_code": "string",
          "designer_code": "string",
          "merchandiser": "string",
          "designer": "string",
          "tags": "string",
          "status": "string",
          "status_name": "string",
          "name": "string",
          "care_labels": "string",
          "unit": "string",
          "specifications": "string",
          "product_type": "string",
          "product_collections": [
            "string"
          ]
        },
        "variant_prices": [
          {
            "id": 0,
            "retail_price": 0,
            "variant_id": 0,
            "currency_code": "string",
            "currency_symbol": "string",
            "tax_percent": 0,
            "cost_price": 0,
            "import_price": 0,
            "wholesale_price": 0
          }
        ],
        "variant_images": [
          {
            "id": 0,
            "variant_id": 0,
            "position": 0,
            "image_id": 0,
            "url": "string",
            "product_avatar": true,
            "variant_avatar": true
          }
        ],
        "composites": [
          {
            "id": 0,
            "variant_id": 0,
            "sub_variant_id": 0,
            "quantity": 0
          }
        ]
      },
      "product_id": 0,
      "product": "string",
      "variant": "string",
      "retail_price": 0,
      "product_type": "string",
      "quantity": 0,
      "receipt_quantity": 0,
      "planned_quantity": 0,
      "price": 0,
      "amount": 0,
      "note": "string",
      "type": "string",
      "variant_image": "string",
      "unit": "string",
      "tax": 0,
      "tax_rate": 0,
      "line_amount_after_line_discount": 0,
      "discount_rate": 0,
      "discount_value": 0,
      "discount_amount": 0,
      "position": 0,
      "purchase_order_id": 0
    }
  ],
  "return_orders": [
    {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "line_return_items": [
        {
          "id": 0,
          "code": "string",
          "version": 0,
          "created_by": "string",
          "created_name": "string",
          "created_date": "2019-08-24T14:15:22Z",
          "updated_by": "string",
          "updated_name": "string",
          "updated_date": "2019-08-24T14:15:22Z",
          "sku": "string",
          "barcode": "string",
          "variant_id": 0,
          "product_id": 0,
          "product": "string",
          "variant": "string",
          "retail_price": 0,
          "product_type": "string",
          "quantity": 0,
          "quantity_return": 0,
          "receipt_quantity": 0,
          "planned_quantity": 0,
          "price": 0,
          "amount": 0,
          "note": "string",
          "type": "string",
          "variant_image": "string",
          "unit": "string",
          "tax": 0,
          "tax_rate": 0,
          "line_amount_after_line_discount": 0,
          "discount_rate": 0,
          "discount_value": 0,
          "discount_amount": 0,
          "position": 0,
          "untaxed_amount_refunds": 0,
          "amount_tax_refunds": 0,
          "return_reason": "string",
          "payment_return_note": "string",
          "purchase_order_id": 0
        }
      ],
      "expect_return_date": "2019-08-24T14:15:22Z",
      "store_id": 0,
      "untaxed_amount_refunds": 0,
      "amount_tax_refunds": 0,
      "total_refunds": 0,
      "return_reason": "string",
      "payment_return_note": "string"
    }
  ],
  "phone": "string",
  "supplier_note": "string",
  "expect_import_date": "2019-08-24T14:15:22Z",
  "expect_return_date": "2019-08-24T14:15:22Z",
  "expect_store_id": 0,
  "expect_store": "string",
  "payment_condition_id": 0,
  "payment_condition_name": "string",
  "payment_note": "string",
  "note": "string",
  "tags": "string",
  "policy_price_code": "string",
  "tax_included": true,
  "payments": [
    {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "account_code": "string",
      "amount": 0,
      "reference": "string",
      "payment_method_code": "string",
      "payment_method": "string",
      "status": "string",
      "status_name": "string",
      "note": "string",
      "is_refund": true,
      "purchase_order_id": 0,
      "transaction_date": "2019-08-24T14:15:22Z",
      "transaction_date_string": "string"
    }
  ],
  "payment_refunds": [
    {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "account_code": "string",
      "amount": 0,
      "reference": "string",
      "payment_method_code": "string",
      "status": "string",
      "status_name": "string",
      "note": "string",
      "purchase_order_id": 0,
      "transaction_date": "2019-08-24T14:15:22Z"
    }
  ],
  "procurements": [
    {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "reference": "string",
      "store_id": 0,
      "store": "string",
      "expect_receipt_date": "2019-08-24T14:15:22Z",
      "note": "string",
      "status": "string",
      "status_name": "string",
      "activated_date": "2019-08-24T14:15:22Z",
      "activated_by": "string",
      "stock_in_date": "2019-08-24T14:15:22Z",
      "stock_in_by": "string",
      "is_cancelled": true,
      "created_date_str": "string",
      "purchase_order": {
        "id": 0,
        "company_id": 0,
        "merchandiser_code": "string",
        "merchandiser": "string",
        "designer_code": "string",
        "designer": "string",
        "qc_code": "string",
        "qc": "string",
        "reference": "string",
        "type": "string",
        "code": "string",
        "supplier_id": 0,
        "supplier_code": "string",
        "supplier": "string",
        "phone": "string"
      },
      "procurement_items": [
        {
          "id": 0,
          "code": "string",
          "version": 0,
          "created_by": "string",
          "created_name": "string",
          "created_date": "2019-08-24T14:15:22Z",
          "updated_by": "string",
          "updated_name": "string",
          "updated_date": "2019-08-24T14:15:22Z",
          "line_item_id": 0,
          "sku": "string",
          "barcode": "string",
          "variant": "string",
          "variant_image": "string",
          "variant_id": 0,
          "retail_price": 0,
          "ordered_quantity": 0,
          "accepted_quantity": 0,
          "planned_quantity": 0,
          "quantity": 0,
          "real_quantity": 0,
          "note": "string",
          "price": 0,
          "vat": 0,
          "vat_rate": 0,
          "amount": 0
        }
      ]
    }
  ],
  "cost_lines": [
    {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "title": "string",
      "amount": 0
    }
  ],
  "total_cost_line": 0,
  "tax_lines": [
    {
      "rate": 0,
      "amount": 0
    }
  ],
  "payment_discount_rate": 0,
  "payment_discount_value": 0,
  "payment_discount_amount": 0,
  "trade_discount_rate": 0,
  "trade_discount_value": 0,
  "trade_discount_amount": 0,
  "untaxed_amount": 0,
  "untaxed_amount_refunds": 0,
  "tax": 0,
  "total": 0,
  "total_payment": 0,
  "total_paid": 0,
  "total_refunds": 0,
  "receipt_quantity": 0,
  "planned_quantity": 0,
  "status": "string",
  "status_name": "string",
  "financial_status": "string",
  "receive_status": "string",
  "cancel_reason": "string",
  "order_date": "2019-08-24T14:15:22Z",
  "order_date_string": "string",
  "cancelled_date": "2019-08-24T14:15:22Z",
  "activated_date": "2019-08-24T14:15:22Z",
  "completed_date": "2019-08-24T14:15:22Z",
  "completed_stock_date": "2019-08-24T14:15:22Z",
  "is_grid_mode": true,
  "is_grid_mode_supplement": true,
  "receive_finished_date": "2019-08-24T14:15:22Z",
  "waiting_approval_date": "2019-08-24T14:15:22Z"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|company_id|integer(int64)|false|none|none|
|merchandiser_code|string|false|none|none|
|merchandiser|string|false|none|none|
|designer_code|string|false|none|none|
|designer|string|false|none|none|
|qc_code|string|false|none|none|
|qc|string|false|none|none|
|reference|string|false|none|none|
|type|string|false|none|none|
|supplier_id|integer(int64)|false|none|none|
|supplier_code|string|false|none|none|
|supplier|string|false|none|none|
|billing_address|[AddressDto](#schemaaddressdto)|false|none|none|
|supplier_address|[AddressDto](#schemaaddressdto)|false|none|none|
|line_items|[[PurchaseOrderLineDto](#schemapurchaseorderlinedto)]|false|none|none|
|return_orders|[[PurchaseOrderReturnDto](#schemapurchaseorderreturndto)]|false|none|none|
|phone|string|false|none|none|
|supplier_note|string|false|none|none|
|expect_import_date|string(date-time)|false|none|none|
|expect_return_date|string(date-time)|false|none|none|
|expect_store_id|integer(int64)|false|none|none|
|expect_store|string|false|none|none|
|payment_condition_id|integer(int64)|false|none|none|
|payment_condition_name|string|false|none|none|
|payment_note|string|false|none|none|
|note|string|false|none|none|
|tags|string|false|none|none|
|policy_price_code|string|false|none|none|
|tax_included|boolean|false|none|none|
|payments|[[PaymentDto](#schemapaymentdto)]|false|none|none|
|payment_refunds|[[PaymentRefundsDto](#schemapaymentrefundsdto)]|false|none|none|
|procurements|[[ProcurementDto](#schemaprocurementdto)]|false|none|none|
|cost_lines|[[CostDto](#schemacostdto)]|false|none|none|
|total_cost_line|number|false|none|none|
|tax_lines|[[TaxLineDto](#schemataxlinedto)]|false|none|none|
|payment_discount_rate|number|false|none|none|
|payment_discount_value|number|false|none|none|
|payment_discount_amount|number|false|none|none|
|trade_discount_rate|number|false|none|none|
|trade_discount_value|number|false|none|none|
|trade_discount_amount|number|false|none|none|
|untaxed_amount|number|false|none|none|
|untaxed_amount_refunds|number|false|none|none|
|tax|number|false|none|none|
|total|number|false|none|none|
|total_payment|number|false|none|none|
|total_paid|number|false|none|none|
|total_refunds|number|false|none|none|
|receipt_quantity|number|false|none|none|
|planned_quantity|number|false|none|none|
|status|string|false|none|none|
|status_name|string|false|none|none|
|financial_status|string|false|none|none|
|receive_status|string|false|none|none|
|cancel_reason|string|false|none|none|
|order_date|string(date-time)|false|none|none|
|order_date_string|string|false|none|none|
|cancelled_date|string(date-time)|false|none|none|
|activated_date|string(date-time)|false|none|none|
|completed_date|string(date-time)|false|none|none|
|completed_stock_date|string(date-time)|false|none|none|
|is_grid_mode|boolean|false|none|none|
|is_grid_mode_supplement|boolean|false|none|none|
|receive_finished_date|string(date-time)|false|none|none|
|waiting_approval_date|string(date-time)|false|none|none|

<h2 id="tocS_PurchaseOrderLineDto">PurchaseOrderLineDto</h2>
<!-- backwards compatibility -->
<a id="schemapurchaseorderlinedto"></a>
<a id="schema_PurchaseOrderLineDto"></a>
<a id="tocSpurchaseorderlinedto"></a>
<a id="tocspurchaseorderlinedto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "sku": "string",
  "barcode": "string",
  "variant_id": 0,
  "variant_detail": {
    "id": 0,
    "code": "string",
    "version": 0,
    "created_by": "string",
    "created_name": "string",
    "created_date": "2019-08-24T14:15:22Z",
    "updated_by": "string",
    "updated_name": "string",
    "updated_date": "2019-08-24T14:15:22Z",
    "name": "string",
    "on_hand": 0,
    "available": 0,
    "committed": 0,
    "in_coming": 0,
    "on_way": 0,
    "on_hold": 0,
    "defect": 0,
    "transferring": 0,
    "shipping": 0,
    "total_stock": 0,
    "supplier_id": 0,
    "supplier": "string",
    "color_id": 0,
    "color": "string",
    "size_id": 0,
    "size": "string",
    "barcode": "string",
    "reference_id": 0,
    "taxable": true,
    "saleable": true,
    "sku": "string",
    "status": "string",
    "status_name": "string",
    "composite": true,
    "width": 0,
    "length": 0,
    "height": 0,
    "weight": 0,
    "weight_unit": "string",
    "length_unit": "string",
    "product_id": 0,
    "product": {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "category_id": 0,
      "category": "string",
      "material_id": 0,
      "goods": "string",
      "material": "string",
      "brand": "string",
      "brand_name": "string",
      "made_in_id": 0,
      "made_in": "string",
      "description": "string",
      "content": "string",
      "merchandiser_code": "string",
      "designer_code": "string",
      "merchandiser": "string",
      "designer": "string",
      "tags": "string",
      "status": "string",
      "status_name": "string",
      "name": "string",
      "care_labels": "string",
      "unit": "string",
      "specifications": "string",
      "product_type": "string",
      "product_collections": [
        "string"
      ]
    },
    "variant_prices": [
      {
        "id": 0,
        "retail_price": 0,
        "variant_id": 0,
        "currency_code": "string",
        "currency_symbol": "string",
        "tax_percent": 0,
        "cost_price": 0,
        "import_price": 0,
        "wholesale_price": 0
      }
    ],
    "variant_images": [
      {
        "id": 0,
        "variant_id": 0,
        "position": 0,
        "image_id": 0,
        "url": "string",
        "product_avatar": true,
        "variant_avatar": true
      }
    ],
    "composites": [
      {
        "id": 0,
        "variant_id": 0,
        "sub_variant_id": 0,
        "quantity": 0
      }
    ]
  },
  "product_id": 0,
  "product": "string",
  "variant": "string",
  "retail_price": 0,
  "product_type": "string",
  "quantity": 0,
  "receipt_quantity": 0,
  "planned_quantity": 0,
  "price": 0,
  "amount": 0,
  "note": "string",
  "type": "string",
  "variant_image": "string",
  "unit": "string",
  "tax": 0,
  "tax_rate": 0,
  "line_amount_after_line_discount": 0,
  "discount_rate": 0,
  "discount_value": 0,
  "discount_amount": 0,
  "position": 0,
  "purchase_order_id": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|sku|string|false|none|none|
|barcode|string|false|none|none|
|variant_id|integer(int64)|false|none|none|
|variant_detail|[VariantDetailDto](#schemavariantdetaildto)|false|none|none|
|product_id|integer(int64)|false|none|none|
|product|string|false|none|none|
|variant|string|false|none|none|
|retail_price|number|false|none|none|
|product_type|string|false|none|none|
|quantity|number|false|none|none|
|receipt_quantity|number|false|none|none|
|planned_quantity|number|false|none|none|
|price|number|false|none|none|
|amount|number|false|none|none|
|note|string|false|none|none|
|type|string|false|none|none|
|variant_image|string|false|none|none|
|unit|string|false|none|none|
|tax|number|false|none|none|
|tax_rate|number(float)|false|none|none|
|line_amount_after_line_discount|number|false|none|none|
|discount_rate|number|false|none|none|
|discount_value|number|false|none|none|
|discount_amount|number|false|none|none|
|position|integer(int32)|false|none|none|
|purchase_order_id|integer(int64)|false|none|none|

<h2 id="tocS_PurchaseOrderLineReturnDto">PurchaseOrderLineReturnDto</h2>
<!-- backwards compatibility -->
<a id="schemapurchaseorderlinereturndto"></a>
<a id="schema_PurchaseOrderLineReturnDto"></a>
<a id="tocSpurchaseorderlinereturndto"></a>
<a id="tocspurchaseorderlinereturndto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "sku": "string",
  "barcode": "string",
  "variant_id": 0,
  "product_id": 0,
  "product": "string",
  "variant": "string",
  "retail_price": 0,
  "product_type": "string",
  "quantity": 0,
  "quantity_return": 0,
  "receipt_quantity": 0,
  "planned_quantity": 0,
  "price": 0,
  "amount": 0,
  "note": "string",
  "type": "string",
  "variant_image": "string",
  "unit": "string",
  "tax": 0,
  "tax_rate": 0,
  "line_amount_after_line_discount": 0,
  "discount_rate": 0,
  "discount_value": 0,
  "discount_amount": 0,
  "position": 0,
  "untaxed_amount_refunds": 0,
  "amount_tax_refunds": 0,
  "return_reason": "string",
  "payment_return_note": "string",
  "purchase_order_id": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|sku|string|false|none|none|
|barcode|string|false|none|none|
|variant_id|integer(int64)|false|none|none|
|product_id|integer(int64)|false|none|none|
|product|string|false|none|none|
|variant|string|false|none|none|
|retail_price|number|false|none|none|
|product_type|string|false|none|none|
|quantity|number|false|none|none|
|quantity_return|number|false|none|none|
|receipt_quantity|number|false|none|none|
|planned_quantity|number|false|none|none|
|price|number|false|none|none|
|amount|number|false|none|none|
|note|string|false|none|none|
|type|string|false|none|none|
|variant_image|string|false|none|none|
|unit|string|false|none|none|
|tax|number|false|none|none|
|tax_rate|number(float)|false|none|none|
|line_amount_after_line_discount|number|false|none|none|
|discount_rate|number|false|none|none|
|discount_value|number|false|none|none|
|discount_amount|number|false|none|none|
|position|integer(int32)|false|none|none|
|untaxed_amount_refunds|number|false|none|none|
|amount_tax_refunds|number|false|none|none|
|return_reason|string|false|none|none|
|payment_return_note|string|false|none|none|
|purchase_order_id|integer(int64)|false|none|none|

<h2 id="tocS_PurchaseOrderProcurementDto">PurchaseOrderProcurementDto</h2>
<!-- backwards compatibility -->
<a id="schemapurchaseorderprocurementdto"></a>
<a id="schema_PurchaseOrderProcurementDto"></a>
<a id="tocSpurchaseorderprocurementdto"></a>
<a id="tocspurchaseorderprocurementdto"></a>

```json
{
  "id": 0,
  "company_id": 0,
  "merchandiser_code": "string",
  "merchandiser": "string",
  "designer_code": "string",
  "designer": "string",
  "qc_code": "string",
  "qc": "string",
  "reference": "string",
  "type": "string",
  "code": "string",
  "supplier_id": 0,
  "supplier_code": "string",
  "supplier": "string",
  "phone": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|company_id|integer(int64)|false|none|none|
|merchandiser_code|string|false|none|none|
|merchandiser|string|false|none|none|
|designer_code|string|false|none|none|
|designer|string|false|none|none|
|qc_code|string|false|none|none|
|qc|string|false|none|none|
|reference|string|false|none|none|
|type|string|false|none|none|
|code|string|false|none|none|
|supplier_id|integer(int64)|false|none|none|
|supplier_code|string|false|none|none|
|supplier|string|false|none|none|
|phone|string|false|none|none|

<h2 id="tocS_PurchaseOrderReturnDto">PurchaseOrderReturnDto</h2>
<!-- backwards compatibility -->
<a id="schemapurchaseorderreturndto"></a>
<a id="schema_PurchaseOrderReturnDto"></a>
<a id="tocSpurchaseorderreturndto"></a>
<a id="tocspurchaseorderreturndto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "line_return_items": [
    {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "sku": "string",
      "barcode": "string",
      "variant_id": 0,
      "product_id": 0,
      "product": "string",
      "variant": "string",
      "retail_price": 0,
      "product_type": "string",
      "quantity": 0,
      "quantity_return": 0,
      "receipt_quantity": 0,
      "planned_quantity": 0,
      "price": 0,
      "amount": 0,
      "note": "string",
      "type": "string",
      "variant_image": "string",
      "unit": "string",
      "tax": 0,
      "tax_rate": 0,
      "line_amount_after_line_discount": 0,
      "discount_rate": 0,
      "discount_value": 0,
      "discount_amount": 0,
      "position": 0,
      "untaxed_amount_refunds": 0,
      "amount_tax_refunds": 0,
      "return_reason": "string",
      "payment_return_note": "string",
      "purchase_order_id": 0
    }
  ],
  "expect_return_date": "2019-08-24T14:15:22Z",
  "store_id": 0,
  "untaxed_amount_refunds": 0,
  "amount_tax_refunds": 0,
  "total_refunds": 0,
  "return_reason": "string",
  "payment_return_note": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|line_return_items|[[PurchaseOrderLineReturnDto](#schemapurchaseorderlinereturndto)]|false|none|none|
|expect_return_date|string(date-time)|false|none|none|
|store_id|integer(int64)|false|none|none|
|untaxed_amount_refunds|number|false|none|none|
|amount_tax_refunds|number|false|none|none|
|total_refunds|number|false|none|none|
|return_reason|string|false|none|none|
|payment_return_note|string|false|none|none|

<h2 id="tocS_ResultPurchaseOrderDto">ResultPurchaseOrderDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultpurchaseorderdto"></a>
<a id="schema_ResultPurchaseOrderDto"></a>
<a id="tocSresultpurchaseorderdto"></a>
<a id="tocsresultpurchaseorderdto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": {
    "id": 0,
    "code": "string",
    "version": 0,
    "created_by": "string",
    "created_name": "string",
    "created_date": "2019-08-24T14:15:22Z",
    "updated_by": "string",
    "updated_name": "string",
    "updated_date": "2019-08-24T14:15:22Z",
    "company_id": 0,
    "merchandiser_code": "string",
    "merchandiser": "string",
    "designer_code": "string",
    "designer": "string",
    "qc_code": "string",
    "qc": "string",
    "reference": "string",
    "type": "string",
    "supplier_id": 0,
    "supplier_code": "string",
    "supplier": "string",
    "billing_address": {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "name": "string",
      "email": "string",
      "phone": "string",
      "tax_code": "string",
      "country_id": 0,
      "country": "string",
      "city_id": 0,
      "city": "string",
      "district_id": 0,
      "district": "string",
      "ward_id": 0,
      "ward": "string",
      "zip_code": "string",
      "full_address": "string",
      "bank_number": "string",
      "bank_name": "string",
      "beneficiary": "string",
      "position": "string"
    },
    "supplier_address": {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "name": "string",
      "email": "string",
      "phone": "string",
      "tax_code": "string",
      "country_id": 0,
      "country": "string",
      "city_id": 0,
      "city": "string",
      "district_id": 0,
      "district": "string",
      "ward_id": 0,
      "ward": "string",
      "zip_code": "string",
      "full_address": "string",
      "bank_number": "string",
      "bank_name": "string",
      "beneficiary": "string",
      "position": "string"
    },
    "line_items": [
      {
        "id": 0,
        "code": "string",
        "version": 0,
        "created_by": "string",
        "created_name": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "updated_by": "string",
        "updated_name": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "sku": "string",
        "barcode": "string",
        "variant_id": 0,
        "variant_detail": {
          "id": 0,
          "code": "string",
          "version": 0,
          "created_by": "string",
          "created_name": "string",
          "created_date": "2019-08-24T14:15:22Z",
          "updated_by": "string",
          "updated_name": "string",
          "updated_date": "2019-08-24T14:15:22Z",
          "name": "string",
          "on_hand": 0,
          "available": 0,
          "committed": 0,
          "in_coming": 0,
          "on_way": 0,
          "on_hold": 0,
          "defect": 0,
          "transferring": 0,
          "shipping": 0,
          "total_stock": 0,
          "supplier_id": 0,
          "supplier": "string",
          "color_id": 0,
          "color": "string",
          "size_id": 0,
          "size": "string",
          "barcode": "string",
          "reference_id": 0,
          "taxable": true,
          "saleable": true,
          "sku": "string",
          "status": "string",
          "status_name": "string",
          "composite": true,
          "width": 0,
          "length": 0,
          "height": 0,
          "weight": 0,
          "weight_unit": "string",
          "length_unit": "string",
          "product_id": 0,
          "product": {
            "id": 0,
            "code": "string",
            "version": 0,
            "created_by": "string",
            "created_name": "string",
            "created_date": "2019-08-24T14:15:22Z",
            "updated_by": "string",
            "updated_name": "string",
            "updated_date": "2019-08-24T14:15:22Z",
            "category_id": 0,
            "category": "string",
            "material_id": 0,
            "goods": "string",
            "material": "string",
            "brand": "string",
            "brand_name": "string",
            "made_in_id": 0,
            "made_in": "string",
            "description": "string",
            "content": "string",
            "merchandiser_code": "string",
            "designer_code": "string",
            "merchandiser": "string",
            "designer": "string",
            "tags": "string",
            "status": "string",
            "status_name": "string",
            "name": "string",
            "care_labels": "string",
            "unit": "string",
            "specifications": "string",
            "product_type": "string",
            "product_collections": [
              "string"
            ]
          },
          "variant_prices": [
            {
              "id": 0,
              "retail_price": 0,
              "variant_id": 0,
              "currency_code": "string",
              "currency_symbol": "string",
              "tax_percent": 0,
              "cost_price": 0,
              "import_price": 0,
              "wholesale_price": 0
            }
          ],
          "variant_images": [
            {
              "id": 0,
              "variant_id": 0,
              "position": 0,
              "image_id": 0,
              "url": "string",
              "product_avatar": true,
              "variant_avatar": true
            }
          ],
          "composites": [
            {
              "id": 0,
              "variant_id": 0,
              "sub_variant_id": 0,
              "quantity": 0
            }
          ]
        },
        "product_id": 0,
        "product": "string",
        "variant": "string",
        "retail_price": 0,
        "product_type": "string",
        "quantity": 0,
        "receipt_quantity": 0,
        "planned_quantity": 0,
        "price": 0,
        "amount": 0,
        "note": "string",
        "type": "string",
        "variant_image": "string",
        "unit": "string",
        "tax": 0,
        "tax_rate": 0,
        "line_amount_after_line_discount": 0,
        "discount_rate": 0,
        "discount_value": 0,
        "discount_amount": 0,
        "position": 0,
        "purchase_order_id": 0
      }
    ],
    "return_orders": [
      {
        "id": 0,
        "code": "string",
        "version": 0,
        "created_by": "string",
        "created_name": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "updated_by": "string",
        "updated_name": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "line_return_items": [
          {
            "id": 0,
            "code": "string",
            "version": 0,
            "created_by": "string",
            "created_name": "string",
            "created_date": "2019-08-24T14:15:22Z",
            "updated_by": "string",
            "updated_name": "string",
            "updated_date": "2019-08-24T14:15:22Z",
            "sku": "string",
            "barcode": "string",
            "variant_id": 0,
            "product_id": 0,
            "product": "string",
            "variant": "string",
            "retail_price": 0,
            "product_type": "string",
            "quantity": 0,
            "quantity_return": 0,
            "receipt_quantity": 0,
            "planned_quantity": 0,
            "price": 0,
            "amount": 0,
            "note": "string",
            "type": "string",
            "variant_image": "string",
            "unit": "string",
            "tax": 0,
            "tax_rate": 0,
            "line_amount_after_line_discount": 0,
            "discount_rate": 0,
            "discount_value": 0,
            "discount_amount": 0,
            "position": 0,
            "untaxed_amount_refunds": 0,
            "amount_tax_refunds": 0,
            "return_reason": "string",
            "payment_return_note": "string",
            "purchase_order_id": 0
          }
        ],
        "expect_return_date": "2019-08-24T14:15:22Z",
        "store_id": 0,
        "untaxed_amount_refunds": 0,
        "amount_tax_refunds": 0,
        "total_refunds": 0,
        "return_reason": "string",
        "payment_return_note": "string"
      }
    ],
    "phone": "string",
    "supplier_note": "string",
    "expect_import_date": "2019-08-24T14:15:22Z",
    "expect_return_date": "2019-08-24T14:15:22Z",
    "expect_store_id": 0,
    "expect_store": "string",
    "payment_condition_id": 0,
    "payment_condition_name": "string",
    "payment_note": "string",
    "note": "string",
    "tags": "string",
    "policy_price_code": "string",
    "tax_included": true,
    "payments": [
      {
        "id": 0,
        "code": "string",
        "version": 0,
        "created_by": "string",
        "created_name": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "updated_by": "string",
        "updated_name": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "account_code": "string",
        "amount": 0,
        "reference": "string",
        "payment_method_code": "string",
        "payment_method": "string",
        "status": "string",
        "status_name": "string",
        "note": "string",
        "is_refund": true,
        "purchase_order_id": 0,
        "transaction_date": "2019-08-24T14:15:22Z",
        "transaction_date_string": "string"
      }
    ],
    "payment_refunds": [
      {
        "id": 0,
        "code": "string",
        "version": 0,
        "created_by": "string",
        "created_name": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "updated_by": "string",
        "updated_name": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "account_code": "string",
        "amount": 0,
        "reference": "string",
        "payment_method_code": "string",
        "status": "string",
        "status_name": "string",
        "note": "string",
        "purchase_order_id": 0,
        "transaction_date": "2019-08-24T14:15:22Z"
      }
    ],
    "procurements": [
      {
        "id": 0,
        "code": "string",
        "version": 0,
        "created_by": "string",
        "created_name": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "updated_by": "string",
        "updated_name": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "reference": "string",
        "store_id": 0,
        "store": "string",
        "expect_receipt_date": "2019-08-24T14:15:22Z",
        "note": "string",
        "status": "string",
        "status_name": "string",
        "activated_date": "2019-08-24T14:15:22Z",
        "activated_by": "string",
        "stock_in_date": "2019-08-24T14:15:22Z",
        "stock_in_by": "string",
        "is_cancelled": true,
        "created_date_str": "string",
        "purchase_order": {
          "id": 0,
          "company_id": 0,
          "merchandiser_code": "string",
          "merchandiser": "string",
          "designer_code": "string",
          "designer": "string",
          "qc_code": "string",
          "qc": "string",
          "reference": "string",
          "type": "string",
          "code": "string",
          "supplier_id": 0,
          "supplier_code": "string",
          "supplier": "string",
          "phone": "string"
        },
        "procurement_items": [
          {
            "id": 0,
            "code": "string",
            "version": 0,
            "created_by": "string",
            "created_name": "string",
            "created_date": "2019-08-24T14:15:22Z",
            "updated_by": "string",
            "updated_name": "string",
            "updated_date": "2019-08-24T14:15:22Z",
            "line_item_id": 0,
            "sku": "string",
            "barcode": "string",
            "variant": "string",
            "variant_image": "string",
            "variant_id": 0,
            "retail_price": 0,
            "ordered_quantity": 0,
            "accepted_quantity": 0,
            "planned_quantity": 0,
            "quantity": 0,
            "real_quantity": 0,
            "note": "string",
            "price": 0,
            "vat": 0,
            "vat_rate": 0,
            "amount": 0
          }
        ]
      }
    ],
    "cost_lines": [
      {
        "id": 0,
        "code": "string",
        "version": 0,
        "created_by": "string",
        "created_name": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "updated_by": "string",
        "updated_name": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "title": "string",
        "amount": 0
      }
    ],
    "total_cost_line": 0,
    "tax_lines": [
      {
        "rate": 0,
        "amount": 0
      }
    ],
    "payment_discount_rate": 0,
    "payment_discount_value": 0,
    "payment_discount_amount": 0,
    "trade_discount_rate": 0,
    "trade_discount_value": 0,
    "trade_discount_amount": 0,
    "untaxed_amount": 0,
    "untaxed_amount_refunds": 0,
    "tax": 0,
    "total": 0,
    "total_payment": 0,
    "total_paid": 0,
    "total_refunds": 0,
    "receipt_quantity": 0,
    "planned_quantity": 0,
    "status": "string",
    "status_name": "string",
    "financial_status": "string",
    "receive_status": "string",
    "cancel_reason": "string",
    "order_date": "2019-08-24T14:15:22Z",
    "order_date_string": "string",
    "cancelled_date": "2019-08-24T14:15:22Z",
    "activated_date": "2019-08-24T14:15:22Z",
    "completed_date": "2019-08-24T14:15:22Z",
    "completed_stock_date": "2019-08-24T14:15:22Z",
    "is_grid_mode": true,
    "is_grid_mode_supplement": true,
    "receive_finished_date": "2019-08-24T14:15:22Z",
    "waiting_approval_date": "2019-08-24T14:15:22Z"
  },
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[PurchaseOrderDto](#schemapurchaseorderdto)|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_TaxLineDto">TaxLineDto</h2>
<!-- backwards compatibility -->
<a id="schemataxlinedto"></a>
<a id="schema_TaxLineDto"></a>
<a id="tocStaxlinedto"></a>
<a id="tocstaxlinedto"></a>

```json
{
  "rate": 0,
  "amount": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|rate|number(float)|false|none|none|
|amount|number|false|none|none|

<h2 id="tocS_VariantDetailDto">VariantDetailDto</h2>
<!-- backwards compatibility -->
<a id="schemavariantdetaildto"></a>
<a id="schema_VariantDetailDto"></a>
<a id="tocSvariantdetaildto"></a>
<a id="tocsvariantdetaildto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "name": "string",
  "on_hand": 0,
  "available": 0,
  "committed": 0,
  "in_coming": 0,
  "on_way": 0,
  "on_hold": 0,
  "defect": 0,
  "transferring": 0,
  "shipping": 0,
  "total_stock": 0,
  "supplier_id": 0,
  "supplier": "string",
  "color_id": 0,
  "color": "string",
  "size_id": 0,
  "size": "string",
  "barcode": "string",
  "reference_id": 0,
  "taxable": true,
  "saleable": true,
  "sku": "string",
  "status": "string",
  "status_name": "string",
  "composite": true,
  "width": 0,
  "length": 0,
  "height": 0,
  "weight": 0,
  "weight_unit": "string",
  "length_unit": "string",
  "product_id": 0,
  "product": {
    "id": 0,
    "code": "string",
    "version": 0,
    "created_by": "string",
    "created_name": "string",
    "created_date": "2019-08-24T14:15:22Z",
    "updated_by": "string",
    "updated_name": "string",
    "updated_date": "2019-08-24T14:15:22Z",
    "category_id": 0,
    "category": "string",
    "material_id": 0,
    "goods": "string",
    "material": "string",
    "brand": "string",
    "brand_name": "string",
    "made_in_id": 0,
    "made_in": "string",
    "description": "string",
    "content": "string",
    "merchandiser_code": "string",
    "designer_code": "string",
    "merchandiser": "string",
    "designer": "string",
    "tags": "string",
    "status": "string",
    "status_name": "string",
    "name": "string",
    "care_labels": "string",
    "unit": "string",
    "specifications": "string",
    "product_type": "string",
    "product_collections": [
      "string"
    ]
  },
  "variant_prices": [
    {
      "id": 0,
      "retail_price": 0,
      "variant_id": 0,
      "currency_code": "string",
      "currency_symbol": "string",
      "tax_percent": 0,
      "cost_price": 0,
      "import_price": 0,
      "wholesale_price": 0
    }
  ],
  "variant_images": [
    {
      "id": 0,
      "variant_id": 0,
      "position": 0,
      "image_id": 0,
      "url": "string",
      "product_avatar": true,
      "variant_avatar": true
    }
  ],
  "composites": [
    {
      "id": 0,
      "variant_id": 0,
      "sub_variant_id": 0,
      "quantity": 0
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|name|string|false|none|none|
|on_hand|number|false|none|none|
|available|number|false|none|none|
|committed|number|false|none|none|
|in_coming|number|false|none|none|
|on_way|number|false|none|none|
|on_hold|number|false|none|none|
|defect|number|false|none|none|
|transferring|number|false|none|none|
|shipping|number|false|none|none|
|total_stock|number|false|none|none|
|supplier_id|integer(int64)|false|none|none|
|supplier|string|false|none|none|
|color_id|integer(int64)|false|none|none|
|color|string|false|none|none|
|size_id|integer(int64)|false|none|none|
|size|string|false|none|none|
|barcode|string|false|none|none|
|reference_id|integer(int64)|false|none|none|
|taxable|boolean|false|none|none|
|saleable|boolean|false|none|none|
|sku|string|false|none|none|
|status|string|false|none|none|
|status_name|string|false|none|none|
|composite|boolean|false|none|none|
|width|number|false|none|none|
|length|number|false|none|none|
|height|number|false|none|none|
|weight|number|false|none|none|
|weight_unit|string|false|none|none|
|length_unit|string|false|none|none|
|product_id|integer(int64)|false|none|none|
|product|[ProductVariantDto](#schemaproductvariantdto)|false|none|none|
|variant_prices|[[VariantPriceDto](#schemavariantpricedto)]|false|none|none|
|variant_images|[[VariantImageDto](#schemavariantimagedto)]|false|none|none|
|composites|[[ProductCompositeDto](#schemaproductcompositedto)]|false|none|none|

<h2 id="tocS_VariantImageDto">VariantImageDto</h2>
<!-- backwards compatibility -->
<a id="schemavariantimagedto"></a>
<a id="schema_VariantImageDto"></a>
<a id="tocSvariantimagedto"></a>
<a id="tocsvariantimagedto"></a>

```json
{
  "id": 0,
  "variant_id": 0,
  "position": 0,
  "image_id": 0,
  "url": "string",
  "product_avatar": true,
  "variant_avatar": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|variant_id|integer(int64)|false|none|none|
|position|integer(int32)|false|none|none|
|image_id|integer(int64)|false|none|none|
|url|string|false|none|none|
|product_avatar|boolean|false|none|none|
|variant_avatar|boolean|false|none|none|

<h2 id="tocS_VariantPriceDto">VariantPriceDto</h2>
<!-- backwards compatibility -->
<a id="schemavariantpricedto"></a>
<a id="schema_VariantPriceDto"></a>
<a id="tocSvariantpricedto"></a>
<a id="tocsvariantpricedto"></a>

```json
{
  "id": 0,
  "retail_price": 0,
  "variant_id": 0,
  "currency_code": "string",
  "currency_symbol": "string",
  "tax_percent": 0,
  "cost_price": 0,
  "import_price": 0,
  "wholesale_price": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|retail_price|number|false|none|none|
|variant_id|integer(int64)|false|none|none|
|currency_code|string|false|none|none|
|currency_symbol|string|false|none|none|
|tax_percent|number(float)|false|none|none|
|cost_price|number|false|none|none|
|import_price|number|false|none|none|
|wholesale_price|number|false|none|none|

<h2 id="tocS_ProcurementItemRequest">ProcurementItemRequest</h2>
<!-- backwards compatibility -->
<a id="schemaprocurementitemrequest"></a>
<a id="schema_ProcurementItemRequest"></a>
<a id="tocSprocurementitemrequest"></a>
<a id="tocsprocurementitemrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "line_item_id": 0,
  "sku": "string",
  "barcode": "string",
  "variant": "string",
  "variant_image": "string",
  "variant_id": 0,
  "retail_price": 0,
  "ordered_quantity": 0,
  "accepted_quantity": 0,
  "planned_quantity": 0,
  "quantity": 0,
  "real_quantity": 0,
  "note": "string",
  "procurement_id": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|id|integer(int64)|false|none|none|
|line_item_id|integer(int64)|true|none|none|
|sku|string|true|none|none|
|barcode|string|false|none|none|
|variant|string|false|none|none|
|variant_image|string|false|none|none|
|variant_id|integer(int64)|false|none|none|
|retail_price|number|false|none|none|
|ordered_quantity|number|false|none|none|
|accepted_quantity|number|false|none|none|
|planned_quantity|number|false|none|none|
|quantity|number|true|none|none|
|real_quantity|number|false|none|none|
|note|string|false|none|none|
|procurement_id|integer(int64)|false|none|none|

<h2 id="tocS_ProcurementRequest">ProcurementRequest</h2>
<!-- backwards compatibility -->
<a id="schemaprocurementrequest"></a>
<a id="schema_ProcurementRequest"></a>
<a id="tocSprocurementrequest"></a>
<a id="tocsprocurementrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "reference": "string",
  "store_id": 0,
  "store": "string",
  "expect_receipt_date": "2019-08-24T14:15:22Z",
  "note": "string",
  "status": "string",
  "status_name": "string",
  "activated_date": "2019-08-24T14:15:22Z",
  "activated_by": "string",
  "stock_in_date": "2019-08-24T14:15:22Z",
  "stock_in_by": "string",
  "procurement_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "line_item_id": 0,
      "sku": "string",
      "barcode": "string",
      "variant": "string",
      "variant_image": "string",
      "variant_id": 0,
      "retail_price": 0,
      "ordered_quantity": 0,
      "accepted_quantity": 0,
      "planned_quantity": 0,
      "quantity": 0,
      "real_quantity": 0,
      "note": "string",
      "procurement_id": 0
    }
  ],
  "refer_ids": [
    0
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|reference|string|false|none|none|
|store_id|integer(int64)|false|none|none|
|store|string|false|none|none|
|expect_receipt_date|string(date-time)|false|none|none|
|note|string|false|none|none|
|status|string|true|none|none|
|status_name|string|false|none|none|
|activated_date|string(date-time)|false|none|none|
|activated_by|string|false|none|none|
|stock_in_date|string(date-time)|false|none|none|
|stock_in_by|string|false|none|none|
|procurement_items|[[ProcurementItemRequest](#schemaprocurementitemrequest)]|false|none|none|
|refer_ids|[integer]|false|none|none|

<h2 id="tocS_ProcurementUpdateNoteRequest">ProcurementUpdateNoteRequest</h2>
<!-- backwards compatibility -->
<a id="schemaprocurementupdatenoterequest"></a>
<a id="schema_ProcurementUpdateNoteRequest"></a>
<a id="tocSprocurementupdatenoterequest"></a>
<a id="tocsprocurementupdatenoterequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "note": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|note|string|false|none|none|

<h2 id="tocS_ResultString">ResultString</h2>
<!-- backwards compatibility -->
<a id="schemaresultstring"></a>
<a id="schema_ResultString"></a>
<a id="tocSresultstring"></a>
<a id="tocsresultstring"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": "string",
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|string|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_PaymentRequest">PaymentRequest</h2>
<!-- backwards compatibility -->
<a id="schemapaymentrequest"></a>
<a id="schema_PaymentRequest"></a>
<a id="tocSpaymentrequest"></a>
<a id="tocspaymentrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "amount": 0,
  "reference": "string",
  "payment_method_code": "string",
  "status": "string",
  "status_name": "string",
  "transaction_date": "2019-08-24T14:15:22Z",
  "is_refund": true,
  "purchase_order_id": 0,
  "note": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|id|integer(int64)|false|none|none|
|amount|number|true|none|none|
|reference|string|false|none|none|
|payment_method_code|string|false|none|none|
|status|string|true|none|none|
|status_name|string|false|none|none|
|transaction_date|string(date-time)|true|none|none|
|is_refund|boolean|true|none|none|
|purchase_order_id|integer(int64)|false|none|none|
|note|string|false|none|none|

<h2 id="tocS_BasicRequest">BasicRequest</h2>
<!-- backwards compatibility -->
<a id="schemabasicrequest"></a>
<a id="schema_BasicRequest"></a>
<a id="tocSbasicrequest"></a>
<a id="tocsbasicrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|

<h2 id="tocS_AddressRequest">AddressRequest</h2>
<!-- backwards compatibility -->
<a id="schemaaddressrequest"></a>
<a id="schema_AddressRequest"></a>
<a id="tocSaddressrequest"></a>
<a id="tocsaddressrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "name": "string",
  "email": "string",
  "phone": "string",
  "tax_code": "string",
  "country_id": 0,
  "country": "string",
  "city_id": 0,
  "city": "string",
  "district_id": 0,
  "district": "string",
  "ward_id": 0,
  "ward": "string",
  "zip_code": "string",
  "full_address": "string",
  "bank_number": "string",
  "bank_name": "string",
  "beneficiary": "string",
  "position": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|id|integer(int64)|false|none|none|
|name|string|false|none|none|
|email|string|false|none|none|
|phone|string|false|none|none|
|tax_code|string|false|none|none|
|country_id|integer(int64)|false|none|none|
|country|string|false|none|none|
|city_id|integer(int64)|false|none|none|
|city|string|false|none|none|
|district_id|integer(int64)|false|none|none|
|district|string|false|none|none|
|ward_id|integer(int64)|false|none|none|
|ward|string|false|none|none|
|zip_code|string|false|none|none|
|full_address|string|false|none|none|
|bank_number|string|false|none|none|
|bank_name|string|false|none|none|
|beneficiary|string|false|none|none|
|position|string|false|none|none|

<h2 id="tocS_CostRequest">CostRequest</h2>
<!-- backwards compatibility -->
<a id="schemacostrequest"></a>
<a id="schema_CostRequest"></a>
<a id="tocScostrequest"></a>
<a id="tocscostrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "title": "string",
  "amount": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|id|integer(int64)|false|none|none|
|title|string|false|none|none|
|amount|number|true|none|none|

<h2 id="tocS_PurchaseOrderLineRequest">PurchaseOrderLineRequest</h2>
<!-- backwards compatibility -->
<a id="schemapurchaseorderlinerequest"></a>
<a id="schema_PurchaseOrderLineRequest"></a>
<a id="tocSpurchaseorderlinerequest"></a>
<a id="tocspurchaseorderlinerequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "sku": "string",
  "variant_id": 0,
  "barcode": "string",
  "product_id": 0,
  "product": "string",
  "variant": "string",
  "retail_price": 0,
  "product_type": "string",
  "quantity": 0,
  "receipt_quantity": 0,
  "planned_quantity": 0,
  "price": 0,
  "amount": 0,
  "note": "string",
  "type": "string",
  "variant_image": "string",
  "unit": "string",
  "tax": 0,
  "tax_rate": 0,
  "line_amount_after_line_discount": 0,
  "discount_rate": 0,
  "discount_value": 0,
  "discount_amount": 0,
  "position": 0,
  "purchase_order_id": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|sku|string|true|none|none|
|variant_id|integer(int64)|true|none|none|
|barcode|string|false|none|none|
|product_id|integer(int64)|false|none|none|
|product|string|false|none|none|
|variant|string|true|none|none|
|retail_price|number|false|none|none|
|product_type|string|false|none|none|
|quantity|number|true|none|none|
|receipt_quantity|number|false|none|none|
|planned_quantity|number|false|none|none|
|price|number|false|none|none|
|amount|number|false|none|none|
|note|string|false|none|none|
|type|string|false|none|none|
|variant_image|string|false|none|none|
|unit|string|false|none|none|
|tax|number|false|none|none|
|tax_rate|number(float)|false|none|none|
|line_amount_after_line_discount|number|false|none|none|
|discount_rate|number|false|none|none|
|discount_value|number|false|none|none|
|discount_amount|number|false|none|none|
|position|integer(int32)|false|none|none|
|purchase_order_id|integer(int64)|false|none|none|

<h2 id="tocS_UpdatePurchaseOrderRequest">UpdatePurchaseOrderRequest</h2>
<!-- backwards compatibility -->
<a id="schemaupdatepurchaseorderrequest"></a>
<a id="schema_UpdatePurchaseOrderRequest"></a>
<a id="tocSupdatepurchaseorderrequest"></a>
<a id="tocsupdatepurchaseorderrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "company_id": 0,
  "merchandiser_code": "string",
  "merchandiser": "string",
  "designer_code": "string",
  "designer": "string",
  "qc_code": "string",
  "qc": "string",
  "reference": "string",
  "type": "string",
  "supplier_id": 0,
  "supplier_code": "string",
  "supplier": "string",
  "phone": "string",
  "supplier_note": "string",
  "billing_address": {
    "created_by": "string",
    "created_name": "string",
    "updated_by": "string",
    "updated_name": "string",
    "request_id": "string",
    "operator_kc_id": "string",
    "id": 0,
    "name": "string",
    "email": "string",
    "phone": "string",
    "tax_code": "string",
    "country_id": 0,
    "country": "string",
    "city_id": 0,
    "city": "string",
    "district_id": 0,
    "district": "string",
    "ward_id": 0,
    "ward": "string",
    "zip_code": "string",
    "full_address": "string",
    "bank_number": "string",
    "bank_name": "string",
    "beneficiary": "string",
    "position": "string"
  },
  "supplier_address": {
    "created_by": "string",
    "created_name": "string",
    "updated_by": "string",
    "updated_name": "string",
    "request_id": "string",
    "operator_kc_id": "string",
    "id": 0,
    "name": "string",
    "email": "string",
    "phone": "string",
    "tax_code": "string",
    "country_id": 0,
    "country": "string",
    "city_id": 0,
    "city": "string",
    "district_id": 0,
    "district": "string",
    "ward_id": 0,
    "ward": "string",
    "zip_code": "string",
    "full_address": "string",
    "bank_number": "string",
    "bank_name": "string",
    "beneficiary": "string",
    "position": "string"
  },
  "line_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "code": "string",
      "sku": "string",
      "variant_id": 0,
      "barcode": "string",
      "product_id": 0,
      "product": "string",
      "variant": "string",
      "retail_price": 0,
      "product_type": "string",
      "quantity": 0,
      "receipt_quantity": 0,
      "planned_quantity": 0,
      "price": 0,
      "amount": 0,
      "note": "string",
      "type": "string",
      "variant_image": "string",
      "unit": "string",
      "tax": 0,
      "tax_rate": 0,
      "line_amount_after_line_discount": 0,
      "discount_rate": 0,
      "discount_value": 0,
      "discount_amount": 0,
      "position": 0,
      "purchase_order_id": 0
    }
  ],
  "expect_import_date": "2019-08-24T14:15:22Z",
  "expect_store_id": 0,
  "expect_store": "string",
  "payment_condition_id": 0,
  "payment_condition_name": "string",
  "payment_note": "string",
  "note": "string",
  "tags": "string",
  "policy_price_code": "string",
  "tax_included": true,
  "payments": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "amount": 0,
      "reference": "string",
      "payment_method_code": "string",
      "status": "string",
      "status_name": "string",
      "transaction_date": "2019-08-24T14:15:22Z",
      "is_refund": true,
      "purchase_order_id": 0,
      "note": "string"
    }
  ],
  "procurements": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "code": "string",
      "reference": "string",
      "store_id": 0,
      "store": "string",
      "expect_receipt_date": "2019-08-24T14:15:22Z",
      "note": "string",
      "status": "string",
      "status_name": "string",
      "activated_date": "2019-08-24T14:15:22Z",
      "activated_by": "string",
      "stock_in_date": "2019-08-24T14:15:22Z",
      "stock_in_by": "string",
      "procurement_items": [
        {
          "created_by": "string",
          "created_name": "string",
          "updated_by": "string",
          "updated_name": "string",
          "request_id": "string",
          "operator_kc_id": "string",
          "id": 0,
          "line_item_id": 0,
          "sku": "string",
          "barcode": "string",
          "variant": "string",
          "variant_image": "string",
          "variant_id": 0,
          "retail_price": 0,
          "ordered_quantity": 0,
          "accepted_quantity": 0,
          "planned_quantity": 0,
          "quantity": 0,
          "real_quantity": 0,
          "note": "string",
          "procurement_id": 0
        }
      ],
      "refer_ids": [
        0
      ]
    }
  ],
  "payment_discount_rate": 0,
  "payment_discount_value": 0,
  "payment_discount_amount": 0,
  "trade_discount_rate": 0,
  "trade_discount_value": 0,
  "trade_discount_amount": 0,
  "cost_lines": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "title": "string",
      "amount": 0
    }
  ],
  "untaxed_amount": 0,
  "tax": 0,
  "total": 0,
  "total_paid": 0,
  "total_refunds": 0,
  "receipt_quantity": 0,
  "planned_quantity": 0,
  "status": "string",
  "financial_status": "string",
  "receive_status": "string",
  "cancel_reason": "string",
  "is_grid_mode": true,
  "is_grid_mode_supplement": true,
  "version": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|company_id|integer(int64)|false|none|none|
|merchandiser_code|string|true|none|none|
|merchandiser|string|false|none|none|
|designer_code|string|false|none|none|
|designer|string|false|none|none|
|qc_code|string|false|none|none|
|qc|string|false|none|none|
|reference|string|false|none|none|
|type|string|false|none|none|
|supplier_id|integer(int64)|true|none|none|
|supplier_code|string|false|none|none|
|supplier|string|false|none|none|
|phone|string|false|none|none|
|supplier_note|string|false|none|none|
|billing_address|[AddressRequest](#schemaaddressrequest)|false|none|none|
|supplier_address|[AddressRequest](#schemaaddressrequest)|false|none|none|
|line_items|[[PurchaseOrderLineRequest](#schemapurchaseorderlinerequest)]|true|none|none|
|expect_import_date|string(date-time)|false|none|none|
|expect_store_id|integer(int64)|false|none|none|
|expect_store|string|false|none|none|
|payment_condition_id|integer(int64)|false|none|none|
|payment_condition_name|string|false|none|none|
|payment_note|string|false|none|none|
|note|string|false|none|none|
|tags|string|false|none|none|
|policy_price_code|string|false|none|none|
|tax_included|boolean|false|none|none|
|payments|[[PaymentRequest](#schemapaymentrequest)]|false|none|none|
|procurements|[[ProcurementRequest](#schemaprocurementrequest)]|false|none|none|
|payment_discount_rate|number|false|none|none|
|payment_discount_value|number|false|none|none|
|payment_discount_amount|number|false|none|none|
|trade_discount_rate|number|false|none|none|
|trade_discount_value|number|false|none|none|
|trade_discount_amount|number|false|none|none|
|cost_lines|[[CostRequest](#schemacostrequest)]|false|none|none|
|untaxed_amount|number|false|none|none|
|tax|number|false|none|none|
|total|number|false|none|none|
|total_paid|number|false|none|none|
|total_refunds|number|false|none|none|
|receipt_quantity|number|false|none|none|
|planned_quantity|number|false|none|none|
|status|string|false|none|none|
|financial_status|string|false|none|none|
|receive_status|string|false|none|none|
|cancel_reason|string|false|none|none|
|is_grid_mode|boolean|false|none|none|
|is_grid_mode_supplement|boolean|false|none|none|
|version|integer(int32)|false|none|none|

<h2 id="tocS_UpdateNotesRequest">UpdateNotesRequest</h2>
<!-- backwards compatibility -->
<a id="schemaupdatenotesrequest"></a>
<a id="schema_UpdateNotesRequest"></a>
<a id="tocSupdatenotesrequest"></a>
<a id="tocsupdatenotesrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "note": "string",
  "supplier_note": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|note|string|false|none|none|
|supplier_note|string|false|none|none|

<h2 id="tocS_PaymentConditionRequest">PaymentConditionRequest</h2>
<!-- backwards compatibility -->
<a id="schemapaymentconditionrequest"></a>
<a id="schema_PaymentConditionRequest"></a>
<a id="tocSpaymentconditionrequest"></a>
<a id="tocspaymentconditionrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "code": "string",
  "timeout": 0,
  "note": "string",
  "default": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|code|string|false|none|none|
|timeout|integer(int32)|false|none|none|
|note|string|false|none|none|
|default|boolean|false|none|none|

<h2 id="tocS_CreatePurchaseOrderRequest">CreatePurchaseOrderRequest</h2>
<!-- backwards compatibility -->
<a id="schemacreatepurchaseorderrequest"></a>
<a id="schema_CreatePurchaseOrderRequest"></a>
<a id="tocScreatepurchaseorderrequest"></a>
<a id="tocscreatepurchaseorderrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "company_id": 0,
  "merchandiser_code": "string",
  "merchandiser": "string",
  "designer_code": "string",
  "designer": "string",
  "qc_code": "string",
  "qc": "string",
  "reference": "string",
  "type": "string",
  "supplier_id": 0,
  "supplier_code": "string",
  "supplier": "string",
  "phone": "string",
  "supplier_note": "string",
  "billing_address": {
    "created_by": "string",
    "created_name": "string",
    "updated_by": "string",
    "updated_name": "string",
    "request_id": "string",
    "operator_kc_id": "string",
    "id": 0,
    "name": "string",
    "email": "string",
    "phone": "string",
    "tax_code": "string",
    "country_id": 0,
    "country": "string",
    "city_id": 0,
    "city": "string",
    "district_id": 0,
    "district": "string",
    "ward_id": 0,
    "ward": "string",
    "zip_code": "string",
    "full_address": "string",
    "bank_number": "string",
    "bank_name": "string",
    "beneficiary": "string",
    "position": "string"
  },
  "supplier_address": {
    "created_by": "string",
    "created_name": "string",
    "updated_by": "string",
    "updated_name": "string",
    "request_id": "string",
    "operator_kc_id": "string",
    "id": 0,
    "name": "string",
    "email": "string",
    "phone": "string",
    "tax_code": "string",
    "country_id": 0,
    "country": "string",
    "city_id": 0,
    "city": "string",
    "district_id": 0,
    "district": "string",
    "ward_id": 0,
    "ward": "string",
    "zip_code": "string",
    "full_address": "string",
    "bank_number": "string",
    "bank_name": "string",
    "beneficiary": "string",
    "position": "string"
  },
  "line_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "code": "string",
      "sku": "string",
      "variant_id": 0,
      "barcode": "string",
      "product_id": 0,
      "product": "string",
      "variant": "string",
      "retail_price": 0,
      "product_type": "string",
      "quantity": 0,
      "receipt_quantity": 0,
      "planned_quantity": 0,
      "price": 0,
      "amount": 0,
      "note": "string",
      "type": "string",
      "variant_image": "string",
      "unit": "string",
      "tax": 0,
      "tax_rate": 0,
      "line_amount_after_line_discount": 0,
      "discount_rate": 0,
      "discount_value": 0,
      "discount_amount": 0,
      "position": 0,
      "purchase_order_id": 0
    }
  ],
  "expect_import_date": "2019-08-24T14:15:22Z",
  "expect_store_id": 0,
  "expect_store": "string",
  "payment_condition_id": 0,
  "payment_condition_name": "string",
  "payment_note": "string",
  "note": "string",
  "tags": "string",
  "policy_price_code": "string",
  "tax_included": true,
  "payments": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "amount": 0,
      "reference": "string",
      "payment_method_code": "string",
      "status": "string",
      "status_name": "string",
      "transaction_date": "2019-08-24T14:15:22Z",
      "is_refund": true,
      "purchase_order_id": 0,
      "note": "string"
    }
  ],
  "procurements": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "code": "string",
      "reference": "string",
      "store_id": 0,
      "store": "string",
      "expect_receipt_date": "2019-08-24T14:15:22Z",
      "note": "string",
      "status": "string",
      "status_name": "string",
      "activated_date": "2019-08-24T14:15:22Z",
      "activated_by": "string",
      "stock_in_date": "2019-08-24T14:15:22Z",
      "stock_in_by": "string",
      "procurement_items": [
        {
          "created_by": "string",
          "created_name": "string",
          "updated_by": "string",
          "updated_name": "string",
          "request_id": "string",
          "operator_kc_id": "string",
          "id": 0,
          "line_item_id": 0,
          "sku": "string",
          "barcode": "string",
          "variant": "string",
          "variant_image": "string",
          "variant_id": 0,
          "retail_price": 0,
          "ordered_quantity": 0,
          "accepted_quantity": 0,
          "planned_quantity": 0,
          "quantity": 0,
          "real_quantity": 0,
          "note": "string",
          "procurement_id": 0
        }
      ],
      "refer_ids": [
        0
      ]
    }
  ],
  "payment_discount_rate": 0,
  "payment_discount_value": 0,
  "payment_discount_amount": 0,
  "trade_discount_rate": 0,
  "trade_discount_value": 0,
  "trade_discount_amount": 0,
  "cost_lines": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "title": "string",
      "amount": 0
    }
  ],
  "untaxed_amount": 0,
  "tax": 0,
  "total": 0,
  "total_paid": 0,
  "total_refunds": 0,
  "receipt_quantity": 0,
  "planned_quantity": 0,
  "status": "string",
  "financial_status": "string",
  "receive_status": "string",
  "cancel_reason": "string",
  "is_grid_mode": true,
  "is_grid_mode_supplement": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|company_id|integer(int64)|false|none|none|
|merchandiser_code|string|true|none|none|
|merchandiser|string|false|none|none|
|designer_code|string|false|none|none|
|designer|string|false|none|none|
|qc_code|string|false|none|none|
|qc|string|false|none|none|
|reference|string|false|none|none|
|type|string|false|none|none|
|supplier_id|integer(int64)|true|none|none|
|supplier_code|string|false|none|none|
|supplier|string|false|none|none|
|phone|string|false|none|none|
|supplier_note|string|false|none|none|
|billing_address|[AddressRequest](#schemaaddressrequest)|false|none|none|
|supplier_address|[AddressRequest](#schemaaddressrequest)|false|none|none|
|line_items|[[PurchaseOrderLineRequest](#schemapurchaseorderlinerequest)]|true|none|none|
|expect_import_date|string(date-time)|false|none|none|
|expect_store_id|integer(int64)|false|none|none|
|expect_store|string|false|none|none|
|payment_condition_id|integer(int64)|false|none|none|
|payment_condition_name|string|false|none|none|
|payment_note|string|false|none|none|
|note|string|false|none|none|
|tags|string|false|none|none|
|policy_price_code|string|false|none|none|
|tax_included|boolean|false|none|none|
|payments|[[PaymentRequest](#schemapaymentrequest)]|false|none|none|
|procurements|[[ProcurementRequest](#schemaprocurementrequest)]|false|none|none|
|payment_discount_rate|number|false|none|none|
|payment_discount_value|number|false|none|none|
|payment_discount_amount|number|false|none|none|
|trade_discount_rate|number|false|none|none|
|trade_discount_value|number|false|none|none|
|trade_discount_amount|number|false|none|none|
|cost_lines|[[CostRequest](#schemacostrequest)]|false|none|none|
|untaxed_amount|number|false|none|none|
|tax|number|false|none|none|
|total|number|false|none|none|
|total_paid|number|false|none|none|
|total_refunds|number|false|none|none|
|receipt_quantity|number|false|none|none|
|planned_quantity|number|false|none|none|
|status|string|false|none|none|
|financial_status|string|false|none|none|
|receive_status|string|false|none|none|
|cancel_reason|string|false|none|none|
|is_grid_mode|boolean|false|none|none|
|is_grid_mode_supplement|boolean|false|none|none|

<h2 id="tocS_PurchaseOrderLineReturnRequest">PurchaseOrderLineReturnRequest</h2>
<!-- backwards compatibility -->
<a id="schemapurchaseorderlinereturnrequest"></a>
<a id="schema_PurchaseOrderLineReturnRequest"></a>
<a id="tocSpurchaseorderlinereturnrequest"></a>
<a id="tocspurchaseorderlinereturnrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "sku": "string",
  "barcode": "string",
  "variant_id": 0,
  "product_id": 0,
  "product": "string",
  "variant": "string",
  "retail_price": 0,
  "product_type": "string",
  "quantity": 0,
  "quantity_return": 0,
  "receipt_quantity": 0,
  "planned_quantity": 0,
  "price": 0,
  "amount": 0,
  "note": "string",
  "type": "string",
  "variant_image": "string",
  "unit": "string",
  "tax": 0,
  "tax_rate": 0,
  "line_amount_after_line_discount": 0,
  "discount_rate": 0,
  "discount_value": 0,
  "discount_amount": 0,
  "position": 0,
  "purchase_order_id": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|sku|string|true|none|none|
|barcode|string|false|none|none|
|variant_id|integer(int64)|true|none|none|
|product_id|integer(int64)|false|none|none|
|product|string|false|none|none|
|variant|string|true|none|none|
|retail_price|number|false|none|none|
|product_type|string|false|none|none|
|quantity|number|true|none|none|
|quantity_return|number|true|none|none|
|receipt_quantity|number|false|none|none|
|planned_quantity|number|false|none|none|
|price|number|true|none|none|
|amount|number|false|none|none|
|note|string|false|none|none|
|type|string|false|none|none|
|variant_image|string|false|none|none|
|unit|string|false|none|none|
|tax|number|false|none|none|
|tax_rate|number(float)|false|none|none|
|line_amount_after_line_discount|number|false|none|none|
|discount_rate|number|false|none|none|
|discount_value|number|false|none|none|
|discount_amount|number|false|none|none|
|position|integer(int32)|false|none|none|
|purchase_order_id|integer(int64)|false|none|none|

<h2 id="tocS_PurchaseOrderReturnRequest">PurchaseOrderReturnRequest</h2>
<!-- backwards compatibility -->
<a id="schemapurchaseorderreturnrequest"></a>
<a id="schema_PurchaseOrderReturnRequest"></a>
<a id="tocSpurchaseorderreturnrequest"></a>
<a id="tocspurchaseorderreturnrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "code": "string",
  "store_id": 0,
  "line_return_items": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "code": "string",
      "sku": "string",
      "barcode": "string",
      "variant_id": 0,
      "product_id": 0,
      "product": "string",
      "variant": "string",
      "retail_price": 0,
      "product_type": "string",
      "quantity": 0,
      "quantity_return": 0,
      "receipt_quantity": 0,
      "planned_quantity": 0,
      "price": 0,
      "amount": 0,
      "note": "string",
      "type": "string",
      "variant_image": "string",
      "unit": "string",
      "tax": 0,
      "tax_rate": 0,
      "line_amount_after_line_discount": 0,
      "discount_rate": 0,
      "discount_value": 0,
      "discount_amount": 0,
      "position": 0,
      "purchase_order_id": 0
    }
  ],
  "expect_return_date": "2019-08-24T14:15:22Z",
  "untaxed_amount_refunds": 0,
  "amount_tax_refunds": 0,
  "total_refunds": 0,
  "return_reason": "string",
  "payment_return_note": "string",
  "payments": [
    {
      "created_by": "string",
      "created_name": "string",
      "updated_by": "string",
      "updated_name": "string",
      "request_id": "string",
      "operator_kc_id": "string",
      "id": 0,
      "amount": 0,
      "reference": "string",
      "payment_method_code": "string",
      "status": "string",
      "status_name": "string",
      "transaction_date": "2019-08-24T14:15:22Z",
      "is_refund": true,
      "purchase_order_id": 0,
      "note": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|store_id|integer(int64)|false|none|none|
|line_return_items|[[PurchaseOrderLineReturnRequest](#schemapurchaseorderlinereturnrequest)]|true|none|none|
|expect_return_date|string(date-time)|true|none|none|
|untaxed_amount_refunds|number|false|none|none|
|amount_tax_refunds|number|false|none|none|
|total_refunds|number|false|none|none|
|return_reason|string|true|none|none|
|payment_return_note|string|false|none|none|
|payments|[[PaymentRequest](#schemapaymentrequest)]|false|none|none|

<h2 id="tocS_ResultListString">ResultListString</h2>
<!-- backwards compatibility -->
<a id="schemaresultliststring"></a>
<a id="schema_ResultListString"></a>
<a id="tocSresultliststring"></a>
<a id="tocsresultliststring"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": [
    "string"
  ],
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[string]|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_CreatePurchaseOrderDraftRequest">CreatePurchaseOrderDraftRequest</h2>
<!-- backwards compatibility -->
<a id="schemacreatepurchaseorderdraftrequest"></a>
<a id="schema_CreatePurchaseOrderDraftRequest"></a>
<a id="tocScreatepurchaseorderdraftrequest"></a>
<a id="tocscreatepurchaseorderdraftrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "data": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|data|string|false|none|none|

<h2 id="tocS_PurchaseOrderDraftDto">PurchaseOrderDraftDto</h2>
<!-- backwards compatibility -->
<a id="schemapurchaseorderdraftdto"></a>
<a id="schema_PurchaseOrderDraftDto"></a>
<a id="tocSpurchaseorderdraftdto"></a>
<a id="tocspurchaseorderdraftdto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "data": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|data|string|false|none|none|

<h2 id="tocS_ResultPurchaseOrderDraftDto">ResultPurchaseOrderDraftDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultpurchaseorderdraftdto"></a>
<a id="schema_ResultPurchaseOrderDraftDto"></a>
<a id="tocSresultpurchaseorderdraftdto"></a>
<a id="tocsresultpurchaseorderdraftdto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": {
    "id": 0,
    "code": "string",
    "version": 0,
    "created_by": "string",
    "created_name": "string",
    "created_date": "2019-08-24T14:15:22Z",
    "updated_by": "string",
    "updated_name": "string",
    "updated_date": "2019-08-24T14:15:22Z",
    "data": "string"
  },
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[PurchaseOrderDraftDto](#schemapurchaseorderdraftdto)|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_PaymentConditionDto">PaymentConditionDto</h2>
<!-- backwards compatibility -->
<a id="schemapaymentconditiondto"></a>
<a id="schema_PaymentConditionDto"></a>
<a id="tocSpaymentconditiondto"></a>
<a id="tocspaymentconditiondto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "timeout": 0,
  "note": "string",
  "default": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|timeout|integer(int32)|false|none|none|
|note|string|false|none|none|
|default|boolean|false|none|none|

<h2 id="tocS_ResultPaymentConditionDto">ResultPaymentConditionDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultpaymentconditiondto"></a>
<a id="schema_ResultPaymentConditionDto"></a>
<a id="tocSresultpaymentconditiondto"></a>
<a id="tocsresultpaymentconditiondto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": {
    "id": 0,
    "code": "string",
    "version": 0,
    "created_by": "string",
    "created_name": "string",
    "created_date": "2019-08-24T14:15:22Z",
    "updated_by": "string",
    "updated_name": "string",
    "updated_date": "2019-08-24T14:15:22Z",
    "timeout": 0,
    "note": "string",
    "default": true
  },
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[PaymentConditionDto](#schemapaymentconditiondto)|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_CreateImportJobRequest">CreateImportJobRequest</h2>
<!-- backwards compatibility -->
<a id="schemacreateimportjobrequest"></a>
<a id="schema_CreateImportJobRequest"></a>
<a id="tocScreateimportjobrequest"></a>
<a id="tocscreateimportjobrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "conditions": "string",
  "type": "string",
  "hidden_fields": "string",
  "url": "string",
  "note": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|conditions|string|false|none|none|
|type|string|false|none|none|
|hidden_fields|string|false|none|none|
|url|string|true|none|none|
|note|string|false|none|none|

<h2 id="tocS_JobDto">JobDto</h2>
<!-- backwards compatibility -->
<a id="schemajobdto"></a>
<a id="schema_JobDto"></a>
<a id="tocSjobdto"></a>
<a id="tocsjobdto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "name": "string",
  "status": "string",
  "num_of_record": 0,
  "total": 0,
  "url": "string",
  "total_process": 0,
  "processed": 0,
  "success": 0,
  "percent": 0,
  "error": 0,
  "message": [
    {}
  ],
  "note": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|name|string|false|none|none|
|status|string|false|none|none|
|num_of_record|integer(int32)|false|none|none|
|total|integer(int64)|false|none|none|
|url|string|false|none|none|
|total_process|integer(int64)|false|none|none|
|processed|integer(int64)|false|none|none|
|success|integer(int64)|false|none|none|
|percent|integer(int64)|false|none|none|
|error|integer(int64)|false|none|none|
|message|[object]|false|none|none|
|note|string|false|none|none|

<h2 id="tocS_ResultJobDto">ResultJobDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultjobdto"></a>
<a id="schema_ResultJobDto"></a>
<a id="tocSresultjobdto"></a>
<a id="tocsresultjobdto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": {
    "id": 0,
    "code": "string",
    "version": 0,
    "created_by": "string",
    "created_name": "string",
    "created_date": "2019-08-24T14:15:22Z",
    "updated_by": "string",
    "updated_name": "string",
    "updated_date": "2019-08-24T14:15:22Z",
    "name": "string",
    "status": "string",
    "num_of_record": 0,
    "total": 0,
    "url": "string",
    "total_process": 0,
    "processed": 0,
    "success": 0,
    "percent": 0,
    "error": 0,
    "message": [
      {}
    ],
    "note": "string"
  },
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[JobDto](#schemajobdto)|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_CreateExportJobRequest">CreateExportJobRequest</h2>
<!-- backwards compatibility -->
<a id="schemacreateexportjobrequest"></a>
<a id="schema_CreateExportJobRequest"></a>
<a id="tocScreateexportjobrequest"></a>
<a id="tocscreateexportjobrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "conditions": "string",
  "type": "string",
  "hidden_fields": "string",
  "url": "string",
  "url_template": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|conditions|string|false|none|none|
|type|string|false|none|none|
|hidden_fields|string|false|none|none|
|url|string|false|none|none|
|url_template|string|false|none|none|

<h2 id="tocS_PurchaseOrderConfigRequest">PurchaseOrderConfigRequest</h2>
<!-- backwards compatibility -->
<a id="schemapurchaseorderconfigrequest"></a>
<a id="schema_PurchaseOrderConfigRequest"></a>
<a id="tocSpurchaseorderconfigrequest"></a>
<a id="tocspurchaseorderconfigrequest"></a>

```json
{
  "created_by": "string",
  "created_name": "string",
  "updated_by": "string",
  "updated_name": "string",
  "request_id": "string",
  "operator_kc_id": "string",
  "id": 0,
  "json_content": "string",
  "name": "string",
  "type": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|request_id|string|false|none|none|
|operator_kc_id|string|false|none|none|
|id|integer(int64)|false|none|none|
|json_content|string|false|none|none|
|name|string|false|none|none|
|type|string|true|none|none|

<h2 id="tocS_PurchaseOrderConfigDto">PurchaseOrderConfigDto</h2>
<!-- backwards compatibility -->
<a id="schemapurchaseorderconfigdto"></a>
<a id="schema_PurchaseOrderConfigDto"></a>
<a id="tocSpurchaseorderconfigdto"></a>
<a id="tocspurchaseorderconfigdto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "status": "string",
  "json_content": "string",
  "name": "string",
  "type": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|status|string|false|none|none|
|json_content|string|false|none|none|
|name|string|false|none|none|
|type|string|false|none|none|

<h2 id="tocS_ResultPurchaseOrderConfigDto">ResultPurchaseOrderConfigDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultpurchaseorderconfigdto"></a>
<a id="schema_ResultPurchaseOrderConfigDto"></a>
<a id="tocSresultpurchaseorderconfigdto"></a>
<a id="tocsresultpurchaseorderconfigdto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": {
    "id": 0,
    "code": "string",
    "version": 0,
    "created_by": "string",
    "created_name": "string",
    "created_date": "2019-08-24T14:15:22Z",
    "updated_by": "string",
    "updated_name": "string",
    "updated_date": "2019-08-24T14:15:22Z",
    "status": "string",
    "json_content": "string",
    "name": "string",
    "type": "string"
  },
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[PurchaseOrderConfigDto](#schemapurchaseorderconfigdto)|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_Metadata">Metadata</h2>
<!-- backwards compatibility -->
<a id="schemametadata"></a>
<a id="schema_Metadata"></a>
<a id="tocSmetadata"></a>
<a id="tocsmetadata"></a>

```json
{
  "total": 0,
  "page": 0,
  "limit": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|total|integer(int64)|false|none|none|
|page|integer(int32)|false|none|none|
|limit|integer(int32)|false|none|none|

<h2 id="tocS_PageableDtoSimplePurchaseOrderDto">PageableDtoSimplePurchaseOrderDto</h2>
<!-- backwards compatibility -->
<a id="schemapageabledtosimplepurchaseorderdto"></a>
<a id="schema_PageableDtoSimplePurchaseOrderDto"></a>
<a id="tocSpageabledtosimplepurchaseorderdto"></a>
<a id="tocspageabledtosimplepurchaseorderdto"></a>

```json
{
  "metadata": {
    "total": 0,
    "page": 0,
    "limit": 0
  },
  "items": [
    {
      "id": 0,
      "companyId": 0,
      "merchandiserCode": "string",
      "merchandiser": "string",
      "designerCode": "string",
      "designer": "string",
      "qcCode": "string",
      "qc": "string",
      "reference": "string",
      "type": "string",
      "code": "string",
      "supplierId": 0,
      "supplierCode": "string",
      "supplier": "string",
      "phone": "string",
      "supplierNote": "string",
      "expectImportDate": "2019-08-24T14:15:22Z",
      "expectReturnDate": "2019-08-24T14:15:22Z",
      "expectStoreId": 0,
      "expectStore": "string",
      "paymentConditionId": 0,
      "paymentConditionName": "string",
      "paymentNote": "string",
      "note": "string",
      "tags": "string",
      "policyPriceCode": "string",
      "taxIncluded": true,
      "paymentDiscountRate": 0,
      "paymentDiscountValue": 0,
      "paymentDiscountAmount": 0,
      "tradeDiscountRate": 0,
      "tradeDiscountValue": 0,
      "tradeDiscountAmount": 0,
      "untaxedAmount": 0,
      "untaxedAmountRefunds": 0,
      "tax": 0,
      "total": 0,
      "totalPayment": 0,
      "totalPaid": 0,
      "totalRefunds": 0,
      "receiptQuantity": 0,
      "plannedQuantity": 0,
      "status": "string",
      "financialStatus": "string",
      "receiveStatus": "string",
      "cancelReason": "string",
      "orderDate": "2019-08-24T14:15:22Z",
      "cancelledDate": "2019-08-24T14:15:22Z",
      "activatedDate": "2019-08-24T14:15:22Z",
      "completedDate": "2019-08-24T14:15:22Z",
      "completedStockDate": "2019-08-24T14:15:22Z",
      "createdDate": "2019-08-24T14:15:22Z",
      "updatedDate": "2019-08-24T14:15:22Z",
      "createdBy": "string",
      "createdName": "string",
      "updatedBy": "string",
      "updatedName": "string",
      "procurements": [
        {
          "id": 0,
          "reference": "string",
          "storeId": 0,
          "store": "string",
          "expectReceiptDate": "2019-08-24T14:15:22Z",
          "note": "string",
          "status": "string",
          "statusName": "string",
          "activatedDate": "2019-08-24T14:15:22Z",
          "activatedBy": "string",
          "stockInDate": "2019-08-24T14:15:22Z",
          "stockInBy": "string",
          "isCancelled": true,
          "purchaseOrderId": 0
        }
      ]
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|metadata|[Metadata](#schemametadata)|false|none|none|
|items|[[SimplePurchaseOrderDto](#schemasimplepurchaseorderdto)]|false|none|none|

<h2 id="tocS_ResultPageableDtoSimplePurchaseOrderDto">ResultPageableDtoSimplePurchaseOrderDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultpageabledtosimplepurchaseorderdto"></a>
<a id="schema_ResultPageableDtoSimplePurchaseOrderDto"></a>
<a id="tocSresultpageabledtosimplepurchaseorderdto"></a>
<a id="tocsresultpageabledtosimplepurchaseorderdto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": {
    "metadata": {
      "total": 0,
      "page": 0,
      "limit": 0
    },
    "items": [
      {
        "id": 0,
        "companyId": 0,
        "merchandiserCode": "string",
        "merchandiser": "string",
        "designerCode": "string",
        "designer": "string",
        "qcCode": "string",
        "qc": "string",
        "reference": "string",
        "type": "string",
        "code": "string",
        "supplierId": 0,
        "supplierCode": "string",
        "supplier": "string",
        "phone": "string",
        "supplierNote": "string",
        "expectImportDate": "2019-08-24T14:15:22Z",
        "expectReturnDate": "2019-08-24T14:15:22Z",
        "expectStoreId": 0,
        "expectStore": "string",
        "paymentConditionId": 0,
        "paymentConditionName": "string",
        "paymentNote": "string",
        "note": "string",
        "tags": "string",
        "policyPriceCode": "string",
        "taxIncluded": true,
        "paymentDiscountRate": 0,
        "paymentDiscountValue": 0,
        "paymentDiscountAmount": 0,
        "tradeDiscountRate": 0,
        "tradeDiscountValue": 0,
        "tradeDiscountAmount": 0,
        "untaxedAmount": 0,
        "untaxedAmountRefunds": 0,
        "tax": 0,
        "total": 0,
        "totalPayment": 0,
        "totalPaid": 0,
        "totalRefunds": 0,
        "receiptQuantity": 0,
        "plannedQuantity": 0,
        "status": "string",
        "financialStatus": "string",
        "receiveStatus": "string",
        "cancelReason": "string",
        "orderDate": "2019-08-24T14:15:22Z",
        "cancelledDate": "2019-08-24T14:15:22Z",
        "activatedDate": "2019-08-24T14:15:22Z",
        "completedDate": "2019-08-24T14:15:22Z",
        "completedStockDate": "2019-08-24T14:15:22Z",
        "createdDate": "2019-08-24T14:15:22Z",
        "updatedDate": "2019-08-24T14:15:22Z",
        "createdBy": "string",
        "createdName": "string",
        "updatedBy": "string",
        "updatedName": "string",
        "procurements": [
          {
            "id": 0,
            "reference": "string",
            "storeId": 0,
            "store": "string",
            "expectReceiptDate": "2019-08-24T14:15:22Z",
            "note": "string",
            "status": "string",
            "statusName": "string",
            "activatedDate": "2019-08-24T14:15:22Z",
            "activatedBy": "string",
            "stockInDate": "2019-08-24T14:15:22Z",
            "stockInBy": "string",
            "isCancelled": true,
            "purchaseOrderId": 0
          }
        ]
      }
    ]
  },
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[PageableDtoSimplePurchaseOrderDto](#schemapageabledtosimplepurchaseorderdto)|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_SimpleProcurementDto">SimpleProcurementDto</h2>
<!-- backwards compatibility -->
<a id="schemasimpleprocurementdto"></a>
<a id="schema_SimpleProcurementDto"></a>
<a id="tocSsimpleprocurementdto"></a>
<a id="tocssimpleprocurementdto"></a>

```json
{
  "id": 0,
  "reference": "string",
  "storeId": 0,
  "store": "string",
  "expectReceiptDate": "2019-08-24T14:15:22Z",
  "note": "string",
  "status": "string",
  "statusName": "string",
  "activatedDate": "2019-08-24T14:15:22Z",
  "activatedBy": "string",
  "stockInDate": "2019-08-24T14:15:22Z",
  "stockInBy": "string",
  "isCancelled": true,
  "purchaseOrderId": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|reference|string|false|none|none|
|storeId|integer(int64)|false|none|none|
|store|string|false|none|none|
|expectReceiptDate|string(date-time)|false|none|none|
|note|string|false|none|none|
|status|string|false|none|none|
|statusName|string|false|none|none|
|activatedDate|string(date-time)|false|none|none|
|activatedBy|string|false|none|none|
|stockInDate|string(date-time)|false|none|none|
|stockInBy|string|false|none|none|
|isCancelled|boolean|false|none|none|
|purchaseOrderId|integer(int64)|false|none|none|

<h2 id="tocS_SimplePurchaseOrderDto">SimplePurchaseOrderDto</h2>
<!-- backwards compatibility -->
<a id="schemasimplepurchaseorderdto"></a>
<a id="schema_SimplePurchaseOrderDto"></a>
<a id="tocSsimplepurchaseorderdto"></a>
<a id="tocssimplepurchaseorderdto"></a>

```json
{
  "id": 0,
  "companyId": 0,
  "merchandiserCode": "string",
  "merchandiser": "string",
  "designerCode": "string",
  "designer": "string",
  "qcCode": "string",
  "qc": "string",
  "reference": "string",
  "type": "string",
  "code": "string",
  "supplierId": 0,
  "supplierCode": "string",
  "supplier": "string",
  "phone": "string",
  "supplierNote": "string",
  "expectImportDate": "2019-08-24T14:15:22Z",
  "expectReturnDate": "2019-08-24T14:15:22Z",
  "expectStoreId": 0,
  "expectStore": "string",
  "paymentConditionId": 0,
  "paymentConditionName": "string",
  "paymentNote": "string",
  "note": "string",
  "tags": "string",
  "policyPriceCode": "string",
  "taxIncluded": true,
  "paymentDiscountRate": 0,
  "paymentDiscountValue": 0,
  "paymentDiscountAmount": 0,
  "tradeDiscountRate": 0,
  "tradeDiscountValue": 0,
  "tradeDiscountAmount": 0,
  "untaxedAmount": 0,
  "untaxedAmountRefunds": 0,
  "tax": 0,
  "total": 0,
  "totalPayment": 0,
  "totalPaid": 0,
  "totalRefunds": 0,
  "receiptQuantity": 0,
  "plannedQuantity": 0,
  "status": "string",
  "financialStatus": "string",
  "receiveStatus": "string",
  "cancelReason": "string",
  "orderDate": "2019-08-24T14:15:22Z",
  "cancelledDate": "2019-08-24T14:15:22Z",
  "activatedDate": "2019-08-24T14:15:22Z",
  "completedDate": "2019-08-24T14:15:22Z",
  "completedStockDate": "2019-08-24T14:15:22Z",
  "createdDate": "2019-08-24T14:15:22Z",
  "updatedDate": "2019-08-24T14:15:22Z",
  "createdBy": "string",
  "createdName": "string",
  "updatedBy": "string",
  "updatedName": "string",
  "procurements": [
    {
      "id": 0,
      "reference": "string",
      "storeId": 0,
      "store": "string",
      "expectReceiptDate": "2019-08-24T14:15:22Z",
      "note": "string",
      "status": "string",
      "statusName": "string",
      "activatedDate": "2019-08-24T14:15:22Z",
      "activatedBy": "string",
      "stockInDate": "2019-08-24T14:15:22Z",
      "stockInBy": "string",
      "isCancelled": true,
      "purchaseOrderId": 0
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|companyId|integer(int64)|false|none|none|
|merchandiserCode|string|false|none|none|
|merchandiser|string|false|none|none|
|designerCode|string|false|none|none|
|designer|string|false|none|none|
|qcCode|string|false|none|none|
|qc|string|false|none|none|
|reference|string|false|none|none|
|type|string|false|none|none|
|code|string|false|none|none|
|supplierId|integer(int64)|false|none|none|
|supplierCode|string|false|none|none|
|supplier|string|false|none|none|
|phone|string|false|none|none|
|supplierNote|string|false|none|none|
|expectImportDate|string(date-time)|false|none|none|
|expectReturnDate|string(date-time)|false|none|none|
|expectStoreId|integer(int64)|false|none|none|
|expectStore|string|false|none|none|
|paymentConditionId|integer(int64)|false|none|none|
|paymentConditionName|string|false|none|none|
|paymentNote|string|false|none|none|
|note|string|false|none|none|
|tags|string|false|none|none|
|policyPriceCode|string|false|none|none|
|taxIncluded|boolean|false|none|none|
|paymentDiscountRate|number|false|none|none|
|paymentDiscountValue|number|false|none|none|
|paymentDiscountAmount|number|false|none|none|
|tradeDiscountRate|number|false|none|none|
|tradeDiscountValue|number|false|none|none|
|tradeDiscountAmount|number|false|none|none|
|untaxedAmount|number|false|none|none|
|untaxedAmountRefunds|number|false|none|none|
|tax|number|false|none|none|
|total|number|false|none|none|
|totalPayment|number|false|none|none|
|totalPaid|number|false|none|none|
|totalRefunds|number|false|none|none|
|receiptQuantity|number|false|none|none|
|plannedQuantity|number|false|none|none|
|status|string|false|none|none|
|financialStatus|string|false|none|none|
|receiveStatus|string|false|none|none|
|cancelReason|string|false|none|none|
|orderDate|string(date-time)|false|none|none|
|cancelledDate|string(date-time)|false|none|none|
|activatedDate|string(date-time)|false|none|none|
|completedDate|string(date-time)|false|none|none|
|completedStockDate|string(date-time)|false|none|none|
|createdDate|string(date-time)|false|none|none|
|updatedDate|string(date-time)|false|none|none|
|createdBy|string|false|none|none|
|createdName|string|false|none|none|
|updatedBy|string|false|none|none|
|updatedName|string|false|none|none|
|procurements|[[SimpleProcurementDto](#schemasimpleprocurementdto)]|false|none|none|

<h2 id="tocS_PurchaseOrderLogDto">PurchaseOrderLogDto</h2>
<!-- backwards compatibility -->
<a id="schemapurchaseorderlogdto"></a>
<a id="schema_PurchaseOrderLogDto"></a>
<a id="tocSpurchaseorderlogdto"></a>
<a id="tocspurchaseorderlogdto"></a>

```json
{
  "id": 0,
  "root_id": 0,
  "code": "string",
  "updated_name": "string",
  "updated_by": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "created_name": "string",
  "created_by": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "data": "string",
  "action": "string",
  "status_before": "string",
  "status_after": "string",
  "ip_address": "string",
  "device": "string",
  "procurement_code": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|root_id|integer(int64)|false|none|none|
|code|string|false|none|none|
|updated_name|string|false|none|none|
|updated_by|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|created_name|string|false|none|none|
|created_by|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|data|string|false|none|none|
|action|string|false|none|none|
|status_before|string|false|none|none|
|status_after|string|false|none|none|
|ip_address|string|false|none|none|
|device|string|false|none|none|
|procurement_code|string|false|none|none|

<h2 id="tocS_ResultListPurchaseOrderLogDto">ResultListPurchaseOrderLogDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultlistpurchaseorderlogdto"></a>
<a id="schema_ResultListPurchaseOrderLogDto"></a>
<a id="tocSresultlistpurchaseorderlogdto"></a>
<a id="tocsresultlistpurchaseorderlogdto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": [
    {
      "id": 0,
      "root_id": 0,
      "code": "string",
      "updated_name": "string",
      "updated_by": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "created_name": "string",
      "created_by": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "data": "string",
      "action": "string",
      "status_before": "string",
      "status_after": "string",
      "ip_address": "string",
      "device": "string",
      "procurement_code": "string"
    }
  ],
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[[PurchaseOrderLogDto](#schemapurchaseorderlogdto)]|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_PageableDtoProcurementDto">PageableDtoProcurementDto</h2>
<!-- backwards compatibility -->
<a id="schemapageabledtoprocurementdto"></a>
<a id="schema_PageableDtoProcurementDto"></a>
<a id="tocSpageabledtoprocurementdto"></a>
<a id="tocspageabledtoprocurementdto"></a>

```json
{
  "metadata": {
    "total": 0,
    "page": 0,
    "limit": 0
  },
  "items": [
    {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "reference": "string",
      "store_id": 0,
      "store": "string",
      "expect_receipt_date": "2019-08-24T14:15:22Z",
      "note": "string",
      "status": "string",
      "status_name": "string",
      "activated_date": "2019-08-24T14:15:22Z",
      "activated_by": "string",
      "stock_in_date": "2019-08-24T14:15:22Z",
      "stock_in_by": "string",
      "is_cancelled": true,
      "created_date_str": "string",
      "purchase_order": {
        "id": 0,
        "company_id": 0,
        "merchandiser_code": "string",
        "merchandiser": "string",
        "designer_code": "string",
        "designer": "string",
        "qc_code": "string",
        "qc": "string",
        "reference": "string",
        "type": "string",
        "code": "string",
        "supplier_id": 0,
        "supplier_code": "string",
        "supplier": "string",
        "phone": "string"
      },
      "procurement_items": [
        {
          "id": 0,
          "code": "string",
          "version": 0,
          "created_by": "string",
          "created_name": "string",
          "created_date": "2019-08-24T14:15:22Z",
          "updated_by": "string",
          "updated_name": "string",
          "updated_date": "2019-08-24T14:15:22Z",
          "line_item_id": 0,
          "sku": "string",
          "barcode": "string",
          "variant": "string",
          "variant_image": "string",
          "variant_id": 0,
          "retail_price": 0,
          "ordered_quantity": 0,
          "accepted_quantity": 0,
          "planned_quantity": 0,
          "quantity": 0,
          "real_quantity": 0,
          "note": "string",
          "price": 0,
          "vat": 0,
          "vat_rate": 0,
          "amount": 0
        }
      ]
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|metadata|[Metadata](#schemametadata)|false|none|none|
|items|[[ProcurementDto](#schemaprocurementdto)]|false|none|none|

<h2 id="tocS_ResultPageableDtoProcurementDto">ResultPageableDtoProcurementDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultpageabledtoprocurementdto"></a>
<a id="schema_ResultPageableDtoProcurementDto"></a>
<a id="tocSresultpageabledtoprocurementdto"></a>
<a id="tocsresultpageabledtoprocurementdto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": {
    "metadata": {
      "total": 0,
      "page": 0,
      "limit": 0
    },
    "items": [
      {
        "id": 0,
        "code": "string",
        "version": 0,
        "created_by": "string",
        "created_name": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "updated_by": "string",
        "updated_name": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "reference": "string",
        "store_id": 0,
        "store": "string",
        "expect_receipt_date": "2019-08-24T14:15:22Z",
        "note": "string",
        "status": "string",
        "status_name": "string",
        "activated_date": "2019-08-24T14:15:22Z",
        "activated_by": "string",
        "stock_in_date": "2019-08-24T14:15:22Z",
        "stock_in_by": "string",
        "is_cancelled": true,
        "created_date_str": "string",
        "purchase_order": {
          "id": 0,
          "company_id": 0,
          "merchandiser_code": "string",
          "merchandiser": "string",
          "designer_code": "string",
          "designer": "string",
          "qc_code": "string",
          "qc": "string",
          "reference": "string",
          "type": "string",
          "code": "string",
          "supplier_id": 0,
          "supplier_code": "string",
          "supplier": "string",
          "phone": "string"
        },
        "procurement_items": [
          {
            "id": 0,
            "code": "string",
            "version": 0,
            "created_by": "string",
            "created_name": "string",
            "created_date": "2019-08-24T14:15:22Z",
            "updated_by": "string",
            "updated_name": "string",
            "updated_date": "2019-08-24T14:15:22Z",
            "line_item_id": 0,
            "sku": "string",
            "barcode": "string",
            "variant": "string",
            "variant_image": "string",
            "variant_id": 0,
            "retail_price": 0,
            "ordered_quantity": 0,
            "accepted_quantity": 0,
            "planned_quantity": 0,
            "quantity": 0,
            "real_quantity": 0,
            "note": "string",
            "price": 0,
            "vat": 0,
            "vat_rate": 0,
            "amount": 0
          }
        ]
      }
    ]
  },
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[PageableDtoProcurementDto](#schemapageabledtoprocurementdto)|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_ResultProcurementDto">ResultProcurementDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultprocurementdto"></a>
<a id="schema_ResultProcurementDto"></a>
<a id="tocSresultprocurementdto"></a>
<a id="tocsresultprocurementdto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": {
    "id": 0,
    "code": "string",
    "version": 0,
    "created_by": "string",
    "created_name": "string",
    "created_date": "2019-08-24T14:15:22Z",
    "updated_by": "string",
    "updated_name": "string",
    "updated_date": "2019-08-24T14:15:22Z",
    "reference": "string",
    "store_id": 0,
    "store": "string",
    "expect_receipt_date": "2019-08-24T14:15:22Z",
    "note": "string",
    "status": "string",
    "status_name": "string",
    "activated_date": "2019-08-24T14:15:22Z",
    "activated_by": "string",
    "stock_in_date": "2019-08-24T14:15:22Z",
    "stock_in_by": "string",
    "is_cancelled": true,
    "created_date_str": "string",
    "purchase_order": {
      "id": 0,
      "company_id": 0,
      "merchandiser_code": "string",
      "merchandiser": "string",
      "designer_code": "string",
      "designer": "string",
      "qc_code": "string",
      "qc": "string",
      "reference": "string",
      "type": "string",
      "code": "string",
      "supplier_id": 0,
      "supplier_code": "string",
      "supplier": "string",
      "phone": "string"
    },
    "procurement_items": [
      {
        "id": 0,
        "code": "string",
        "version": 0,
        "created_by": "string",
        "created_name": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "updated_by": "string",
        "updated_name": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "line_item_id": 0,
        "sku": "string",
        "barcode": "string",
        "variant": "string",
        "variant_image": "string",
        "variant_id": 0,
        "retail_price": 0,
        "ordered_quantity": 0,
        "accepted_quantity": 0,
        "planned_quantity": 0,
        "quantity": 0,
        "real_quantity": 0,
        "note": "string",
        "price": 0,
        "vat": 0,
        "vat_rate": 0,
        "amount": 0
      }
    ]
  },
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[ProcurementDto](#schemaprocurementdto)|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_PageableDtoProcurementItemCustomDto">PageableDtoProcurementItemCustomDto</h2>
<!-- backwards compatibility -->
<a id="schemapageabledtoprocurementitemcustomdto"></a>
<a id="schema_PageableDtoProcurementItemCustomDto"></a>
<a id="tocSpageabledtoprocurementitemcustomdto"></a>
<a id="tocspageabledtoprocurementitemcustomdto"></a>

```json
{
  "metadata": {
    "total": 0,
    "page": 0,
    "limit": 0
  },
  "items": [
    {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "line_item_id": 0,
      "sku": "string",
      "barcode": "string",
      "product_id": 0,
      "variant_id": 0,
      "variant": "string",
      "variant_image": "string",
      "ordered_quantity": 0,
      "accepted_quantity": 0,
      "planned_quantity": 0,
      "quantity": 0,
      "real_quantity": 0,
      "note": "string",
      "procurement": {
        "id": 0,
        "code": "string",
        "version": 0,
        "created_by": "string",
        "created_name": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "updated_by": "string",
        "updated_name": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "reference": "string",
        "store_id": 0,
        "store": "string",
        "expect_receipt_date": "2019-08-24T14:15:22Z",
        "note": "string",
        "status": "string",
        "status_name": "string",
        "activated_date": "2019-08-24T14:15:22Z",
        "activated_by": "string",
        "stock_in_date": "2019-08-24T14:15:22Z",
        "stock_in_by": "string",
        "is_cancelled": true,
        "purchase_order": {
          "id": 0,
          "company_id": 0,
          "merchandiser_code": "string",
          "merchandiser": "string",
          "designer_code": "string",
          "designer": "string",
          "qc_code": "string",
          "qc": "string",
          "reference": "string",
          "type": "string",
          "code": "string",
          "supplier_id": 0,
          "supplier_code": "string",
          "supplier": "string",
          "phone": "string"
        }
      }
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|metadata|[Metadata](#schemametadata)|false|none|none|
|items|[[ProcurementItemCustomDto](#schemaprocurementitemcustomdto)]|false|none|none|

<h2 id="tocS_ProcurementCustomDto">ProcurementCustomDto</h2>
<!-- backwards compatibility -->
<a id="schemaprocurementcustomdto"></a>
<a id="schema_ProcurementCustomDto"></a>
<a id="tocSprocurementcustomdto"></a>
<a id="tocsprocurementcustomdto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "reference": "string",
  "store_id": 0,
  "store": "string",
  "expect_receipt_date": "2019-08-24T14:15:22Z",
  "note": "string",
  "status": "string",
  "status_name": "string",
  "activated_date": "2019-08-24T14:15:22Z",
  "activated_by": "string",
  "stock_in_date": "2019-08-24T14:15:22Z",
  "stock_in_by": "string",
  "is_cancelled": true,
  "purchase_order": {
    "id": 0,
    "company_id": 0,
    "merchandiser_code": "string",
    "merchandiser": "string",
    "designer_code": "string",
    "designer": "string",
    "qc_code": "string",
    "qc": "string",
    "reference": "string",
    "type": "string",
    "code": "string",
    "supplier_id": 0,
    "supplier_code": "string",
    "supplier": "string",
    "phone": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|reference|string|false|none|none|
|store_id|integer(int64)|false|none|none|
|store|string|false|none|none|
|expect_receipt_date|string(date-time)|false|none|none|
|note|string|false|none|none|
|status|string|false|none|none|
|status_name|string|false|none|none|
|activated_date|string(date-time)|false|none|none|
|activated_by|string|false|none|none|
|stock_in_date|string(date-time)|false|none|none|
|stock_in_by|string|false|none|none|
|is_cancelled|boolean|false|none|none|
|purchase_order|[PurchaseOrderProcurementDto](#schemapurchaseorderprocurementdto)|false|none|none|

<h2 id="tocS_ProcurementItemCustomDto">ProcurementItemCustomDto</h2>
<!-- backwards compatibility -->
<a id="schemaprocurementitemcustomdto"></a>
<a id="schema_ProcurementItemCustomDto"></a>
<a id="tocSprocurementitemcustomdto"></a>
<a id="tocsprocurementitemcustomdto"></a>

```json
{
  "id": 0,
  "code": "string",
  "version": 0,
  "created_by": "string",
  "created_name": "string",
  "created_date": "2019-08-24T14:15:22Z",
  "updated_by": "string",
  "updated_name": "string",
  "updated_date": "2019-08-24T14:15:22Z",
  "line_item_id": 0,
  "sku": "string",
  "barcode": "string",
  "product_id": 0,
  "variant_id": 0,
  "variant": "string",
  "variant_image": "string",
  "ordered_quantity": 0,
  "accepted_quantity": 0,
  "planned_quantity": 0,
  "quantity": 0,
  "real_quantity": 0,
  "note": "string",
  "procurement": {
    "id": 0,
    "code": "string",
    "version": 0,
    "created_by": "string",
    "created_name": "string",
    "created_date": "2019-08-24T14:15:22Z",
    "updated_by": "string",
    "updated_name": "string",
    "updated_date": "2019-08-24T14:15:22Z",
    "reference": "string",
    "store_id": 0,
    "store": "string",
    "expect_receipt_date": "2019-08-24T14:15:22Z",
    "note": "string",
    "status": "string",
    "status_name": "string",
    "activated_date": "2019-08-24T14:15:22Z",
    "activated_by": "string",
    "stock_in_date": "2019-08-24T14:15:22Z",
    "stock_in_by": "string",
    "is_cancelled": true,
    "purchase_order": {
      "id": 0,
      "company_id": 0,
      "merchandiser_code": "string",
      "merchandiser": "string",
      "designer_code": "string",
      "designer": "string",
      "qc_code": "string",
      "qc": "string",
      "reference": "string",
      "type": "string",
      "code": "string",
      "supplier_id": 0,
      "supplier_code": "string",
      "supplier": "string",
      "phone": "string"
    }
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int64)|false|none|none|
|code|string|false|none|none|
|version|integer(int32)|false|none|none|
|created_by|string|false|none|none|
|created_name|string|false|none|none|
|created_date|string(date-time)|false|none|none|
|updated_by|string|false|none|none|
|updated_name|string|false|none|none|
|updated_date|string(date-time)|false|none|none|
|line_item_id|integer(int64)|false|none|none|
|sku|string|false|none|none|
|barcode|string|false|none|none|
|product_id|integer(int64)|false|none|none|
|variant_id|integer(int64)|false|none|none|
|variant|string|false|none|none|
|variant_image|string|false|none|none|
|ordered_quantity|number|false|none|none|
|accepted_quantity|number|false|none|none|
|planned_quantity|number|false|none|none|
|quantity|number|false|none|none|
|real_quantity|number|false|none|none|
|note|string|false|none|none|
|procurement|[ProcurementCustomDto](#schemaprocurementcustomdto)|false|none|none|

<h2 id="tocS_ResultPageableDtoProcurementItemCustomDto">ResultPageableDtoProcurementItemCustomDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultpageabledtoprocurementitemcustomdto"></a>
<a id="schema_ResultPageableDtoProcurementItemCustomDto"></a>
<a id="tocSresultpageabledtoprocurementitemcustomdto"></a>
<a id="tocsresultpageabledtoprocurementitemcustomdto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": {
    "metadata": {
      "total": 0,
      "page": 0,
      "limit": 0
    },
    "items": [
      {
        "id": 0,
        "code": "string",
        "version": 0,
        "created_by": "string",
        "created_name": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "updated_by": "string",
        "updated_name": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "line_item_id": 0,
        "sku": "string",
        "barcode": "string",
        "product_id": 0,
        "variant_id": 0,
        "variant": "string",
        "variant_image": "string",
        "ordered_quantity": 0,
        "accepted_quantity": 0,
        "planned_quantity": 0,
        "quantity": 0,
        "real_quantity": 0,
        "note": "string",
        "procurement": {
          "id": 0,
          "code": "string",
          "version": 0,
          "created_by": "string",
          "created_name": "string",
          "created_date": "2019-08-24T14:15:22Z",
          "updated_by": "string",
          "updated_name": "string",
          "updated_date": "2019-08-24T14:15:22Z",
          "reference": "string",
          "store_id": 0,
          "store": "string",
          "expect_receipt_date": "2019-08-24T14:15:22Z",
          "note": "string",
          "status": "string",
          "status_name": "string",
          "activated_date": "2019-08-24T14:15:22Z",
          "activated_by": "string",
          "stock_in_date": "2019-08-24T14:15:22Z",
          "stock_in_by": "string",
          "is_cancelled": true,
          "purchase_order": {
            "id": 0,
            "company_id": 0,
            "merchandiser_code": "string",
            "merchandiser": "string",
            "designer_code": "string",
            "designer": "string",
            "qc_code": "string",
            "qc": "string",
            "reference": "string",
            "type": "string",
            "code": "string",
            "supplier_id": 0,
            "supplier_code": "string",
            "supplier": "string",
            "phone": "string"
          }
        }
      }
    ]
  },
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[PageableDtoProcurementItemCustomDto](#schemapageabledtoprocurementitemcustomdto)|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_ProcurementPrintForm">ProcurementPrintForm</h2>
<!-- backwards compatibility -->
<a id="schemaprocurementprintform"></a>
<a id="schema_ProcurementPrintForm"></a>
<a id="tocSprocurementprintform"></a>
<a id="tocsprocurementprintform"></a>

```json
{
  "procurementId": 0,
  "htmlContent": "string",
  "size": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|procurementId|integer(int64)|false|none|none|
|htmlContent|string|false|none|none|
|size|string|false|none|none|

<h2 id="tocS_PurchaseOrderPrintForm">PurchaseOrderPrintForm</h2>
<!-- backwards compatibility -->
<a id="schemapurchaseorderprintform"></a>
<a id="schema_PurchaseOrderPrintForm"></a>
<a id="tocSpurchaseorderprintform"></a>
<a id="tocspurchaseorderprintform"></a>

```json
{
  "purchaseOrderId": 0,
  "htmlContent": "string",
  "size": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|purchaseOrderId|integer(int64)|false|none|none|
|htmlContent|string|false|none|none|
|size|string|false|none|none|

<h2 id="tocS_ResultObject">ResultObject</h2>
<!-- backwards compatibility -->
<a id="schemaresultobject"></a>
<a id="schema_ResultObject"></a>
<a id="tocSresultobject"></a>
<a id="tocsresultobject"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": {},
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|object|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_ResultListPurchaseOrderDto">ResultListPurchaseOrderDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultlistpurchaseorderdto"></a>
<a id="schema_ResultListPurchaseOrderDto"></a>
<a id="tocSresultlistpurchaseorderdto"></a>
<a id="tocsresultlistpurchaseorderdto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": [
    {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "company_id": 0,
      "merchandiser_code": "string",
      "merchandiser": "string",
      "designer_code": "string",
      "designer": "string",
      "qc_code": "string",
      "qc": "string",
      "reference": "string",
      "type": "string",
      "supplier_id": 0,
      "supplier_code": "string",
      "supplier": "string",
      "billing_address": {
        "id": 0,
        "code": "string",
        "version": 0,
        "created_by": "string",
        "created_name": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "updated_by": "string",
        "updated_name": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "name": "string",
        "email": "string",
        "phone": "string",
        "tax_code": "string",
        "country_id": 0,
        "country": "string",
        "city_id": 0,
        "city": "string",
        "district_id": 0,
        "district": "string",
        "ward_id": 0,
        "ward": "string",
        "zip_code": "string",
        "full_address": "string",
        "bank_number": "string",
        "bank_name": "string",
        "beneficiary": "string",
        "position": "string"
      },
      "supplier_address": {
        "id": 0,
        "code": "string",
        "version": 0,
        "created_by": "string",
        "created_name": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "updated_by": "string",
        "updated_name": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "name": "string",
        "email": "string",
        "phone": "string",
        "tax_code": "string",
        "country_id": 0,
        "country": "string",
        "city_id": 0,
        "city": "string",
        "district_id": 0,
        "district": "string",
        "ward_id": 0,
        "ward": "string",
        "zip_code": "string",
        "full_address": "string",
        "bank_number": "string",
        "bank_name": "string",
        "beneficiary": "string",
        "position": "string"
      },
      "line_items": [
        {
          "id": 0,
          "code": "string",
          "version": 0,
          "created_by": "string",
          "created_name": "string",
          "created_date": "2019-08-24T14:15:22Z",
          "updated_by": "string",
          "updated_name": "string",
          "updated_date": "2019-08-24T14:15:22Z",
          "sku": "string",
          "barcode": "string",
          "variant_id": 0,
          "variant_detail": {
            "id": 0,
            "code": "string",
            "version": 0,
            "created_by": "string",
            "created_name": "string",
            "created_date": "2019-08-24T14:15:22Z",
            "updated_by": "string",
            "updated_name": "string",
            "updated_date": "2019-08-24T14:15:22Z",
            "name": "string",
            "on_hand": 0,
            "available": 0,
            "committed": 0,
            "in_coming": 0,
            "on_way": 0,
            "on_hold": 0,
            "defect": 0,
            "transferring": 0,
            "shipping": 0,
            "total_stock": 0,
            "supplier_id": 0,
            "supplier": "string",
            "color_id": 0,
            "color": "string",
            "size_id": 0,
            "size": "string",
            "barcode": "string",
            "reference_id": 0,
            "taxable": true,
            "saleable": true,
            "sku": "string",
            "status": "string",
            "status_name": "string",
            "composite": true,
            "width": 0,
            "length": 0,
            "height": 0,
            "weight": 0,
            "weight_unit": "string",
            "length_unit": "string",
            "product_id": 0,
            "product": {
              "id": 0,
              "code": "string",
              "version": 0,
              "created_by": "string",
              "created_name": "string",
              "created_date": "2019-08-24T14:15:22Z",
              "updated_by": "string",
              "updated_name": "string",
              "updated_date": "2019-08-24T14:15:22Z",
              "category_id": 0,
              "category": "string",
              "material_id": 0,
              "goods": "string",
              "material": "string",
              "brand": "string",
              "brand_name": "string",
              "made_in_id": 0,
              "made_in": "string",
              "description": "string",
              "content": "string",
              "merchandiser_code": "string",
              "designer_code": "string",
              "merchandiser": "string",
              "designer": "string",
              "tags": "string",
              "status": "string",
              "status_name": "string",
              "name": "string",
              "care_labels": "string",
              "unit": "string",
              "specifications": "string",
              "product_type": "string",
              "product_collections": [
                "string"
              ]
            },
            "variant_prices": [
              {
                "id": 0,
                "retail_price": 0,
                "variant_id": 0,
                "currency_code": "string",
                "currency_symbol": "string",
                "tax_percent": 0,
                "cost_price": 0,
                "import_price": 0,
                "wholesale_price": 0
              }
            ],
            "variant_images": [
              {
                "id": 0,
                "variant_id": 0,
                "position": 0,
                "image_id": 0,
                "url": "string",
                "product_avatar": true,
                "variant_avatar": true
              }
            ],
            "composites": [
              {
                "id": 0,
                "variant_id": 0,
                "sub_variant_id": 0,
                "quantity": 0
              }
            ]
          },
          "product_id": 0,
          "product": "string",
          "variant": "string",
          "retail_price": 0,
          "product_type": "string",
          "quantity": 0,
          "receipt_quantity": 0,
          "planned_quantity": 0,
          "price": 0,
          "amount": 0,
          "note": "string",
          "type": "string",
          "variant_image": "string",
          "unit": "string",
          "tax": 0,
          "tax_rate": 0,
          "line_amount_after_line_discount": 0,
          "discount_rate": 0,
          "discount_value": 0,
          "discount_amount": 0,
          "position": 0,
          "purchase_order_id": 0
        }
      ],
      "return_orders": [
        {
          "id": 0,
          "code": "string",
          "version": 0,
          "created_by": "string",
          "created_name": "string",
          "created_date": "2019-08-24T14:15:22Z",
          "updated_by": "string",
          "updated_name": "string",
          "updated_date": "2019-08-24T14:15:22Z",
          "line_return_items": [
            {
              "id": 0,
              "code": "string",
              "version": 0,
              "created_by": "string",
              "created_name": "string",
              "created_date": "2019-08-24T14:15:22Z",
              "updated_by": "string",
              "updated_name": "string",
              "updated_date": "2019-08-24T14:15:22Z",
              "sku": "string",
              "barcode": "string",
              "variant_id": 0,
              "product_id": 0,
              "product": "string",
              "variant": "string",
              "retail_price": 0,
              "product_type": "string",
              "quantity": 0,
              "quantity_return": 0,
              "receipt_quantity": 0,
              "planned_quantity": 0,
              "price": 0,
              "amount": 0,
              "note": "string",
              "type": "string",
              "variant_image": "string",
              "unit": "string",
              "tax": 0,
              "tax_rate": 0,
              "line_amount_after_line_discount": 0,
              "discount_rate": 0,
              "discount_value": 0,
              "discount_amount": 0,
              "position": 0,
              "untaxed_amount_refunds": 0,
              "amount_tax_refunds": 0,
              "return_reason": "string",
              "payment_return_note": "string",
              "purchase_order_id": 0
            }
          ],
          "expect_return_date": "2019-08-24T14:15:22Z",
          "store_id": 0,
          "untaxed_amount_refunds": 0,
          "amount_tax_refunds": 0,
          "total_refunds": 0,
          "return_reason": "string",
          "payment_return_note": "string"
        }
      ],
      "phone": "string",
      "supplier_note": "string",
      "expect_import_date": "2019-08-24T14:15:22Z",
      "expect_return_date": "2019-08-24T14:15:22Z",
      "expect_store_id": 0,
      "expect_store": "string",
      "payment_condition_id": 0,
      "payment_condition_name": "string",
      "payment_note": "string",
      "note": "string",
      "tags": "string",
      "policy_price_code": "string",
      "tax_included": true,
      "payments": [
        {
          "id": 0,
          "code": "string",
          "version": 0,
          "created_by": "string",
          "created_name": "string",
          "created_date": "2019-08-24T14:15:22Z",
          "updated_by": "string",
          "updated_name": "string",
          "updated_date": "2019-08-24T14:15:22Z",
          "account_code": "string",
          "amount": 0,
          "reference": "string",
          "payment_method_code": "string",
          "payment_method": "string",
          "status": "string",
          "status_name": "string",
          "note": "string",
          "is_refund": true,
          "purchase_order_id": 0,
          "transaction_date": "2019-08-24T14:15:22Z",
          "transaction_date_string": "string"
        }
      ],
      "payment_refunds": [
        {
          "id": 0,
          "code": "string",
          "version": 0,
          "created_by": "string",
          "created_name": "string",
          "created_date": "2019-08-24T14:15:22Z",
          "updated_by": "string",
          "updated_name": "string",
          "updated_date": "2019-08-24T14:15:22Z",
          "account_code": "string",
          "amount": 0,
          "reference": "string",
          "payment_method_code": "string",
          "status": "string",
          "status_name": "string",
          "note": "string",
          "purchase_order_id": 0,
          "transaction_date": "2019-08-24T14:15:22Z"
        }
      ],
      "procurements": [
        {
          "id": 0,
          "code": "string",
          "version": 0,
          "created_by": "string",
          "created_name": "string",
          "created_date": "2019-08-24T14:15:22Z",
          "updated_by": "string",
          "updated_name": "string",
          "updated_date": "2019-08-24T14:15:22Z",
          "reference": "string",
          "store_id": 0,
          "store": "string",
          "expect_receipt_date": "2019-08-24T14:15:22Z",
          "note": "string",
          "status": "string",
          "status_name": "string",
          "activated_date": "2019-08-24T14:15:22Z",
          "activated_by": "string",
          "stock_in_date": "2019-08-24T14:15:22Z",
          "stock_in_by": "string",
          "is_cancelled": true,
          "created_date_str": "string",
          "purchase_order": {
            "id": 0,
            "company_id": 0,
            "merchandiser_code": "string",
            "merchandiser": "string",
            "designer_code": "string",
            "designer": "string",
            "qc_code": "string",
            "qc": "string",
            "reference": "string",
            "type": "string",
            "code": "string",
            "supplier_id": 0,
            "supplier_code": "string",
            "supplier": "string",
            "phone": "string"
          },
          "procurement_items": [
            {
              "id": 0,
              "code": "string",
              "version": 0,
              "created_by": "string",
              "created_name": "string",
              "created_date": "2019-08-24T14:15:22Z",
              "updated_by": "string",
              "updated_name": "string",
              "updated_date": "2019-08-24T14:15:22Z",
              "line_item_id": 0,
              "sku": "string",
              "barcode": "string",
              "variant": "string",
              "variant_image": "string",
              "variant_id": 0,
              "retail_price": 0,
              "ordered_quantity": 0,
              "accepted_quantity": 0,
              "planned_quantity": 0,
              "quantity": 0,
              "real_quantity": 0,
              "note": "string",
              "price": 0,
              "vat": 0,
              "vat_rate": 0,
              "amount": 0
            }
          ]
        }
      ],
      "cost_lines": [
        {
          "id": 0,
          "code": "string",
          "version": 0,
          "created_by": "string",
          "created_name": "string",
          "created_date": "2019-08-24T14:15:22Z",
          "updated_by": "string",
          "updated_name": "string",
          "updated_date": "2019-08-24T14:15:22Z",
          "title": "string",
          "amount": 0
        }
      ],
      "total_cost_line": 0,
      "tax_lines": [
        {
          "rate": 0,
          "amount": 0
        }
      ],
      "payment_discount_rate": 0,
      "payment_discount_value": 0,
      "payment_discount_amount": 0,
      "trade_discount_rate": 0,
      "trade_discount_value": 0,
      "trade_discount_amount": 0,
      "untaxed_amount": 0,
      "untaxed_amount_refunds": 0,
      "tax": 0,
      "total": 0,
      "total_payment": 0,
      "total_paid": 0,
      "total_refunds": 0,
      "receipt_quantity": 0,
      "planned_quantity": 0,
      "status": "string",
      "status_name": "string",
      "financial_status": "string",
      "receive_status": "string",
      "cancel_reason": "string",
      "order_date": "2019-08-24T14:15:22Z",
      "order_date_string": "string",
      "cancelled_date": "2019-08-24T14:15:22Z",
      "activated_date": "2019-08-24T14:15:22Z",
      "completed_date": "2019-08-24T14:15:22Z",
      "completed_stock_date": "2019-08-24T14:15:22Z",
      "is_grid_mode": true,
      "is_grid_mode_supplement": true,
      "receive_finished_date": "2019-08-24T14:15:22Z",
      "waiting_approval_date": "2019-08-24T14:15:22Z"
    }
  ],
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[[PurchaseOrderDto](#schemapurchaseorderdto)]|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_PageableDtoPurchaseOrderLogDto">PageableDtoPurchaseOrderLogDto</h2>
<!-- backwards compatibility -->
<a id="schemapageabledtopurchaseorderlogdto"></a>
<a id="schema_PageableDtoPurchaseOrderLogDto"></a>
<a id="tocSpageabledtopurchaseorderlogdto"></a>
<a id="tocspageabledtopurchaseorderlogdto"></a>

```json
{
  "metadata": {
    "total": 0,
    "page": 0,
    "limit": 0
  },
  "items": [
    {
      "id": 0,
      "root_id": 0,
      "code": "string",
      "updated_name": "string",
      "updated_by": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "created_name": "string",
      "created_by": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "data": "string",
      "action": "string",
      "status_before": "string",
      "status_after": "string",
      "ip_address": "string",
      "device": "string",
      "procurement_code": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|metadata|[Metadata](#schemametadata)|false|none|none|
|items|[[PurchaseOrderLogDto](#schemapurchaseorderlogdto)]|false|none|none|

<h2 id="tocS_ResultPageableDtoPurchaseOrderLogDto">ResultPageableDtoPurchaseOrderLogDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultpageabledtopurchaseorderlogdto"></a>
<a id="schema_ResultPageableDtoPurchaseOrderLogDto"></a>
<a id="tocSresultpageabledtopurchaseorderlogdto"></a>
<a id="tocsresultpageabledtopurchaseorderlogdto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": {
    "metadata": {
      "total": 0,
      "page": 0,
      "limit": 0
    },
    "items": [
      {
        "id": 0,
        "root_id": 0,
        "code": "string",
        "updated_name": "string",
        "updated_by": "string",
        "updated_date": "2019-08-24T14:15:22Z",
        "created_name": "string",
        "created_by": "string",
        "created_date": "2019-08-24T14:15:22Z",
        "data": "string",
        "action": "string",
        "status_before": "string",
        "status_after": "string",
        "ip_address": "string",
        "device": "string",
        "procurement_code": "string"
      }
    ]
  },
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[PageableDtoPurchaseOrderLogDto](#schemapageabledtopurchaseorderlogdto)|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_ResultPurchaseOrderLogDto">ResultPurchaseOrderLogDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultpurchaseorderlogdto"></a>
<a id="schema_ResultPurchaseOrderLogDto"></a>
<a id="tocSresultpurchaseorderlogdto"></a>
<a id="tocsresultpurchaseorderlogdto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": {
    "id": 0,
    "root_id": 0,
    "code": "string",
    "updated_name": "string",
    "updated_by": "string",
    "updated_date": "2019-08-24T14:15:22Z",
    "created_name": "string",
    "created_by": "string",
    "created_date": "2019-08-24T14:15:22Z",
    "data": "string",
    "action": "string",
    "status_before": "string",
    "status_after": "string",
    "ip_address": "string",
    "device": "string",
    "procurement_code": "string"
  },
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[PurchaseOrderLogDto](#schemapurchaseorderlogdto)|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_ResultListPaymentConditionDto">ResultListPaymentConditionDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultlistpaymentconditiondto"></a>
<a id="schema_ResultListPaymentConditionDto"></a>
<a id="tocSresultlistpaymentconditiondto"></a>
<a id="tocsresultlistpaymentconditiondto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": [
    {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "timeout": 0,
      "note": "string",
      "default": true
    }
  ],
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[[PaymentConditionDto](#schemapaymentconditiondto)]|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

<h2 id="tocS_ResultListPurchaseOrderConfigDto">ResultListPurchaseOrderConfigDto</h2>
<!-- backwards compatibility -->
<a id="schemaresultlistpurchaseorderconfigdto"></a>
<a id="schema_ResultListPurchaseOrderConfigDto"></a>
<a id="tocSresultlistpurchaseorderconfigdto"></a>
<a id="tocsresultlistpurchaseorderconfigdto"></a>

```json
{
  "code": 0,
  "message": "string",
  "data": [
    {
      "id": 0,
      "code": "string",
      "version": 0,
      "created_by": "string",
      "created_name": "string",
      "created_date": "2019-08-24T14:15:22Z",
      "updated_by": "string",
      "updated_name": "string",
      "updated_date": "2019-08-24T14:15:22Z",
      "status": "string",
      "json_content": "string",
      "name": "string",
      "type": "string"
    }
  ],
  "response_time": "2019-08-24T14:15:22Z",
  "errors": [
    "string"
  ],
  "request_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer(int32)|false|none|none|
|message|string|false|none|none|
|data|[[PurchaseOrderConfigDto](#schemapurchaseorderconfigdto)]|false|none|none|
|response_time|string(date-time)|false|none|none|
|errors|[string]|false|none|none|
|request_id|string|false|none|none|

