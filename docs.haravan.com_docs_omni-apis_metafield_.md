---
url: "https://docs.haravan.com/docs/omni-apis/metafield/"
title: "Metafield | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/metafield/#)

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

  - [Shipping](https://docs.haravan.com/docs/omni-apis/shipping-rates/)

  - [Store properties](https://docs.haravan.com/docs/omni-apis/country/)

  - [Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [Home page](https://docs.haravan.com/)
- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)
- Metafield

On this page

# Metafield

`Version: 1.0`

The Metafield resource allows you to add additional information to store's resources. Metafields can be used in several ways, such as to add a summary to a blog post. You can also use metafields to share information with other Haravan apps.

### Resources that can have metafields [​](https://docs.haravan.com/docs/omni-apis/metafield/\#resources-that-can-have-metafields "Direct link to heading")

Metafields can be added to the following resources:

| **Type of resource** | **Location of metafields** |
| --- | --- |
| Page | [https://apis.haravan.com/web/pages/#{id}/metafields.json](https://docs.haravan.com/docs/omni-apis/metafield/#) |
| Blog | [https://apis.haravan.com/web/blogs/#{id}/metafields.json](https://docs.haravan.com/docs/omni-apis/metafield/#) |
| Article | [https://apis.haravan.com/web/blogs/#{id}/articles/#{id}/metafields.json](https://docs.haravan.com/docs/omni-apis/metafield/#) |
| CustomCollection and SmartCollection | [https://apis.haravan.com/com/collections/#{id}/metafields.json](https://docs.haravan.com/docs/omni-apis/metafield/#) |
| Customer | [https://apis.haravan.com/com/customers/#{id}/metafields.json](https://docs.haravan.com/docs/omni-apis/metafield/#) |
| Order | [https://apis.haravan.com/com/orders/#{id}/metafields.json](https://docs.haravan.com/docs/omni-apis/metafield/#) |
| Product | [https://apis.haravan.com/com/products/#{id}/metafields.json](https://docs.haravan.com/docs/omni-apis/metafield/#) |
| Product Variant | [https://apis.haravan.com/com/variants/#{id}/metafields.json](https://docs.haravan.com/docs/omni-apis/metafield/#) |
| Product Image | [https://apis.haravan.com/com/images/#{id}/metafields.json](https://docs.haravan.com/docs/omni-apis/metafield/#) |
| Shop | [https://apis.haravan.com/com/metafields.json](https://docs.haravan.com/docs/omni-apis/metafield/#) |

Metafields have four required properties: a key, a namespace, a value and a value\_type. The key is the identifier for a metafield. The namespace functions a container for a set of metafields which help to distinguish between metadata that you created and metadata created by others with a similair namespace. The value is the content of the metafield. The value\_type describe the state of the value, whether it is a 'string', an 'integer' or an 'json'. There also exists an optional description property that provides additional information about the metafield.

### What can you do with Metafield? [​](https://docs.haravan.com/docs/omni-apis/metafield/\#what-can-you-do-with-metafield "Direct link to heading")

The Haravan API lets you do the following with the Metafield resource. More detailed versions of these general actions may be available:

- GET `https://apis.haravan.com/com/metafields.json`
  - **[Retrieves metafields that belong to a store](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-metafields-that-belong-to-a-store)**
- GET `https://apis.haravan.com/com/products/#{id}/metafields.json`
  - **[Retrieves metafields that belong to a product](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-metafields-that-belong-to-a-product)**
- GET `https://apis.haravan.com/com/metafields.json?metafield[owner_id]=850703190&metafield[owner_resource]=product_image`
  - **[Retrieves metafields that belong to a product image](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-metafields-that-belong-to-a-product-image)**
- GET `https://apis.haravan.com/com/metafields/count.json`
  - **[Retrieves a count of metafields that belong to a store](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-a-count-of-metafields-that-belong-to-a-store)**
- GET `https://apis.haravan.com/com/products/#{id}/metafields/count.json`
  - **[Retrieves a count of metafields that belong to a product](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-a-count-of-metafields-that-belong-to-a-product)**
- GET `https://apis.haravan.com/com/metafields/#{id}.json`
  - **[Retrieves a single store metafield by its ID](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-a-single-store-metafield-by-its-id)**
- GET `https://apis.haravan.com/com/products/#{id}/metafields/#{id}.json`
  - **[Retrieves a single product metafield by its ID](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-a-single-product-metafield-by-its-id)**
- POST `https://apis.haravan.com/com/metafields.json`
  - **[Create a new metafield for a store](https://docs.haravan.com/docs/omni-apis/metafield/#create-a-new-metafield-for-a-store)**
- POST `https://apis.haravan.com/com/products/#{id}/metafields.json`
  - **[Create a new metafield for a product](https://docs.haravan.com/docs/omni-apis/metafield/#create-a-new-metafield-for-a-product)**
- PUT `https://apis.haravan.com/com/metafields/#{id}.json`
  - **[Update a store metafield](https://docs.haravan.com/docs/omni-apis/metafield/#update-a-store-metafield)**
- PUT `https://apis.haravan.com/com/products/#{id}/metafields/#{id}.json`
  - **[Update a product metafield](https://docs.haravan.com/docs/omni-apis/metafield/#update-a-product-metafield)**
- DELETE `https://apis.haravan.com/com/metafields/#{id}.json`
  - **[Delete a store metafield](https://docs.haravan.com/docs/omni-apis/metafield/#delete-a-store-metafield)**
- DELETE `https://apis.haravan.com/com/products/#{id}/metafields/#{id}.json`
  - **[Delete a product metafield](https://docs.haravan.com/docs/omni-apis/metafield/#delete-a-product-metafield)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/metafield/\#properties "Direct link to heading")

* * *

`created_at` : `string` `Read-only`

```codeBlockLines_e6Vv
{"created_at": "2021-11-30T08:40:33.594Z"}

```

The date and time when the metafield was created. The API returns this value in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format.

`updated_at` : `string` `Read-only`

```codeBlockLines_e6Vv
{"updated_at": "2021-12-13T06:32:35.731Z"}

```

The date and time when the metafield was published. The API returns this value in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format.

`description` : `string` `optional`

```codeBlockLines_e6Vv
{ "description" : "abc" }

```

Additional information about the metafield.

`id` : `number` `Read-only`

```codeBlockLines_e6Vv
{ "id" : 915396206 }

```

The unique ID of the metafield.

`key` : `string`

```codeBlockLines_e6Vv
{ "key" : "warehouse" }

```

The name of the metafield. Minimum length: 3 characters. Maximum length: 30 characters.

`namespace` : `string`

```codeBlockLines_e6Vv
{ "namespace" : "inventory" }

```

Container for a set of metadata. Namespaces help distinguish between metadata you created against metadata created by another individual with a similar namespace. Minimum length: 2 characters. Maximum length: 20 characters.

`owner_id` : `number`

```codeBlockLines_e6Vv
{ "owner_id" : 690933842 }

```

The unique ID of the resource that the metafield is attached to.

`owner_resource` : `string`

```codeBlockLines_e6Vv
{ "owner_resource" : "shop" }

```

The type of resource that the metafield is attached to.

`value` : `string`

```codeBlockLines_e6Vv
{ "value" : "25" }

```

Information to be stored as metadata.

Minimum length: 1 characters. Maximum length: 80000 characters.

`value_type` : `string`

```codeBlockLines_e6Vv
{ "value_type" : "integer" }

```

States whether the information in the value is stored as a 'string', 'integer' or 'json'.

### Metafield types [​](https://docs.haravan.com/docs/omni-apis/metafield/\#metafield-types "Direct link to heading")

Each metafield and metafield definition has a value\_type, which defines the type of information that it can store.

When using the API to read and write metafields, the value is always entered and stored as a string, regardless of value\_type.

Metafields and definitions can have the following value types:

#### Value Types [​](https://docs.haravan.com/docs/omni-apis/metafield/\#value-types "Direct link to heading")

`string`

```codeBlockLines_e6Vv
{"value": "This item contains dairy products."}

```

A text field.

* * *

`integer`

```codeBlockLines_e6Vv
{"value": "10"}

```

A whole number in the range of +/-9,007,199,254,740,991.

* * *

`json`

```codeBlockLines_e6Vv
{"value":"{\"price\":10000,\"stock\":\"instock\",\"meta\":[{\"k\":\"v1\"},{\"k\":\"v2\"}]}"}

```

A JSON-formatted string.

* * *

### Retrieves metafields that belong to a store [​](https://docs.haravan.com/docs/omni-apis/metafield/\#retrieves-metafields-that-belong-to-a-store "Direct link to heading")

GET

https://apis.haravan.com/com/metafields.json

Get metafields that belong to a store.

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/metafield/\#parameters "Direct link to heading")

* * *

`page`

Page to show the result.

* * *

`limit`

Amount of results. (default: 50) (maximum: 50)

* * *

`since_id`

Restrict results to after the specified ID.

* * *

`created_at_min`

Show metafields created after date. (format: 2021-11-30T08:40:33.594Z)

* * *

`created_at_max`

Show metafields created before date. (format: 2021-11-30T08:40:33.594Z)

* * *

`updated_at_min`

Show metafields last updated after date. (format: 2021-11-30T08:40:33.594Z)

* * *

`updated_at_max`

Show metafields last updated before date. (format: 2021-11-30T08:40:33.594Z)

* * *

`namepace`

Show metafields with given namespace.

* * *

`key`

Show metafields with given key.

* * *

`value_type`

- **string** : Show only metafields with string value types.

- **integer** : Show only metafields with integer value types.

- **json**: Show only metafields with json value types.


* * *

`fields`

comma-separated list of fields to include in the response.

* * *

Get all metafields that belong to a store.

- GET `https://apis.haravan.com/com/metafields.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
  "metafields": [\
    {\
      "created_at": "2021-11-30T08:40:33.594Z",\
      "description": null,\
      "id": 721389482,\
      "key": "Wash",\
      "namespace": "instructions",\
      "owner_id": 690933842,\
      "updated_at": "2021-12-13T06:32:35.731Z",\
      "value": "Cold",\
      "value_type": "string",\
      "owner_resource": "shop"\
    }\
  ]
}

```

Get all metafields after the specified ID.

- GET `https://apis.haravan.com/com/metafields.json?since_id=721389482`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK

{
  "metafields": [\
    {\
      "created_at": "2021-12-15T10:37:38.363Z",\
      "description": null,\
      "id": 996577826,\
      "key": "warehouse",\
      "namespace": "inventory",\
      "owner_id": 690933842,\
      "updated_at": "2021-12-15T10:38:37.54Z",\
      "value": 25,\
      "value_type": "integer",\
      "owner_resource": "shop"\
    }\
  ]
}

```

### Retrieves metafields that belong to a product [​](https://docs.haravan.com/docs/omni-apis/metafield/\#retrieves-metafields-that-belong-to-a-product "Direct link to heading")

GET

https://apis.haravan.com/com/products/#{id}/metafields.json

Get all metafields that belong to a product.

- GET `https://apis.haravan.com/com/products/632910392/metafields.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
  "metafields": [\
    {\
      "created_at": "2021-11-30T08:40:33.594Z",\
      "description": "French product title",\
      "id": 845366454,\
      "key": "title_fr",\
      "namespace": "translations",\
      "owner_id": 632910392,\
      "updated_at": "2021-12-13T06:32:35.731Z",\
      "value": "produit",\
      "value_type": "string",\
      "owner_resource": "product"\
    }\
  ]
}

```

### Retrieves metafields that belong to a product image [​](https://docs.haravan.com/docs/omni-apis/metafield/\#retrieves-metafields-that-belong-to-a-product-image "Direct link to heading")

GET

https://apis.haravan.com/com/metafields.json

Get all metafields that belong to the images of a product.

- GET `https://apis.haravan.com/com/metafields.json?metafield[owner_id]=850703190&metafield[owner_resource]=product_image`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
  "metafields": [\
    {\
      "created_at": "2021-11-30T08:40:33.594Z",\
      "description": "French product image title",\
      "id": 625663657,\
      "key": "title_fr",\
      "namespace": "translation",\
      "owner_id": 850703190,\
      "updated_at": "2021-12-13T06:32:35.731Z",\
      "value": "tbn",\
      "value_type": "string",\
      "owner_resource": "product_image"\
    }\
  ]
}

```

### Retrieves a count of metafields that belong to a store [​](https://docs.haravan.com/docs/omni-apis/metafield/\#retrieves-a-count-of-metafields-that-belong-to-a-store "Direct link to heading")

GET

https://apis.haravan.com/com/metafields/count.json

Get a count of metafields that belong to a store.

- GET `https://apis.haravan.com/com/metafields/count.json`

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
  "count": 1
}

```

### Retrieves a count of metafields that belong to a product [​](https://docs.haravan.com/docs/omni-apis/metafield/\#retrieves-a-count-of-metafields-that-belong-to-a-product "Direct link to heading")

GET

https://apis.haravan.com/com/products/#{id}/metafields/count.json

Get a count of all metafields that belong to a product.

- GET `https://apis.haravan.com/com/products/632910392/metafields/count.json`

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
  "count": 1
}

```

### Retrieves a single store metafield by its ID [​](https://docs.haravan.com/docs/omni-apis/metafield/\#retrieves-a-single-store-metafield-by-its-id "Direct link to heading")

GET

https://apis.haravan.com/com/metafields/#{id}.json

Get a single store metafield by its ID.

* * *

`fields`

Comma-separated list of fields to include in the response.

* * *

Get a single store metafield by ID. A metafield belonging to any resource can be found this way.

- GET `https://apis.haravan.com/com/metafields/721389482.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
  "metafield": {
    "created_at": "2021-11-30T08:40:33.594Z",
    "description": null,
    "id": 721389482,
    "key": "app_key",
    "namespace": "affiliates",
    "owner_id": 690933842,
    "updated_at": "2021-12-13T06:32:35.731Z",
    "value": "app_key",
    "value_type": "string",
    "owner_resource": "shop"
  }
}

```

### Retrieves a single product metafield by its ID [​](https://docs.haravan.com/docs/omni-apis/metafield/\#retrieves-a-single-product-metafield-by-its-id "Direct link to heading")

GET

https://apis.haravan.com/com/products/#{id}/metafields/#{id}.json

Get a single product metafield using the metafield's nested resource path.

- GET `https://apis.haravan.com/com/products/632910392/metafields/845366454.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
  "metafield": {
    "created_at": "2021-11-30T08:40:33.594Z",
    "description": "French product title",
    "id": 845366454,
    "key": "title_fr",
    "namespace": "translations",
    "owner_id": 632910392,
    "updated_at": "2021-12-13T06:32:35.731Z",
    "value": "produit",
    "value_type": "string",
    "owner_resource": "product"
  }
}

```

### Create a new metafield for a store [​](https://docs.haravan.com/docs/omni-apis/metafield/\#create-a-new-metafield-for-a-store "Direct link to heading")

POST

https://apis.haravan.com/com/metafields.json

Create a new metafield for a store.

- POST `https://apis.haravan.com/com/metafields.json`

```codeBlockLines_e6Vv
{
  "metafield": {
    "namespace": "inventory",
    "key": "warehouse",
    "value": 25,
    "value_type": "integer"
  }
}

```

Details

```codeBlockLines_e6Vv

HTTP/1.1 201 Created
{
  "metafield": {
    "created_at": "2016-09-15T09:53:02.887Z",
    "description": null,
    "id": 1003594533,
    "key": "warehouse",
    "namespace": "inventory",
    "owner_id": 1000045110,
    "owner_resource": "shop",
    "value": "25",
    "value_type": "integer",
    "updated_at": "2021-12-21T06:58:17.290Z"
  }
}

```

Trying to create a metafield without a key will return an error.

- POST `https://apis.haravan.com/com/metafields.json`

```codeBlockLines_e6Vv
{
  "metafield": {
    "key": null
  }
}

```

Details

```codeBlockLines_e6Vv

HTTP/1.1 422 Unprocessable Entity

{
    "errors": "Key can't be blank"
}

```

### Create a new metafield for a product [​](https://docs.haravan.com/docs/omni-apis/metafield/\#create-a-new-metafield-for-a-product "Direct link to heading")

POST

https://apis.haravan.com/com/products/#{id}/metafields.json

Create a new metafield for a product.

- POST `https://apis.haravan.com/com/products/1037394594/metafields.json`

```codeBlockLines_e6Vv
{
  "metafield": {
    "namespace": "inventory",
    "key": "warehouse",
    "value": 25,
    "value_type": "integer"
  }
}

```

Details

```codeBlockLines_e6Vv

HTTP/1.1 201 Created

{
  "metafield": {
    "created_at": "2021-12-21T07:41:41.298Z",
    "description": null,
    "id": 1015890158,
    "key": "warehouse",
    "namespace": "inventory",
    "owner_id": 1037394594,
    "owner_resource": "product",
    "value": "25",
    "value_type": "integer",
    "updated_at": "2021-12-21T07:41:41.298Z"
  }
}

```

Create a new metafield for a product with `"value_type": "json"`. A JSON-formatted string.

- POST `https://apis.haravan.com/com/products/1037394594/metafields.json`

```codeBlockLines_e6Vv
{
  "metafield": {
    "namespace": "inventory",
    "key": "warehouse",
    "value": "[{\"k\":\"v1\"},{\"k\":\"v2\"}]",
    "value_type": "json"
  }
}

```

Details

```codeBlockLines_e6Vv

HTTP/1.1 201 Created

{
  "metafield": {
    "created_at": "2021-12-22T04:33:44.121Z",
    "description": null,
    "id": 1015892658,
    "key": "warehouse",
    "namespace": "inventory",
    "owner_id": 1037394594,
    "owner_resource": "product",
    "value": "[{\"k\":\"v1\"},{\"k\":\"v2\"}]",
    "value_type": "json",
    "updated_at": "2021-12-22T04:33:44.121Z"
  }
}

```

Another example JSON-formatted string.

- POST `https://apis.haravan.com/com/products/1037394594/metafields.json`

```codeBlockLines_e6Vv
{
  "metafield": {
    "namespace": "inventory",
    "key": "warehouse",
    "value": "{\"price\":10000,\"stock\":\"instock\",\"meta\":[{\"k\":\"v1\"},{\"k\":\"v2\"}]}",
    "value_type": "json"
  }
}

```

Details

```codeBlockLines_e6Vv

HTTP/1.1 201 Created

{
  "metafield": {
    "created_at": "2021-12-22T04:33:44.121Z",
    "description": null,
    "id": 1015892658,
    "key": "warehouse",
    "namespace": "inventory",
    "owner_id": 1037394594,
    "owner_resource": "product",
    "value": "{\"price\":10000,\"stock\":\"instock\",\"meta\":[{\"k\":\"v1\"},{\"k\":\"v2\"}]}",
    "value_type": "json",
    "updated_at": "2021-12-22T04:46:38.624Z"
  }
}

```

Code Liquid in `product.liquid`:

- POST `https://apis.haravan.com/com/products/1037394594/metafields.json`

```codeBlockLines_e6Vv
{%- if product.metafields.inventory != blank -%}
  type: {{ product.metafields.inventory.warehouse.type }} <br/>
  price: {{ product.metafields.inventory.warehouse.value.price }} <br/>
  stock: {{ product.metafields.inventory.warehouse.value.stock }} <br/>
  {%- for field in product.metafields.inventory.warehouse.value.meta -%}
    {{ field.k }} <br/>
  {%- endfor -%}
{%- endif -%}

```

### Update a store metafield [​](https://docs.haravan.com/docs/omni-apis/metafield/\#update-a-store-metafield "Direct link to heading")

PUT

https://apis.haravan.com/com/metafields/#{id}.json

Update an existing store metafield. A metafield belonging to any resource can be updated this way. Namespace and key of an existing metafield cannot be changed.

- PUT `https://apis.haravan.com/com/metafields/1003594533.json`

```codeBlockLines_e6Vv
{
  "metafield": {
    "id": 1003594533,
    "value": "something new",
    "value_type": "string"
  }
}

```

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK

{
  "metafield": {
    "created_at": "2016-09-15T09:53:02.887Z",
    "description": null,
    "id": 1003594533,
    "key": "warehouse",
    "namespace": "inventory",
    "owner_id": 1000045110,
    "owner_resource": "shop",
    "value": "something new",
    "value_type": "string",
    "updated_at": "2021-12-21T07:47:01.191Z"
  }
}

```

### Update a product metafield [​](https://docs.haravan.com/docs/omni-apis/metafield/\#update-a-product-metafield "Direct link to heading")

PUT

https://apis.haravan.com/com/metafields/#{id}.json

Update an existing store metafield. A metafield belonging to any resource can be updated this way. Namespace and key of an existing metafield cannot be changed.

- PUT `https://apis.haravan.com/com/products/1037394594/metafields/1015890158.json`

```codeBlockLines_e6Vv
{
  "metafield": {
    "id": 1015890158,
    "value": "titre",
    "value_type": "string"
  }
}

```

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK

{
  "metafield": {
    "created_at": "2021-12-21T07:41:41.298Z",
    "description": null,
    "id": 1015890158,
    "key": "warehouse",
    "namespace": "inventory",
    "owner_id": 1037394594,
    "owner_resource": "product",
    "value": "titre",
    "value_type": "string",
    "updated_at": "2021-12-21T07:52:47.536Z"
  }
}

```

### Delete a store metafield [​](https://docs.haravan.com/docs/omni-apis/metafield/\#delete-a-store-metafield "Direct link to heading")

DELETE

https://apis.haravan.com/com/metafields/#{id}.json

Delete an existing store metafield by id. A metafield belonging to any resource can be deleted this way.

- DELETE `https://apis.haravan.com/com/metafields/721389482.json`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK

{}

```

### Delete a product metafield [​](https://docs.haravan.com/docs/omni-apis/metafield/\#delete-a-product-metafield "Direct link to heading")

DELETE

https://apis.haravan.com/com/products/#{id}/metafields/#{id}.json

Delete existing metafield belonging to a product using the nested resource path.

- DELETE `https://apis.haravan.com/com/products/632910392/metafields/845366454.json`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK

{}

```

[Previous\\
\\
Inventory Transfer](https://docs.haravan.com/docs/omni-apis/inventory-transfer/) [Next\\
\\
Article](https://docs.haravan.com/docs/omni-apis/articles/)

- [Resources that can have metafields](https://docs.haravan.com/docs/omni-apis/metafield/#resources-that-can-have-metafields)
- [What can you do with Metafield?](https://docs.haravan.com/docs/omni-apis/metafield/#what-can-you-do-with-metafield)
- [Properties](https://docs.haravan.com/docs/omni-apis/metafield/#properties)
- [Metafield types](https://docs.haravan.com/docs/omni-apis/metafield/#metafield-types)
- [Retrieves metafields that belong to a store](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-metafields-that-belong-to-a-store)
- [Retrieves metafields that belong to a product](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-metafields-that-belong-to-a-product)
- [Retrieves metafields that belong to a product image](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-metafields-that-belong-to-a-product-image)
- [Retrieves a count of metafields that belong to a store](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-a-count-of-metafields-that-belong-to-a-store)
- [Retrieves a count of metafields that belong to a product](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-a-count-of-metafields-that-belong-to-a-product)
- [Retrieves a single store metafield by its ID](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-a-single-store-metafield-by-its-id)
- [Retrieves a single product metafield by its ID](https://docs.haravan.com/docs/omni-apis/metafield/#retrieves-a-single-product-metafield-by-its-id)
- [Create a new metafield for a store](https://docs.haravan.com/docs/omni-apis/metafield/#create-a-new-metafield-for-a-store)
- [Create a new metafield for a product](https://docs.haravan.com/docs/omni-apis/metafield/#create-a-new-metafield-for-a-product)
- [Update a store metafield](https://docs.haravan.com/docs/omni-apis/metafield/#update-a-store-metafield)
- [Update a product metafield](https://docs.haravan.com/docs/omni-apis/metafield/#update-a-product-metafield)
- [Delete a store metafield](https://docs.haravan.com/docs/omni-apis/metafield/#delete-a-store-metafield)
- [Delete a product metafield](https://docs.haravan.com/docs/omni-apis/metafield/#delete-a-product-metafield)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.