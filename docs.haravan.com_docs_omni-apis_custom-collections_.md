---
url: "https://docs.haravan.com/docs/omni-apis/custom-collections/"
title: "CustomCollection | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/custom-collections/#)

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
- CustomCollection

On this page

# CustomCollection

`Version: 1.0`

A custom collection is a grouping of products that a shop owner can create to make their shops easier to browse. A shop owner creates a custom collection and then selects the products that will go into it..

Custom collections are typically displayed to customers so that customers can select them to view only the products in the collection they've selected. They're typically used to break down a catalog of products into categories to make the shop easier to browse. haravan shops start with a single custom collection called frontpage — the collection of products shown on the shop's front page.

**Authenticated access scopes**: `com.read_products`, `com.write_products`

### What you can do with Custom Collection [​](https://docs.haravan.com/docs/omni-apis/custom-collections/\#what-you-can-do-with-custom-collection "Direct link to heading")

The Haravan API lets you do the following with the Custom Collection resource.

- GET `https://apis.haravan.com/com/custom_collections.json`
  - **[Retrieves a list of custom collections](https://docs.haravan.com/docs/omni-apis/custom-collections/#retrieves-a-list-of-custom-collections)**
- GET `https://apis.haravan.com/com/custom_collections/count.json`
  - **[Retrieves a count of custom collections](https://docs.haravan.com/docs/omni-apis/custom-collections/#retrieves-a-count-of-custom-collections)**
- GET `https://apis.haravan.com/com/custom_collections/{custom_collections_id}.json`
  - **[Retrieves detail a custom collection](https://docs.haravan.com/docs/omni-apis/custom-collections/#retrieves-detail-a-custom-collection)**
- POST `https://apis.haravan.com/com/custom_collections.json`
  - **[Create a custom collection](https://docs.haravan.com/docs/omni-apis/custom-collections/#create-a-custom-collection)**
- PUT `https://apis.haravan.com/com/custom_collections/{custom_collections_id}.json`
  - **[Update a custom collection](https://docs.haravan.com/docs/omni-apis/custom-collections/#update-a-custom-collection)**
- DELETE `https://apis.haravan.com/com/custom_collections/{custom_collections_id}.json`
  - **[Delete a custom collection](https://docs.haravan.com/docs/omni-apis/custom-collections/#delete-a-custom-collection)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/custom-collections/\#properties "Direct link to heading")

* * *

`body_html` : `string`

```codeBlockLines_e6Vv
"body_html": "The best selling ipod ever"

```

The description of the custom collection, complete with HTML markup. Many templates display this on their custom collection pages.

* * *

`handle` : `string`

```codeBlockLines_e6Vv
"handle": "ipods"

```

The description of the custom collection, complete with HTML markup. Many templates display this on their custom collection pages.

* * *

`image` : `string`

```codeBlockLines_e6Vv
"image": null

```

Image associated with the custom collection. Valid values are:

**attachment**: An image attached to a shop's theme returned as Base64-encoded binary data.

**src**: Source URL that specifies the location of the image.

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id": 841564295

```

The unique numeric identifier for the custom collection.

* * *

`published` : `boolean`

```codeBlockLines_e6Vv
"published": true

```

States whether the custom collection is visible. Valid values are "true" for visible and "false" for hidden.

* * *

`published_at` : `string`

```codeBlockLines_e6Vv
"published_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the collection was published.

* * *

`published_scope` : `string`

```codeBlockLines_e6Vv
"published_scope": "global"

```

The sales channels in which the custom collection is visible.

* * *

`sort_order` : `string`

```codeBlockLines_e6Vv
"sort_order": "manual"

```

The order in which products in the custom collection appear. Valid values are:

- **alpha-asc**: Alphabetically, in ascending order (A - Z).
- **alpha-desc**: Alphabetically, in descending order (Z - A).
- **best-selling**: By best-selling products.
- **created**: By date created, in ascending order (oldest - newest).
- **created-desc**: By date created, in descending order (newest - oldest).
- **manual**: Order created by the shop owner.
- **price-asc**: By price, in ascending order (lowest-highest).
- **price-desc**: By price, in descending order (highest - lowest).

* * *

`template_suffix` : `string`

```codeBlockLines_e6Vv
"template_suffix": null

```

The suffix of the liquid template being used. By default, the original template is called product.liquid, without any suffix. Any additional templates will be: product.suffix.liquid.

* * *

`title` : `string`

```codeBlockLines_e6Vv
"title": "Machine"

```

The name of the custom collection. Limit of 255 characters.

* * *

`updated_at` : `string`

```codeBlockLines_e6Vv
"updated_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the collection was updated.

* * *

### Retrieves a list of custom collections [​](https://docs.haravan.com/docs/omni-apis/custom-collections/\#retrieves-a-list-of-custom-collections "Direct link to heading")

GET

https://apis.haravan.com/com/custom\_collections.json

### Parameters [​](https://docs.haravan.com/docs/omni-apis/custom-collections/\#parameters "Direct link to heading")

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

`title`

Filter result by the title.

* * *

`product_id`

Filter result by the product id

* * *

`handle`

Filter result by the handle.

* * *

`updated_at_min`

Show custom collections last updated after date (format: 2008-12-31 03:00).

* * *

`updated_at_max`

Show custom collections last updated before date (format: 2008-12-31 03:00).

* * *

`published_at_min`

Show custom collections last updated after date (format: 2008-12-31 03:00).

* * *

`published_at_max`

Show custom collections last updated before date (format: 2008-12-31 03:00).

* * *

`published_status`

**published** \- Show only published custom collections

**unpublished** \- Show only unpublished custom collections

**any** \- Show all custom collections (default)

* * *

`fields`

Comma-separated list of fields to include in the response.

* * *

Retrieve all custom collection by page number. By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/com/custom_collections.json?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "custom_collections": [\
    {\
            "body_html": null,\
            "handle": "onsale",\
            "image": null,\
            "id": 1002326115,\
            "published": false,\
            "published_at": "2020-09-18T04:10:31.961Z",\
            "published_scope": "web",\
            "sort_order": "alpha_asc",\
            "template_suffix": "collection",\
            "title": "Sản phẩm khuyến mãi",\
            "updated_at": "2021-02-02T10:19:48.052Z"\
        },\
        {\
            "body_html": null,\
            "handle": "hot-products",\
            "image": null,\
            "id": 1002326116,\
            "published": false,\
            "published_at": "2020-09-18T04:10:32.851Z",\
            "published_scope": "web",\
            "sort_order": "alpha_asc",\
            "template_suffix": "collection",\
            "title": "Sản phẩm nổi bật",\
            "updated_at": "2020-09-18T04:10:33.12Z"\
        }\
  ]
}

```

Retrieve all custom collection by title.

- GET ` https://apis.haravan.com/com/custom_collections.json?title=Sản phẩm`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK
{
    "custom_collections": [\
        {\
            "body_html": null,\
            "handle": "onsale",\
            "image": null,\
            "id": 1002326115,\
            "published": false,\
            "published_at": "2020-09-18T04:10:31.961Z",\
            "published_scope": "web",\
            "sort_order": "alpha_asc",\
            "template_suffix": "collection",\
            "title": "Sản phẩm khuyến mãi",\
            "updated_at": "2021-02-02T10:19:48.052Z"\
        },\
        {\
            "body_html": null,\
            "handle": "hot-products",\
            "image": null,\
            "id": 1002326116,\
            "published": false,\
            "published_at": "2020-09-18T04:10:32.851Z",\
            "published_scope": "web",\
            "sort_order": "alpha_asc",\
            "template_suffix": "collection",\
            "title": "Sản phẩm nổi bật",\
            "updated_at": "2020-09-18T04:10:33.12Z"\
        }\
    ]
}

```

Retrieve all collections by product id.

- GET `https://apis.haravan.com/com/custom_collections.json?product_id=1028183686`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "custom_collections": [\
        {\
            "body_html": null,\
            "handle": "onsale",\
            "image": null,\
            "id": 1002326115,\
            "published": false,\
            "published_at": "2020-09-18T04:10:31.961Z",\
            "published_scope": "web",\
            "sort_order": "alpha_asc",\
            "template_suffix": "collection",\
            "title": "Sản phẩm khuyến mãi",\
            "updated_at": "2021-02-02T10:19:48.052Z"\
        }\
    ]
}

```

### Retrieves a count of custom collections [​](https://docs.haravan.com/docs/omni-apis/custom-collections/\#retrieves-a-count-of-custom-collections "Direct link to heading")

GET

https://apis.haravan.com/com/custom\_collections/count.json

Count all custom collections for your shop.

- GET `https://apis.haravan.com/com/custom_collections/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 2
}

```

Count only collections for a certain product.

- GET `https://apis.haravan.com/com/custom_collections/count.json?product_id=1028183686`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 2
}

```

### Retrieves detail a custom collection [​](https://docs.haravan.com/docs/omni-apis/custom-collections/\#retrieves-detail-a-custom-collection "Direct link to heading")

GET

https://apis.haravan.com/com/custom\_collections/{custom\_collection\_id}.json

Retrieves detail a custom collection with id.

- GET `https://apis.haravan.com/com/custom_collections/1002326115.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "custom_collection": {
        "body_html": null,
        "handle": "onsale",
        "image": null,
        "id": 1002326115,
        "published": false,
        "published_at": "2020-09-18T04:10:31.961Z",
        "published_scope": "web",
        "sort_order": "alpha_asc",
        "template_suffix": "collection",
        "title": "Sản phẩm khuyến mãi",
        "updated_at": "2021-02-02T10:19:48.052Z"
    }
}

