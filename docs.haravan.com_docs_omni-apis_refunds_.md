---
url: "https://docs.haravan.com/docs/omni-apis/refunds/"
title: "Refund | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/refunds/#)

[![Haravan Platform](https://docs.haravan.com/img/logo-haravan.svg)](https://docs.haravan.com/)[Get Started](https://docs.haravan.com/docs/get-started/overview/) [Tutorials](https://docs.haravan.com/docs/tutorials/authentication/apps-overview/) [Haravan APIs](https://docs.haravan.com/docs/omni-apis/) [Themes](https://docs.haravan.com/docs/themes/) [Partners](https://docs.haravan.com/docs/partners/)

[Sign In](https://partners.haravan.com/) [Sign Up](https://partners.haravan.com/signup)

Search...

- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)

  - [AccessScope](https://docs.haravan.com/docs/omni-apis/access-scopes/)
  - [API Rate Limits](https://docs.haravan.com/docs/omni-apis/api-call-limit/)
  - [Customers](https://docs.haravan.com/docs/omni-apis/customer/)

  - [Discounts](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/)

  - [Events](https://docs.haravan.com/docs/omni-apis/event/)
  - [Inventory](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/)

  - [Metafield](https://docs.haravan.com/docs/omni-apis/metafield/)
  - [Online store](https://docs.haravan.com/docs/omni-apis/articles/)

  - [Orders](https://docs.haravan.com/docs/omni-apis/orders/)

    - [Order](https://docs.haravan.com/docs/omni-apis/orders/)
    - [Refund](https://docs.haravan.com/docs/omni-apis/refunds/)
    - [Transaction](https://docs.haravan.com/docs/omni-apis/transactions/)
  - [Products](https://docs.haravan.com/docs/omni-apis/collects/)

  - [Shipping](https://docs.haravan.com/docs/omni-apis/shipping-rates/)

  - [Store properties](https://docs.haravan.com/docs/omni-apis/country/)

  - [Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [Home page](https://docs.haravan.com/)
- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)
- [Orders](https://docs.haravan.com/docs/omni-apis/orders/)
- Refund

On this page

# Refund

`Version: 1.0`

A refund is a record of the money returned to the customer, and/or the return of any items on an order which may or may not have been restocked.

**Authenticated access scopes**: `com.read_orders` , `com.write_orders`

### What you can do with Refund [​](https://docs.haravan.com/docs/omni-apis/refunds/\#what-you-can-do-with-refund "Direct link to heading")

The Haravan API lets you do the following with the Refund resource.

- GET `https://apis.haravan.com/com/orders/{order_id}/refunds.json`
  - **[Retrieves a list refund of order](https://docs.haravan.com/docs/omni-apis/refunds/#retrieves-a-list-refund-of-order)**
- GET `https://apis.haravan.com/com/orders/{order_id}/refunds/{refund_id}.json`
  - **[Retrieves single refund of the order](https://docs.haravan.com/docs/omni-apis/refunds/#retrieves-single-refund-of-the-order)**
- POST `https://apis.haravan.com/com/orders/{order_id}/refunds.json`
  - **[Create a refund for an existing Order](https://docs.haravan.com/docs/omni-apis/refunds/#create-a-refund-for-an-existing-order)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/refunds/\#properties "Direct link to heading")

* * *

`created_at`: `string`

```codeBlockLines_e6Vv
"created_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the refund was created.

`id`: `number`

```codeBlockLines_e6Vv
"id":1054978733

```

The unique numeric identifier for the refund. This one is used for API purposes.

`note`: `string`

```codeBlockLines_e6Vv
"note":"Item was damaged during shipping"

```

The optional note attached to a refund.

`refund_line_items`: `array`

```codeBlockLines_e6Vv
"refund_line_items": [\
\
    {\
\
        "id": 1013304806,\
\
        "line_item": {\
\
            "fulfillment_service": null,\
\
            "fulfillment_status": null,\
\
            "grams": 0.0000,\
\
            "price": 15000000.0000,\
\
            "product_id": 1035729103,\
\
            "quantity": 3,\
\
            "requires_shipping": true,\
\
            "sku": "S0710A-2",\
\
            "title": "SP0710A",\
\
            "variant_id": 1078450814,\
\
            "variant_title": null,\
\
            "vendor": "14S",\
\
            "name": "SP0710A",\
\
            "id": 0,\
\
            "barcode": null,\
\
            "properties": null\
\
        },\
\
        "line_item_id": 1308268732,\
\
        "quantity": 2\
\
    }\
\
]

```

Details about one returned/refunded item. It has the following properties:

- **id**: The unique identifier of the refund line item.
- **line\_item**: The single line item being returned. References to object properties in Order API.
- **line\_item\_id**: The id of the related line item.
- **quantity**: The quantity of the associated line item that was returned.

`user_id`: `number`

```codeBlockLines_e6Vv
"user_id":200000497867

```

The unique identifier of the user who performed the refund.

`location_id`: `number`

```codeBlockLines_e6Vv
"location_id":null

```

The unique identifier of product return location.

`transactions`: `array`

```codeBlockLines_e6Vv
"transactions": [\
\
    {\
\
        "amount": -1500000.0000,\
\
        "authorization": null,\
\
        "created_at": "2021-10-15T07:43:05.115Z",\
\
        "device_id": null,\
\
        "gateway": "Thanh toán khi giao hàng (COD)",\
\
        "id": 1094983274,\
\
        "kind": "refund",\
\
        "order_id": 1231656323,\
\
        "receipt": null,\
\
        "status": "Thành công",\
\
        "test": false,\
\
        "user_id": 200000497867,\
\
        "location_id": 963414,\
\
        "payment_details": null,\
\
        "parent_id": null,\
\
        "currency": "VND",\
\
        "haravan_transaction_id": null,\
\
        "external_transaction_id": null,\
\
        "send_email": false,\
\
        "is_cod_gateway": false\
\
    }\
\
]

```

The list of transactions involved in the refund. References to object properties in [Transaction API](https://docs.haravan.com/docs/omni-apis/transactions/).

### Retrieves a list refund of order [​](https://docs.haravan.com/docs/omni-apis/refunds/\#retrieves-a-list-refund-of-order "Direct link to heading")

GET

https://apis.haravan.com/com/orders/{order\_id}/refunds.json

Retrieves a list all refund of order. You can filter resources by params.

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/refunds/\#parameters "Direct link to heading")

* * *

`fields`
comma-separated list of fields to include in the response.

* * *

Retrieve all refund order.

- GET `https://apis.haravan.com/com/orders/1231656323/refunds.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "refunds": [\
        {\
            "created_at": "2021-10-15T07:36:32.377Z",\
            "id": 1011637849,\
            "note": "wrong size",\
            "refund_line_items": [\
                {\
                    "id": 1013304743,\
                    "line_item": {\
                        "fulfillment_service": null,\
                        "fulfillment_status": null,\
                        "grams": 0.0000,\
                        "price": 15000000.0000,\
                        "product_id": 1035729103,\
                        "quantity": 3,\
                        "requires_shipping": true,\
                        "sku": "S0710A-2",\
                        "title": "SP0710A",\
                        "variant_id": 1078450814,\
                        "variant_title": null,\
                        "vendor": "14S",\
                        "name": "SP0710A",\
                        "id": 0,\
                        "barcode": null,\
                        "properties": null\
                    },\
                    "line_item_id": 1308268732,\
                    "quantity": 1\
                }\
            ],\
            "restock": true,\
            "user_id": 200000497867,\
            "order_id": 1231656323,\
            "location_id": null,\
            "transactions": []\
        },\
        {\
            "created_at": "2021-10-15T07:38:26.889Z",\
            "id": 1011637904,\
            "note": "wrong size",\
            "refund_line_items": [\
                {\
                    "id": 1013304806,\
                    "line_item": {\
                        "fulfillment_service": null,\
                        "fulfillment_status": null,\
                        "grams": 0.0000,\
                        "price": 15000000.0000,\
                        "product_id": 1035729103,\
                        "quantity": 3,\
                        "requires_shipping": true,\
                        "sku": "S0710A-2",\
                        "title": "SP0710A",\
                        "variant_id": 1078450814,\
                        "variant_title": null,\
                        "vendor": "14S",\
                        "name": "SP0710A",\
                        "id": 0,\
                        "barcode": null,\
                        "properties": null\
                    },\
                    "line_item_id": 1308268732,\
                    "quantity": 2\
                }\
            ],\
            "restock": true,\
            "user_id": 200000497867,\
            "order_id": 1231656323,\
            "location_id": null,\
            "transactions": []\
        },\
        {\
            "created_at": "2021-10-15T07:43:05.12Z",\
            "id": 1011638030,\
            "note": "hoàn tiền",\
            "refund_line_items": [],\
            "restock": null,\
            "user_id": 200000497867,\
            "order_id": 1231656323,\
            "location_id": null,\
            "transactions": [\
                {\
                    "amount": -1500000.0000,\
                    "authorization": null,\
                    "created_at": "2021-10-15T07:43:05.115Z",\
                    "device_id": null,\
                    "gateway": "Thanh toán khi giao hàng (COD)",\
                    "id": 1094983274,\
                    "kind": "refund",\
                    "order_id": 1231656323,\
                    "receipt": null,\
                    "status": "Thành công",\
                    "test": false,\
                    "user_id": 200000497867,\
                    "location_id": 963414,\
                    "payment_details": null,\
                    "parent_id": null,\
                    "currency": "VND",\
                    "haravan_transaction_id": null,\
                    "external_transaction_id": null,\
                    "send_email": false,\
                    "is_cod_gateway": false\
                }\
            ]\
        }\
    ]
}

```

List all refund of order, showing only some attributesr.

- GET `https://apis.haravan.com/com/orders/1231656323/refunds.json?fields=restock,refund_line_items`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "refunds": [\
        {\
            "created_at": "2021-10-15T07:36:32.377Z",\
            "id": 1011637849,\
            "note": "wrong size",\
            "refund_line_items": [\
                {\
                    "id": 1013304743,\
                    "line_item": {\
                        "fulfillment_service": null,\
                        "fulfillment_status": null,\
                        "grams": 0.0000,\
                        "price": 15000000.0000,\
                        "product_id": 1035729103,\
                        "quantity": 3,\
                        "requires_shipping": true,\
                        "sku": "S0710A-2",\
                        "title": "SP0710A",\
                        "variant_id": 1078450814,\
                        "variant_title": null,\
                        "vendor": "14S",\
                        "name": "SP0710A",\
                        "id": 0,\
                        "barcode": null,\
                        "properties": null\
                    },\
                    "line_item_id": 1308268732,\
                    "quantity": 1\
                }\
            ],\
            "restock": true,\
            "user_id": 200000497867,\
            "order_id": 1231656323,\
            "location_id": null,\
            "transactions": []\
        },\
        {\
            "created_at": "2021-10-15T07:38:26.889Z",\
            "id": 1011637904,\
            "note": "wrong size",\
            "refund_line_items": [\
                {\
                    "id": 1013304806,\
                    "line_item": {\
                        "fulfillment_service": null,\
                        "fulfillment_status": null,\
                        "grams": 0.0000,\
                        "price": 15000000.0000,\
                        "product_id": 1035729103,\
                        "quantity": 3,\
                        "requires_shipping": true,\
                        "sku": "S0710A-2",\
                        "title": "SP0710A",\
                        "variant_id": 1078450814,\
                        "variant_title": null,\
                        "vendor": "14S",\
                        "name": "SP0710A",\
                        "id": 0,\
                        "barcode": null,\
                        "properties": null\
                    },\
                    "line_item_id": 1308268732,\
                    "quantity": 2\
                }\
            ],\
            "restock": true,\
            "user_id": 200000497867,\
            "order_id": 1231656323,\
            "location_id": null,\
            "transactions": []\
        },\
        {\
            "created_at": "2021-10-15T07:43:05.12Z",\
            "id": 1011638030,\
            "note": "hoàn tiền",\
            "refund_line_items": [],\
            "restock": null,\
            "user_id": 200000497867,\
            "order_id": 1231656323,\
            "location_id": null,\
            "transactions": [\
                {\
                    "amount": -1500000.0000,\
                    "authorization": null,\
                    "created_at": "2021-10-15T07:43:05.115Z",\
                    "device_id": null,\
                    "gateway": "Thanh toán khi giao hàng (COD)",\
                    "id": 1094983274,\
                    "kind": "refund",\
                    "order_id": 1231656323,\
                    "receipt": null,\
                    "status": "Thành công",\
                    "test": false,\
                    "user_id": 200000497867,\
                    "location_id": 963414,\
                    "payment_details": null,\
                    "parent_id": null,\
                    "currency": "VND",\
                    "haravan_transaction_id": null,\
                    "external_transaction_id": null,\
                    "send_email": false,\
                    "is_cod_gateway": false\
                }\
            ]\
        }\
    ]
}

```

### Retrieves single refund of the order [​](https://docs.haravan.com/docs/omni-apis/refunds/\#retrieves-single-refund-of-the-order "Direct link to heading")

GET

https://apis.haravan.com/com/orders/{order\_id}/refunds/{refund\_id}.json

Retrieves single refund of order by ID.

- GET `https://apis.haravan.com/com/orders/1231656323/refunds/1011637849.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "refund": {
        "created_at": "2021-10-15T07:36:32.377Z",
        "id": 1011637849,
        "note": "wrong size",
        "refund_line_items": [\
            {\
                "id": 1013304743,\
                "line_item": {\
                    "fulfillment_service": null,\
                    "fulfillment_status": null,\
                    "grams": 0.0000,\
                    "price": 15000000.0000,\
                    "product_id": 1035729103,\
                    "quantity": 3,\
                    "requires_shipping": true,\
                    "sku": "S0710A-2",\
                    "title": "SP0710A",\
                    "variant_id": 1078450814,\
                    "variant_title": null,\
                    "vendor": "14S",\
                    "name": "SP0710A",\
                    "id": 0,\
                    "barcode": null,\
                    "properties": null\
                },\
                "line_item_id": 1308268732,\
                "quantity": 1\
            }\
        ],
        "restock": true,
        "user_id": 200000497867,
        "order_id": 1231656323,
        "location_id": null,
        "transactions": []
    }
}

```

### Create a refund for an existing Order [​](https://docs.haravan.com/docs/omni-apis/refunds/\#create-a-refund-for-an-existing-order "Direct link to heading")

POST

https://apis.haravan.com/com/orders/{order\_id}/refunds.json

Create a Refund for an existing Order.

#### Request body [​](https://docs.haravan.com/docs/omni-apis/refunds/\#request-body "Direct link to heading")

* * *

`restock`

Boolean, whether or not to add the line items back to the store inventory.

* * *

`notify`

Boolean, set to `true` to send a refund notification to the customer.

* * *

`note`

An optional comment attached to a refund.

* * *

`refund_line_items`

Array of line item IDs and quantities to refund.

- **line\_item\_id**: The id of the related line item (line\_item\_id = order.line\_items\[\].id).

* * *

`transactions`

Array of transactions to process as refunds.

* * *

Create a new refund for an order.

- POST `https://apis.haravan.com/com/orders/1234121123/refunds.json`

```codeBlockLines_e6Vv
{
  "refund": {
    "restock": true,
    "notify": true,
    "note": "restock",
    "refund_line_items": [\
      {\
        "line_item_id": 1312358460,\
        "quantity": 1\
      }\
    ],
    "transactions": [\
      {\
        "amount": 100000,\
        "kind": "refund"\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created

{
    "refund": {
        "created_at": "2021-10-15T11:37:43.0230186Z",
        "id": 1011644929,
        "note": "restock",
        "refund_line_items": [\
            {\
                "id": 1013315622,\
                "line_item": {\
                    "fulfillment_service": null,\
                    "fulfillment_status": null,\
                    "grams": 10.0000,\
                    "price": 400000.0000,\
                    "product_id": 1028183686,\
                    "quantity": 1,\
                    "requires_shipping": true,\
                    "sku": "AO551",\
                    "title": "Váy Quây dài",\
                    "variant_id": 1061514767,\
                    "variant_title": null,\
                    "vendor": "Khác",\
                    "name": "Váy Quây dài",\
                    "id": 0,\
                    "barcode": null,\
                    "properties": null\
                },\
                "line_item_id": 1312358460,\
                "quantity": 1\
            }\
        ],
        "restock": true,
        "user_id": 200000497867,
        "order_id": 1234121123,
        "location_id": null,
        "transactions": [\
            {\
                "amount": -100000.0,\
                "authorization": null,\
                "created_at": "2021-10-15T11:37:43.0145178Z",\
                "device_id": null,\
                "gateway": "Thanh toán khi giao hàng (COD)",\
                "id": 1095037982,\
                "kind": "refund",\
                "order_id": 1234121123,\
                "receipt": null,\
                "status": "Thành công",\
                "test": false,\
                "user_id": 200000497867,\
                "location_id": 963414,\
                "payment_details": null,\
                "parent_id": null,\
                "currency": "VND",\
                "haravan_transaction_id": null,\
                "external_transaction_id": null,\
                "send_email": false,\
                "is_cod_gateway": false\
            }\
        ]
    }
}

```

[Previous\\
\\
Order](https://docs.haravan.com/docs/omni-apis/orders/) [Next\\
\\
Transaction](https://docs.haravan.com/docs/omni-apis/transactions/)

- [What you can do with Refund](https://docs.haravan.com/docs/omni-apis/refunds/#what-you-can-do-with-refund)
- [Properties](https://docs.haravan.com/docs/omni-apis/refunds/#properties)
- [Retrieves a list refund of order](https://docs.haravan.com/docs/omni-apis/refunds/#retrieves-a-list-refund-of-order)
- [Retrieves single refund of the order](https://docs.haravan.com/docs/omni-apis/refunds/#retrieves-single-refund-of-the-order)
- [Create a refund for an existing Order](https://docs.haravan.com/docs/omni-apis/refunds/#create-a-refund-for-an-existing-order)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.