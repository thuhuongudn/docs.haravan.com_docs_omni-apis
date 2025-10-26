---
url: "https://docs.haravan.com/docs/omni-apis/discount/promotions/"
title: "Promotion | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/discount/promotions/#)

[![Haravan Platform](https://docs.haravan.com/img/logo-haravan.svg)](https://docs.haravan.com/)[Get Started](https://docs.haravan.com/docs/get-started/overview/) [Tutorials](https://docs.haravan.com/docs/tutorials/authentication/apps-overview/) [Haravan APIs](https://docs.haravan.com/docs/omni-apis/) [Themes](https://docs.haravan.com/docs/themes/) [Partners](https://docs.haravan.com/docs/partners/)

[Sign In](https://partners.haravan.com/) [Sign Up](https://partners.haravan.com/signup)

Search...

- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)

  - [AccessScope](https://docs.haravan.com/docs/omni-apis/access-scopes/)
  - [API Rate Limits](https://docs.haravan.com/docs/omni-apis/api-call-limit/)
  - [Customers](https://docs.haravan.com/docs/omni-apis/customer/)

  - [Discounts](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/)

    - [DiscountCode](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/)
    - [Promotion](https://docs.haravan.com/docs/omni-apis/discount/promotions/)
  - [Events](https://docs.haravan.com/docs/omni-apis/event/)
  - [Inventory](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/)

  - [Metafield](https://docs.haravan.com/docs/omni-apis/metafield/)
  - [Online store](https://docs.haravan.com/docs/omni-apis/articles/)

  - [Orders](https://docs.haravan.com/docs/omni-apis/orders/)

  - [Products](https://docs.haravan.com/docs/omni-apis/collects/)

  - [Shipping](https://docs.haravan.com/docs/omni-apis/shipping-rates/)

  - [Store properties](https://docs.haravan.com/docs/omni-apis/country/)

  - [Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [Home page](https://docs.haravan.com/)
- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)
- [Discounts](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/)
- Promotion

On this page

# Promotion

`Version: 1.0`

You can use the Promotion resource to create a promotion.

**Authenticated access scopes**: `com.read_discounts`, `com.write_discounts` (Only used by [the private app](https://docs.haravan.com/docs/tutorials/authentication/private-app/))

### What you can do with Promotion [​](https://docs.haravan.com/docs/omni-apis/discount/promotions/\#what-you-can-do-with-promotion "Direct link to heading")

The Haravan API lets you do the following with the Promotion resource.

- GET `https://apis.haravan.com/com/promotions.json`
  - **[Retrieves a list of enabling promotions](https://docs.haravan.com/docs/omni-apis/discount/promotions/#retrieves-a-list-of-enabling-promotions)**
- GET `https://apis.haravan.com/com/promotions/{promotion_id}.json`
  - **[Retrieves single the promotion](https://docs.haravan.com/docs/omni-apis/discount/promotions/#retrieves-single-the-promotion)**
- POST `https://apis.haravan.com/com/promotions.json`
  - **[Create a promotion](https://docs.haravan.com/docs/omni-apis/discount/promotions/#create-a-promotion)**
- PUT `https://apis.haravan.com/com/discounts/{promotion_id}/enable.json`
  - **[Update status enable a promotion](https://docs.haravan.com/docs/omni-apis/discount/promotions/#update-status-enable-a-promotion)**
- PUT `https://apis.haravan.com/com/discounts/{promotion_id}/disable.json`
  - **[Update status disable a promotion](https://docs.haravan.com/docs/omni-apis/discount/promotions/#update-status-disable-a-promotion)**
- DELETE `https://apis.haravan.com/com/promotions/{promotion_id}.json`
  - **[Delete a promotion](https://docs.haravan.com/docs/omni-apis/discount/promotions/#delete-a-promotion)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/discount/promotions/\#properties "Direct link to heading")

* * *

`name`: `string`

```codeBlockLines_e6Vv
"name": "Happy new year"

```

Name of the promotion.

* * *

`ends_at`: `string`

```codeBlockLines_e6Vv
"ends_at": "2022-08-11T09:35:59Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the promotion was expired.

* * *

`id`: `number`

```codeBlockLines_e6Vv
"id": 1206854680

```

A unique identifier for the promotion.

* * *

`starts_at`: `string`

```codeBlockLines_e6Vv
"starts_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the promotion was applied.

* * *

`discount_type`: `string`

```codeBlockLines_e6Vv
"discount_type": "fixed_amount"

```

- **fixed\_amount**: Applies a discount of value as a unit of the store's currency.

- **percentage**: Applies a percentage discount of value.

- **same\_price**: Same price.


* * *

`value`: `number`

```codeBlockLines_e6Vv
"value ": 150000

```

Promotion value depend on "discount\_type".

If discount\_type is "percentage". The value will be percent.

* * *

`applies_to_resource`: `string`

```codeBlockLines_e6Vv
"applies_to_resource": "product"

```

- **null**: Apply to all orders.
- **product**: Apply to the product.
- **collection**: Apply to the collection.
- **product\_variant**: Apply to product variants.

* * *

`applies_to_quantity`: `number`

```codeBlockLines_e6Vv
"applies_to_quantity":2

```

Minimum quantity of items to be applied promotion.

* * *

`applies_to_id`: `number`

```codeBlockLines_e6Vv
"applies_to_id":0

```

The ID of the product to be applied promotion.

* * *

`order_over`: `number`

```codeBlockLines_e6Vv
"order_over":100000

```

Minimum purchase amount to be applied promotion.

* * *

`promotion_apply_type`: `number`

```codeBlockLines_e6Vv
"promotion_apply_type":1

```

- 1: Minimum quantity of items.

- 2: Minimum purchase amount.


* * *

`variants`: `array`

```codeBlockLines_e6Vv
"variants": [\
\
    {\
\
        "product_id": 1028183633,\
\
        "variant_id": 1061514629\
\
    },\
\
    {\
\
        "product_id": 1028183633,\
\
        "variant_id": 1061514630\
\
    }\
\
]

```

Array to product ids and variant id objects to which the promotion will be applied.

* * *

`created_at`: `string`

```codeBlockLines_e6Vv
"created_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the promotion was created.

* * *

`updated_at`: `string`

```codeBlockLines_e6Vv
"updated_at": "2021-05-13T07:29:20.808Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the promotion was last updated.

* * *

`first_name`: `string`

```codeBlockLines_e6Vv
"first_name":"John"

```

The first name of the user created the promotion.

* * *

`last_name`: `string`

```codeBlockLines_e6Vv
"last_name":"Smit"

```

The last name of the user created the promotion.

* * *

`create_user`: `number`

```codeBlockLines_e6Vv
"create_user":200000493247

```

The ID of the user-created the promotion.

* * *

`status`: `string`

```codeBlockLines_e6Vv
"status":"enabled"

```

Status of the promotion. Values are valid:

- **enabled**: The promotion is active.
- **disabled**: The promotion is disabled.

* * *

Applicable products

`products_selection` : `string`

```codeBlockLines_e6Vv
"products_selection" : "all"

```

- all : All
- collection\_prerequisite : Prerequisite collection
- variant\_prerequisite : Prerequisite variant
- product\_prerequisite : Prerequisite product

* * *

Applicable customer

`customers_selection` : `string`

```codeBlockLines_e6Vv
"customers_selection" : "all"

```

- all : All
- customersegment\_prerequisite : Prerequisite customer segment
- customer\_prerequisite : Prerequisite customer

* * *

Applicable shipping location

`provinces_selection` : `string`

```codeBlockLines_e6Vv
"provinces_selection" : "all"

```

- all: All
- province\_prerequisite: Prerequisite province

* * *

Applicable channels

`channels_selection` : `string`

```codeBlockLines_e6Vv
"channels_selection" : "all"

```

- all: All
- channel\_prerequisite: Prerequisite channel

* * *

Applicable locations

`locations_selection` : `string`

```codeBlockLines_e6Vv
"locations_selection" : "all"

```

- all: All
- location\_prerequisite Prerequisite location

* * *

Applicable collections

`entitled_collection_ids` : `array`

```codeBlockLines_e6Vv
"entitled_collection_ids" : [1004145086, 1004145085, 1004145084]

```

- entitled\_collection\_ids: Entitled collection

* * *

Applicable products

`entitled_product_ids` : `array`

```codeBlockLines_e6Vv
"entitled_product_ids" : [1055262740, 1055262741, 1055262730]

```

- entitled\_product\_ids: Entitled product ids

* * *

Applicable variants

`entitled_variant_ids` : `array`

```codeBlockLines_e6Vv
"entitled_variant_ids" : [1124400234, 1124400235, 1124400233]

```

- entitled\_variant\_ids: Entitled variant ids

* * *

Applicable customers

`entitled_customer_ids` : `array`

```codeBlockLines_e6Vv
"entitled_customer_ids" : [1128891111]

```

- entitled\_customer\_ids: Entitled customer ids

* * *

Customer eligibility

`entitled_customer_segment_ids` : `array`

```codeBlockLines_e6Vv
"entitled_customer_segment_ids" : [73624622, 73624623, 73624624]

```

- entitled\_customer\_segment\_ids: Entitled custoemr segment ids

* * *

Applicable shipping location

`entitled_province_ids` : `array`

```codeBlockLines_e6Vv
"entitled_province_ids" : [50, 32, 57]

```

- entitled\_province\_ids: Entitled province ids

* * *

Applicable channels

`entitled_channels` : `array`

```codeBlockLines_e6Vv
"entitled_channels" : ["pos", "web", "harasocial"]

```

- entitled\_channels: Entitled channels

* * *

Applicable locations

`entitled_location_ids` : `array`

```codeBlockLines_e6Vv
"entitled_location_ids" : [1690961]

```

- entitled\_location\_ids: Entitled location ids

* * *

Rule customs

`rule_customs` : `array`

```codeBlockLines_e6Vv
"rule_customs" : [\
    {\
      "name": "customer_limit_used",\
      "value": "5"\
    },\
    {\
      "name": "time_range",\
      "value": "[{\"name\":\"monday\",\"value_range\":[]},{\"name\":\"tuesday\",\"value_range\":[]},{\"name\":\"wednesday\",\"value_range\":[[\"1:00\",\"1:30\"]]},{\"name\":\"thursday\",\"value_range\":[]}]"\
    },\
    {\
      "name": "shipping_max_apply_value",\
      "value": "100"\
    }\
]

```

- customer\_limit\_used: Limit to one use per customer
- time\_range: Active dates
- shipping\_max\_apply\_value: Shipping max

* * *

Discount type

`take_type` : `string`

```codeBlockLines_e6Vv
"take_type" : "fixed_amount"

```

- fixed\_amount : Fixed amount
- percentage : Percentage

* * *

Usage limits

`usage_limit` : `number`

```codeBlockLines_e6Vv
"usage_limit" : 10

```

- usage\_limit: Limit number of times this discount can be used in total

* * *

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/discount/promotions/\#endpoints "Direct link to heading")

### Retrieves a list of enabling promotions [​](https://docs.haravan.com/docs/omni-apis/discount/promotions/\#retrieves-a-list-of-enabling-promotions "Direct link to heading")

GET

https://apis.haravan.com/com/promotions.json

### Parameters [​](https://docs.haravan.com/docs/omni-apis/discount/promotions/\#parameters "Direct link to heading")

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

`code`

Filter result by the code.

* * *

Retrieves a list of enabling discount codes by page number.

By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/com/promotions.json?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "promotions": [\
        {\
            "name": "Happy new year",\
            "ends_at": "2022-03-04T16:59:59Z",\
            "id": 1024173229,\
            "starts_at": "2022-03-04T03:54:00Z",\
            "value": 10000.0000,\
            "discount_type": "fixed_amount",\
            "applies_to_resource": "product_variant",\
            "applies_to_quantity": 0,\
            "applies_to_id": 0,\
            "set_time_active": false,\
            "order_over": 1000000,\
            "promotion_apply_type": 2,\
            "variants": [\
                {\
                    "product_id": 1028183633,\
                    "variant_id": 1061514629\
                },\
                {\
                    "product_id": 1028183633,\
                    "variant_id": 1061514630\
                }\
            ],\
            "created_at": "2022-03-04T03:56:37.215Z",\
            "updated_at": "2022-03-04T03:56:37.215Z",\
            "first_name": null,\
            "last_name": null,\
            "create_user": 200000493247,\
            "applies_customer_group_id": null,\
            "status": "enabled",\
            "products_selection": "collection_prerequisite",\
            "customers_selection": "customersegment_prerequisite",\
            "provinces_selection": "all",\
            "channels_selection": "channel_prerequisite",\
            "locations_selection": "location_prerequisite",\
            "entitled_collection_ids": [\
                1004145086,\
                1004145085,\
                1004145084\
            ],\
            "entitled_product_ids": [],\
            "entitled_variant_ids": [],\
            "entitled_customer_ids": [],\
            "entitled_customer_segment_ids": [\
                73624622,\
                73624623,\
                73624613,\
                73624621,\
                73624624\
            ],\
            "entitled_province_ids": [],\
            "entitled_channels": [\
                "pos",\
                "web",\
                "harasocial"\
            ],\
            "entitled_location_ids": [\
                1690961\
            ],\
            "rule_customs": [],\
            "take_type": "percentage",\
            "usage_limit": 10\
        },\
        {\
            "name": "Vallentine",\
            "ends_at": "2022-08-11T09:35:59Z",\
            "id": 1022775866,\
            "starts_at": "2021-08-11T08:35:00Z",\
            "value": 10.0000,\
            "discount_type": "percentage",\
            "applies_to_resource": "product",\
            "applies_to_quantity": 1,\
            "applies_to_id": 1028183633,\
            "set_time_active": false,\
            "order_over": null,\
            "promotion_apply_type": 1,\
            "variants": [],\
            "created_at": "2022-01-25T12:07:59.374Z",\
            "updated_at": "2022-01-25T12:07:59.374Z",\
            "first_name": null,\
            "last_name": null,\
            "create_user": 200000497867,\
            "applies_customer_group_id": null,\
            "status": "enabled",\
            "products_selection": "collection_prerequisite",\
            "customers_selection": "customersegment_prerequisite",\
            "provinces_selection": "all",\
            "channels_selection": "channel_prerequisite",\
            "locations_selection": "location_prerequisite",\
            "entitled_collection_ids": [\
                1004145086,\
                1004145085,\
                1004145084\
            ],\
            "entitled_product_ids": [],\
            "entitled_variant_ids": [],\
            "entitled_customer_ids": [],\
            "entitled_customer_segment_ids": [\
                73624622,\
                73624623,\
                73624613,\
                73624621,\
                73624624\
            ],\
            "entitled_province_ids": [],\
            "entitled_channels": [\
                "pos",\
                "web",\
                "harasocial"\
            ],\
            "entitled_location_ids": [\
                1690961\
            ],\
            "rule_customs": [],\
            "take_type": "percentage",\
            "usage_limit": 10\
        }\
    ]
}

```

### Retrieves single the promotion [​](https://docs.haravan.com/docs/omni-apis/discount/promotions/\#retrieves-single-the-promotion "Direct link to heading")

GET

https://apis.haravan.com/com/promotions/{promotion\_id}.json

Retrieves single the discount code.

- GET `https://apis.haravan.com/com/promotions/1024173229.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "promotion": {
        "name": "Happy new year",
        "ends_at": "2022-03-04T16:59:59Z",
        "id": 1024173229,
        "starts_at": "2022-03-04T03:54:00Z",
        "value": 10000.0000,
        "discount_type": "fixed_amount",
        "applies_to_resource": "product_variant",
        "applies_to_quantity": 0,
        "applies_to_id": 0,
        "set_time_active": false,
        "order_over": 1000000,
        "promotion_apply_type": 2,
        "variants": [\
            {\
                "product_id": 1028183633,\
                "variant_id": 1061514629\
            },\
            {\
                "product_id": 1028183633,\
                "variant_id": 1061514630\
            }\
        ],
        "created_at": "2022-03-04T03:56:37.215Z",
        "updated_at": "2022-03-04T03:56:37.215Z",
        "first_name": null,
        "last_name": null,
        "create_user": 200000493247,
        "applies_customer_group_id": null,
        "status": "enabled",
        "products_selection": "collection_prerequisite",
        "customers_selection": "customersegment_prerequisite",
        "provinces_selection": "all",
        "channels_selection": "channel_prerequisite",
        "locations_selection": "location_prerequisite",
        "entitled_collection_ids": [\
            1004145086,\
            1004145085,\
            1004145084\
        ],
        "entitled_product_ids": [],
        "entitled_variant_ids": [],
        "entitled_customer_ids": [],
        "entitled_customer_segment_ids": [\
            73624622,\
            73624623,\
            73624613,\
            73624621,\
            73624624\
        ],
        "entitled_province_ids": [],
        "entitled_channels": [\
            "pos",\
            "web",\
            "harasocial"\
        ],
        "entitled_location_ids": [\
            1690961\
        ],
        "rule_customs": [],
        "take_type": "percentage",
        "usage_limit": 10
    }
}

```

### Create a promotion [​](https://docs.haravan.com/docs/omni-apis/discount/promotions/\#create-a-promotion "Direct link to heading")

POST

https://apis.haravan.com/com/promotions.json

Create a promotion.

- POST `https://apis.haravan.com/com/promotions.json`

```codeBlockLines_e6Vv
{
    "promotion":
        {
            "name": "Happy new year",
            "ends_at": "2022-03-04T16:59:59Z",
            "id": 1024173229,
            "starts_at": "2022-03-04T03:54:00Z",
            "value": 10000.0000,
            "discount_type": "fixed_amount",
            "applies_to_resource": "product_variant",
            "applies_to_quantity": 0,
            "applies_to_id": 0,
            "order_over": 1000000,
            "promotion_apply_type": 2,
            "variants": [\
                {\
                    "product_id": 1028183633,\
                    "variant_id": 1061514629\
                },\
                {\
                    "product_id": 1028183633,\
                    "variant_id": 1061514630\
                }\
            ]
        }
}

```

Details

```codeBlockLines_e6Vv
{
    "promotion":
        {
            "name": "Happy new year",
            "ends_at": "2022-03-04T16:59:59Z",
            "id": 1024173229,
            "starts_at": "2022-03-04T03:54:00Z",
            "value": 10000.0000,
            "discount_type": "fixed_amount",
            "applies_to_resource": "product_variant",
            "applies_to_quantity": 0,
            "applies_to_id": 0,
            "order_over": 1000000,
            "promotion_apply_type": 2,
            "variants": [\
                {\
                    "product_id": 1028183633,\
                    "variant_id": 1061514629\
                },\
                {\
                    "product_id": 1028183633,\
                    "variant_id": 1061514630\
                }\
            ],
            "created_at": "2024-06-17T05:22:22.4108288Z",
            "updated_at": "2024-06-17T05:22:22.4108459Z",
            "first_name": "--",
            "last_name": null,
            "create_user": 200002377565,
            "applies_customer_group_id": null,
            "status": "enabled",
            "products_selection": "variant_prerequisite",
            "customers_selection": "all",
            "provinces_selection": "all",
            "channels_selection": "all",
            "locations_selection": "all",
            "entitled_collection_ids": [],
            "entitled_product_ids": [],
            "entitled_variant_ids": [\
                1061514629, 1061514630\
            ],
            "entitled_customer_ids": [],
            "entitled_customer_segment_ids": [],
            "entitled_province_ids": [],
            "entitled_channels": [],
            "entitled_location_ids": [],
            "rule_customs": [],
            "take_type": "fixed_amount",
            "usage_limit": null
        }
}

```

### Update status enable a promotion [​](https://docs.haravan.com/docs/omni-apis/discount/promotions/\#update-status-enable-a-promotion "Direct link to heading")

PUT

https://apis.haravan.com/com/discounts/{promotion\_id}/enable.json

Update status enable a promotion.

- PUT `https://apis.haravan.com/com/discounts/1024177200/enable.json`

```codeBlockLines_e6Vv
{}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "discount": {
        "applies_once": false,
        "applies_to_id": null,
        "code": "Happy new year",
        "ends_at": "2022-03-04T16:59:59Z",
        "id": 1024177200,
        "minimum_order_amount": 1000000.0,
        "starts_at": "2022-03-03T17:00:00Z",
        "status": "enabled",
        "usage_limit": 0,
        "value": 10000.0000,
        "discount_type": "fixed_amount",
        "times_used": 0,
        "is_promotion": false,
        "applies_to_resource": "product_variant",
        "variants": [\
            {\
                "product_id": 1028183633,\
                "variant_id": 1061514629\
            },\
            {\
                "product_id": 1028183633,\
                "variant_id": 1061514630\
            }\
        ],
        "location_ids": null,
        "create_user": 200000497867,
        "first_name": null,
        "last_name": null,
        "applies_customer_group_id": null,
        "created_at": "2022-03-04T07:58:40.772Z",
        "updated_at": "2022-03-04T08:04:57.1469947Z",
        "promotion_apply_type": 2,
        "applies_to_quantity": 0,
        "order_over": 1000000,
        "is_new_coupon": true,
        "channel": null,
        "max_amount_apply": null,
        "is_advance_same_price_discount": false,
        "advance_same_prices": null,
        "once_per_customer": false,
        "products_selection": "variant_prerequisite",
        "customers_selection": "customer_prerequisite",
        "provinces_selection": "all",
        "channels_selection": "channel_prerequisite",
        "locations_selection": "location_prerequisite",
        "entitled_collection_ids": [],
        "entitled_product_ids": [],
        "entitled_variant_ids": [\
            1124400234,\
            1124400233\
        ],
        "entitled_customer_ids": [\
            1128891111\
        ],
        "entitled_customer_segment_ids": [],
        "entitled_province_ids": [],
        "entitled_channels": [\
            "pos",\
            "web",\
            "harasocial"\
        ],
        "entitled_location_ids": [\
            1690961\
        ],
        "rule_customs": [\
            {\
                "name": "time_range",\
                "value": "[{\"name\":\"monday\",\"value_range\":[]},{\"name\":\"tuesday\",\"value_range\":[]},{\"name\":\"wednesday\",\"value_range\":[]},{\"name\":\"thursday\",\"value_range\":[]}]"\
            }\
        ],
        "take_type": "fixed_amount"
    }
}

```

### Update status disable a promotion [​](https://docs.haravan.com/docs/omni-apis/discount/promotions/\#update-status-disable-a-promotion "Direct link to heading")

PUT

https://apis.haravan.com/com/discounts/{promotion\_id}/disable.json

Update status disable a promotion.

- PUT `https://apis.haravan.com/com/discounts/1017981791/disable.json`

```codeBlockLines_e6Vv
{}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "discount": {
        "applies_once": false,
        "applies_to_id": null,
        "code": "Happy new year",
        "ends_at": "2022-03-04T16:59:59Z",
        "id": 1024177200,
        "minimum_order_amount": 1000000.0,
        "starts_at": "2022-03-03T17:00:00Z",
        "status": "disabled",
        "usage_limit": 0,
        "value": 10000.0000,
        "discount_type": "fixed_amount",
        "times_used": 0,
        "is_promotion": false,
        "applies_to_resource": "product_variant",
        "variants": [\
            {\
                "product_id": 1028183633,\
                "variant_id": 1061514629\
            },\
            {\
                "product_id": 1028183633,\
                "variant_id": 1061514630\
            }\
        ],
        "location_ids": null,
        "create_user": 200000497867,
        "first_name": null,
        "last_name": null,
        "applies_customer_group_id": null,
        "created_at": "2022-03-04T07:58:40.772Z",
        "updated_at": "2022-03-04T08:06:28.493101Z",
        "promotion_apply_type": 2,
        "applies_to_quantity": 0,
        "order_over": 1000000,
        "is_new_coupon": true,
        "channel": null,
        "max_amount_apply": null,
        "is_advance_same_price_discount": false,
        "advance_same_prices": null,
        "once_per_customer": false,
        "products_selection": "variant_prerequisite",
        "customers_selection": "customer_prerequisite",
        "provinces_selection": "all",
        "channels_selection": "channel_prerequisite",
        "locations_selection": "location_prerequisite",
        "entitled_collection_ids": [],
        "entitled_product_ids": [],
        "entitled_variant_ids": [\
            1124400234,\
            1124400233\
        ],
        "entitled_customer_ids": [\
            1128891111\
        ],
        "entitled_customer_segment_ids": [],
        "entitled_province_ids": [],
        "entitled_channels": [\
            "pos",\
            "web",\
            "harasocial"\
        ],
        "entitled_location_ids": [\
            1690961\
        ],
        "rule_customs": [\
            {\
                "name": "time_range",\
                "value": "[{\"name\":\"monday\",\"value_range\":[]},{\"name\":\"tuesday\",\"value_range\":[]},{\"name\":\"wednesday\",\"value_range\":[]},{\"name\":\"thursday\",\"value_range\":[]}]"\
            }\
        ],
        "take_type": "fixed_amount"
    }
}

```

### Delete a promotion [​](https://docs.haravan.com/docs/omni-apis/discount/promotions/\#delete-a-promotion "Direct link to heading")

DELETE

https://apis.haravan.com/com/promotions/{promotion\_id}.json

Delete a promotion.

- DELETE `https://apis.haravan.com/com/promotions/1024177200.json`

```codeBlockLines_e6Vv
{}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{}

```

[Previous\\
\\
DiscountCode](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/) [Next\\
\\
Events](https://docs.haravan.com/docs/omni-apis/event/)

- [What you can do with Promotion](https://docs.haravan.com/docs/omni-apis/discount/promotions/#what-you-can-do-with-promotion)
- [Properties](https://docs.haravan.com/docs/omni-apis/discount/promotions/#properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/discount/promotions/#endpoints)
- [Retrieves a list of enabling promotions](https://docs.haravan.com/docs/omni-apis/discount/promotions/#retrieves-a-list-of-enabling-promotions)
- [Parameters](https://docs.haravan.com/docs/omni-apis/discount/promotions/#parameters)
- [Retrieves single the promotion](https://docs.haravan.com/docs/omni-apis/discount/promotions/#retrieves-single-the-promotion)
- [Create a promotion](https://docs.haravan.com/docs/omni-apis/discount/promotions/#create-a-promotion)
- [Update status enable a promotion](https://docs.haravan.com/docs/omni-apis/discount/promotions/#update-status-enable-a-promotion)
- [Update status disable a promotion](https://docs.haravan.com/docs/omni-apis/discount/promotions/#update-status-disable-a-promotion)
- [Delete a promotion](https://docs.haravan.com/docs/omni-apis/discount/promotions/#delete-a-promotion)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.