---
url: "https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/"
title: "Inventory Purchase Return | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/#)

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
- Inventory Purchase Return

On this page

# Inventory Purchase Return

You can use the Purchase Receives resource to document the sale of products and services to be delivered at a late date.

**Authenticated access scopes**: `com.read_inventories`, `com.write_inventories`

### What you can do with Purchase Return [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/\#what-you-can-do-with-purchase-return "Direct link to heading")

The Haravan API lets you do the following with the Purchase Receives resource.

- GET `https://apis.haravan.com/com/v2/inventories/purchase_returns.json`
  - **[Retrieves a list of purchase returns.](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/#retrieves-a-list-of-purchase-returns)**
- GET `https://apis.haravan.com/com/v2/inventories/purchase_returns/{purchase_return_id}.json`
  - **[Retrieves single the purchase return.](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/#retrieves-single-the-purchase-return)**

### Purchase Return properties [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/\#purchase-return-properties "Direct link to heading")

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id": 1001004628

```

A unique identifier for the purchase return.

* * *

`return_number` : `string`

```codeBlockLines_e6Vv
"return_number": "IR1000000007"

```

The number of the purchase return.

* * *

`ref_number` : `string`

```codeBlockLines_e6Vv
"ref_number": "#732000"

```

Reference number of the purchase return.

* * *

`ref_receive_id` : `number`

```codeBlockLines_e6Vv
"ref_receive_id": null

```

Reference purchase order number of the purchase return.

* * *

`tags`: `string`

```codeBlockLines_e6Vv
"tags": "tagsational, tag1, tag2, tag3"

```

Tags are additional short descriptors formatted as a string of comma-separated values. For example, if an article has three tags: tag1, tag2, tag3.

* * *

`created_at` : `string`

```codeBlockLines_e6Vv
"created_at": "2022-08-25T05:15:12.917Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format) when the purchase return was created.

* * *

`updated_at` : `string`

```codeBlockLines_e6Vv
"updated_at": "2022-09-05T02:27:46.779Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format) when the purchase return was updated.

* * *

`returned_at` : `string`

```codeBlockLines_e6Vv
"returned_at": "2022-08-25T05:15:12.917Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format) when the purchase return was returned.

* * *

`notes` : `string`

```codeBlockLines_e6Vv
"notes": "Notes"

```

An optional note that a shop owner can attach to the purchase return.

* * *

`status` : `string`

```codeBlockLines_e6Vv
"status": "Đã xuất trả"

```

**Nháp**: draft.

**Đã nhập hàng**: has received the product.

**Đã xuất trả**: has returned the product.

**Đã hủy**: has canceled the product.

* * *

`total` : `number`

```codeBlockLines_e6Vv
"total": 1100

```

Total quantity of purchase receive.

* * *

`total_cost` : `number`

```codeBlockLines_e6Vv
"total_cost": 1080100

```

Total cost of purchase receive.

* * *

`supplier` : `json`

Details

- **id**: A unique numeric identifier for the supplier.
- **name**: The name owner of the supplier.
- **supplier\_name**: The name of the supplier.
- **phone**: The phone number of the supplier.
- **email**: The email of the supplier.
- **address**: The address of the supplier.
- **zip**: The zip or postal code.
- **city**: The city the supplier is in.
- **created\_at**: The date and time when the supplier was created.
- **updated\_at**: The date and time when the supplier was last updated.
- **country**: The country name the supplier is in.
- **country\_code**: The country code the supplier is in.
- **province**: The province name the supplier is in.
- **province\_code**: The province code the supplier is in.
- **district**: The district name the supplier is in.
- **district\_code**: The district code the supplier is in.
- **ward**: The ward name the supplier is in.
- **ward\_code**: The ward code the supplier is in.

* * *

`location` : `json`

Details

- **id**: A unique numeric identifier for the location.
- **name**: The name of the location.
- **location\_type**: The location type. There are **ontheroad** and **default** type.
- **email**: The email of the location.
- **address1**: The first line of the address.
- **address2**: The second line of the address.
- **zip**: The zip or postal code.
- **city**: The city the location is in.
- **phone**: The phone number of the location.
- **country**: The country name the location is in.
- **country\_code**: The country code the location is in.
- **country\_name**: The country name the location is in.
- **province**: The province name the location is in.
- **province\_code**: The province code the location is in.
- **district**: The district name the location is in.
- **district\_code**: The district code the location is in.
- **ward**: The ward name the location is in.
- **ward\_code**: The ward code the location is in.
- **created\_at**: The date and time when the location was created.
- **updated\_at**: The date and time when the location was last updated.
- **is\_primary**: The primary location if **true**. Vice versa, the normal location.
- **is\_unavailable\_quantity**: Allowable use decimal number if true. Vice versa, just long number.
- **type**: The location type. There are **ontheroad** and **default** type.

* * *

`line_items` : `json`

Details

- **id**: A unique numeric identifier for the line item.
- **product\_name**: The name of the product.
- **product\_id**: The unique numeric identifier for the product.
- **product\_variant\_id**: The unique numeric identifier for the product variant.
- **variant\_title**: The name of the product variant.
- **sku**: A unique identifier for the product in the shop.
- **barcode**: The barcode, UPC, or ISBN number for the product.
- **original\_cost**: The price for this product variant.
- **discount\_amount**: Discount for this product variant.
- **cost**: The cost for this product variant after discount.
- **quantity**: The number of items in the line item for this product variant.
- **total\_cost**: The total cost for this product variant after discount..
- **variant\_unit**: The unit of the product variant.

```codeBlockLines_e6Vv
{
  "id": 1001007754,
  "product_name": "Long body superman FM-D08",
  "product_id": 10041031921,
  "product_variant_id": 142558673,
  "variant_title": "Dark blue / 4T",
  "sku": null,
  "barcode": null,
  "original_cost": 0,
  "discount_amount": 0,
  "cost": 0,
  "quantity": 1,
  "total_cost": 0,
   "variant_unit":
    {
      "id": 0,
      "unit": null,
      "base": false,
      "sellable": false,
      "ratio": 1,
      "barcode": null,
      "sku": null,
      "price": 0
    }
}

```

- **lots**: List lot of the product variant.

```codeBlockLines_e6Vv
[\
  {\
    "lot_no": "Lot 1",\
    "expire_date": "2022-09-10T17:00:00Z",\
    "quantity": 100\
  },\
  {\
    "lot_no": "Lot 2",\
    "expire_date": "2022-09-10T17:00:00Z",\
    "quantity": 100\
  },\
]

```

* * *

### Retrieves a list of purchase returns. [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/\#retrieves-a-list-of-purchase-returns "Direct link to heading")

GET

https://apis.haravan.com/com/v2/inventories/purchase\_returns.json

Retrieves a list of purchase returns. You can filter resources by params.

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/\#parameters "Direct link to heading")

* * *

`limit`

Limit of the result.

* * *

`page`

Page to show the result.

* * *

Retrieve all of the resources of the purchase receives by page number. By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/com/v2/inventories/purchase_returns.json?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
  "purchase_returns": [\
    {\
      "id": 1001004833,\
      "return_number": "PR1000000000",\
      "supplier": {\
        "id": 1040044131,\
        "name": "",\
        "supplier_name": "Nhà làm",\
        "phone": "",\
        "email": "",\
        "address": "102/18 tô hiến thành",\
        "zip": null,\
        "city": null,\
        "created_at": "2022-08-22T08:15:33.044Z",\
        "updated_at": "2022-08-22T08:15:33.044Z",\
        "country": "Vietnam",\
        "country_code": "VN",\
        "province": "Hồ Chí Minh",\
        "province_code": "HC",\
        "district": "Quận 10",\
        "district_code": "HC475",\
        "ward": "Phường 15",\
        "ward_code": "27163"\
      },\
      "location": {\
        "id": 497789,\
        "name": "Địa điểm mặc định",\
        "location_type": "default",\
        "email": null,\
        "address1": "số 14 đường Phan Tôn",\
        "address2": null,\
        "zip": "700000",\
        "city": null,\
        "province": "Hồ Chí Minh",\
        "country": "Vietnam",\
        "phone": "0784665872",\
        "country_code": "VN",\
        "country_name": "Vietnam",\
        "province_code": "HC",\
        "district": "Quận 1",\
        "district_code": "HC466",\
        "ward": "Phường Đa Kao",\
        "ward_code": "26737",\
        "created_at": "2022-06-13T07:43:47.654Z",\
        "updated_at": "2022-10-14T04:12:16.992Z",\
        "is_primary": true,\
        "is_unavailable_quantity": false,\
        "type": "default"\
      },\
      "created_at": "2022-10-21T02:43:02.725Z",\
      "updated_at": "2022-10-21T02:43:02.876Z",\
      "returned_at": "2022-10-21T02:43:02.725Z",\
      "notes": null,\
      "status": "3",\
      "total": 3,\
      "total_cost": 0,\
      "tags": null,\
      "ref_receive_id": null,\
      "ref_number": null,\
      "line_items": null\
    }\
  ]
}

```

### Retrieves single the purchase return. [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/\#retrieves-single-the-purchase-return "Direct link to heading")

GET

https://apis.haravan.com/com/v2/inventories/purchase\_returns/{purchase\_return\_id}.json

Retrieves single the purchase receive.

- GET `https://apis.haravan.com/com/v2/inventories/purchase_returns/1001004833.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "purchase_return": {
    "id": 1001004833,
    "return_number": "PR1000000000",
    "supplier": {
      "id": 1040044131,
      "name": "",
      "supplier_name": "Nhà làm",
      "phone": "",
      "email": "",
      "address": "102/18 tô hiến thành",
      "zip": null,
      "city": null,
      "created_at": "2022-08-22T08:15:33.044Z",
      "updated_at": "2022-08-22T08:15:33.044Z",
      "country": "Vietnam",
      "country_code": "VN",
      "province": "Hồ Chí Minh",
      "province_code": "HC",
      "district": "Quận 10",
      "district_code": "HC475",
      "ward": "Phường 15",
      "ward_code": "27163"
    },
    "location": {
      "id": 497789,
      "name": "Địa điểm mặc định",
      "location_type": "default",
      "email": null,
      "address1": "số 14 đường Phan Tôn",
      "address2": null,
      "zip": "700000",
      "city": null,
      "province": "Hồ Chí Minh",
      "country": null,
      "phone": "0784665872",
      "country_code": "VN",
      "country_name": "Vietnam",
      "province_code": "HC",
      "district": "Quận 1",
      "district_code": "HC466",
      "ward": "Phường Đa Kao",
      "ward_code": "26737",
      "created_at": "2022-06-13T07:43:47.654Z",
      "updated_at": "2022-10-14T04:12:16.992Z",
      "is_primary": true,
      "is_unavailable_quantity": false,
      "type": "default"
    },
    "created_at": "2022-10-21T02:43:02.725Z",
    "updated_at": "2022-10-21T02:43:02.876Z",
    "returned_at": "2022-10-21T02:43:02.725Z",
    "notes": null,
    "status": "Đã xuất trả",
    "total": 3,
    "total_cost": 46382,
    "tags": null,
    "ref_receive_id": null,
    "ref_number": null,
    "line_items": [\
      {\
        "id": 1001007754,\
        "product_name": "Long body superman FM-D08",\
        "product_id": 10041031921,\
        "product_variant_id": 142558673,\
        "variant_title": "Dark blue / 4T",\
        "sku": null,\
        "barcode": null,\
        "original_cost": 0,\
        "discount_amount": 0,\
        "cost": 0,\
        "quantity": 1,\
        "total_cost": 0,\
        "variant_unit": {\
          "id": 0,\
          "unit": null,\
          "base": false,\
          "sellable": false,\
          "ratio": 1,\
          "barcode": null,\
          "sku": null,\
          "price": 0\
        },\
        "lots": []\
      },\
      {\
        "id": 1001007755,\
        "product_name": "Long body superman FM-D08",\
        "product_id": 10041031921,\
        "product_variant_id": 142558672,\
        "variant_title": "Orange / 3T",\
        "sku": null,\
        "barcode": null,\
        "original_cost": 0,\
        "discount_amount": 0,\
        "cost": 0,\
        "quantity": 1,\
        "total_cost": 0,\
        "variant_unit": {\
          "id": 0,\
          "unit": null,\
          "base": false,\
          "sellable": false,\
          "ratio": 1,\
          "barcode": null,\
          "sku": null,\
          "price": 0\
        },\
        "lots": []\
      },\
      {\
        "id": 1001007756,\
        "product_name": "Long body superman FM-D08",\
        "product_id": 10041031921,\
        "product_variant_id": 142558671,\
        "variant_title": "Grey / 4T",\
        "sku": null,\
        "barcode": null,\
        "original_cost": 46382,\
        "discount_amount": 0,\
        "cost": 46382,\
        "quantity": 1,\
        "total_cost": 46382,\
        "variant_unit": {\
          "id": 0,\
          "unit": null,\
          "base": false,\
          "sellable": false,\
          "ratio": 1,\
          "barcode": null,\
          "sku": null,\
          "price": 0\
        },\
        "lots": []\
      }\
    ]
  }
}

```

[Previous\\
\\
Inventory Purchase Receive](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/) [Next\\
\\
Inventory Transfer](https://docs.haravan.com/docs/omni-apis/inventory-transfer/)

- [What you can do with Purchase Return](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/#what-you-can-do-with-purchase-return)
- [Purchase Return properties](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/#purchase-return-properties)
- [Retrieves a list of purchase returns.](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/#retrieves-a-list-of-purchase-returns)
- [Retrieves single the purchase return.](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/#retrieves-single-the-purchase-return)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.