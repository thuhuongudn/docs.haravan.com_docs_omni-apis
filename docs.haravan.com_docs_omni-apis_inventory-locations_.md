---
url: "https://docs.haravan.com/docs/omni-apis/inventory-locations/"
title: "Inventory Location Balance | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/inventory-locations/#)

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
- Inventory Location Balance

On this page

# Inventory Location Balance

`Version: 1.0`

An inventory item represents the physical goods available to be shipped to a customer. It holds essential information about the physical good, including its SKU and whether its inventory is tracked.

You can use the location id with variant id to query the inventory locations resources to retrieve inventory information.

**Authenticated access scopes**: `com.read_inventories`, `com.write_inventories`

### What you can do with Inventory Locations [​](https://docs.haravan.com/docs/omni-apis/inventory-locations/\#what-you-can-do-with-inventory-locations "Direct link to heading")

The Haravan API lets you do the following with the Inventory Locations resource.

- GET `https://apis.haravan.com/com/inventory_locations.json?location_ids={location_ids}&variant_ids={variant_ids}`
  - **[Retrieves a list of inventory items.](https://docs.haravan.com/docs/omni-apis/inventory-locations/#retrieves-a-list-of-inventory-items)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/inventory-locations/\#properties "Direct link to heading")

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id": 1206854680

```

The ID of the inventory item.

`loc_id` : `number`

```codeBlockLines_e6Vv
"loc_id": 963414

```

`product_id` : `number`

```codeBlockLines_e6Vv
"product_id": 1028183686

```

The ID of the product.

`variant_id` : `number`

```codeBlockLines_e6Vv
"variant_id": 1064240649

```

The ID of the product variant.

`qty_onhand` : `number`

```codeBlockLines_e6Vv
"qty_onhand": 0

```

The quantity of inventory items.

`qty_commited` : `number`

```codeBlockLines_e6Vv
"qty_commited": 7

```

The quantity of inventory items ordered.

`qty_incoming` : `number`

```codeBlockLines_e6Vv
"qty_incoming": 1

```

The quantity of inventory items ordered.

`qty_available` : `number`

```codeBlockLines_e6Vv
"qty_available": 5

```

The quantity of inventory items available for sale.

`updated_at` : `string`

```codeBlockLines_e6Vv
"updated_at": "2021-05-13T07:29:20.808Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the inventory item was last updated.

### Retrieves a list of inventory items [​](https://docs.haravan.com/docs/omni-apis/inventory-locations/\#retrieves-a-list-of-inventory-items "Direct link to heading")

GET

https://apis.haravan.com/com/inventory\_locations.json?location\_ids={location\_ids}&variant\_ids={variant\_ids}

Retrieves a list of inventory items.

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/inventory-locations/\#parameters "Direct link to heading")

* * *

`limit`

Limit of the result.(default: 250, maximum: 250)

* * *

`location_ids`

Filter result by the comma-separated list of location ids. (maximum: 50)

* * *

`vatiant_ids`

Filter result by the comma-separated list of variant ids. (maximum: 50)

* * *

`updated_at_min`

Show inventory locations updated at or after date.

* * *

`since_id`

Show inventory locations after the specified ID.

* * *

`order`

Sort result by order id or order update\_at order=id or order=updated\_at.

* * *

`direction`

Sort result by the order direction=asc or direction=desc.

* * *

Retrieves a list of inventory items.

- GET `https://apis.haravan.com/com/inventory_locations.json?location_ids=1007284,963414&variant_ids=1061514767,1064240649`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "inventory_locations": [\
        {\
            "id": 1003098484,\
            "loc_id": 1007284,\
            "product_id": 1028183686,\
            "variant_id": 1064240649,\
            "qty_onhand": 0,\
            "qty_commited": 0,\
            "qty_incoming": 0,\
            "qty_available": 0,\
            "updated_at": "2021-08-04T08:32:02.01Z"\
        },\
        {\
            "id": 1006907070,\
            "loc_id": 1007284,\
            "product_id": 1028183686,\
            "variant_id": 1061514767,\
            "qty_onhand": 15,\
            "qty_commited": 0,\
            "qty_incoming": 1,\
            "qty_available": 15,\
            "updated_at": "2021-07-30T06:05:24.332Z"\
        },\
        {\
            "id": 1003226632,\
            "loc_id": 963414,\
            "product_id": 1028183686,\
            "variant_id": 1064240649,\
            "qty_onhand": 0,\
            "qty_commited": 7,\
            "qty_incoming": 0,\
            "qty_available": -7,\
            "updated_at": "2021-07-08T01:47:17.612Z"\
        },\
        {\
            "id": 1007549786,\
            "loc_id": 963414,\
            "product_id": 1028183686,\
            "variant_id": 1061514767,\
            "qty_onhand": -3,\
            "qty_commited": 12,\
            "qty_incoming": 0,\
            "qty_available": -15,\
            "updated_at": "2021-07-08T01:47:17.6Z"\
        }\
    ]
}

```

[Previous\\
\\
Inventory Adjustment](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/) [Next\\
\\
Inventory Purchase Order](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/)

- [What you can do with Inventory Locations](https://docs.haravan.com/docs/omni-apis/inventory-locations/#what-you-can-do-with-inventory-locations)
- [Properties](https://docs.haravan.com/docs/omni-apis/inventory-locations/#properties)
- [Retrieves a list of inventory items](https://docs.haravan.com/docs/omni-apis/inventory-locations/#retrieves-a-list-of-inventory-items)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.