---
url: "https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/"
title: "Inventory Purchase Order | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/#)

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

    - [Inventory Adjustment](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/)
    - [Inventory Location Balance](https://docs.haravan.com/docs/omni-apis/inventory-locations/)
    - [Inventory Purchase Order](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/)
    - [Inventory Purchase Receive](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/)
    - [Inventory Purchase Return](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/)
    - [Inventory Transfer](https://docs.haravan.com/docs/omni-apis/inventory-transfer/)
  - [Metafield](https://docs.haravan.com/docs/omni-apis/metafield/)
  - [Online store](https://docs.haravan.com/docs/omni-apis/articles/)

  - [Orders](https://docs.haravan.com/docs/omni-apis/orders/)

  - [Products](https://docs.haravan.com/docs/omni-apis/collects/)

  - [Shipping](https://docs.haravan.com/docs/omni-apis/shipping-rates/)

  - [Store properties](https://docs.haravan.com/docs/omni-apis/country/)

  - [Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [Home page](https://docs.haravan.com/)
- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)
- [Inventory](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/)
- Inventory Purchase Order

On this page

# Inventory Purchase Order

You can use the Purchase Orders resource to document the sale of products and services to be delivered at a late date.

**Authenticated access scopes**: `com.read_inventories`, `com.write_inventories`

### What you can do with Purchase Orders [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/\#what-you-can-do-with-purchase-orders "Direct link to heading")

The Haravan API lets you do the following with the Purchase Orders resource.

- GET `https://apis.haravan.com/com/inventories/purchase_orders.json`
  - **[Retrieves a list of purchase orders.](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/#retrieves-a-list-of-purchase-orders)**
- GET `https://apis.haravan.com/com/inventories/purchase_orders/{purchase_id}.json`
  - **[Retrieves single the purchase order.](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/#retrieves-single-the-purchase-order)**

### Purchase Orders properties [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/\#purchase-orders-properties "Direct link to heading")

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id":  1206854680

```

A unique identifier for the purchase order.

`created_at` : `string`

```codeBlockLines_e6Vv
"created_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format) when the purchase order was created.

`notes` : `string`

```codeBlockLines_e6Vv
"notes": "nhập hàng tháng 11"

```

An optional note that a shop owner can attach to the purchase order.

`status` : `string`

```codeBlockLines_e6Vv
"status": "Chưa nhận hàng"

```

"Chưa nhận hàng": has not received the product.

"Hoàn thành": has received the product.

`tran_date` : `string`

```codeBlockLines_e6Vv
"tran_date": "2021-07-27T03:29:32Z"

```

Expected date of delivery.The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format).

`completed_at` : `string`

```codeBlockLines_e6Vv
"completed_at": "2021-07-27T03:29:32Z"

```

Received date of delivery.The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format).

`closed_at` : `string`

```codeBlockLines_e6Vv
"closed_at": "2014-12-18T00:00:00-05:00"

```

Purchase order closing date.The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format).

`ref_number` : `string`

```codeBlockLines_e6Vv
"ref_number": "IN_3007"

```

Reference number of the purchase order.

`supplier` : `string`

```codeBlockLines_e6Vv
"supplier": "Khác"

```

Supplier of the purchase order.

`location` : `json`

Details

- **id**: A unique numeric identifier for the location.
- **name**: The name of the location.
- **location\_type**: The location type.
- **address1**: The first line of the address.
- **address2**: The second line of the address.
- **zip**: The zip or postal code.
- **city**: The city the location is in.
- **province**: The province the location is in.
- **country**: The country the location is in.
- **phone**: The phone number of the location.
- **created\_at**: The date and time when the location was created.
- **updated\_at**: The date and time when the location was last updated.

`line_item` : `json`

Details

- **id**: A unique numeric identifier for the line items.
- **product\_id**: The unique numeric identifier for the product.
- **product\_variant\_id**: The unique numeric identifier for the product variant.
- **product\_name**: The name of the product.
- **variant\_title**: The name of the product variant.
- **sku**: A unique identifier for the product in the shop.
- **barcode**: The barcode, UPC, or ISBN number for the product.
- **quantity**: The number of items in the line item for this product variant.
- **cost\_amount**: The cost for this product variant.
- **status**: The delivery status for this product variant.
- **receive\_id**: A unique identifier for the receipt.
- **receive\_date**: The date and time when the item was received.

### Retrieves a list of purchase orders. [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/\#retrieves-a-list-of-purchase-orders "Direct link to heading")

GET

https://apis.haravan.com/com/inventories/purchase\_orders.json

Retrieves a list of purchase orders.

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/\#parameters "Direct link to heading")

* * *

`limit`

Limit of the result.

* * *

`page`

Page to show the result.

* * *

Retrieves a list of purchase orders by page number. By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/com/inventories/purchase_orders?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "purchase_orders": [\
        {\
            "id": 1000355305,\
            "purchase_number": "PO100001",\
            "notes": "",\
            "status": "Chưa nhận hàng",\
            "tran_date": "2021-07-30T06:04:34Z",\
            "created_at": "2021-07-30T06:05:24.336Z",\
            "updated_at": "2021-07-30T06:05:24.925Z",\
            "completed_at": null,\
            "closed_at": null,\
            "ref_number": "iN_3007",\
            "supplier": null,\
            "location": {\
                "id": 1007284,\
                "name": "Dottie Phan Đăng Lưu",\
                "location_type": null,\
                "email": null,\
                "address1": "123 Phan Đăng Lưu",\
                "address2": null,\
                "zip": "70000",\
                "city": null,\
                "province": "Hồ Chí Minh",\
                "country": "Vietnam",\
                "phone": "0796060700",\
                "country_code": null,\
                "country_name": "Vietnam",\
                "province_code": "HC",\
                "district": "Quận Phú Nhuận",\
                "district_code": "HC481",\
                "ward": null,\
                "ward_code": null,\
                "created_at": "2020-11-16T02:22:43.485Z",\
                "updated_at": "2020-11-16T02:22:43.485Z",\
                "is_primary": false,\
                "is_unavailable_quantity": false,\
                "type": null\
            },\
            "line_item": {\
                "received_items": null,\
                "not_received_items": [\
                    {\
                        "id": 1002496132,\
                        "product_id": 1028183686,\
                        "product_variant_id": 1061514767,\
                        "product_name": "Váy Quây dài",\
                        "variant_title": "Đen / S",\
                        "sku": "AO551",\
                        "barcode": "AO551",\
                        "quantity": 1,\
                        "cost_amount": 0.00,\
                        "status": "Chưa nhận hàng",\
                        "receive_id": null,\
                        "receive_date": null\
                    }\
                ]\
            }\
        },\
        {\
            "id": 1000354988,\
            "purchase_number": "PO100000",\
            "notes": "",\
            "status": "Hoàn thành",\
            "tran_date": "2021-07-27T03:29:32Z",\
            "created_at": "2021-07-27T03:33:38.404Z",\
            "updated_at": "2021-07-30T05:58:31.483Z",\
            "completed_at": "2021-07-30T05:58:31Z",\
            "closed_at": null,\
            "ref_number": "IN_2707",\
            "supplier": null,\
            "location": {\
                "id": 1007284,\
                "name": "Dottie Phan Đăng Lưu",\
                "location_type": null,\
                "email": null,\
                "address1": "123 Phan Đăng Lưu",\
                "address2": null,\
                "zip": "70000",\
                "city": null,\
                "province": "Hồ Chí Minh",\
                "country": "Vietnam",\
                "phone": "0796060700",\
                "country_code": null,\
                "country_name": "Vietnam",\
                "province_code": "HC",\
                "district": "Quận Phú Nhuận",\
                "district_code": "HC481",\
                "ward": null,\
                "ward_code": null,\
                "created_at": "2020-11-16T02:22:43.485Z",\
                "updated_at": "2020-11-16T02:22:43.485Z",\
                "is_primary": false,\
                "is_unavailable_quantity": false,\
                "type": null\
            },\
            "line_item": {\
                "received_items": [\
                    {\
                        "id": 1002494198,\
                        "product_id": 1028183663,\
                        "product_variant_id": 1061514702,\
                        "product_name": "Đầm Bẹt Vai Thô Phối Bèo",\
                        "variant_title": "Default Title",\
                        "sku": "D-0003",\
                        "barcode": null,\
                        "quantity": 10,\
                        "cost_amount": 1000000.00,\
                        "status": "Hoàn thành",\
                        "receive_id": 1000345765,\
                        "receive_date": "2021-07-30T12:58:22Z"\
                    }\
                ],\
                "not_received_items": null\
            }\
        }\
    ]
}

```

### Retrieves single the purchase order. [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/\#retrieves-single-the-purchase-order "Direct link to heading")

GET

https://apis.haravan.com/com/inventories/purchase\_orders/{purchase\_id}.json

Retrieves single the purchase order.

- GET `https://apis.haravan.com/com/inventories/purchase_orders/1000355305.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "purchase_order": {
        "id": 1000355305,
        "purchase_number": "PO100001",
        "notes": "",
        "status": "Chưa nhận hàng",
        "tran_date": "2021-07-30T06:04:34Z",
        "created_at": "2021-07-30T06:05:24.336Z",
        "updated_at": "2021-07-30T06:05:24.925Z",
        "completed_at": null,
        "closed_at": null,
        "ref_number": "iN_3007",
        "supplier": null,
        "location": {
            "id": 1007284,
            "name": "Dottie Phan Đăng Lưu",
            "location_type": null,
            "email": null,
            "address1": "123 Phan Đăng Lưu",
            "address2": null,
            "zip": "70000",
            "city": null,
            "province": "Hồ Chí Minh",
            "country": "Vietnam",
            "phone": "0796060700",
            "country_code": null,
            "country_name": "Vietnam",
            "province_code": "HC",
            "district": "Quận Phú Nhuận",
            "district_code": "HC481",
            "ward": null,
            "ward_code": null,
            "created_at": "2020-11-16T02:22:43.485Z",
            "updated_at": "2020-11-16T02:22:43.485Z",
            "is_primary": false,
            "is_unavailable_quantity": false,
            "type": null
        },
        "line_item": {
            "received_items": null,
            "not_received_items": [\
                {\
                    "id": 1002496132,\
                    "product_id": 1028183686,\
                    "product_variant_id": 1061514767,\
                    "product_name": "Váy Quây dài",\
                    "variant_title": "Đen / S",\
                    "sku": "AO551",\
                    "barcode": "AO551",\
                    "quantity": 1,\
                    "cost_amount": 0.00,\
                    "status": "Chưa nhận hàng",\
                    "receive_id": null,\
                    "receive_date": null\
                }\
            ]
        }
    }
}

```

[Previous\\
\\
Inventory Location Balance](https://docs.haravan.com/docs/omni-apis/inventory-locations/) [Next\\
\\
Inventory Purchase Receive](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/)

- [What you can do with Purchase Orders](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/#what-you-can-do-with-purchase-orders)
- [Purchase Orders properties](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/#purchase-orders-properties)
- [Retrieves a list of purchase orders.](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/#retrieves-a-list-of-purchase-orders)
- [Retrieves single the purchase order.](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/#retrieves-single-the-purchase-order)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.