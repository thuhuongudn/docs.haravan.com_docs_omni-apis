---
url: "https://docs.haravan.com/docs/omni-apis/collects/"
title: "Collect | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/collects/#)

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

  - [Products](https://docs.haravan.com/docs/omni-apis/collects/)

    - [Collect](https://docs.haravan.com/docs/omni-apis/collects/)
    - [CustomCollection](https://docs.haravan.com/docs/omni-apis/custom-collections/)
    - [Product](https://docs.haravan.com/docs/omni-apis/products/)
    - [Product Image](https://docs.haravan.com/docs/omni-apis/product-images/)
    - [Product Variant](https://docs.haravan.com/docs/omni-apis/product-variants/)
    - [SmartCollection](https://docs.haravan.com/docs/omni-apis/smart-collections/)
  - [Shipping](https://docs.haravan.com/docs/omni-apis/shipping-rates/)

  - [Store properties](https://docs.haravan.com/docs/omni-apis/country/)

  - [Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [Home page](https://docs.haravan.com/)
- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)
- Products

On this page

# Collect

`Version: 1.0`

A collect is an object that connects a product to a custom collection.

For every product in a custom collection, there exists a collect that tracks the ids of both the product and the custom collection it's a member of. A product can be a member of more than one collection and will have more than one collect connecting the product to each collection. Unlike many haravan resources, collects aren't apparent to shop owners; they're objects for managing the relationship between products and custom collections.

**Authenticated access scopes**: `com.read_products`, `com.write_products`

### What you can do with Collect [​](https://docs.haravan.com/docs/omni-apis/collects/\#what-you-can-do-with-collect "Direct link to heading")

The Haravan API lets you do the following with the Collect resource.

- GET `https://apis.haravan.com/com/collects.json`
  - **[Retrieves a list of collects](https://docs.haravan.com/docs/omni-apis/collects/#retrieves-a-list-of-collects)**
- GET `https://apis.haravan.com/com/collects/count.json`
  - **[Retrieves a count of all collects](https://docs.haravan.com/docs/omni-apis/collects/#retrieves-a-count-of-all-collects)**
- GET `https://apis.haravan.com/com/collects/{collect_id}.json`
  - **[Retrieves detail a collects](https://docs.haravan.com/docs/omni-apis/collects/#retrieves-detail-a-collect)**
- POST `https://apis.haravan.com/com/collects.json`
  - **[Create a collect](https://docs.haravan.com/docs/omni-apis/collects/#create-a-collect)**
- DELETE `https://apis.haravan.com/com/collects/{collect_id}.json`
  - **[Delete a collect](https://docs.haravan.com/docs/omni-apis/collects/#delete-a-collect)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/collects/\#properties "Direct link to heading")

* * *

`collection_id` : `number`

```codeBlockLines_e6Vv
"collection_id": 841564295

```

The id of the custom collection containing the product.

* * *

`created_at` : `string`

```codeBlockLines_e6Vv
"created_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the collect was created.

* * *

`featured` : `boolean`

```codeBlockLines_e6Vv
"featured": false

```

States whether or not the collect is featured. Valid values are "true" or "false".

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id": 841564295

```

A unique numeric identifier for the collect.

* * *

`carrier_code` : `string`

```codeBlockLines_e6Vv
"carrier_code": "haravanexpress"

```

The code for the carrier.

* * *

`position` : `string`

```codeBlockLines_e6Vv
"position":"2"

```

A number specifying the manually sorted position of this product in a custom collection. The first position is 1. This value only applies when the custom collection is viewed using the Manual sort order.

* * *

`product_id` : `number`

```codeBlockLines_e6Vv
"product_id":632910392

```

The unique numeric identifier for the product in the custom collection.

* * *

`sort_value`: `string`

```codeBlockLines_e6Vv
"sort_value":"0000000002"

```

This is the same value as but padded with leading zeroes to make it alphanumeric-sortable.

* * *

`created_at` : `string`

```codeBlockLines_e6Vv
"updated_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the collect was updated.

* * *

### Retrieves a list of collects [​](https://docs.haravan.com/docs/omni-apis/collects/\#retrieves-a-list-of-collects "Direct link to heading")

GET

https://apis.haravan.com/com/collects.json

### Parameters [​](https://docs.haravan.com/docs/omni-apis/collects/\#parameters "Direct link to heading")

* * *

`limit`

Limit of the result (Max: 500).

* * *

`page`

Page to show the result.

* * *

`collection_id`

Filter result by the collection id.

* * *

`product_id`

Filter result by the product id.

* * *

`fields`

Comma-separated list of fields to include in the response.

* * *

Retrieve all collects by page number. By default, the number of resources on the page is 50. (Max: 500)

- GET `https://apis.haravan.com/com/collects.json?page=1&limit=50`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "collects": [\
    {\
      "collection_id": 395646240,\
      "created_at": null,\
      "featured": false,\
      "id": 395646240,\
      "position": 1,\
      "product_id": 632910392,\
      "updated_at": null,\
      "sort_value": "0000000001"\
    },\
    {\
      "collection_id": 841564295,\
      "created_at": null,\
      "featured": false,\
      "id": 841564295,\
      "position": 1,\
      "product_id": 632910392,\
      "updated_at": null,\
      "sort_value": "0000000001"\
    }\
  ]
}

```

Retrieve all collects by collection id.

- GET `https://apis.haravan.com/com/collects.json?colection_id=1002507494`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK
{
    "collects": [\
        {\
            "collection_id": 1002507494,\
            "created_at": "2021-01-13T12:28:01.614Z",\
            "featured": false,\
            "id": 1059375051,\
            "position": 0,\
            "product_id": 1028183633,\
            "sort_value": "0000000000",\
            "updated_at": "2021-01-13T12:28:02.614Z"\
        }\
    ]
}

```

Retrieve all collects by product id.

- GET `https://apis.haravan.com/com/collects.json?product_id=1028183633`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "collects": [\
        {\
            "collection_id": 1002507492,\
            "created_at": "2021-01-13T12:28:01.248Z",\
            "featured": false,\
            "id": 1059375049,\
            "position": 0,\
            "product_id": 1028183633,\
            "sort_value": "0000000000",\
            "updated_at": "2021-01-13T12:28:02.248Z"\
        },\
        {\
            "collection_id": 1002507493,\
            "created_at": "2021-01-13T12:28:01.431Z",\
            "featured": false,\
            "id": 1059375050,\
            "position": 0,\
            "product_id": 1028183633,\
            "sort_value": "0000000000",\
            "updated_at": "2021-01-13T12:28:02.431Z"\
        }\
    ]
}

```

### Retrieves a count of all collects [​](https://docs.haravan.com/docs/omni-apis/collects/\#retrieves-a-count-of-all-collects "Direct link to heading")

GET

https://apis.haravan.com/com/collects/count.json

Count all collects for your shop.

- GET `https://apis.haravan.com/com/collects/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 2
}

```

Count only collects for a certain collection.

- GET `https://apis.haravan.com/com/collects/count.json?collection_id=841564295`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 1
}

```

Count only collects for a certain product.

- GET `https://apis.haravan.com/com/collects/count.json?product_id=632910392`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 2
}

```

### Retrieves detail a collect [​](https://docs.haravan.com/docs/omni-apis/collects/\#retrieves-detail-a-collect "Direct link to heading")

GET

https://apis.haravan.com/com/collects/{collect\_id}.json

Retrieves detail a collect with id.

- GET `https://apis.haravan.com/com/collects/841564295.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "collect": {
    "collection_id": 841564295,
    "created_at": null,
    "featured": false,
    "id": 841564295,
    "position": 1,
    "product_id": 632910392,
    "updated_at": null,
    "sort_value": "0000000001"
  }
}

```

### Create a collect [​](https://docs.haravan.com/docs/omni-apis/collects/\#create-a-collect "Direct link to heading")

POST

https://apis.haravan.com/com/collects.json

Note: Collects are for specifying the membership of products in custom collections only; smart collections use rules to determine which products are their members. Creating a collect that links a product to a smart collection results in a 403 Forbidden error.

Create a new collect.

- POST `https://apis.haravan.com/com/collects.json`

```codeBlockLines_e6Vv
{
  "collect": {
    "product_id": 921728736,
    "collection_id": 841564295
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "collect": {
    "collection_id": 841564295,
    "created_at": "2015-03-28T13:27:21-04:00",
    "featured": false,
    "id": 1071559574,
    "position": 2,
    "product_id": 921728736,
    "updated_at": "2015-03-28T13:27:21-04:00",
    "sort_value": "0000000002"
  }
}

```

### Delete a collect [​](https://docs.haravan.com/docs/omni-apis/collects/\#delete-a-collect "Direct link to heading")

DELETE

https://apis.haravan.com/com/collects/{collect\_id}.json

Delete a collect.

- DELETE `https://apis.haravan.com/com/collects/841564295.json`

```codeBlockLines_e6Vv
{}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
[]

```

[Previous\\
\\
Transaction](https://docs.haravan.com/docs/omni-apis/transactions/) [Next\\
\\
Collect](https://docs.haravan.com/docs/omni-apis/collects/)

- [What you can do with Collect](https://docs.haravan.com/docs/omni-apis/collects/#what-you-can-do-with-collect)
- [Properties](https://docs.haravan.com/docs/omni-apis/collects/#properties)
- [Retrieves a list of collects](https://docs.haravan.com/docs/omni-apis/collects/#retrieves-a-list-of-collects)
- [Parameters](https://docs.haravan.com/docs/omni-apis/collects/#parameters)
- [Retrieves a count of all collects](https://docs.haravan.com/docs/omni-apis/collects/#retrieves-a-count-of-all-collects)
- [Retrieves detail a collect](https://docs.haravan.com/docs/omni-apis/collects/#retrieves-detail-a-collect)
- [Create a collect](https://docs.haravan.com/docs/omni-apis/collects/#create-a-collect)
- [Delete a collect](https://docs.haravan.com/docs/omni-apis/collects/#delete-a-collect)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.