```

### Create a custom collection [​](https://docs.haravan.com/docs/omni-apis/custom-collections/\#create-a-custom-collection "Direct link to heading")

POST

https://apis.haravan.com/com/custom\_collections.json

Create a collection with a collect.

- POST `https://apis.haravan.com/com/custom_collections.json`

```codeBlockLines_e6Vv
{
  "custom_collection": {
    "title": "IPods",
    "collects": [\
      {\
        "product_id": 921728736\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "custom_collection": {
    "body_html": null,
    "handle": "ipods-1",
    "id": 1063001312,
    "published_at": "2021-02-02T10:19:48.052Z",
    "published_scope": "global",
    "sort_order": "alpha-asc",
    "template_suffix": null,
    "title": "IPods",
    "updated_at": "2021-02-02T10:19:48.052Z"
  }
}

```

Create a collection with the title.

- POST `https://apis.haravan.com/com/custom_collections.json`

```codeBlockLines_e6Vv
{
  "custom_collection": {
    "title": "Macbooks"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "custom_collection": {
    "body_html": null,
    "handle": "macbooks",
    "id": 1063001314,
    "published_at": "2021-03-28T13:27:38-04:00Z",
    "published_scope": "global",
    "sort_order": "alpha-asc",
    "template_suffix": null,
    "title": "Macbooks",
    "updated_at": "2021-03-28T13:27:38-04:00Z"
  }
}

```

