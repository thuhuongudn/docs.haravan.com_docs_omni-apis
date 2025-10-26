---
url: "https://docs.haravan.com/docs/omni-apis/inventory-transfer/"
title: "Inventory Transfer | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/inventory-transfer/#)

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
- Inventory Transfer

On this page

# Inventory Transfer

`Version: 1.0`

You can track inventory transfer history in your shop. Alternatively, you can use it to transfer the available quantity of an inventory item from a location to another location.

**Authenticated access scopes**: `com.read_inventories`, `com.write_inventories`

### What you can do with Inventory Transfer [​](https://docs.haravan.com/docs/omni-apis/inventory-transfer/\#what-you-can-do-with-inventory-transfer "Direct link to heading")

The Haravan API lets you do the following with the Inventory Transfer resource.

- GET `https://apis.haravan.com/com/inventories/transfers.json`
  - **[Retrieves a list of inventory transfers](https://docs.haravan.com/docs/omni-apis/inventory-transfer/#retrieves-a-list-of-inventory-transfers)**
- GET `https://apis.haravan.com/com/inventories/transfers/count.json`
  - **[Retrieve a count of the inventory transfer](https://docs.haravan.com/docs/omni-apis/inventory-transfer/#retrieve-a-count-of-the-inventory-transfer)**
- GET `https://apis.haravan.com/com/inventorytransfer/detail/{inventory_tranfer_id}.json`
  - **[Retrieves single the inventory transfer](https://docs.haravan.com/docs/omni-apis/inventory-transfer/#retrieves-single-the-inventory-transfer)**
- POST `https://apis.haravan.com/com/inventories/transfer.json`
  - **[Create an inventory transfer](https://docs.haravan.com/docs/omni-apis/inventory-transfer/#create-an-inventory-transfer)**
- POST `https://apis.haravan.com/com/inventories/transfer/{inventory_tranfer_id}/recive.json`
  - **[Receive an inventory transfer](https://docs.haravan.com/docs/omni-apis/inventory-transfer/#receive-an-inventory-transfer)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/inventory-transfer/\#properties "Direct link to heading")

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id": 1001030743

```

A unique identifier for the inventory transfer.

`created_at` : `string`

```codeBlockLines_e6Vv
"created_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the inventory adjustment was created.

`updated_at` : `string`

```codeBlockLines_e6Vv
"updated_at":"2021-05-13T07:29:20.808Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the inventory adjustment was last updated.

`transfer_number` : `string`

```codeBlockLines_e6Vv
"transfer_number":"IT100001"

```

The number of inventory transfers.

`tran_date` : `string`

```codeBlockLines_e6Vv
"tran_date": "2021-05-13T07:29:20.079Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the inventory adjustment was changed.

`from_loc_id` : `number`

```codeBlockLines_e6Vv
"from_loc_id": 963414

```

The ID of the inventory transfer. You can get location information at the Location API.

`to_loc_id` : `number`

```codeBlockLines_e6Vv
"to_loc_id": 1007284

```

The ID of the inventory received. You can get location information at the location API.

`total` : `number`

```codeBlockLines_e6Vv
"total": 10

```

Amount quantity products of inventory transfer.

`reason` : `string`

```codeBlockLines_e6Vv
"reason": "newproduct"

```

Valid values are: newproduct , returned , productionofgoods , damaged , shrinkage , promotion.

newproduct: New product.
returned: Refund p.
productionofgoods: Produce more products.
damaged: Damanged.
shrinkage: Loss.
promotion: Promotion.
transfer: Transfer.

if the type was not transferred, the default type is "newproduct".

`user_id` : `number`

```codeBlockLines_e6Vv
"user_id": 200000493247

```

A unique identifier of the user. Can you get user information at User API.

`note` : `string`

```codeBlockLines_e6Vv
"note": "hàng hư hỏng do nhà sản xuất"

```

A note about the inventory transfer.

`tags` : `string`

```codeBlockLines_e6Vv
"tags": "Hư hỏng"

```

Tags that the shop owner has attached to the inventory transfer, formatted as a string of comma-separated values.

`line_items` : `array`

Details

```codeBlockLines_e6Vv
"line_items": [\
\
  {\
\
    "id": 1116232509,\
\
    "product_id": 1031046355,\
\
    "product_variant_id": 1068095306,\
\
    "quantity": 50000,\
\
    "cost_amount": 150000000000.00,\
\
    "sku": "IPOD123",\
\
    "barcode": "123_pink",\
\
    "product_name": "ipod pink"\
\
  }\
\
]

```

- **id**: A unique identifier for the item in this line item.

- **product\_id**: A unique identifier for this product.

- **product\_variant\_id**: A unique identifier for this product variant.

- **quantity**: The number of the item for this product variant.

- **sku**: A unique identifier for this product variant.


### Retrieves a list of inventory transfers [​](https://docs.haravan.com/docs/omni-apis/inventory-transfer/\#retrieves-a-list-of-inventory-transfers "Direct link to heading")

GET

https://apis.haravan.com/com/inventories/transfers.json

Retrieves a list of inventory transfers. You can filter resources by params.

#### Params [​](https://docs.haravan.com/docs/omni-apis/inventory-transfer/\#params "Direct link to heading")

* * *

`limit`

Limit of the result.

* * *

`page`

Page to show the result.

* * *

`since_id`

Restrict results to after the specified ID.

* * *

`from_location_id`

Filter result by the specified transfer location ID.

* * *

`to_location_id`

Filter result by the specified receive location ID.

* * *

Retrieve all of the resources of the inventory transfers by page number. By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/com/inventories/transfers.json?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "transfers": [\
        {\
            "id": 1001030743,\
            "transfer_number": "IT100001",\
            "from_loc_id": 963414,\
            "to_loc_id": 1007284,\
            "reason": "shrinkage",\
            "tran_date": "2021-06-01T09:36:22.046Z",\
            "note": "Hoàn chuyển kho số #IT100000",\
            "total": 10,\
            "created_at": "2021-06-01T09:36:22.07Z",\
            "updated_at": "2021-07-08T01:49:29.734Z",\
            "status": "Received",\
            "actived_at": "2021-06-01T09:36:22.046Z",\
            "received_at": "2021-06-01T09:33:14.835Z",\
            "created_user": 200000493247,\
            "received_user": null,\
            "tags": null,\
            "line_items": [\
                {\
                    "id": 1009626370,\
                    "product_id": 1028183686,\
                    "product_variant_id": 1061514767,\
                    "quantity": 5,\
                    "sku": "AO551",\
                    "barcode": "AO551",\
                    "variant_title": "Đen / S",\
                    "product_name": "Váy Quây dài"\
                },\
                {\
                    "id": 1009626371,\
                    "product_id": 1028183686,\
                    "product_variant_id": 1064240649,\
                    "quantity": 5,\
                    "sku": "30061644-45-KEZ",\
                    "barcode": "30061644-45-KEZ",\
                    "variant_title": "Đỏ / XL",\
                    "product_name": "Váy Quây dài"\
                }\
            ]\
        },\
        {\
            "id": 1001030739,\
            "transfer_number": "IT100000",\
            "from_loc_id": 1007284,\
            "to_loc_id": 963414,\
            "reason": "shrinkage",\
            "tran_date": "2021-06-01T09:34:03.769Z",\
            "note": "test",\
            "total": 10,\
            "created_at": "2021-06-01T09:34:03.792Z",\
            "updated_at": "2021-06-01T09:34:11.15Z",\
            "status": "Received",\
            "actived_at": "2021-06-01T09:34:03.769Z",\
            "received_at": "2021-06-01T09:33:14.835Z",\
            "created_user": 200000493247,\
            "received_user": null,\
            "tags": null,\
            "line_items": [\
                {\
                    "id": 1009626360,\
                    "product_id": 1028183686,\
                    "product_variant_id": 1061514767,\
                    "quantity": 5,\
                    "sku": "AO551",\
                    "barcode": "AO551",\
                    "variant_title": "Đen / S",\
                    "product_name": "Váy Quây dài"\
                },\
                {\
                    "id": 1009626361,\
                    "product_id": 1028183686,\
                    "product_variant_id": 1064240649,\
                    "quantity": 5,\
                    "sku": "30061644-45-KEZ",\
                    "barcode": "30061644-45-KEZ",\
                    "variant_title": "Đỏ / XL",\
                    "product_name": "Váy Quây dài"\
                }\
            ]\
        }\
    ]
}

```

Retrieve resources of the inventory adjustment by transfer location id or receive location id.

- GET `https://apis.haravan.com/com/inventories/transfers.json?from_location_id=963414`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK

{
    "transfers": [\
        {\
            "id": 1001030743,\
            "transfer_number": "IT100001",\
            "from_loc_id": 963414,\
            "to_loc_id": 1007284,\
            "reason": "shrinkage",\
            "tran_date": "2021-06-01T09:36:22.046Z",\
            "note": "Hoàn chuyển kho số #IT100000",\
            "total": 10,\
            "created_at": "2021-06-01T09:36:22.07Z",\
            "updated_at": "2021-07-08T01:49:29.734Z",\
            "status": "Received",\
            "actived_at": "2021-06-01T09:36:22.046Z",\
            "received_at": "2021-06-01T09:33:14.835Z",\
            "created_user": 200000493247,\
            "received_user": null,\
            "tags": null,\
            "line_items": [\
                {\
                    "id": 1009626370,\
                    "product_id": 1028183686,\
                    "product_variant_id": 1061514767,\
                    "quantity": 5,\
                    "sku": "AO551",\
                    "barcode": "AO551",\
                    "variant_title": "Đen / S",\
                    "product_name": "Váy Quây dài"\
                },\
                {\
                    "id": 1009626371,\
                    "product_id": 1028183686,\
                    "product_variant_id": 1064240649,\
                    "quantity": 5,\
                    "sku": "30061644-45-KEZ",\
                    "barcode": "30061644-45-KEZ",\
                    "variant_title": "Đỏ / XL",\
                    "product_name": "Váy Quây dài"\
                }\
            ]\
        }\
    ]
}

```

### Retrieve a count of the inventory transfer [​](https://docs.haravan.com/docs/omni-apis/inventory-transfer/\#retrieve-a-count-of-the-inventory-transfer "Direct link to heading")

GET

https://apis.haravan.com/com/inventories/transfers/count.json

Retrieve a count of the inventory transfer.

- GET `https://apis.haravan.com/com/inventories/transfers/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 2
}

```

### Retrieves single the inventory transfer [​](https://docs.haravan.com/docs/omni-apis/inventory-transfer/\#retrieves-single-the-inventory-transfer "Direct link to heading")

GET

https://apis.haravan.com/com/inventorytransfer/detail/{inventory\_tranfer\_id}.json

Retrieves single the inventory transfer by ID.

- GET `https://apis.haravan.com/com/inventorytransfer/detail/1001030743.json `

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "inventorytransfer": {
        "id": 1001030743,
        "transfer_number": "IT100001",
        "from_loc_id": 963414,
        "to_loc_id": 1007284,
        "reason": "shrinkage",
        "tran_date": "2021-06-01T09:36:22.046Z",
        "note": "Hoàn chuyển kho số #IT100000",
        "total": 10,
        "created_at": "2021-06-01T09:36:22.07Z",
        "updated_at": "2021-07-08T01:49:29.734Z",
        "status": "Received",
        "actived_at": "2021-06-01T09:36:22.046Z",
        "received_at": "2021-06-01T09:33:14.835Z",
        "created_user": 200000493247,
        "received_user": null,
        "user_id": null,
        "tags": null,
        "line_items": [\
            {\
                "id": 1009626370,\
                "product_id": 1028183686,\
                "product_variant_id": 1061514767,\
                "quantity": 5,\
                "sku": "AO551",\
                "barcode": "AO551",\
                "variant_title": "Đen / S",\
                "product_name": "Váy Quây dài"\
            }\
        ]
    }
}

```

### Create an inventory transfer [​](https://docs.haravan.com/docs/omni-apis/inventory-transfer/\#create-an-inventory-transfer "Direct link to heading")

POST

https://apis.haravan.com/com/inventories/transfer.json

Create an inventory transfer.

- POST `https://apis.haravan.com/com/inventories/transfer.json`

```codeBlockLines_e6Vv
{
    "transfer": {
        "from_loc_id": 479749,
        "to_loc_id": 479754,
        "note": "chuyển kho",
        "reason": "newproduct",
        "received_at": "2017-06-09T17:00:00Z",
        "user_id": 3,
        "line_items": [\
            {\
                "product_id": 10000260270,\
                "product_variant_id": 101021136,\
                "quantity": 1\
            }\
        ]
    }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "transfer": {
        "id": 1000100351,
        "transfer_number": "IT1000100306",
        "from_loc_id": 479749,
        "to_loc_id": 479754,
        "tran_date": "2016-05-24T07:34:32.164Z",
        "note": "xdadada",
        "reason": "newproduct",
        "total": 1,
        "created_at": "2016-05-24T07:34:32.213Z",
        "updated_at": "2016-05-31T03:01:08.855Z",
        "status": "Active",
        "actived_at": "2016-05-24T07:34:32.164Z",
        "received_at": "2016-05-31T03:01:08.849Z",
        "created_user": 3,
        "received_user": 3,
        "line_items": [\
            {\
                "id": 1000100732,\
                "product_id": 10000260270,\
                "product_variant_id": 101021136,\
                "quantity": 1,\
                "sku": null,\
                "barcode": "19728011003",\
                "variant_title": "Trắng",\
                "product_name": "Bao da IPad Air 2 Kakusiga Transparent"\
            }\
        ]
    }
}

```

### Receive an inventory transfer [​](https://docs.haravan.com/docs/omni-apis/inventory-transfer/\#receive-an-inventory-transfer "Direct link to heading")

POST

https://apis.haravan.com/com/inventories/transfer/{inventory\_tranfer\_id}/recive.json

Receive an inventory transfer.

- POST `https://apis.haravan.com/com/inventories/transfer/1000100351/receive.json`

```codeBlockLines_e6Vv
{
    "transfer": {
        "user_id": 3
    }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "transfer": {
        "id": 1000100351,
        "transfer_number": "IT1000100306",
        "from_loc_id": 479749,
        "to_loc_id": 479754,
        "tran_date": "2016-05-24T07:34:32.164Z",
        "note": "xdadada",
        "reason": "newproduct",
        "total": 1,
        "created_at": "2016-05-24T07:34:32.213Z",
        "updated_at": "2016-05-31T03:01:08.855Z",
        "status": "Active",
        "actived_at": "2016-05-24T07:34:32.164Z",
        "received_at": "2016-05-31T03:01:08.849Z",
        "created_user": 3,
        "received_user": 3,
        "line_items": [\
            {\
                "id": 1000100732,\
                "product_id": 10000260270,\
                "product_variant_id": 101021136,\
                "quantity": 1,\
                "sku": null,\
                "barcode": "19728011003",\
                "variant_title": "Trắng",\
                "product_name": "Bao da IPad Air 2 Kakusiga Transparent"\
            }\
        ]
    }
}

```

[Previous\\
\\
Inventory Purchase Return](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/) [Next\\
\\
Metafield](https://docs.haravan.com/docs/omni-apis/metafield/)

- [What you can do with Inventory Transfer](https://docs.haravan.com/docs/omni-apis/inventory-transfer/#what-you-can-do-with-inventory-transfer)
- [Properties](https://docs.haravan.com/docs/omni-apis/inventory-transfer/#properties)
- [Retrieves a list of inventory transfers](https://docs.haravan.com/docs/omni-apis/inventory-transfer/#retrieves-a-list-of-inventory-transfers)
- [Retrieve a count of the inventory transfer](https://docs.haravan.com/docs/omni-apis/inventory-transfer/#retrieve-a-count-of-the-inventory-transfer)
- [Retrieves single the inventory transfer](https://docs.haravan.com/docs/omni-apis/inventory-transfer/#retrieves-single-the-inventory-transfer)
- [Create an inventory transfer](https://docs.haravan.com/docs/omni-apis/inventory-transfer/#create-an-inventory-transfer)
- [Receive an inventory transfer](https://docs.haravan.com/docs/omni-apis/inventory-transfer/#receive-an-inventory-transfer)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.