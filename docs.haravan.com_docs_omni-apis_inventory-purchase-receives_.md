---
url: "https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/"
title: "Inventory Purchase Receive | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/#)

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
- Inventory Purchase Receive

On this page

# Inventory Purchase Receive

You can use the Purchase Receives resource to document the sale of products and services to be delivered at a late date.

**Authenticated access scopes**: `com.read_inventories`, `com.write_inventories`

### What you can do with Purchase Receives [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/\#what-you-can-do-with-purchase-receives "Direct link to heading")

The Haravan API lets you do the following with the Purchase Receives resource.

- GET `https://apis.haravan.com/com/v2/inventories/purchase_receives.json`
  - **[Retrieves a list of purchase receives.](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/#retrieves-a-list-of-purchase-receives)**
- GET `https://apis.haravan.com/com/v2/inventories/purchase_receives/{purchase_receive_id}.json`
  - **[Retrieves single the purchase receive.](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/#retrieves-single-the-purchase-receive)**

### Purchase Receives properties [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/\#purchase-receives-properties "Direct link to heading")

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id": 1001004628

```

A unique identifier for the purchase receive.

* * *

`receive_number` : `string`

```codeBlockLines_e6Vv
"receive_number": "IR1000000007"

```

The number of the purchase receive.

* * *

`ref_number` : `string`

```codeBlockLines_e6Vv
"ref_number": "#732000"

```

Reference number of the purchase receive.

* * *

`ref_purchase_order_id` : `number`

```codeBlockLines_e6Vv
"ref_purchase_order_id": null

```

Reference purchase order number of the purchase receive.

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

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format) when the purchase receive was created.

* * *

`updated_at` : `string`

```codeBlockLines_e6Vv
"updated_at": "2022-09-05T02:27:46.779Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format) when the purchase receive was updated.

* * *

`received_at` : `string`

```codeBlockLines_e6Vv
"received_at": "2022-08-25T05:15:12.917Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format) when the purchase receive was received.

* * *

`notes` : `string`

```codeBlockLines_e6Vv
"notes": "Notes"

```

An optional note that a shop owner can attach to the purchase receive.

* * *

`status` : `string`

```codeBlockLines_e6Vv
"status": "Đã nhập hàng"

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
  "id": 1000002202,
  "unit": "unit",
  "base": true,
  "sellable": true,
  "ratio": 1,
  "barcode": null,
  "sku": null,
  "price": 0
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

### Retrieves a list of purchase receives. [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/\#retrieves-a-list-of-purchase-receives "Direct link to heading")

GET

https://apis.haravan.com/com/v2/inventories/purchase\_receives.json

Retrieves a list of purchase receives. You can filter resources by params.

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/\#parameters "Direct link to heading")

* * *

`limit`

Limit of the result.

* * *

`page`

Page to show the result.

* * *

Retrieve all of the resources of the purchase receives by page number. By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/com/v2/inventories/purchase_receives.json?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
  "purchase_receives": [\
    {\
      "id": 1001004580,\
      "receive_number": "IR1000000001",\
      "supplier": {\
        "id": 1040044131,\
        "name": "",\
        "supplier_name": "Supplier Name",\
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
      "created_at": "2022-08-23T08:22:39.71Z",\
      "updated_at": "2022-09-06T07:27:39.106Z",\
      "received_at": "2022-08-23T08:22:39.71Z",\
      "notes": null,\
      "status": "Đã nhập hàng",\
      "total": 100,\
      "total_cost": 10000000,\
      "tags": "IR1000000001,IR1000000002",\
      "ref_purchase_order_id": 1040148821,\
      "ref_number": "THAMCHIEUIR1000000001",\
      "line_items": null\
    },\
    {\
      "id": 1001004562,\
      "receive_number": "IR1000000000",\
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
        "id": 497980,\
        "name": "Kho Hồ Chí Minh",\
        "location_type": "default",\
        "email": "hrv@gmail.com",\
        "address1": "102/18 Tô hiến thành",\
        "address2": null,\
        "zip": null,\
        "city": null,\
        "province": "Hồ Chí Minh",\
        "country": "Vietnam",\
        "phone": "0784665872",\
        "country_code": "VN",\
        "country_name": "Vietnam",\
        "province_code": "HC",\
        "district": "Quận 10",\
        "district_code": "HC475",\
        "ward": "Phường 15",\
        "ward_code": "27163",\
        "created_at": "2022-07-07T02:21:22.595Z",\
        "updated_at": "2022-10-14T04:12:17.037Z",\
        "is_primary": false,\
        "is_unavailable_quantity": false,\
        "type": "default"\
      },\
      "created_at": "2022-08-22T08:16:19.926Z",\
      "updated_at": "2022-08-22T08:16:20.032Z",\
      "received_at": "2022-08-22T08:16:19.926Z",\
      "notes": null,\
      "status": "Đã nhập hàng",\
      "total": 100,\
      "total_cost": 50000000,\
      "tags": null,\
      "ref_purchase_order_id": null,\
      "ref_number": null,\
      "line_items": null\
    }\
  ]
}

```

### Retrieves single the purchase receive. [​](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/\#retrieves-single-the-purchase-receive "Direct link to heading")

GET

https://apis.haravan.com/com/v2/inventories/purchase\_receives/{purchase\_receive\_id}.json

Retrieves single the purchase receive.

- GET `https://apis.haravan.com/com/v2/inventories/purchase_receives/1001004628.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "purchase_receive": {
    "id": 1001004628,
    "receive_number": "IR1000000007",
    "supplier": {
      "id": 1040044132,
      "name": "Nguyễn Ngọc Sáng",
      "supplier_name": "NGỌC SÁNG FnD",
      "phone": "09876542321",
      "email": "email@haravan.com",
      "address": "Ấp Cẩm An",
      "zip": null,
      "city": null,
      "created_at": "2022-08-25T03:18:07.743Z",
      "updated_at": "2022-08-25T03:18:07.744Z",
      "country": "Vietnam",
      "country_code": "VN",
      "province": "Tây Ninh",
      "province_code": "TN",
      "district": "Huyện Gò Dầu",
      "district_code": "TN519",
      "ward": "Xã Cẩm Giang",
      "ward_code": "25660"
    },
    "location": {
      "id": 498250,
      "name": "Kho Tây Ninh",
      "location_type": "default",
      "email": "tayninh_inventory@gmail.com",
      "address1": "182 Lê Đại Hành",
      "address2": null,
      "zip": "700000",
      "city": null,
      "province": "Hồ Chí Minh",
      "country": null,
      "phone": "0868946949",
      "country_code": "VN",
      "country_name": "Vietnam",
      "province_code": "HC",
      "district": "Quận 11",
      "district_code": "HC476",
      "ward": "Phường 15",
      "ward_code": "27208",
      "created_at": "2022-08-22T07:22:05.726Z",
      "updated_at": "2022-09-09T06:51:15.618Z",
      "is_primary": true,
      "is_unavailable_quantity": false,
      "type": "default"
    },
    "created_at": "2022-08-25T05:15:12.917Z",
    "updated_at": "2022-09-05T02:27:46.779Z",
    "received_at": "2022-08-25T05:15:12.917Z",
    "notes": "Notes",
    "status": "Đã nhập hàng",
    "total": 1100,
    "total_cost": 1080100,
    "tags": "tag1,tag2,tag3",
    "ref_purchase_order_id": null,
    "ref_number": "#732000",
    "line_items": [\
      {\
        "id": 1001007428,\
        "product_name": "open-api purchase-receives",\
        "product_id": 10041037168,\
        "product_variant_id": 142568269,\
        "variant_title": "OK-2",\
        "sku": null,\
        "barcode": null,\
        "original_cost": 1200,\
        "discount_amount": 120,\
        "cost": 1080,\
        "quantity": 1000,\
        "total_cost": 1080000,\
        "variant_unit": {\
          "id": 1000002202,\
          "unit": "Thùng",\
          "base": true,\
          "sellable": true,\
          "ratio": 1,\
          "barcode": null,\
          "sku": null,\
          "price": 0\
        },\
        "lots": []\
      },\
      {\
        "id": 1001007429,\
        "product_name": "open-api purchase-receives",\
        "product_id": 10041037168,\
        "product_variant_id": 142568260,\
        "variant_title": "OK",\
        "sku": "open-api-purchase-receives",\
        "barcode": "open-api-purchase-receives",\
        "original_cost": 1000,\
        "discount_amount": 999,\
        "cost": 1,\
        "quantity": 100,\
        "total_cost": 100,\
        "variant_unit": {\
          "id": 1000002199,\
          "unit": "Cái",\
          "base": true,\
          "sellable": true,\
          "ratio": 1,\
          "barcode": "open-api-purchase-receives",\
          "sku": "open-api-purchase-receives",\
          "price": 0\
        },\
        "lots": [\
          {\
            "lot_no": "Lô 902",\
            "expire_date": "2022-09-10T17:00:00Z",\
            "quantity": 100\
          }\
        ]\
      }\
    ]
  }
}

```

[Previous\\
\\
Inventory Purchase Order](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/) [Next\\
\\
Inventory Purchase Return](https://docs.haravan.com/docs/omni-apis/inventory-purchase-returns/)

- [What you can do with Purchase Receives](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/#what-you-can-do-with-purchase-receives)
- [Purchase Receives properties](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/#purchase-receives-properties)
- [Retrieves a list of purchase receives.](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/#retrieves-a-list-of-purchase-receives)
- [Retrieves single the purchase receive.](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/#retrieves-single-the-purchase-receive)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.