Create a new, but an unpublished collection.

- POST `https://apis.haravan.com/com/custom_collections.json`

```codeBlockLines_e6Vv
{
  "custom_collection": {
    "title": "Macbooks",
     "published": false
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "custom_collection": {
    "body_html": null,
    "handle": "macbooks",
    "id": 1063001314,
    "published_at": null,
    "published_scope": "global",
    "sort_order": "alpha-asc",
    "template_suffix": null,
    "title": "Macbooks",
    "updated_at": "2021-03-28T13:27:38-04:00Z"
  }
}

```

### Update a custom collection [​](https://docs.haravan.com/docs/omni-apis/custom-collections/\#update-a-custom-collection "Direct link to heading")

PUT

https://apis.haravan.com/com/custom\_collections/{custom\_collection\_id}.json

Change the description of a custom collection.

- PUT `https://apis.haravan.com/com/custom_collections/841564295.json`

```codeBlockLines_e6Vv
{
  "custom_collection": {
    "id": 841564295,
    "body_html": "5000 songs in your pocket"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 Ok
{
  "custom_collection": {
    "body_html": "5000 songs in your pocket",
    "handle": "ipods",
    "id": 841564295,
    "published_at": "2021-02-01T19:00:00-05:00Z",
    "published_scope": "global",
    "sort_order": "manual",
    "template_suffix": null,
    "title": "IPods",
    "updated_at": "2021-03-28T13:27:40-04:00Z",
    "image": null
  }
}

```

Add a collect to an existing collection and update the sort value of the existing collect.

- PUT `https://apis.haravan.com/com/custom_collections/841564295.json`

```codeBlockLines_e6Vv
{
    "custom_collection": {
        "collects": [\
            {\
                "product_id": 1032861656,\
                "sort_value": "0000000001"\
            }\
        ]
    }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 Ok
{
    "custom_collection": {
        "body_html": null,
        "handle": "onsale",
        "image": null,
        "id": 1002326115,
        "published": true,
        "published_at": "2020-09-18T04:10:31.961Z",
        "published_scope": "web",
        "sort_order": "alpha_asc",
        "template_suffix": "collection",
        "title": "Sản phẩm khuyến mãi",
        "updated_at": "2021-08-17T09:07:51.6120872Z",
        "products_count": 2
    }
}

```

### Delete a custom collection [​](https://docs.haravan.com/docs/omni-apis/custom-collections/\#delete-a-custom-collection "Direct link to heading")

DELETE

https://apis.haravan.com/com/custom\_collections/{custom\_collection\_id}.json

Delete a collection.

- DELETE `https://apis.haravan.com/com/custom_collections/841564295.json`

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
Collect](https://docs.haravan.com/docs/omni-apis/collects/) [Next\\
\\
Product](https://docs.haravan.com/docs/omni-apis/products/)

- [What you can do with Custom Collection](https://docs.haravan.com/docs/omni-apis/custom-collections/#what-you-can-do-with-custom-collection)
- [Properties](https://docs.haravan.com/docs/omni-apis/custom-collections/#properties)
- [Retrieves a list of custom collections](https://docs.haravan.com/docs/omni-apis/custom-collections/#retrieves-a-list-of-custom-collections)
- [Parameters](https://docs.haravan.com/docs/omni-apis/custom-collections/#parameters)
- [Retrieves a count of custom collections](https://docs.haravan.com/docs/omni-apis/custom-collections/#retrieves-a-count-of-custom-collections)
- [Retrieves detail a custom collection](https://docs.haravan.com/docs/omni-apis/custom-collections/#retrieves-detail-a-custom-collection)
- [Create a custom collection](https://docs.haravan.com/docs/omni-apis/custom-collections/#create-a-custom-collection)
- [Update a custom collection](https://docs.haravan.com/docs/omni-apis/custom-collections/#update-a-custom-collection)
- [Delete a custom collection](https://docs.haravan.com/docs/omni-apis/custom-collections/#delete-a-custom-collection)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.