---
url: "https://docs.haravan.com/docs/omni-apis/inventory-adjustment/"
title: "Inventory Adjustment | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/#)

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
- Inventory

On this page

# Inventory Adjustment

`Version: 1.0`

You can track inventory adjustment history in your shop. Alternatively, you can use it to change the available quantity of an inventory item at a single location.

**Authenticated access scopes**: `com.read_inventories`, `com.write_inventories`

### What you can do with Inventory Adjustment [​](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/\#what-you-can-do-with-inventory-adjustment "Direct link to heading")

The Haravan API lets you do the following with the Inventory Adjustment resource.

- GET `https://apis.haravan.com/com/inventories/adjustments.json`
  - **[Retrieves a list of inventory adjustments.](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/#retrieves-a-list-of-inventory-adjustments)**
- GET `https://apis.haravan.com/com/inventories/adjustments/count.json`
  - **[Retrieve a count of the inventory adjustments.](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/#retrieve-a-count-of-the-inventory-adjustments)**
- GET `https://apis.haravan.com/com/inventories/adjustments/{inventory_adjustment_id}.json`
  - **[Retrieves single the inventory adjustments.](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/#retrieves-single-the-inventory-adjustments)**
- POST `https://apis.haravan.com/com/inventories/adjustorset.json`
  - **[Create an inventory adjustment.](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/#create-an-inventory-adjustment)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/\#properties "Direct link to heading")

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id": 1206854680

```

A unique identifier for the inventory adjustment.

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

`adjust_number` : `string`

```codeBlockLines_e6Vv
"adjust_number":"IA100017"

```

The number of inventory adjustments.

`tran_date` : `string`

```codeBlockLines_e6Vv
"tran_date": "2021-05-13T07:29:20.079Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the inventory adjustment was changed.

`location_id` : `number`

```codeBlockLines_e6Vv
"location_id": 963414

```

The ID of the inventory. You can get location information at the Location API.

`type` : `string`

```codeBlockLines_e6Vv
"type": "adjust"

```

Valid values are: adjust, set.

adjust: add the new quantity with the old quantity.

set: override the new quantity with the old quantity.

if the type was not transferred, the default type is "adjust".

`reason` : `array`

```codeBlockLines_e6Vv
"reason": "newproduct"

```

Valid values are: newproduct , returned , productionofgoods , damaged , shrinkage , promotion .

newproduct: New product.
returned: Refund product.
productionofgoods: Produce more products.
damaged: Damanged.
shrinkage: Loss.
promotion: Promotion.
transfer: Transfer.

if the type was not transferred, the default type is "newproduct".

`total_quantity` : `number`

```codeBlockLines_e6Vv
"total_quantity": 50000

```

The quantity products of this inventory adjustment.

`note` : `string`

```codeBlockLines_e6Vv
"note": "hàng hư hỏng do nhà sản xuất"

```

A note about the inventory adjustment.

`total_cost` : `number`

```codeBlockLines_e6Vv
"total_cost": 150000000000.00

```

Total amount cost product of the inventory adjustment.

`tags` : `string`

```codeBlockLines_e6Vv
"tags": "Hư hỏng"

```

Tags that the shop owner has attached to the inventory adjustment, formatted as a string of comma-separated values.

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
    "barcode": "123_pink"\
\
  }\
]

```

Best supports 200 items for a request.

- **id**: A unique identifier for the item in this line item.

- **product\_id**: A unique identifier for this product.

- **product\_variant\_id**: A unique identifier for this product variant.

- **quantity**: The number of the item for this product variant.

- **sku**: A unique identifier for this product variant.

- **barcode**: The barcode, UPC, or ISBN number for this product.


### Retrieves a list of inventory adjustments. [​](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/\#retrieves-a-list-of-inventory-adjustments "Direct link to heading")

GET

https://apis.haravan.com/com/inventories/adjustments.json

Retrieves a list of inventory adjustments. You can filter resources by params.

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/\#parameters "Direct link to heading")

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

`location_id`

Filter result by the specified location ID.

* * *

Retrieve all of the resources of the inventory adjustment by page number. By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/com/inventories/adjustments.json?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "adjustments": [\
        {\
            "id": 1206854680,\
            "created_at": "2021-05-13T07:29:20.1Z",\
            "updated_at": "2021-05-13T07:29:20.808Z",\
            "adjust_number": "IA100017",\
            "tran_date": "2021-05-13T07:29:20.079Z",\
            "location_id": 1007284,\
            "type": null,\
            "total_quantity": 1,\
            "reason": "damaged",\
            "note": null,\
            "total_cost": 1000000.00,\
            "tags": null,\
            "line_items": [\
                {\
                    "id": 1124119453,\
                    "product_id": 1032963075,\
                    "product_variant_id": 1072106808,\
                    "quantity": -11,\
                    "cost_amount": -11000000.00,\
                    "sku": null,\
                    "barcode": null\
                }\
            ]\
        },\
        {\
            "id": 1186433005,\
            "created_at": "2021-03-03T14:52:13.548Z",\
            "updated_at": "2021-03-03T14:52:13.6Z",\
            "adjust_number": "IA100016",\
            "tran_date": "2021-03-03T14:52:13.519Z",\
            "location_id": 963414,\
            "type": null,\
            "total_quantity": 50000,\
            "reason": "productionofgoods",\
            "note": null,\
            "total_cost": 150000000000.00,\
            "tags": null,\
            "line_items": [\
                {\
                    "id": 1116232509,\
                    "product_id": 1031046355,\
                    "product_variant_id": 1068095306,\
                    "quantity": 50000,\
                    "cost_amount": 150000000000.00,\
                    "sku": null,\
                    "barcode": null\
                }\
            ]\
        }\
    ]
}

```

Retrieve resources of the inventory adjustment by location id.

- GET `https://apis.haravan.com/com/inventories/adjustments.json?location_id=963414`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK

{
    "adjustments": [\
        {\
            "id": 1206854680,\
            "created_at": "2021-05-13T07:29:20.1Z",\
            "updated_at": "2021-05-13T07:29:20.808Z",\
            "adjust_number": "IA100017",\
            "tran_date": "2021-05-13T07:29:20.079Z",\
            "location_id": 963414,\
            "type": null,\
            "total_quantity": 1,\
            "reason": "damaged",\
            "note": null,\
            "total_cost": 1000000.00,\
            "tags": null,\
            "line_items": [\
                {\
                    "id": 1124119453,\
                    "product_id": 1032963075,\
                    "product_variant_id": 1072106808,\
                    "quantity": -11,\
                    "cost_amount": -11000000.00,\
                    "sku": null,\
                    "barcode": null\
                }\
            ]\
        },\
        {\
            "id": 1186433005,\
            "created_at": "2021-03-03T14:52:13.548Z",\
            "updated_at": "2021-03-03T14:52:13.6Z",\
            "adjust_number": "IA100016",\
            "tran_date": "2021-03-03T14:52:13.519Z",\
            "location_id": 963414,\
            "type": null,\
            "total_quantity": 50000,\
            "reason": "productionofgoods",\
            "note": null,\
            "total_cost": 150000000000.00,\
            "tags": null,\
            "line_items": [\
                {\
                    "id": 1116232509,\
                    "product_id": 1031046355,\
                    "product_variant_id": 1068095306,\
                    "quantity": 50000,\
                    "cost_amount": 150000000000.00,\
                    "sku": null,\
                    "barcode": null\
                }\
            ]\
        }\
    ]
}

```

### Retrieve a count of the inventory adjustments. [​](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/\#retrieve-a-count-of-the-inventory-adjustments "Direct link to heading")

GET

https://apis.haravan.com/com/inventories/adjustments/count.json

Retrieve the count of resources of the inventory adjustment.

- GET `https://apis.haravan.com/com/inventories/adjustments/count.json`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK

{
    "count": 2
}

```

### Retrieves single the inventory adjustments. [​](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/\#retrieves-single-the-inventory-adjustments "Direct link to heading")

GET

https://apis.haravan.com/com/inventories/adjustments/{adjustment\_id}.json

Retrieves single the inventory adjustment.

- GET `https://apis.haravan.com/com/inventories/adjustments/1186432974.json`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK

{
    "adjustment": {
        "id": 1186432974,
        "created_at": "2021-03-03T14:50:47.016Z",
        "updated_at": "2021-03-03T14:50:47.989Z",
        "adjust_number": "IA100015",
        "tran_date": "2021-03-03T14:50:47.001Z",
        "location_id": 963414,
        "type": null,
        "total_quantity": 1,
        "reason": "productionofgoods",
        "note": null,
        "total_cost": 3000000.00,
        "tags": null,
        "line_items": [\
            {\
                "id": 1116232425,\
                "product_id": 1031046355,\
                "product_variant_id": 1068095306,\
                "quantity": 1,\
                "cost_amount": 3000000.00,\
                "sku": null,\
                "barcode": null\
            }\
        ]
    }
}

```

### Create an inventory adjustment. [​](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/\#create-an-inventory-adjustment "Direct link to heading")

POST

https://apis.haravan.com/com/inventories/adjustorset.json

Create an inventory adjustment.

- POST `https://apis.haravan.com/com/inventories/adjustorset.json`

```codeBlockLines_e6Vv

{
    "inventory": {
        "location_id": 963414,
        "type": "set",
        "reason": "newproduct",
        "note": "update from api",
        "line_items": [\
            {\
                "product_id": 1031046355,\
                "product_variant_id": 1068095306,\
                "quantity": 4\
            },\
            {\
                "product_id": 1031046356,\
                "product_variant_id": 1068095307,\
                "quantity": 9\
            }\
        ]
    }
}

```

The API best supports arrays of 100 items per request.

[Previous\\
\\
Events](https://docs.haravan.com/docs/omni-apis/event/) [Next\\
\\
Inventory Adjustment](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/)

- [What you can do with Inventory Adjustment](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/#what-you-can-do-with-inventory-adjustment)
- [Properties](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/#properties)
- [Retrieves a list of inventory adjustments.](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/#retrieves-a-list-of-inventory-adjustments)
- [Retrieve a count of the inventory adjustments.](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/#retrieve-a-count-of-the-inventory-adjustments)
- [Retrieves single the inventory adjustments.](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/#retrieves-single-the-inventory-adjustments)
- [Create an inventory adjustment.](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/#create-an-inventory-adjustment)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.