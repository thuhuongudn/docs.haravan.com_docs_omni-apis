---
url: "https://docs.haravan.com/docs/omni-apis/smart-collections/"
title: "SmartCollection | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/smart-collections/#)

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
- [Products](https://docs.haravan.com/docs/omni-apis/collects/)
- SmartCollection

On this page

# SmartCollection

`Version: 1.0`

A smart collection is a grouping of products defined by simple rules set by shop owners. A shop owner creates a smart collection and then sets the rules that determine which products go in them. haravan automatically changes the contents of smart collections based on their rules.

Smart Collections also use collects to connect a product to that smart collection. These collects, however, are managed by the rules of the smart collection and therefore cannot be added or removed through the API.

Haravan's collections — both smart collections and custom collections — are typically displayed to customers so that customers can select them and then view only the products in the collection they selected. They're typically used to break down the catalog of products into categories and make the shop easier to browse.

In addition to smart collections, there are also custom collections, which are groupings of products defined by the shop owner.

**Authenticated access scopes**: `com.read_products`, `com.write_products`

### What you can do with Smart Collection [​](https://docs.haravan.com/docs/omni-apis/smart-collections/\#what-you-can-do-with-smart-collection "Direct link to heading")

The Haravan API lets you do the following with the Smart Collection resource.

- GET `https://apis.haravan.com/com/smart_collections.json`
  - **[Retrieves a list of smart collections](https://docs.haravan.com/docs/omni-apis/smart-collections/#retrieves-a-list-of-smart-collections)**
- GET `https://apis.haravan.com/com/smart_collections/count.json`
  - **[Retrieves a count of smart collections](https://docs.haravan.com/docs/omni-apis/smart-collections/#retrieves-a-count-of-smart-collections)**
- GET `https://apis.haravan.com/com/smart_collections/{smart_collections_id}.json`
  - **[Retrieves detail a smart collection](https://docs.haravan.com/docs/omni-apis/smart-collections/#retrieves-detail-a-smart-collection)**
- POST `https://apis.haravan.com/com/smart_collections.json`
  - **[Create a smart collection](https://docs.haravan.com/docs/omni-apis/smart-collections/#create-a-smart-collection)**
- PUT `https://apis.haravan.com/com/smart_collections/{smart_collections_id}.json`
  - **[Update a smart collection](https://docs.haravan.com/docs/omni-apis/smart-collections/#update-a-smart-collection)**
- PUT `https://apis.haravan.com/com/smart_collections/{smart_collections_id}/order.json`
  - **[Set the ordering type and/or the manual order of products in a smart collection](https://docs.haravan.com/docs/omni-apis/smart-collections/#set-the-ordering-type-and/or-the-manual-order-of-products-in-a-smart-collection)**
- DELETE `https://apis.haravan.com/com/smart_collections/{smart_collections_id}.json`
  - **[Delete a smart collection](https://docs.haravan.com/docs/omni-apis/smart-collections/#delete-a-smart-collections)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/smart-collections/\#properties "Direct link to heading")

* * *

`body_html` : `string`

```codeBlockLines_e6Vv
"body_html": "The best selling ipod ever"

```

The description of the custom collection, complete with HTML markup. Many templates display this on their smart collection pages.

`handle` : `string`

```codeBlockLines_e6Vv
"handle": "ipods"

```

The description of the custom collection, complete with HTML markup. Many templates display this on their smart collection pages.

`image` : `string`

```codeBlockLines_e6Vv
"image": null

```

Image associated with the smart collection. Valid values are:

**attachment**: An image attached to a shop's theme returned as Base64-encoded binary data.

**src**: Source URL that specifies the location of the image.

`id` : `number`

```codeBlockLines_e6Vv
"id": 841564295

```

The unique numeric identifier for the smart collection.

`published_at` : `string`

```codeBlockLines_e6Vv
"published_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the collection was published.

`published_scope` : `string`

```codeBlockLines_e6Vv
"published_scope": "global"

```

The sales channels in which the smart collection is visible.

`rules` : `string`

```codeBlockLines_e6Vv
"rules": "relation"

```

The list of rules that define what products go into the smart collection. Each rule has the following properties:

- **relation**: The relation between the identifier for the condition and the numeric amount.

- **condition**: Select products for a collection using a condition.

- **column**: The value in the formula

  - **title**: Product title.
  - **type**: Product type.
  - **vendor**: Product vendor.
  - **variant\_price**: Product price.
  - **tag**: Product tag.
  - **variant\_compare\_at\_price**: Compare at price.
  - **variant\_weight**: Weight.
  - **variant\_inventory**: Inventory stock.
  - **variant\_title**: Variant's title.

`disjunctive` : `boolean`

```codeBlockLines_e6Vv
"disjunctive": true

```

If false, products must match all of the rules to be included in the collection. If true, products can only match one of the rules.

`sort_order` : `string`

```codeBlockLines_e6Vv
"sort_order": "manual"

```

The order in which products in the smart collection appear. Valid values are:

- **alpha-asc**: Alphabetically, in ascending order (A - Z).
- **alpha-desc**: Alphabetically, in descending order (Z - A).
- **best-selling**: By best-selling products.
- **created**: By date created, in ascending order (oldest - newest).
- **created-desc**: By date created, in descending order (newest - oldest).
- **manual**: Order created by the shop owner.
- **price-asc**: By price, in ascending order (lowest-highest).
- **price-desc**: By price, in descending order (highest - lowest).

`template_suffix` : `string`

```codeBlockLines_e6Vv
"template_suffix": null

```

The suffix of the liquid template being used. By default, the original template is called product.liquid, without any suffix. Any additional templates will be: product.suffix.liquid.

`title` : `string`

```codeBlockLines_e6Vv
"title": "Machine"

```

The name of the smart collection. Limit of 255 characters.

`updated_at` : `string`

```codeBlockLines_e6Vv
"updated_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the collection was updated.

### Retrieves a list of smart collections [​](https://docs.haravan.com/docs/omni-apis/smart-collections/\#retrieves-a-list-of-smart-collections "Direct link to heading")

GET

https://apis.haravan.com/com/smart\_collections.json

Retrieves a list of smart collections.

### Parameters [​](https://docs.haravan.com/docs/omni-apis/smart-collections/\#parameters "Direct link to heading")

* * *

`limit`

Limit of the result.

* * *

`page`

Page to show the result.

* * *

`since_id`

Restrict results to after the specified ID

* * *

`title`

Filter result by the title.

* * *

`product_id`

Filter result by the product id.

* * *

`handle`

Filter result by the handle.

* * *

`updated_at_min`

Show smart collections last updated after date (format: 2008-12-31 03:00).

* * *

`updated_at_max`

Show smart collections last updated before date (format: 2008-12-31 03:00).

* * *

`published_at_min`

Show smart collections last updated after date (format: 2008-12-31 03:00).

* * *

`published_at_max`

Show smart collections last updated before date (format: 2008-12-31 03:00).

* * *

`published_status`

- **published** \- Show only published smart collections
- **unpublished** \- Show only unpublished smart collections
- **any** \- Show all smart collections (default)

* * *

`fields`

Comma-separated list of fields to include in the response.

* * *

Retrieve all smart collections by page number. By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/com/smart_collections.json?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "smart_collections": [\
        {\
            "body_html": null,\
            "handle": "km-20",\
            "id": 1002448475,\
            "image": null,\
            "published_at": "2020-12-03T09:42:28.751Z",\
            "published_scope": "global",\
            "rules": [\
                {\
                    "relation": "equals",\
                    "condition": "KM20",\
                    "column": "tag"\
                }\
            ],\
            "disjunctive": true,\
            "sort_order": "alpha_asc",\
            "template_suffix": "collection",\
            "title": "KM 20%",\
            "updated_at": "2020-12-03T09:43:02.959Z"\
        }\
    ]
}

```

Retrieve all smart collections by title.

- GET `https://apis.haravan.com/com/smart_collections.json?title=km`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK
{
    "smart_collections": [\
        {\
            "body_html": null,\
            "handle": "km-20",\
            "id": 1002448475,\
            "image": null,\
            "published_at": "2020-12-03T09:42:28.751Z",\
            "published_scope": "global",\
            "rules": [\
                {\
                    "relation": "equals",\
                    "condition": "KM20",\
                    "column": "tag"\
                }\
            ],\
            "disjunctive": true,\
            "sort_order": "alpha_asc",\
            "template_suffix": "collection",\
            "title": "KM 20%",\
            "updated_at": "2020-12-03T09:43:02.959Z"\
        }\
    ]
}

```

Retrieve all smart collections by product id.

- GET `https://apis.haravan.com/com/smart_collections.json?product_id=1028183686`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "smart_collections": [\
        {\
            "body_html": null,\
            "handle": "km-20",\
            "id": 1002448475,\
            "image": null,\
            "published_at": "2020-12-03T09:42:28.751Z",\
            "published_scope": "global",\
            "rules": [\
                {\
                    "relation": "equals",\
                    "condition": "KM20",\
                    "column": "tag"\
                }\
            ],\
            "disjunctive": true,\
            "sort_order": "alpha_asc",\
            "template_suffix": "collection",\
            "title": "KM 20%",\
            "updated_at": "2020-12-03T09:43:02.959Z"\
        }\
    ]
}

```

### Retrieves a count of smart collections [​](https://docs.haravan.com/docs/omni-apis/smart-collections/\#retrieves-a-count-of-smart-collections "Direct link to heading")

GET

https://apis.haravan.com/com/smart\_collections/count.json

Count all smart collections for your shop.

- GET `https://apis.haravan.com/com/smart_collections/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 1
}

```

Count only collects for a certain product.

- GET `https://apis.haravan.com/com/smart_collections/count.json?product_id=1028183686`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 1
}

```

### Retrieves detail a smart collection [​](https://docs.haravan.com/docs/omni-apis/smart-collections/\#retrieves-detail-a-smart-collection "Direct link to heading")

GET

https://apis.haravan.com/com/smart\_collections/{smart\_collections\_id}.json

Retrieves detail a smart collection with id.

- GET `https://apis.haravan.com/com/smart_collections/1002448475.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "smart_collection": {
        "body_html": null,
        "handle": "km-20",
        "id": 1002448475,
        "image": null,
        "published_at": "2020-12-03T09:42:28.751Z",
        "published_scope": "global",
        "rules": [\
            {\
                "relation": "equals",\
                "condition": "KM20",\
                "column": "tag"\
            }\
        ],
        "disjunctive": true,
        "sort_order": "alpha_asc",
        "template_suffix": "collection",
        "title": "KM 20%",
        "updated_at": "2020-12-03T09:43:02.959Z"
    }
}

```

### Create a smart collection [​](https://docs.haravan.com/docs/omni-apis/smart-collections/\#create-a-smart-collection "Direct link to heading")

POST

https://apis.haravan.com/com/smart\_collections.json

Create a smart collection.

Valid values for Rule fields:

- **column** \- title, type, vendor, variant\_price, variant\_compare\_at\_price, variant\_weight, variant\_inventory, variant\_title
- **relation** \- equals, greater\_than, less\_than, starts\_with, ends\_with, contains
- **condition** \- any string

Create a collection of all products starting with the term iPod.

- POST `https://apis.haravan.com/com/smart_collections.json`

```codeBlockLines_e6Vv
{
  "smart_collection": {
    "title": "IPods",
    "rules": [\
      {\
        "column": "title",\
        "relation": "starts_with",\
        "condition": "iPod"\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
    "smart_collection": {
        "body_html": null,
        "handle": "ipods",
        "id": 1002798878,
        "image": {
            "src": null,
            "created_at": null
        },
        "published_at": "2021-08-18T11:25:28.1096473Z",
        "published_scope": null,
        "rules": [\
            {\
                "relation": "starts_with",\
                "condition": "iPod",\
                "column": "title"\
            }\
        ],
        "disjunctive": false,
        "sort_order": "alpha_asc",
        "template_suffix": "collection",
        "title": "IPods",
        "updated_at": "2021-08-18T11:25:28.1881035Z",
        "products_count": 0
    }
}

```

### Update a smart collection [​](https://docs.haravan.com/docs/omni-apis/smart-collections/\#update-a-smart-collection "Direct link to heading")

PUT

https://apis.haravan.com/com/smart\_collections/{smart\_collection\_id}.json

Change the description of a smart collection.

- PUT `https://apis.haravan.com/com/smart_collections/841564295.json`

```codeBlockLines_e6Vv
{
  "smart_collection": {
    "body_html": "5000 songs in your pocket"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "smart_collection": {
        "body_html": null,
        "handle": "ipods",
        "id": 1002798878,
        "image": null,
        "published_at": "2021-08-18T11:25:28.11Z",
        "published_scope": "web",
        "rules": [\
            {\
                "relation": "starts_with",\
                "condition": "iPod",\
                "column": "title"\
            }\
        ],
        "disjunctive": false,
        "sort_order": "alpha_asc",
        "template_suffix": "collection",
        "title": "IPods",
        "updated_at": "2021-08-18T11:25:28.188Z"
    }
}

```

### Set the ordering type and/or the manual order of products in a smart collection [​](https://docs.haravan.com/docs/omni-apis/smart-collections/\#set-the-ordering-type-andor-the-manual-order-of-products-in-a-smart-collection "Direct link to heading")

PUT

https://apis.haravan.com/com/smart\_collections/{smart\_collection\_id}/order.json

Set the ordering type and/or the manual order of products in a smart collection.

- **products**: Array of product ids in the order you want them arranged. (Applies only when sort\_order is set to "manual")
- **sort\_order**: The type of sorting to apply. Valid values are listed in the Properties section above. (default: (current value))

Change the manual ordering of products in the smart collection.

- PUT `https://apis.haravan.com/com/smart_collections/841564295/order.json?products[]=921728736&products[]=632910392`

```codeBlockLines_e6Vv
{}

```

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{}

```

Change the manual ordering of products in the smart collection.

- PUT `https://apis.haravan.com/com/smart_collections/841564295/order.json?sort_order=alpha-desc`

```codeBlockLines_e6Vv
{}

```

```codeBlockLines_e6Vv
HTTP/1.1 200 Ok
{}

```

### Delete a smart collection [​](https://docs.haravan.com/docs/omni-apis/smart-collections/\#delete-a-smart-collection "Direct link to heading")

DELETE

https://apis.haravan.com/com/smart\_collections/{smart\_collection\_id}.json

Delete a smart collection.

- DELETE `https://apis.haravan.com/com/smart_collections/1002798878.json`

```codeBlockLines_e6Vv
{}

```

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
[]

```

[Previous\\
\\
Product Variant](https://docs.haravan.com/docs/omni-apis/product-variants/) [Next\\
\\
ShippingRate](https://docs.haravan.com/docs/omni-apis/shipping-rates/)

- [What you can do with Smart Collection](https://docs.haravan.com/docs/omni-apis/smart-collections/#what-you-can-do-with-smart-collection)
- [Properties](https://docs.haravan.com/docs/omni-apis/smart-collections/#properties)
- [Retrieves a list of smart collections](https://docs.haravan.com/docs/omni-apis/smart-collections/#retrieves-a-list-of-smart-collections)
- [Parameters](https://docs.haravan.com/docs/omni-apis/smart-collections/#parameters)
- [Retrieves a count of smart collections](https://docs.haravan.com/docs/omni-apis/smart-collections/#retrieves-a-count-of-smart-collections)
- [Retrieves detail a smart collection](https://docs.haravan.com/docs/omni-apis/smart-collections/#retrieves-detail-a-smart-collection)
- [Create a smart collection](https://docs.haravan.com/docs/omni-apis/smart-collections/#create-a-smart-collection)
- [Update a smart collection](https://docs.haravan.com/docs/omni-apis/smart-collections/#update-a-smart-collection)
- [Set the ordering type and/or the manual order of products in a smart collection](https://docs.haravan.com/docs/omni-apis/smart-collections/#set-the-ordering-type-andor-the-manual-order-of-products-in-a-smart-collection)
- [Delete a smart collection](https://docs.haravan.com/docs/omni-apis/smart-collections/#delete-a-smart-collection)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.