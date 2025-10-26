---
url: "https://docs.haravan.com/docs/omni-apis/discount/discount-codes/"
title: "DiscountCode | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#)

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
- Discounts

On this page

# DiscountCode

`Version: 2.0`

You can use the Discount Code resource to create discount codes that enable specific discounts to be redeemed. Merchants can distribute discount codes to their customers using a variety of means, such as an email or URL, and customers can apply these codes at checkout.

**Authenticated access scopes**: `com.read_discounts`, `com.write_discounts` (Only used by [the private app](https://docs.haravan.com/docs/tutorials/authentication/private-app/))

### What you can do with Discount Code [​](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/\#what-you-can-do-with-discount-code "Direct link to heading")

The Haravan API lets you do the following with the Discount Code resource.

- GET `https://apis.haravan.com/com/discounts.json`
  - **[Retrieves a list of enabling discount codes](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#retrieves-a-list-of-enabling-discount-codes)**
- GET `https://apis.haravan.com/com/discounts/{discountId}.json`
  - **[Retrieves single the discount code](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#retrieves-single-the-discount-code)**
- POST `https://apis.haravan.com/com/discounts.json`
  - **[Create a discount code](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#create-a-discount-code)**
- PUT `https://apis.haravan.com/com/discounts/{discountId}/enable.json`
  - **[Update status enables a discount code](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#update-status-enables-a-discount-code)**
- PUT `https://apis.haravan.com/com/discounts/{discountId}/disable.json`
  - **[Update status disables a discount code](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#update-status-disables-a-discount-code)**
- DELETE `https://apis.haravan.com/com/discounts/{discountId}.json`
  - **[Delete a discount code](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#delete-a-discount-code)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/\#properties "Direct link to heading")

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id": 1206854680

```

A unique identifier for the discount code.

* * *

`created_at` : `string`

```codeBlockLines_e6Vv
"created_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the discount code was created.

* * *

`updated_at` : `string`

```codeBlockLines_e6Vv
"updated_at": "2021-05-13T07:29:20.808Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the discount code was last updated.

* * *

`applies_once` : `boolean`

```codeBlockLines_e6Vv
"applies_once": false

```

- **true :** Discount can only be applied once on the entire order.

- **false :** Promotion will apply to each item in the shopping cart.


* * *

`code` : `string`

```codeBlockLines_e6Vv
"code": "XPJR0FYULPGB"

```

The case-insensitive discount code that customers use at checkout. (maximum: 200 characters)

* * *

`ends_at` : `string`

```codeBlockLines_e6Vv
"ends_at": "2021-05-13T07:29:20.1Z"

```

Expiration date.The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format).

- ends\_at = null : Never expires.

- ends\_at != null: Must be greater than current date.


* * *

`starts_at` : `string`

```codeBlockLines_e6Vv
"starts_at":"2021-05-13T07:29:20.1Z"

```

Promotion start date. The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) must be greater than the current date.

* * *

`minimum_order_amount` : `number`

```codeBlockLines_e6Vv
"minimum_order_amount" : 0

```

Minimum purchase value (Applies to all products).

* * *

`usage_limit` : `number`

```codeBlockLines_e6Vv
"usage_limit": 1

```

Limit the total number of times the promotion can be used.

* * *

`discount_type` : `string`

```codeBlockLines_e6Vv
"discount_type": "fixed_amount"

```

- **fixed\_amount**: Applies a discount of value as a unit of the store's currency.

- **percentage**: Applies a percentage discount of value.

- **shipping**: Free shipping.


* * *

`applies_to_resource` : `string`

```codeBlockLines_e6Vv
"applies_to_resource":"product"

```

- **null**: Apply to all orders.

- **product**: Apply to the product.

- **province**: Apply to province.

- **collection**: Apply to the collection.

- **customer**: Apply to customer.

- **group\_customer**: Apply to customer groups.

- **product\_variant**: Apply to product variants.


* * *

`value` : `number`

```codeBlockLines_e6Vv
"value ": 150000

```

Discount value. If discount\_type is "shipping". The value will be the shipping fee. It must be limited to how much shipping charges apply.

* * *

`is_promotion` : `boolean`

```codeBlockLines_e6Vv
"is_promotion":false

```

Apply in conjunction with other promotions.

* * *

`times_used` : `number`

```codeBlockLines_e6Vv
"times_used":1

```

Number of times used.

* * *

`once_per_customer` : `false`

```codeBlockLines_e6Vv
"once_per_customer" : false

```

- true
- false

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

### Retrieves a list of enabling discount codes [​](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/\#retrieves-a-list-of-enabling-discount-codes "Direct link to heading")

GET

https://apis.haravan.com/com/discounts.json

Retrieves a list of enabling discount codes.

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/\#parameters "Direct link to heading")

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

Retrieves a list of enabling discount codes by page number. By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/com/discounts.json?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "discounts": [\
        {\
            "applies_once": false,\
            "applies_to_id": 39550382,\
            "code": "TEST GROUP",\
            "ends_at": null,\
            "id": 1017981560,\
            "minimum_order_amount": 0.0,\
            "starts_at": "2021-07-28T10:12:00Z",\
            "status": "enabled",\
            "usage_limit": 1,\
            "value": 10.0000,\
            "discount_type": "percentage",\
            "times_used": 0,\
            "is_promotion": true,\
            "applies_to_resource": "group_customer",\
            "variants": [],\
            "location_ids": [],\
            "create_user": 200000493247,\
            "first_name": "Trọng",\
            "last_name": "Nhân Lê",\
            "applies_customer_group_id": null,\
            "created_at": "2021-07-28T10:13:35.639Z",\
            "updated_at": "2021-07-28T10:13:35.643Z",\
            "promotion_apply_type": 0,\
            "applies_to_quantity": 0,\
            "order_over": null,\
            "is_new_coupon": false,\
            "channel": null,\
            "max_amount_apply": null,\
            "is_advance_same_price_discount": false,\
            "advance_same_prices": [],\
            "once_per_customer": false,\
            "products_selection": "product_prerequisite",\
            "customers_selection": "all",\
            "provinces_selection": "all",\
            "channels_selection": "all",\
            "locations_selection": "all",\
            "entitled_collection_ids": [],\
            "entitled_product_ids": [\
                1055262740,\
                1055262730,\
                1055262741\
            ],\
            "entitled_variant_ids": [],\
            "entitled_customer_ids": [],\
            "entitled_customer_segment_ids": [],\
            "entitled_province_ids": [],\
            "entitled_channels": [],\
            "entitled_location_ids": [],\
            "rule_customs": [\
                {\
                    "name": "time_range",\
                    "value": "[{\"name\":\"monday\",\"value_range\":[]},{\"name\":\"tuesday\",\"value_range\":[]}]"\
                }\
            ],\
            "take_type": "fixed_amount"\
        },\
        {\
            "applies_once": false,\
            "applies_to_id": null,\
            "code": "EQWEQWEQWEQWEQWEWEWEQEQWEQWEQWEQWEQWEQWEQWE",\
            "ends_at": null,\
            "id": 1017969576,\
            "minimum_order_amount": 0.0,\
            "starts_at": "2021-07-27T05:49:00Z",\
            "status": "enabled",\
            "usage_limit": 1,\
            "value": 10.0000,\
            "discount_type": "fixed_amount",\
            "times_used": 0,\
            "is_promotion": true,\
            "applies_to_resource": null,\
            "variants": [],\
            "location_ids": [],\
            "create_user": 200000493247,\
            "first_name": "Trọng",\
            "last_name": "Nhân Lê",\
            "applies_customer_group_id": null,\
            "created_at": "2021-07-27T05:49:28.333Z",\
            "updated_at": "2021-07-27T05:49:28.333Z",\
            "promotion_apply_type": 0,\
            "applies_to_quantity": 0,\
            "order_over": null,\
            "is_new_coupon": false,\
            "channel": null,\
            "max_amount_apply": null,\
            "is_advance_same_price_discount": false,\
            "advance_same_prices": [],\
            "once_per_customer": false,\
            "products_selection": "product_prerequisite",\
            "customers_selection": "all",\
            "provinces_selection": "province_prerequisite",\
            "channels_selection": "channel_prerequisite",\
            "locations_selection": "location_prerequisite",\
            "entitled_collection_ids": [],\
            "entitled_product_ids": [\
                1055262718,\
                1055262665,\
                1055262732\
            ],\
            "entitled_variant_ids": [],\
            "entitled_customer_ids": [],\
            "entitled_customer_segment_ids": [\
                73624621,\
                73624622,\
                73624623,\
                73624624\
            ],\
            "entitled_province_ids": [\
                1,\
                57\
            ],\
            "entitled_channels": [\
                "harasocial"\
            ],\
            "entitled_location_ids": [\
                1690961\
            ],\
            "rule_customs": [\
                {\
                    "name": "customer_limit_used",\
                    "value": "10"\
                }\
            ],\
            "take_type": "fixed_amount"\
        }\
    ]
}

```

Retrieves a list of enable discount codes by code.

- GET `https://apis.haravan.com/com/discounts.json?code=GARMIN55`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "discounts": [\
        {\
            "applies_once": false,\
            "applies_to_id": null,\
            "code": "GARMIN55",\
            "ends_at": null,\
            "id": 1016875801,\
            "minimum_order_amount": 0.0,\
            "starts_at": "2021-06-22T04:16:00Z",\
            "status": "enabled",\
            "usage_limit": null,\
            "value": 5.0000,\
            "discount_type": "percentage",\
            "times_used": 1,\
            "is_promotion": true,\
            "applies_to_resource": null,\
            "variants": [],\
            "location_ids": [],\
            "create_user": 200000493247,\
            "first_name": "Trọng",\
            "last_name": "Nhân Lê",\
            "applies_customer_group_id": 39550382,\
            "created_at": "2021-06-22T04:17:56.847Z",\
            "updated_at": "2021-06-22T04:17:56.847Z",\
            "promotion_apply_type": 0,\
            "applies_to_quantity": 0,\
            "order_over": null,\
            "is_new_coupon": false,\
            "channel": null,\
            "max_amount_apply": null,\
            "is_advance_same_price_discount": false,\
            "advance_same_prices": [],\
            "once_per_customer": false,\
            "products_selection": "all",\
            "customers_selection": "all",\
            "provinces_selection": "province_prerequisite",\
            "channels_selection": "channel_prerequisite",\
            "locations_selection": "location_prerequisite",\
            "entitled_collection_ids": [],\
            "entitled_product_ids": [],\
            "entitled_variant_ids": [],\
            "entitled_customer_ids": [],\
            "entitled_customer_segment_ids": [\
                73624622,\
                73624623,\
                73624624\
            ],\
            "entitled_province_ids": [\
                50,\
                32,\
                57\
            ],\
            "entitled_channels": [\
                "pos",\
                "web",\
                "harasocial"\
            ],\
            "entitled_location_ids": [\
                1690961\
            ],\
            "rule_customs": [\
                {\
                    "name": "customer_limit_used",\
                    "value": "5"\
                },\
                {\
                    "name": "time_range",\
                    "value": "[{\"name\":\"monday\",\"value_range\":[]},{\"name\":\"tuesday\",\"value_range\":[]},{\"name\":\"wednesday\",\"value_range\":[[\"1:00\",\"1:30\"]]},{\"name\":\"thursday\",\"value_range\":[]}]"\
                }\
            ],\
            "take_type": "fixed_amount"\
        }\
    ]
}

```

### Retrieves single the discount code [​](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/\#retrieves-single-the-discount-code "Direct link to heading")

GET

https://apis.haravan.com/com/discounts/{discountId}.json

Retrieves single the discount code.

- GET `https://apis.haravan.com/com/discounts/1016875801.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{

    "discount": {
        "applies_once": false,
        "applies_to_id": null,
        "code": "GARMIN55",
        "ends_at": null,
        "id": 1016875801,
        "minimum_order_amount": 0.0,
        "starts_at": "2021-06-22T04:16:00Z",
        "status": "enabled",
        "usage_limit": 0,
        "value": 5.0000,
        "discount_type": "percentage",
        "times_used": 1,
        "is_promotion": true,
        "applies_to_resource": null,
        "variants": null,
        "location_ids": null,
        "create_user": 200000493247,
        "first_name": "Trọng",
        "last_name": "Nhân Lê",
        "applies_customer_group_id": 39550382,
        "created_at": "2021-06-22T04:17:56.847Z",
        "updated_at": "2021-06-22T04:17:56.847Z",
        "promotion_apply_type": 0,
        "applies_to_quantity": 0,
        "order_over": null,
        "is_new_coupon": false,
        "channel": null,
        "max_amount_apply": null,
        "is_advance_same_price_discount": false,
        "advance_same_prices": null,
        "once_per_customer": false,
        "products_selection": "all",
        "customers_selection": "all",
        "provinces_selection": "all",
        "channels_selection": "all",
        "locations_selection": "all",
        "entitled_collection_ids": [],
        "entitled_product_ids": [],
        "entitled_variant_ids": [],
        "entitled_customer_ids": [],
        "entitled_customer_segment_ids": [],
        "entitled_province_ids": [],
        "entitled_channels": [],
        "entitled_location_ids": [],
        "rule_customs": [\
            {\
                "name": "time_range",\
                "value": "[{\"name\":\"monday\",\"value_range\":[]},{\"name\":\"tuesday\",\"value_range\":[]},{\"name\":\"wednesday\",\"value_range\":[]}]"\
            }\
        ],
        "take_type": "fixed_amount"
    }
}

```

### Create a discount code [​](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/\#create-a-discount-code "Direct link to heading")

POST

https://apis.haravan.com/com/discounts.json

Create a discount code.

- POST `https://apis.haravan.com/com/discounts.json`

```codeBlockLines_e6Vv
{
  "discount": {
    "is_promotion": true,
    "applies_to_resource": null,
    "applies_to_id": null,
    "applies_once": false,
    "code": "SUMMER_28/07",
    "ends_at": null,
    "minimum_order_amount": 0,
    "starts_at": "2021-07-28T10:53:00Z",
    "usage_limit": 10,
    "value": 100000,
    "discount_type": "fixed_amount",
    "variants": [\
      {\
        "product_id": 1028183633,\
        "variant_id": 1061514625\
      },\
      {\
        "product_id": 1028183633,\
        "variant_id": 1061514629\
      }\
    ],
    "set_time_active": true,
    "applies_customer_group_id": "39550400",
    "location_ids": [1007284]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "discount": {
        "applies_once": false,
        "applies_to_id": null,
        "code": "GARMIN55",
        "ends_at": null,
        "id": 1016875801,
        "minimum_order_amount": 0.0,
        "starts_at": "2021-06-22T04:16:00Z",
        "status": "enabled",
        "usage_limit": 0,
        "value": 5.0000,
        "discount_type": "percentage",
        "times_used": 1,
        "is_promotion": true,
        "applies_to_resource": null,
        "variants": null,
        "location_ids": null,
        "create_user": 200000493247,
        "first_name": "Trọng",
        "last_name": "Nhân Lê",
        "applies_customer_group_id": 39550382,
        "created_at": "2021-06-22T04:17:56.847Z",
        "updated_at": "2021-06-22T04:17:56.847Z",
        "promotion_apply_type": 0,
        "applies_to_quantity": 0,
        "order_over": null,
        "is_new_coupon": false,
        "channel": null,
        "max_amount_apply": null,
        "is_advance_same_price_discount": false,
        "advance_same_prices": null,
        "once_per_customer": false,
        "products_selection": "all",
        "customers_selection": "all",
        "provinces_selection": "all",
        "channels_selection": "all",
        "locations_selection": "location_prerequisite",
        "entitled_collection_ids": [],
        "entitled_product_ids": [],
        "entitled_variant_ids": [],
        "entitled_customer_ids": [],
        "entitled_customer_segment_ids": [],
        "entitled_province_ids": [],
        "entitled_channels": [],
        "entitled_location_ids": [\
            1007284\
        ],
        "rule_customs": [],
        "take_type": "fixed_amount"

    }
}

```

### Update status enables a discount code [​](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/\#update-status-enables-a-discount-code "Direct link to heading")

PUT

https://apis.haravan.com/com/discounts/{discountId}/enable.json

Update status enable a discount code.

- PUT `https://apis.haravan.com/com/discounts/1017981791/enable.json`

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
        "code": "SUMMER_28/07",
        "ends_at": null,
        "id": 1017981791,
        "minimum_order_amount": 0.0,
        "starts_at": "2021-07-28T03:53:00Z",
        "status": "disabled",
        "usage_limit": 10,
        "value": 100000.0000,
        "discount_type": "fixed_amount",
        "times_used": 0,
        "is_promotion": true,
        "applies_to_resource": null,
        "variants": null,
        "location_ids": [\
            1007284\
        ],
        "create_user": 200000497867,
        "first_name": null,
        "last_name": null,
        "applies_customer_group_id": 39550400,
        "created_at": "2021-07-28T11:27:34.029Z",
        "updated_at": "2021-07-28T11:34:45.9148559Z",
        "promotion_apply_type": 0,
        "applies_to_quantity": 0,
        "order_over": null,
        "is_new_coupon": false,
        "channel": null,
        "max_amount_apply": null,
        "is_advance_same_price_discount": false,
        "advance_same_prices": null,
        "once_per_customer": false,
        "products_selection": "all",
        "customers_selection": "all",
        "provinces_selection": "all",
        "channels_selection": "all",
        "locations_selection": "all",
        "entitled_collection_ids": [],
        "entitled_product_ids": [],
        "entitled_variant_ids": [],
        "entitled_customer_ids": [],
        "entitled_customer_segment_ids": [],
        "entitled_province_ids": [],
        "entitled_channels": [],
        "entitled_location_ids": [],
        "rule_customs": [\
            {\
                "name": "time_range",\
                "value": "[{\"name\":\"monday\",\"value_range\":[]},{\"name\":\"tuesday\",\"value_range\":[]},{\"name\":\"wednesday\",\"value_range\":[]}]"\
            }\
        ],
        "take_type": "fixed_amount"
    }
}

```

### Update status disables a discount code [​](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/\#update-status-disables-a-discount-code "Direct link to heading")

PUT

https://apis.haravan.com/com/discounts/{discountId}/disable.json

Update status disables a discount code.

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
        "code": "SUMMER_28/07",
        "ends_at": null,
        "id": 1017981791,
        "minimum_order_amount": 0.0,
        "starts_at": "2021-07-28T03:53:00Z",
        "status": "disabled",
        "usage_limit": 10,
        "value": 100000.0000,
        "discount_type": "fixed_amount",
        "times_used": 0,
        "is_promotion": true,
        "applies_to_resource": null,
        "variants": null,
        "location_ids": [\
            1007284\
        ],
        "create_user": 200000497867,
        "first_name": null,
        "last_name": null,
        "applies_customer_group_id": 39550400,
        "created_at": "2021-07-28T11:27:34.029Z",
        "updated_at": "2021-07-28T11:34:45.9148559Z",
        "promotion_apply_type": 0,
        "applies_to_quantity": 0,
        "order_over": null,
        "is_new_coupon": false,
        "channel": null,
        "max_amount_apply": null,
        "is_advance_same_price_discount": false,
        "advance_same_prices": null,
        "once_per_customer": false,
        "products_selection": "all",
        "customers_selection": "all",
        "provinces_selection": "all",
        "channels_selection": "all",
        "locations_selection": "all",
        "entitled_collection_ids": [],
        "entitled_product_ids": [],
        "entitled_variant_ids": [],
        "entitled_customer_ids": [],
        "entitled_customer_segment_ids": [],
        "entitled_province_ids": [],
        "entitled_channels": [],
        "entitled_location_ids": [],
        "rule_customs": [\
            {\
                "name": "time_range",\
                "value": "[{\"name\":\"monday\",\"value_range\":[]},{\"name\":\"tuesday\",\"value_range\":[]},{\"name\":\"wednesday\",\"value_range\":[]}]"\
            }\
        ],
        "take_type": "fixed_amount"
    }
}

```

### Delete a discount code [​](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/\#delete-a-discount-code "Direct link to heading")

DELETE

https://apis.haravan.com/com/discounts/{discountId}.json

Delete a discount code.

- DELETE `https://apis.haravan.com/com/discounts/1017981791.json`

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
Customer Address](https://docs.haravan.com/docs/omni-apis/customer-address/) [Next\\
\\
DiscountCode](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/)

- [What you can do with Discount Code](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#what-you-can-do-with-discount-code)
- [Properties](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#properties)
- [Retrieves a list of enabling discount codes](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#retrieves-a-list-of-enabling-discount-codes)
- [Retrieves single the discount code](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#retrieves-single-the-discount-code)
- [Create a discount code](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#create-a-discount-code)
- [Update status enables a discount code](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#update-status-enables-a-discount-code)
- [Update status disables a discount code](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#update-status-disables-a-discount-code)
- [Delete a discount code](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/#delete-a-discount-code)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.