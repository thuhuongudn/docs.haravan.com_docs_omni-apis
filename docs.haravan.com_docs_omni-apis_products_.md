---
url: "https://docs.haravan.com/docs/omni-apis/products/"
title: "Product | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/products/#)

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
- Product

On this page

# Product

`Version: 1.0`

The Product resource lets you update and create products in a merchant's store. You can use product variants with the Product resource to create or update different versions of the same product. You can also add or update [Product Images](https://docs.haravan.com/docs/omni-apis/product-images/).

You can add products to collections with the CustomCollection resource and the SmartCollection resource.

**Authenticated access scopes**: `com.read_products`, `com.write_products`

### What you can do with Product [​](https://docs.haravan.com/docs/omni-apis/products/\#what-you-can-do-with-product "Direct link to heading")

The Haravan API lets you do the following with the Product resource.

- GET `https://apis.haravan.com/com/products.json`
  - **[Retrieves a list of products](https://docs.haravan.com/docs/omni-apis/products/#retrieves-a-list-of-products)**
- GET `https://apis.haravan.com/com/products/count.json`
  - **[Retrieve a count of the products](https://docs.haravan.com/docs/omni-apis/products/#retrieve-a-count-of-the-products)**
- GET `https://apis.haravan.com/com/products/{product_id}.json`
  - **[Retrieves single the product](https://docs.haravan.com/docs/omni-apis/products/#retrieves-single-the-product)**
- POST `https://apis.haravan.com/com/products.json`
  - **[Create a product](https://docs.haravan.com/docs/omni-apis/products/#create-a-product)**
- PUT `https://apis.haravan.com/com/products/{product_id}.json`
  - **[Update a product](https://docs.haravan.com/docs/omni-apis/products/#update-a-product)**
- DELETE `https://apis.haravan.com/com/products/{product_id}.json`
  - **[Delete a product](https://docs.haravan.com/docs/omni-apis/products/#delete-a-product)**
- POST `https://apis.haravan.com/com/products/{product_id}/tags.json`
  - **[Add product tags to existing tags](https://docs.haravan.com/docs/omni-apis/products/#add-product-tags-to-existing-tags)**
- DELETE `https://apis.haravan.com/com/products/{product_id}/tags.json`
  - **[Remove tags in existing tags](https://docs.haravan.com/docs/omni-apis/products/#remove-tags-in-existing-tags)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/products/\#properties "Direct link to heading")

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id": 632910392

```

An unsigned 64-bit integer that's used as a unique identifier for the product. Each id is unique across the Haravan system. No two products will have the same id, even if they're from different shops.

`created_at` : `string`

```codeBlockLines_e6Vv
"created_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the product was created.

`updated_at` : `string`

```codeBlockLines_e6Vv
"updated_at":"2021-05-13T07:29:20.808Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the product was last updated.

`published_at` : `string`

```codeBlockLines_e6Vv
"published_at":"2021-05-13T07:29:20.808Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the product was published. Can be set to null to unpublish the product from the Online Store channel.

`published_scope` : `string`

```codeBlockLines_e6Vv
"published_scope": "global"

```

Whether the product is published to the Point of Sale channel.

- **web :** The product is published to the Online Store channel but not published to the Point of Sale channel.
- **pos :** The product is published to the Point of Sale channel but not published to the Online Store channel.
- **global :** The product is published to both the Online Store channel and the Point of Sale channel.

`handle` : `string`

```codeBlockLines_e6Vv
"handle": "iPod-nano"

```

A unique human-friendly string for the product. Automatically generated from the product's title. Used by the Liquid templating language to refer to objects.

`product_type` : `string`

```codeBlockLines_e6Vv
"product_type": "Cult Products"

```

A categorization for the product is used for filtering and searching products.

`images` : `array`

```codeBlockLines_e6Vv
"images": [\
  {\
    "created_at": "2020-09-18T04:12:09.577",\
    "id": 1164472706,\
    "position": 1,\
    "product_id": 1028183686,\
    "src": "https://example.com/burton.jpg",\
    "updated_at": "2020-09-18T04:12:09.577",\
    "filename": "burton.jpg",\
    "variant_ids": [],\
  }\
]

```

- **created\_at :** The date and time when the product image was created.
- **id :** A unique numeric identifier for the product image.
- **position :** The order of the product image in the list. The first product image is at position 1 and is the "main" image for the product.
- **product\_id :** The id of the product associated with the image.
- **variant\_ids :** An array of variant ids associated with the image.
- **src :** Specifies the location of the product image.
- **filename :** Filename of the product image.

`tags` : `string`

```codeBlockLines_e6Vv
"tags": "Emotive, Flash Memory, MP3, Music"

```

A string of comma-separated tags that are used for filtering and search. A product can have up to 250 tags. Each tag can have up to 255 characters.

`template_suffix` : `string`

```codeBlockLines_e6Vv
"template_suffix": "special"

```

The suffix of the Liquid template used for the product page. If this property is specified, then the product page uses a template called "product.suffix.liquid", where "suffix" is the value of this property. If this property is " " or null, then the product page uses the default template "product.liquid". (default: null).

`title` : `string`

```codeBlockLines_e6Vv
"title": "iPod Nano - 8GB"

```

The name of the product.

`vendor` : `string`

```codeBlockLines_e6Vv
"vendor": "Apple"

```

The name of the product's vendor.

`variants` : `array`

```codeBlockLines_e6Vv
"variants": [\
    {\
        "barcode": "AO551",\
        "compare_at_price": 800000.0000,\
        "created_at": "2020-09-18T04:12:09.577Z",\
        "fulfillment_service": null,\
        "grams": 10.0000,\
        "id": 1061514767,\
        "inventory_management": "haravan",\
        "inventory_policy": "deny",\
        "inventory_quantity": 23,\
        "position": 1,\
        "price": 600000.0000,\
        "product_id": 1028183686,\
        "requires_shipping": true,\
        "sku": "AO551",\
        "taxable": true,\
        "title": "Đen / S",\
        "updated_at": "2021-11-26T06:23:12.986Z",\
        "image_id": 1164472706,\
        "option1": "Đen",\
        "option2": "S",\
        "option3": null,\
        "inventory_advance": {\
            "qty_available": 23,\
            "qty_onhand": 47,\
            "qty_commited": 24,\
            "qty_incoming": 0\
        }\
    }\
]

```

An array of [product variants](https://docs.haravan.com/docs/omni-apis/product-variants/), each representing a different version of the product. The position property is read-only. The position of variants is indicated by the order in which they are listed.

`only_hide_from_list` : `boolean`

```codeBlockLines_e6Vv
"only_hide_from_list": true

```

Hide this product in pages search and listing.

`not_allow_promotion` : `boolean`

```codeBlockLines_e6Vv
"not_allow_promotion": true

```

Promotion and coupons are not applicable for this product.

`options` : `array`

```codeBlockLines_e6Vv
"options": [\
    {\
        "name": "Size",\
        "id": 2420902356,\
        "position": 1,\
        "product_id": 1032859333\
    }\
]

```

The custom product properties. For example, Size, Color, and Material. Each product can have up to 3 options and each option value can be up to 255 characters. Product variants are made of up combinations of option values. Options cannot be created without values. To create new options, a variant with an associated option value also needs to be created.

### Retrieves a list of products [​](https://docs.haravan.com/docs/omni-apis/products/\#retrieves-a-list-of-products "Direct link to heading")

GET

https://apis.haravan.com/com/products.json

Retrieves a list of products. You can filter resources by params.

### Parameters [​](https://docs.haravan.com/docs/omni-apis/products/\#parameters "Direct link to heading")

* * *

`ids`

A comma-separated list of product ids.

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

`vendor`

Filter result by the product vendor.

* * *

`handle`

Filter result by the product handle.

* * *

`product_type`

Filter result by the product type.

* * *

`collection_id`

Filter result by the collection id.

* * *

`sku`

Filter result by the variant sku.

* * *

`barcode`

Filter result by the variant barcode.

* * *

`created_at_min`

Show products created after the date (format: 2008-12-31T02:01:27.483Z).

* * *

`created_at_max`

Show products created before date (format: 2008-12-31T02:01:27.483Z).

* * *

`updated_at_min`

Show products last updated after date (format: 2008-12-31T02:01:27.483Z).

* * *

`updated_at_max`

Show products last updated before date (format: 2008-12-31T02:01:27.483Z).

* * *

`published_at_min`

Show products published after the date (format: 2008-12-31T02:01:27.483Z).

* * *

`published_at_max`

Show products published before date (format: 2008-12-31T02:01:27.483Z).

* * *

`fields`

Comma-separated list of fields to include in the response.

* * *

Retrieve all products by page number. By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/com/products.json?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "products": [\
        {\
            "body_html": "Chất vải: Thun Cotton",\
            "body_plain": null,\
            "created_at": "2020-10-22T03:37:03.058Z",\
            "handle": "vay-quay-dai",\
            "id": 1028655526,\
            "images": [\
                {\
                    "created_at": "2020-10-22T03:37:03.058",\
                    "id": 1169154560,\
                    "position": 1,\
                    "product_id": 1028655526,\
                    "src": "https://product.hstatic.net/200000244883/product/nu-7_1d372396a90344edae573a36e40a16d2_52f954b5b29f45b78efdc79540db1cb7_4b75995326454a3a8eb9d5b571d78b81.jpg",\
                    "updated_at": "2020-10-22T03:37:03.058",\
                    "filename": "nu-7_1d372396a90344edae573a36e40a16d2_52f954b5b29f45b78efdc79540db1cb7_4b75995326454a3a8eb9d5b571d78b81.jpg",\
                    "variant_ids": [\
                        1063014645\
                    ]\
                },\
                {\
                    "created_at": "2020-10-22T03:37:03.058",\
                    "id": 1169154575,\
                    "position": 7,\
                    "product_id": 1028655526,\
                    "src": "https://product.hstatic.net/200000244883/product/-7-8_98039f12edbe4ffcbab183935b58b9f2_a6072a8e86c246eaaa20c672a24b615c_9652be441fa34dfcbc09df796779ca21.jpg",\
                    "updated_at": "2020-10-22T03:37:03.058",\
                    "filename": "-7-8_98039f12edbe4ffcbab183935b58b9f2_a6072a8e86c246eaaa20c672a24b615c_9652be441fa34dfcbc09df796779ca21.jpg",\
                    "variant_ids": []\
                }\
            ],\
            "product_type": "Khác",\
            "published_at": "2020-10-22T03:37:00.905Z",\
            "published_scope": "global",\
            "tags": null,\
            "template_suffix": "product",\
            "title": "Váy Quây dài",\
            "updated_at": "2020-10-22T03:37:08.195Z",\
            "variants": [\
                {\
                    "barcode": null,\
                    "compare_at_price": 800000.0000,\
                    "created_at": "2020-10-22T03:37:03.058Z",\
                    "fulfillment_service": null,\
                    "grams": 0.0000,\
                    "id": 1063014645,\
                    "inventory_management": null,\
                    "inventory_policy": "deny",\
                    "inventory_quantity": 0,\
                    "position": 1,\
                    "price": 600000.0000,\
                    "product_id": 1028655526,\
                    "requires_shipping": true,\
                    "sku": "AO551",\
                    "taxable": true,\
                    "title": "Đen / S",\
                    "updated_at": "2020-10-22T03:37:03.121Z",\
                    "image_id": 1169154560,\
                    "option1": "Đen",\
                    "option2": "S",\
                    "option3": null,\
                    "inventory_advance": null\
                },\
                {\
                    "barcode": null,\
                    "compare_at_price": 800000.0000,\
                    "created_at": "2020-10-22T03:37:03.058Z",\
                    "fulfillment_service": null,\
                    "grams": 0.0000,\
                    "id": 1063014647,\
                    "inventory_management": null,\
                    "inventory_policy": "deny",\
                    "inventory_quantity": 0,\
                    "position": 2,\
                    "price": 600000.0000,\
                    "product_id": 1028655526,\
                    "requires_shipping": true,\
                    "sku": "AO552",\
                    "taxable": true,\
                    "title": "Đen / M",\
                    "updated_at": "2020-10-22T03:37:03.121Z",\
                    "image_id": 1169154564,\
                    "option1": "Đen",\
                    "option2": "M",\
                    "option3": null,\
                    "inventory_advance": null\
                }\
            ],\
            "vendor": "Khác",\
            "options": [\
                {\
                    "name": "Color",\
                    "id": 2353555090,\
                    "position": 1,\
                    "product_id": 1028655526\
                },\
                {\
                    "name": "Size",\
                    "id": 2353555091,\
                    "position": 2,\
                    "product_id": 1028655526\
                }\
            ],\
            "only_hide_from_list": false,\
            "not_allow_promotion": false\
        }\
    ]
}

```

Retrieve a list of specific products.

- GET `https://apis.haravan.com/com/products.json?ids=1033237384,1033237559`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK
{
    "products": [\
        {\
            "body_html": "\
Tai nghe Bluetooth True Wireless Mozard DT920 Đen giá rẻ, chính hãng, âm thanh chất lượng cao. Giao hàng tận nơi.",\
            "body_plain": null,\
            "created_at": "2021-05-20T14:40:14.648Z",\
            "handle": "tai-nghe-bluetooth-true-wireless-mozard-dt920-den",\
            "id": 1033237384,\
            "images": [\
                {\
                    "created_at": "2021-05-20T14:40:14.648",\
                    "id": 1196228927,\
                    "position": 1,\
                    "product_id": 1033237384,\
                    "src": "https://product.hstatic.net/200000219339/product/tai-nghe-bluetooth-true-wireless-mozard-dt920-den-1-org_b2e65f00bb80419a8d18d5da6057c5fe.jpg",\
                    "updated_at": "2021-05-20T14:40:14.648",\
                    "filename": "tai-nghe-bluetooth-true-wireless-mozard-dt920-den-1-org_b2e65f00bb80419a8d18d5da6057c5fe.jpg",\
                    "variant_ids": [\
                        1073120878\
                    ]\
                }\
            ],\
            "product_type": "Khác",\
            "published_at": "2021-05-20T14:40:11.148Z",\
            "published_scope": "global",\
            "tags": "dienmayxanh",\
            "template_suffix": "product",\
            "title": "Tai nghe Bluetooth True Wireless Mozard DT920 Đen",\
            "updated_at": "2021-05-20T14:40:15.838Z",\
            "variants": [\
                {\
                    "barcode": null,\
                    "compare_at_price": 0.0000,\
                    "created_at": "2021-05-20T14:40:14.648Z",\
                    "fulfillment_service": null,\
                    "grams": 0.0000,\
                    "id": 1073120878,\
                    "inventory_management": null,\
                    "inventory_policy": "deny",\
                    "inventory_quantity": 0,\
                    "position": 1,\
                    "price": 950000.0000,\
                    "product_id": 1033237384,\
                    "requires_shipping": false,\
                    "sku": null,\
                    "taxable": false,\
                    "title": "Tai nghe Bluetooth True Wireless Mozard DT920 Đen",\
                    "updated_at": "2021-05-20T14:40:15.838Z",\
                    "image_id": 1196228927,\
                    "option1": "Tai nghe Bluetooth True Wireless Mozard DT920 Đen",\
                    "option2": null,\
                    "option3": null,\
                    "inventory_advance": null\
                }\
            ],\
            "vendor": "Khác",\
            "options": [\
                {\
                    "name": "Title",\
                    "id": 2427727973,\
                    "position": 1,\
                    "product_id": 1033237384\
                }\
            ],\
            "only_hide_from_list": false,\
            "not_allow_promotion": false\
        },\
        {\
            "body_html": "\
Điện thoại Samsung Galaxy S21 | Cập nhật thông tin ra mắt, hình ảnh, cấu hình và đánh giá chi tiết nhanh và chính xác. Giải đáp thắc mắc khách hàng ngay tại đây. Click ngay\
",\
\
            "body_plain": null,\
            "created_at": "2021-05-20T14:46:44.959Z",\
            "handle": "dien-thoai-samsung-galaxy-s21-5g-7",\
            "id": 1033237559,\
            "images": [\
                {\
                    "created_at": "2021-05-20T14:46:44.961",\
                    "id": 1196230403,\
                    "position": 19,\
                    "product_id": 1033237559,\
                    "src": "https://product.hstatic.net/200000219339/product/samsung-galaxy-s21-trang-3-org_4e66226f3c3b4974b825feee1638aff2.jpg",\
                    "updated_at": "2021-05-20T14:46:44.961",\
                    "filename": "samsung-galaxy-s21-trang-3-org_4e66226f3c3b4974b825feee1638aff2.jpg",\
                    "variant_ids": []\
                }\
            ],\
            "product_type": "Khác",\
            "published_at": "2021-05-20T14:45:16.835Z",\
            "published_scope": "global",\
            "tags": "thegioididong",\
            "template_suffix": "product",\
            "title": "Điện thoại Samsung Galaxy S21 5G",\
            "updated_at": "2021-05-20T14:46:44.959Z",\
            "variants": [\
                {\
                    "barcode": null,\
                    "compare_at_price": 20990000.0000,\
                    "created_at": "2021-05-20T14:46:44.959Z",\
                    "fulfillment_service": null,\
                    "grams": 0.0000,\
                    "id": 1073121320,\
                    "inventory_management": null,\
                    "inventory_policy": "deny",\
                    "inventory_quantity": 0,\
                    "position": 1,\
                    "price": 18990000.0000,\
                    "product_id": 1033237559,\
                    "requires_shipping": false,\
                    "sku": null,\
                    "taxable": false,\
                    "title": "Tím",\
                    "updated_at": "2021-05-20T14:46:44.959Z",\
                    "image_id": null,\
                    "option1": "Tím",\
                    "option2": null,\
                    "option3": null,\
                    "inventory_advance": null\
                },\
                {\
                    "barcode": null,\
                    "compare_at_price": 20990000.0000,\
                    "created_at": "2021-05-20T14:46:44.959Z",\
                    "fulfillment_service": null,\
                    "grams": 0.0000,\
                    "id": 1073121321,\
                    "inventory_management": null,\
                    "inventory_policy": "deny",\
                    "inventory_quantity": 0,\
                    "position": 2,\
                    "price": 18990000.0000,\
                    "product_id": 1033237559,\
                    "requires_shipping": false,\
                    "sku": null,\
                    "taxable": false,\
                    "title": "Trắng",\
                    "updated_at": "2021-05-20T14:46:44.959Z",\
                    "image_id": null,\
                    "option1": "Trắng",\
                    "option2": null,\
                    "option3": null,\
                    "inventory_advance": null\
                }\
            ],\
            "vendor": "Khác",\
            "options": [\
                {\
                    "name": "Title",\
                    "id": 2427730881,\
                    "position": 1,\
                    "product_id": 1033237559\
                }\
            ],\
            "only_hide_from_list": false,\
            "not_allow_promotion": false\
        }\
    ]
}

```

### Retrieve a count of the products [​](https://docs.haravan.com/docs/omni-apis/products/\#retrieve-a-count-of-the-products "Direct link to heading")

GET

https://apis.haravan.com/com/products/count.json

Retrieve the count of resources of the products.

- GET `https://apis.haravan.com/com/products/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 2
}

```

### Retrieves single the product [​](https://docs.haravan.com/docs/omni-apis/products/\#retrieves-single-the-product "Direct link to heading")

GET

https://apis.haravan.com/com/products/{product\_id}.json

Retrieves single the product by ID.

- GET `https://apis.haravan.com/com/products/1033237559.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "product": {
        "body_html": "<p>Điện thoại Samsung Galaxy S21 | Cập nhật thông tin ra mắt, hình ảnh, cấu hình và đánh giá chi tiết nhanh và chính xác. Giải đáp thắc mắc khách hàng ngay tại đây. Click ngay</p>",
        "body_plain": null,
        "created_at": "2021-05-20T14:46:44.959Z",
        "handle": "dien-thoai-samsung-galaxy-s21-5g-7",
        "id": 1033237559,
        "images": [\
            {\
                "created_at": "2021-05-20T14:46:44.961",\
                "id": 1196230403,\
                "position": 19,\
                "product_id": 1033237559,\
                "src": "https://product.hstatic.net/200000219339/product/samsung-galaxy-s21-trang-3-org_4e66226f3c3b4974b825feee1638aff2.jpg",\
                "updated_at": "2021-05-20T14:46:44.961",\
                "filename": "samsung-galaxy-s21-trang-3-org_4e66226f3c3b4974b825feee1638aff2.jpg",\
                "variant_ids": []\
            }\
        ],
        "product_type": "Khác",
        "published_at": "2021-05-20T14:45:16.835Z",
        "published_scope": "global",
        "tags": "thegioididong",
        "template_suffix": "product",
        "title": "Điện thoại Samsung Galaxy S21 5G",
        "updated_at": "2021-05-20T14:46:44.959Z",
        "variants": [\
            {\
                "barcode": null,\
                "compare_at_price": 20990000.0000,\
                "created_at": "2021-05-20T14:46:44.959Z",\
                "fulfillment_service": null,\
                "grams": 0.0000,\
                "id": 1073121320,\
                "inventory_management": null,\
                "inventory_policy": "deny",\
                "inventory_quantity": 0,\
                "position": 1,\
                "price": 18990000.0000,\
                "product_id": 1033237559,\
                "requires_shipping": false,\
                "sku": null,\
                "taxable": false,\
                "title": "Tím",\
                "updated_at": "2021-05-20T14:46:44.959Z",\
                "image_id": null,\
                "option1": "Tím",\
                "option2": null,\
                "option3": null,\
                "inventory_advance": null\
            },\
            {\
                "barcode": null,\
                "compare_at_price": 20990000.0000,\
                "created_at": "2021-05-20T14:46:44.959Z",\
                "fulfillment_service": null,\
                "grams": 0.0000,\
                "id": 1073121321,\
                "inventory_management": null,\
                "inventory_policy": "deny",\
                "inventory_quantity": 0,\
                "position": 2,\
                "price": 18990000.0000,\
                "product_id": 1033237559,\
                "requires_shipping": false,\
                "sku": null,\
                "taxable": false,\
                "title": "Trắng",\
                "updated_at": "2021-05-20T14:46:44.959Z",\
                "image_id": null,\
                "option1": "Trắng",\
                "option2": null,\
                "option3": null,\
                "inventory_advance": null\
            },\
            {\
                "barcode": null,\
                "compare_at_price": 20990000.0000,\
                "created_at": "2021-05-20T14:46:44.959Z",\
                "fulfillment_service": null,\
                "grams": 0.0000,\
                "id": 1073121322,\
                "inventory_management": null,\
                "inventory_policy": "deny",\
                "inventory_quantity": 0,\
                "position": 3,\
                "price": 18990000.0000,\
                "product_id": 1033237559,\
                "requires_shipping": false,\
                "sku": null,\
                "taxable": false,\
                "title": "Xám",\
                "updated_at": "2021-05-20T14:46:44.959Z",\
                "image_id": null,\
                "option1": "Xám",\
                "option2": null,\
                "option3": null,\
                "inventory_advance": null\
            }\
        ],
        "vendor": "Khác",
        "options": [\
            {\
                "name": "Title",\
                "id": 2427730881,\
                "position": 1,\
                "product_id": 1033237559\
            }\
        ],
        "only_hide_from_list": false,
        "not_allow_promotion": false
    }
}

```

### Create a product [​](https://docs.haravan.com/docs/omni-apis/products/\#create-a-product "Direct link to heading")

POST

https://apis.haravan.com/com/products.json

Create a new product.

- POST `https://apis.haravan.com/com/products.json`

```codeBlockLines_e6Vv
{
    "product": {
        "title": "Burton Custom Freestyle 151",
        "body_html": "Good snowboard!",
        "vendor": "Burton",
        "product_type": "Snowboard",
        "tags": "Barnes & Noble,John's Fav,Big Air"
    }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
    "product": {
        "body_html": "Good snowboard!",
        "body_plain": null,
        "created_at": "2021-05-21T04:44:19.167Z",
        "handle": "burton-custom-freestyle-152",
        "id": 1033252767,
        "images": [],
        "product_type": "Snowboard",
        "published_at": "2021-05-21T04:44:19.142Z",
        "published_scope": "global",
        "tags": "Barnes & Noble,John's Fav,Big Air",
        "template_suffix": "product",
        "title": "Burton Custom Freestyle 151",
        "updated_at": "2021-05-21T04:44:19.167Z",
        "variants": [\
            {\
                "barcode": null,\
                "compare_at_price": 0.0000,\
                "created_at": "2021-05-21T04:44:19.167Z",\
                "fulfillment_service": null,\
                "grams": 0.0000,\
                "id": 1073164443,\
                "inventory_management": null,\
                "inventory_policy": "deny",\
                "inventory_quantity": 0,\
                "old_inventory_quantity": 0,\
                "inventory_quantity_adjustment": null,\
                "position": 1,\
                "price": 0.0000,\
                "product_id": 1033252767,\
                "requires_shipping": false,\
                "sku": null,\
                "taxable": false,\
                "title": "Default Title",\
                "updated_at": "2021-05-21T04:44:19.167Z",\
                "image_id": null,\
                "option1": "Default Title",\
                "option2": null,\
                "option3": null,\
                "inventory_advance": null\
            }\
        ],
        "vendor": "Burton",
        "options": [\
            {\
                "name": "Title",\
                "id": 2428053567,\
                "position": 1,\
                "product_id": 1033252767\
            }\
        ],
        "only_hide_from_list": false,
        "not_allow_promotion": false
    }
}

```

Create a new unpublished product.

- POST `https://apis.haravan.com/com/products.json`

```codeBlockLines_e6Vv
{
    "product": {
        "title": "Burton Custom Freestyle 151",
        "body_html": "Good snowboard!",
        "vendor": "Burton",
        "product_type": "Snowboard",
        "published": false
    }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
    "product": {
        "body_html": "Good snowboard!",
        "body_plain": null,
        "created_at": "2021-05-21T04:42:33.169Z",
        "handle": "burton-custom-freestyle-151",
        "id": 1033252740,
        "images": [],
        "product_type": "Snowboard",
        "published_at": null,
        "published_scope": "pos",
        "tags": null,
        "template_suffix": "product",
        "title": "Burton Custom Freestyle 151",
        "updated_at": "2021-05-21T04:42:33.169Z",
        "variants": [\
            {\
                "barcode": null,\
                "compare_at_price": 0.0000,\
                "created_at": "2021-05-21T04:42:33.169Z",\
                "fulfillment_service": null,\
                "grams": 0.0000,\
                "id": 1073164408,\
                "inventory_management": null,\
                "inventory_policy": "deny",\
                "inventory_quantity": 0,\
                "old_inventory_quantity": 0,\
                "inventory_quantity_adjustment": null,\
                "position": 1,\
                "price": 0.0000,\
                "product_id": 1033252740,\
                "requires_shipping": false,\
                "sku": null,\
                "taxable": false,\
                "title": "Default Title",\
                "updated_at": "2021-05-21T04:42:33.169Z",\
                "image_id": null,\
                "option1": "Default Title",\
                "option2": null,\
                "option3": null,\
                "inventory_advance": null\
            }\
        ],
        "vendor": "Burton",
        "options": [\
            {\
                "name": "Title",\
                "id": 2428052973,\
                "position": 1,\
                "product_id": 1033252740\
            }\
        ],
        "only_hide_from_list": false,
        "not_allow_promotion": false
    }
}

```

Create a new product with the default variant.

- POST `https://apis.haravan.com/com/products.json`

```codeBlockLines_e6Vv
{
    "product": {
        "title": "Burton Custom Freestyle 151",
        "body_html": "Good snowboard!",
        "vendor": "Burton",
        "product_type": "Snowboard"
    }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
    "product": {
        "body_html": "Good snowboard!",
        "body_plain": null,
        "created_at": "2021-08-02T06:59:23.636Z",
        "handle": "burton-custom-freestlye-151",
        "id": 1034911641,
        "images": [],
        "product_type": "Snowboard",
        "published_at": "2021-08-02T06:59:23.551Z",
        "published_scope": "global",
        "tags": null,
        "template_suffix": "product",
        "title": "Burton Custom Freestlye 151",
        "updated_at": "2021-08-02T06:59:23.636Z",
        "variants": [\
            {\
                "barcode": null,\
                "compare_at_price": 0.0000,\
                "created_at": "2021-08-02T06:59:23.636Z",\
                "fulfillment_service": null,\
                "grams": 0.0000,\
                "id": 1076771382,\
                "inventory_management": null,\
                "inventory_policy": "deny",\
                "inventory_quantity": 0,\
                "old_inventory_quantity": 0,\
                "inventory_quantity_adjustment": null,\
                "position": 1,\
                "price": 0.0000,\
                "product_id": 1034911641,\
                "requires_shipping": false,\
                "sku": null,\
                "taxable": false,\
                "title": "Default Title",\
                "updated_at": "2021-08-02T06:59:23.636Z",\
                "image_id": null,\
                "option1": "Default Title",\
                "option2": null,\
                "option3": null,\
                "inventory_advance": null\
            }\
        ],
        "vendor": "Burton",
        "options": [\
            {\
                "name": "Title",\
                "id": 2457329780,\
                "position": 1,\
                "product_id": 1034911641\
            }\
        ],
        "only_hide_from_list": false,
        "not_allow_promotion": false
    }
}

```

Create a new product with multiple product variants.

- POST `https://apis.haravan.com/com/products.json`

```codeBlockLines_e6Vv
{
  "product": {
    "title": "Burton Custom Freestyle 151",
    "body_html": "Good snowboard!",
    "vendor": "Burton",
    "product_type": "Snowboard",
    "variants": [\
      {\
        "option1": "First",\
        "option2": "S",\
        "price": 1000000,\
        "sku": "123",\
        "barcode": "456",\
        "barcode": "456",\
        "lot_support":true,\
        "variant_units": [\
            {\
                "id":0,\
                "unit":"cái",\
                "base":true,\
                "sellable":true,\
                "ratio":1,\
                "barcode":"456",\
                "sku":"123",\
                "price":1000000,\
            },\
            {\
                "id":0,\
                "unit":"lốc",\
                "base":false,\
                "sellable":true,\
                "ratio":5,\
                "barcode":"sp-01",\
                "sku":"sp-01",\
                "price":5000000,\
            }\
        ]\
      },\
      {\
        "option1": "Second",\
        "option2": "XL",\
        "price": 2000000,\
        "sku": "123",\
        "barcode": "456"\
      }\
    ],
    "options": [\
      {\
        "name": "Title",\
        "position": 1\
      },\
      {\
        "name": "Size",\
        "position": 2\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
    "product": {
        "body_html": "Good snowboard!",
        "body_plain": null,
        "created_at": "2022-07-25T03:40:30.681Z",
        "handle": "burton-custom-freestyle-156",
        "id": 1041000208,
        "images": [],
        "product_type": "Snowboard",
        "published_at": "2022-07-25T03:40:30.658Z",
        "published_scope": "global",
        "tags": null,
        "template_suffix": "product",
        "title": "Burton Custom Freestyle 151",
        "updated_at": "2022-07-25T03:40:30.681Z",
        "variants": [\
            {\
                "barcode": "456",\
                "compare_at_price": 0.0,\
                "created_at": "2022-07-25T03:40:30.681Z",\
                "fulfillment_service": null,\
                "grams": 0.0,\
                "id": 1089417357,\
                "inventory_management": null,\
                "inventory_policy": "deny",\
                "inventory_quantity": 0,\
                "old_inventory_quantity": 0,\
                "inventory_quantity_adjustment": null,\
                "position": 1,\
                "price": 1000000.0,\
                "product_id": 1041000208,\
                "requires_shipping": false,\
                "sku": "123",\
                "taxable": false,\
                "title": "First / S",\
                "updated_at": "2022-07-25T03:40:30.681Z",\
                "image_id": null,\
                "option1": "First",\
                "option2": "S",\
                "option3": null,\
                "inventory_advance": null,\
                "lot_support":true,\
                "variant_units": [\
                    {\
                        "id":1000000001,\
                        "unit":"cái",\
                        "base":true,\
                        "sellable":true,\
                        "ratio":1,\
                        "barcode":"456",\
                        "sku":"123",\
                        "price":1000000,\
                    },\
                    {\
                        "id":1000000002,\
                        "unit":"lốc",\
                        "base":false,\
                        "sellable":true,\
                        "ratio":5,\
                        "barcode":"sp-01",\
                        "sku":"sp-01",\
                        "price":5000000,\
                    }\
                ]\
            },\
            {\
                "barcode": "456",\
                "compare_at_price": 0.0,\
                "created_at": "2022-07-25T03:40:30.681Z",\
                "fulfillment_service": null,\
                "grams": 0.0,\
                "id": 1089417358,\
                "inventory_management": null,\
                "inventory_policy": "deny",\
                "inventory_quantity": 0,\
                "old_inventory_quantity": 0,\
                "inventory_quantity_adjustment": null,\
                "position": 2,\
                "price": 2000000.0,\
                "product_id": 1041000208,\
                "requires_shipping": false,\
                "sku": "123",\
                "taxable": false,\
                "title": "Second / XL",\
                "updated_at": "2022-07-25T03:40:30.681Z",\
                "image_id": null,\
                "option1": "Second",\
                "option2": "XL",\
                "option3": null,\
                "inventory_advance": null\
            }\
        ],
        "vendor": "Burton",
        "options": [\
            {\
                "name": "Title",\
                "id": 2659871688,\
                "position": 1,\
                "product_id": 1041000208\
            },\
            {\
                "name": "Size",\
                "id": 2659871689,\
                "position": 2,\
                "product_id": 1041000208\
            }\
        ],
        "only_hide_from_list": false,
        "not_allow_promotion": false
    }
}

```

### Update a product [​](https://docs.haravan.com/docs/omni-apis/products/\#update-a-product "Direct link to heading")

PUT

https://apis.haravan.com/com/products/{product\_id}.json

Update a product's tags.

- PUT `https://apis.haravan.com/com/products/1034911682.json`

```codeBlockLines_e6Vv
{
    "product": {
        "id": 1034911682,
        "tags": "Barnes & Noble, John's Fav"
    }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "product": {
        "body_html": "Good snowboard!",
        "body_plain": null,
        "created_at": "2021-08-02T07:03:50.737Z",
        "handle": "burton-custom-freestyle-151",
        "id": 1034911682,
        "images": [],
        "product_type": "Snowboard",
        "published_at": "2021-08-02T07:03:50.633Z",
        "published_scope": "global",
        "tags": "Barnes & Noble,John's Fav",
        "template_suffix": "product",
        "title": "Burton Custom Freestyle 151",
        "updated_at": "2021-08-02T07:39:24.442Z",
        "variants": [\
            {\
                "barcode": null,\
                "compare_at_price": 0.0000,\
                "created_at": "2021-08-02T07:03:50.737Z",\
                "fulfillment_service": null,\
                "grams": 0.0000,\
                "id": 1076771488,\
                "inventory_management": null,\
                "inventory_policy": "deny",\
                "inventory_quantity": 0,\
                "old_inventory_quantity": 0,\
                "inventory_quantity_adjustment": null,\
                "position": 1,\
                "price": 10.0000,\
                "product_id": 1034911682,\
                "requires_shipping": false,\
                "sku": "123",\
                "taxable": false,\
                "title": "First",\
                "updated_at": "2021-08-02T07:03:50.737Z",\
                "image_id": null,\
                "option1": "First",\
                "option2": null,\
                "option3": null,\
                "inventory_advance": null\
            },\
            {\
                "barcode": null,\
                "compare_at_price": 0.0000,\
                "created_at": "2021-08-02T07:03:50.737Z",\
                "fulfillment_service": null,\
                "grams": 0.0000,\
                "id": 1076771489,\
                "inventory_management": null,\
                "inventory_policy": "deny",\
                "inventory_quantity": 0,\
                "old_inventory_quantity": 0,\
                "inventory_quantity_adjustment": null,\
                "position": 2,\
                "price": 20.0000,\
                "product_id": 1034911682,\
                "requires_shipping": false,\
                "sku": "123",\
                "taxable": false,\
                "title": "Second",\
                "updated_at": "2021-08-02T07:03:50.737Z",\
                "image_id": null,\
                "option1": "Second",\
                "option2": null,\
                "option3": null,\
                "inventory_advance": null\
            }\
        ],
        "vendor": "Burton",
        "options": [\
            {\
                "name": "Title",\
                "id": 2457330565,\
                "position": 1,\
                "product_id": 1034911682\
            }\
        ],
        "only_hide_from_list": false,
        "not_allow_promotion": false
    }
}

```

Update a product's variants.

- PUT `https://apis.haravan.com/com/products/632910392.json`

```codeBlockLines_e6Vv
{
  "product": {
    "id": 1037394594,
    "variants": [\
      {\
        "id": 1081582397,\
        "price": 0,\
        "sku": 456,\
        "barcode": 789,\
        "lot_support":true,\
        "variant_units": [\
            {\
                "id":1000000001,\
                "unit":"cái",\
                "base":true,\
                "sellable":true,\
                "ratio":1,\
                "barcode":"789",\
                "sku":"456",\
                "price":1000000,\
            },\
            {\
                "id":0,\
                "unit":"lốc",\
                "base":false,\
                "sellable":true,\
                "ratio":3,\
                "barcode":"sp-01",\
                "sku":"sp-01",\
                "price":5000000,\
            }\
        ]\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "product": {
        "body_html": "Good snowboard!",
        "body_plain": null,
        "created_at": "2021-05-21T04:48:12.545Z",
        "handle": "burton-custom-freestyle-155",
        "id": 1033252999,
        "images": [\
            {\
                "created_at": "2021-05-21T10:00:09.318",\
                "id": 1194038830,\
                "position": 1,\
                "product_id": 1032859333,\
                "src": "https://product.hstatic.net/product/rails_logo.gif",\
                "updated_at": "2021-05-21T10:00:09.318",\
                "filename": "rails_logo.gif",\
                "variant_ids": []\
            }\
        ],
        "product_type": "Snowboard",
        "published_at": "2021-05-21T04:48:12.46Z",
        "published_scope": "global",
        "tags": "Barnes & Noble,John's Fav",
        "template_suffix": "product",
        "title": "Burton Custom Freestyle 151",
        "updated_at": "2021-05-21T04:52:34.935Z",
        "variants": [\
            {\
                "barcode": null,\
                "compare_at_price": 0.0000,\
                "created_at": "2021-05-21T04:48:12.545Z",\
                "fulfillment_service": null,\
                "grams": 0.0000,\
                "id": 1073164926,\
                "inventory_management": null,\
                "inventory_policy": "deny",\
                "inventory_quantity": 0,\
                "old_inventory_quantity": 0,\
                "inventory_quantity_adjustment": null,\
                "position": 1,\
                "price": 0.0000,\
                "product_id": 1033252999,\
                "requires_shipping": false,\
                "sku": null,\
                "taxable": false,\
                "title": "Default Title",\
                "updated_at": "2021-05-21T04:48:12.545Z",\
                "image_id": null,\
                "option1": "Default Title",\
                "option2": null,\
                "option3": null,\
                "inventory_advance": null,\
                "variant_units": [\
                    {\
                        "id":1000000001,\
                        "unit":"cái",\
                        "base":true,\
                        "sellable":true,\
                        "ratio":1,\
                        "barcode":"789",\
                        "sku":"456",\
                        "price":1000000,\
                    },\
                    {\
                        "id":0,\
                        "unit":"lốc",\
                        "base":false,\
                        "sellable":true,\
                        "ratio":3,\
                        "barcode":"sp-01",\
                        "sku":"sp-01",\
                        "price":5000000,\
                    }\
                ]\
            }\
        ],
        "vendor": "Burton",
        "options": [\
            {\
                "name": "Title",\
                "id": 2428055574,\
                "position": 1,\
                "product_id": 1033252999\
            }\
        ],
        "only_hide_from_list": false,
        "not_allow_promotion": false
    }
}

```

### Delete a product [​](https://docs.haravan.com/docs/omni-apis/products/\#delete-a-product "Direct link to heading")

DELETE

https://apis.haravan.com/com/products/{product\_id}.json

Delete a product along with all its variants and images.

- DELETE `https://apis.haravan.com/com/products/1033252999.json`

```codeBlockLines_e6Vv
{}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

[]

```

### Add product tags to existing tags [​](https://docs.haravan.com/docs/omni-apis/products/\#add-product-tags-to-existing-tags "Direct link to heading")

POST

https://apis.haravan.com/com/products/{product\_id}/tags.json

Add product tags to existing tags.

- POST `https://apis.haravan.com/com/products/1050764416/tags.json`

```codeBlockLines_e6Vv
{
  "tags": "a1,a2"
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
  "tags": "VIP,a1,a2"
}

```

### Remove tags in existing tags [​](https://docs.haravan.com/docs/omni-apis/products/\#remove-tags-in-existing-tags "Direct link to heading")

DELETE

https://apis.haravan.com/com/products/{product\_id}/tags.json

Remove tags in existing tags.

- DELETE [https://apis.haravan.com/com/products/1050764416/tags.json](https://apis.haravan.com/com/products/1050764416/tags.json)

```codeBlockLines_e6Vv
{
  "tags": "a1,a2"
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "tags": "VIP"
}

```

[Previous\\
\\
CustomCollection](https://docs.haravan.com/docs/omni-apis/custom-collections/) [Next\\
\\
Product Image](https://docs.haravan.com/docs/omni-apis/product-images/)

- [What you can do with Product](https://docs.haravan.com/docs/omni-apis/products/#what-you-can-do-with-product)
- [Properties](https://docs.haravan.com/docs/omni-apis/products/#properties)
- [Retrieves a list of products](https://docs.haravan.com/docs/omni-apis/products/#retrieves-a-list-of-products)
- [Parameters](https://docs.haravan.com/docs/omni-apis/products/#parameters)
- [Retrieve a count of the products](https://docs.haravan.com/docs/omni-apis/products/#retrieve-a-count-of-the-products)
- [Retrieves single the product](https://docs.haravan.com/docs/omni-apis/products/#retrieves-single-the-product)
- [Create a product](https://docs.haravan.com/docs/omni-apis/products/#create-a-product)
- [Update a product](https://docs.haravan.com/docs/omni-apis/products/#update-a-product)
- [Delete a product](https://docs.haravan.com/docs/omni-apis/products/#delete-a-product)
- [Add product tags to existing tags](https://docs.haravan.com/docs/omni-apis/products/#add-product-tags-to-existing-tags)
- [Remove tags in existing tags](https://docs.haravan.com/docs/omni-apis/products/#remove-tags-in-existing-tags)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.