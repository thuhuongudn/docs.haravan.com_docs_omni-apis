---
url: "https://docs.haravan.com/docs/omni-apis/product-variants/"
title: "Product Variant | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/product-variants/#)

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
- Product Variant

On this page

# Product Variant

`Version: 1.0`

A product variant is a different version of a product, such as differing sizes or differing colours. Without product variants, you would have to treat the small, medium and large versions of a t-shirt as three separate products; product variants let you treat the small, medium and large versions of a t-shirt as variations of the same product.

Each product can have a maximum of 100 variants.

**Authenticated access scopes**: `com.read_products`, `com.write_products`

### What you can do with Product Variant [​](https://docs.haravan.com/docs/omni-apis/product-variants/\#what-you-can-do-with-product-variant "Direct link to heading")

The Haravan API lets you do the following with the Product Variant resource.

- GET `https://apis.haravan.com/com/products/{product_id}/variants.json`
  - **[Retrieves a list of product variants](https://docs.haravan.com/docs/omni-apis/product-variants/#retrieves-a-list-of-product-variants)**
- GET `https://apis.haravan.com/com/products/{product_id}/count.json`
  - **[Retrieve a count of the product variants](https://docs.haravan.com/docs/omni-apis/product-variants/#retrieve-a-count-of-the-product-variants)**
- GET `https://apis.haravan.com/com/variants/{variant_id}.json`
  - **[Retrieves single the product variant](https://docs.haravan.com/docs/omni-apis/product-variants/#retrieves-single-the-product-variant)**
- POST `https://apis.haravan.com/com/products/{product_id}/variants.json`
  - **[Create a new product variant](https://docs.haravan.com/docs/omni-apis/product-variants/#create-a-new-product-variant)**
- PUT `https://apis.haravan.com/com/variants/{variant_id}.json`
  - **[Update a product variant](https://docs.haravan.com/docs/omni-apis/product-variants/#update-a-product-variant)**
- DELETE `https://apis.haravan.com/com/products/{product_id}/variants/{variant_id}.json`
  - **[Delete a product variant](https://docs.haravan.com/docs/omni-apis/product-variants/#delete-a-product-variant)**

#### Properties [​](https://docs.haravan.com/docs/omni-apis/product-variants/\#properties "Direct link to heading")

* * *

`barcode` : `string`

```codeBlockLines_e6Vv
"barcode": "123_pink"

```

The barcode, UPC or ISBN number for the product.

`compare_at_price` : `number`

```codeBlockLines_e6Vv
"compare_at_price":  0.0000

```

The competitors prices for the same item.

`created_at` : `string`

```codeBlockLines_e6Vv
"created_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the product variant was created.

`fulfillment_service` : `string`

```codeBlockLines_e6Vv
"fulfillment_service": null

```

Service who is doing the fulfillment. Valid values are: null.

`grams` : `number`

```codeBlockLines_e6Vv
"grams": 0.0000

```

The weight of the product variant in grams.

`id` : `number`

```codeBlockLines_e6Vv
"id": 632910392

```

The unique numeric identifier for the product variant.

`inventory_management` : `string`

```codeBlockLines_e6Vv
"inventory_management": "haravan"

```

Specifies whether or not haravan tracks the number of items in stock for this product variant. Valid values are:

- **blank**: haravan does not track the number of items in stock for this product variant.
- **haravan**: haravan does track the number of items in stock for this product variant.

`inventory_policy` : `string`

```codeBlockLines_e6Vv
"inventory_policy": "continue"

```

Specifies whether or not customers are allowed to place an order for a product variant when it's out of stock. Valid values are:

- **deny (default)**: Customers are not allowed to place orders for a product variant when it's out of stock.
- **continue**: Customers are allowed to place orders for a product variant when it's out of stock.

`inventory_quantity` : `number`

```codeBlockLines_e6Vv
"inventory_quantity": 10

```

The number of items in stock for this product variant.

`position` : `number`

```codeBlockLines_e6Vv
"position":1

```

The order of the product variant in the list of product variants. 1 is the first position.

`price` : `number`

```codeBlockLines_e6Vv
"price": 100000.0000

```

The price of the product variant.

`product_id` : `number`

```codeBlockLines_e6Vv
"product_id": 1034037268

```

The unique numeric identifier for the product.

`requires_shipping`: `boolean`

```codeBlockLines_e6Vv
"requires_shipping": true

```

Specifies whether or not a customer needs to provide a shipping address when placing an order for this product variant. Valid values are:

- **true**: Customer needs to supply a shipping address.
- **false**: Customer does not need to supply a shipping address.

`sku` : `string`

```codeBlockLines_e6Vv
"sku":"IPOD2008PINK"

```

A unique identifier for the product in the shop.

`taxable` : `boolean`

```codeBlockLines_e6Vv
"taxable":false

```

Specifies whether or not a tax is charged when the product variant is sole.

`title` : `string`

```codeBlockLines_e6Vv
"title":"pink"

```

The title of the product variant.

`updated_at` : `string`

```codeBlockLines_e6Vv
"updated_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the product variant was updated.

`image_id` : `string`

```codeBlockLines_e6Vv
"image_id":null

```

The unique numeric identifier for one of the product's images.

`option1`: `string`

```codeBlockLines_e6Vv
"option1":size

```

Custom properties that a shop owner can use to define product variants. Multiple options can exist. Options are represented as: option1, option2, option3 etc.

`option2`: `string`

```codeBlockLines_e6Vv
"option2":null

```

Custom properties that a shop owner can use to define product variants. Multiple options can exist. Options are represented as: option1, option2, option3 etc.

`option3`: `string`

```codeBlockLines_e6Vv
"option3":null

```

Custom properties that a shop owner can use to define product variants. Multiple options can exist. Options are represented as: option1, option2, option3 etc.

### Retrieves a list of product variants [​](https://docs.haravan.com/docs/omni-apis/product-variants/\#retrieves-a-list-of-product-variants "Direct link to heading")

GET

https://apis.haravan.com/com/products/{product\_id}/variants.json

Retrieves a list of product variants. You can filter resources by params.

### Parameters [​](https://docs.haravan.com/docs/omni-apis/product-variants/\#parameters "Direct link to heading")

* * *

`ids`

A comma-separated list of product ids

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

`fields`

Comma-separated list of fields to include in the response.

* * *

Retrieve all product variants by page number. By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/com/products/1034037268/variants.json?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "variants": [\
        {\
            "barcode": "CSSWMHRJ",\
            "compare_at_price": 0.0000,\
            "created_at": "2021-06-28T06:15:57.554Z",\
            "fulfillment_service": null,\
            "grams": 0.0000,\
            "id": 1075012798,\
            "inventory_management": "haravan",\
            "inventory_policy": "deny",\
            "inventory_quantity": 0,\
            "position": 0,\
            "price": 9990000.0000,\
            "product_id": 1034037268,\
            "requires_shipping": true,\
            "sku": "CSSWMHRJ",\
            "taxable": false,\
            "title": "Default Title",\
            "updated_at": "2021-08-14T07:50:52.173Z",\
            "image_id": null,\
            "option1": "Size",\
            "option2": null,\
            "option3": null,\
            "inventory_advance": null\
        }\
    ]
}

```

Retrieve a list of specific product variants.

- GET `https://apis.haravan.com/com/products/1034037268/variants.json?fields=sku,title,option1,option2,option3`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK
{
    "variants": [\
        {\
            "id": 1075012798,\
            "sku": "CSSWMHRJ",\
            "title": "Default Title",\
            "option1": "Default Title",\
            "option2": null,\
            "option3": null\
        }\
    ]
}

```

### Retrieve a count of the product variants [​](https://docs.haravan.com/docs/omni-apis/product-variants/\#retrieve-a-count-of-the-product-variants "Direct link to heading")

GET

https://apis.haravan.com/com/products/{product\_id}/variants/count.json

Retrieve the count of resources of the product variants.

- GET `https://apis.haravan.com/com/products/1034037268/variants/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 2
}

```

### Retrieves single the product variant [​](https://docs.haravan.com/docs/omni-apis/product-variants/\#retrieves-single-the-product-variant "Direct link to heading")

GET

https://apis.haravan.com/com/variants/{variant\_id}.json

Retrieves single the product variant by ID.

- GET `https://apis.haravan.com/com/variants/1075012798.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "variant": {
        "barcode": "CSSWMHRJ",
        "compare_at_price": 0.0000,
        "created_at": "2021-06-28T06:15:57.554Z",
        "fulfillment_service": null,
        "grams": 0.0000,
        "id": 1075012798,
        "inventory_management": "haravan",
        "inventory_policy": "deny",
        "inventory_quantity": 0,
        "position": 0,
        "price": 9990000.0000,
        "product_id": 1034037268,
        "requires_shipping": true,
        "sku": "CSSWMHRJ",
        "taxable": false,
        "title": "Default Title",
        "updated_at": "2021-08-14T07:50:52.173Z",
        "image_id": null,
        "option1": "Default Title",
        "option2": null,
        "option3": null,
        "inventory_advance": null
    }
}

```

### Create a new product variant [​](https://docs.haravan.com/docs/omni-apis/product-variants/\#create-a-new-product-variant "Direct link to heading")

POST

https://apis.haravan.com/com/products/{product\_id}/variants.json

Create a new product variant.

- POST `https://apis.haravan.com/com/products/1034037268/variants.json`

```codeBlockLines_e6Vv
{
  "variant": {
    "sku":"CSSWWW",
    "option1": "S",
    "price": 100000
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
    "variant": {
        "barcode": null,
        "compare_at_price": 0.0000,
        "created_at": "2021-09-07T10:51:59.267Z",
        "fulfillment_service": null,
        "grams": 0.0000,
        "id": 1077703228,
        "inventory_management": null,
        "inventory_policy": "deny",
        "inventory_quantity": 1,
        "old_inventory_quantity": 1,
        "inventory_quantity_adjustment": null,
        "position": 0,
        "price": 100000.0000,
        "product_id": 1034037268,
        "requires_shipping": false,
        "sku": "CSSWWW",
        "taxable": false,
        "title": "S",
        "updated_at": "2021-09-07T10:51:59.267Z",
        "image_id": null,
        "option1": "S",
        "option2": "",
        "option3": "",
        "inventory_advance": null
    }
}

```

### Update a product variant [​](https://docs.haravan.com/docs/omni-apis/product-variants/\#update-a-product-variant "Direct link to heading")

PUT

https://apis.haravan.com/com/variants/{variant\_id}.json

Update a product variant.

- PUT `https://apis.haravan.com/com/variants/1077703228.json`

```codeBlockLines_e6Vv
{
  "variant": {
    "sku":"CSSWWW",
    "option1": "M",
    "price": 200000
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "variant": {
        "barcode": null,
        "compare_at_price": 0.0000,
        "created_at": "2021-09-07T10:51:59.267Z",
        "fulfillment_service": null,
        "grams": 0.0000,
        "id": 1077703228,
        "inventory_management": null,
        "inventory_policy": "deny",
        "inventory_quantity": 1,
        "old_inventory_quantity": 1,
        "inventory_quantity_adjustment": null,
        "position": 0,
        "price": 200000.0000,
        "product_id": 1034037268,
        "requires_shipping": false,
        "sku": "CSSWWW",
        "taxable": false,
        "title": "M",
        "updated_at": "2021-09-07T10:56:37.989Z",
        "image_id": null,
        "option1": "M",
        "option2": "",
        "option3": "",
        "inventory_advance": null
    }
}

```

### Delete a product variant [​](https://docs.haravan.com/docs/omni-apis/product-variants/\#delete-a-product-variant "Direct link to heading")

DELETE

https://apis.haravan.com/com/products/{product\_id}/variants/{variant\_id}.json

Delete a product variant.

- DELETE `https://apis.haravan.com/com/products/1034037268/variants/1077703228.json`

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
Product Image](https://docs.haravan.com/docs/omni-apis/product-images/) [Next\\
\\
SmartCollection](https://docs.haravan.com/docs/omni-apis/smart-collections/)

- [What you can do with Product Variant](https://docs.haravan.com/docs/omni-apis/product-variants/#what-you-can-do-with-product-variant)
- [Retrieves a list of product variants](https://docs.haravan.com/docs/omni-apis/product-variants/#retrieves-a-list-of-product-variants)
- [Parameters](https://docs.haravan.com/docs/omni-apis/product-variants/#parameters)
- [Retrieve a count of the product variants](https://docs.haravan.com/docs/omni-apis/product-variants/#retrieve-a-count-of-the-product-variants)
- [Retrieves single the product variant](https://docs.haravan.com/docs/omni-apis/product-variants/#retrieves-single-the-product-variant)
- [Create a new product variant](https://docs.haravan.com/docs/omni-apis/product-variants/#create-a-new-product-variant)
- [Update a product variant](https://docs.haravan.com/docs/omni-apis/product-variants/#update-a-product-variant)
- [Delete a product variant](https://docs.haravan.com/docs/omni-apis/product-variants/#delete-a-product-variant)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.