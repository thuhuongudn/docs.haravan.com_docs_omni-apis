---
url: "https://docs.haravan.com/docs/omni-apis/orders/"
title: "Order | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/orders/#)

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

    - [Order](https://docs.haravan.com/docs/omni-apis/orders/)
    - [Refund](https://docs.haravan.com/docs/omni-apis/refunds/)
    - [Transaction](https://docs.haravan.com/docs/omni-apis/transactions/)
  - [Products](https://docs.haravan.com/docs/omni-apis/collects/)

  - [Shipping](https://docs.haravan.com/docs/omni-apis/shipping-rates/)

  - [Store properties](https://docs.haravan.com/docs/omni-apis/country/)

  - [Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [Home page](https://docs.haravan.com/)
- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)
- Orders

On this page

# Order

`Version: 1.0`

An order is a customer's request to purchase one or more products from a shop. You can create, retrieve, update, and delete orders using the Order resource.

![omni_api_comment_img01](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/42073556554/original/536sFLe7U7-3Q7eIxwnjZVa2fDoPqsckrg.png?1631085567)

You should note that orders can be created through the API, but no payment information will be collected, and no transaction performed. You can mark the order with any payment status. Orders cannot be created through the store's admin panel. The only way to create an order and accept payments via haravan is by entering the storefront, adding items to the cart, and completing checkout.

You should also note that you can change only a few of an order's attributes using the API. You cannot change the items or the quantities in an order.

Orders that have been created via the haravan POS will not necessarily have customer information attached to them.

**Authenticated access scopes**: `com.read_orders` , `com.write_orders`

### What you can do with Orders [​](https://docs.haravan.com/docs/omni-apis/orders/\#what-you-can-do-with-orders "Direct link to heading")

The Haravan API lets you do the following with the Order resource.

- GET `https://apis.haravan.com/com/orders.json`
  - **[Retrieves a list of orders](https://docs.haravan.com/docs/omni-apis/orders/#retrieves-a-list-of-orders)**
- GET `https://apis.haravan.com/com/orders/count.json`
  - **[Retrieve a count of the orders](https://docs.haravan.com/docs/omni-apis/orders/#retrieve-a-count-of-the-orders)**
- GET `https://apis.haravan.com/com/orders/{order_id}.json`
  - **[Retrieves single the order](https://docs.haravan.com/docs/omni-apis/orders/#retrieves-single-the-order)**
- POST `https://apis.haravan.com/com/orders.json`
  - **[Create a new order](https://docs.haravan.com/docs/omni-apis/orders/#create-a-new-order)**
- POST `https://apis.haravan.com/com/orders/{order_id}/confirm.json`
  - **[Confirm an order](https://docs.haravan.com/docs/omni-apis/orders/#confirm-an-order)**
- POST `https://apis.haravan.com/com/orders/{order_id}/close.json`
  - **[Close an order](https://docs.haravan.com/docs/omni-apis/orders/#close-an-order)**
- POST `https://apis.haravan.com/com/orders/{order_id}/open.json`
  - **[Re-open a closed order](https://docs.haravan.com/docs/omni-apis/orders/#re-open-a-closed-order)**
- POST `https://apis.haravan.com/com/orders/{order_id}/cancel.json`
  - **[Cancel an order](https://docs.haravan.com/docs/omni-apis/orders/#cancel-an-order)**
- PUT `https://apis.haravan.com/com/orders/{order_id}.json`
  - **[Update an order](https://docs.haravan.com/docs/omni-apis/orders/#update-an-order)**
- POST `https://apis.haravan.com/com/orders/{order_id}/tags.json`
  - **[Update tags for an order](https://docs.haravan.com/docs/omni-apis/orders/#update-tags-for-an-order)**
- DELETE `https://apis.haravan.com/com/orders/{order_id}/tags.json`
  - **[Delete tags for an order](https://docs.haravan.com/docs/omni-apis/orders/#delete-tags-for-an-order)**
- POST `https://apis.haravan.com/com/orders/{order_id}/assign.json`
  - **[Assign handling user for an order (Support for advanced order processing only)](https://docs.haravan.com/docs/omni-apis/orders/#assign-handling-user-for-an-order-support-for-advanced-order-processing-only)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/orders/\#properties "Direct link to heading")

* * *

`billing_address` : `array`

```codeBlockLines_e6Vv
"billing_address": {

    "address1": "182 Lê Đại Hành",

    "address2": null,

    "city": null,

    "company": null,

    "country": "Vietnam",

    "first_name": "Haravan Demo",

    "id": 1036847352,

    "last_name": null,

    "phone": null,

    "province": "Hồ Chí Minh",

    "zip": null,

    "name": " Haravan Demo",

    "province_code": "HC",

    "country_code": "VN",

    "default": true,

    "district": "Quận 11",

    "district_code": "HC476",

    "ward": "Phường 15",

    "ward_code": "27208"

}

```

The mailing address is associated with the payment method. This address is an optional field that won't be available on orders that do not require a payment method. It has the following properties:

- **address1**: The street address of the billing address.
- **address2**: An optional additional field for the street address of the billing address.
- **city**: The city, town, or village of the billing address.
- **company**: The company of the person associated with the billing address.
- **country**: The name of the country of the billing address.
- **country\_code**: The two-letter code (ISO 3166-1 format) for the country of the billing address.
- **first\_name**: The first name of the person associated with the payment method.
- **last\_name**: The last name of the person associated with the payment method.
- **latitude**: The latitude of the billing address.
- **longitude**: The longitude of the billing address.
- **name**: The full name of the person associated with the payment method.
- **phone**: The phone number at the billing address.
- **province**: The name of the region (for example, province, state, or prefecture) of the billing address.
- **province\_code**: The two-letter abbreviation of the region of the billing address.
- **zip**: The postal code (for example, zip, postcode, or Eircode) of the billing address.

`browser_ip`: `string`

```codeBlockLines_e6Vv
"browser_ip":  null

```

Whether the customer consented to receive email updates from the shop.

`cancel_reason`: `string`

```codeBlockLines_e6Vv
"cancel_reason":  "customer"

```

The reason why the order was cancelled. If the order was not cancelled, this value is "null." If the order was cancelled, the value will be one of the following:

- **customer**: The customer changed or cancelled the order.
- **fraud**: The order was fraudulent.
- **inventory**: Items in the order were not in inventory.
- **declined**: The payment was declined.
- **other**: The order was cancelled for a reason not in the list above.

`cancelled_at`: `string`

```codeBlockLines_e6Vv
"cancelled_at":  null

```

The date and time when the order was cancelled. If the order was cancelled, the API returns this value in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format. If the order was not cancelled, this value is "null".

`cart_token`: `string`

```codeBlockLines_e6Vv
"cart_token":  "68778783ad298f1c80c3bafcddeea"

```

Unique identifier for a particular cart that is attached to a particular order.

`checkout_token`: `string`

```codeBlockLines_e6Vv
"checkout_token":  "bd5a8aa1ecd019dd3520ff791ee3a24c"

```

A unique value when referencing the checkout that's associated with the order.

`client_details`: `array`

```codeBlockLines_e6Vv
"client_details": {

    "accept_language": null,

    "browser_ip": null,

    "session_hash": null,

    "user_agent": null,

    "browser_height": null,

    "browser_width": null

}

```

Information about the browser that the customer used when they placed their order:

- **accept\_language**: The languages and locales that the browser understands.
- **browser\_height**: The browser screen height in pixels, if available.
- **browser\_ip**: The browser IP address.
- **browser\_width**: The browser screen width in pixels, if available.
- **session\_hash**: A hash of the session.
- **user\_agent**: Details of the browsing client, including software and operating versions.

`closed_at`: `string`

```codeBlockLines_e6Vv
"closed_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the order was closed. Returns null if the order isn't closed.

`created_at`: `string`

```codeBlockLines_e6Vv
"created_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the order was created.

`currency`: `string`

```codeBlockLines_e6Vv
"currency": "VND"

```

The three-letter code ( [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217?_ga=2.240635079.534032659.1661757906-719915652.1652320921) format) for the shop currency.

`customer`: `array`

```codeBlockLines_e6Vv
"customer": {

    "accepts_marketing": false,

    "addresses": [\
\
        {\
\
            "address1": "182 Lê Đại Hành",\
\
            "address2": null,\
\
            "city": null,\
\
            "company": null,\
\
            "country": "Vietnam",\
\
            "first_name": "Haravan Demo",\
\
            "id": 1056185840,\
\
            "last_name": null,\
\
            "phone": null,\
\
            "province": "Hồ Chí Minh",\
\
            "zip": null,\
\
            "name": " Haravan Demo",\
\
            "province_code": "HC",\
\
            "country_code": "vn",\
\
            "default": true,\
\
            "district": "Quận 11",\
\
            "district_code": "HC476",\
\
            "ward": "Phường 15",\
\
            "ward_code": "27208"\
\
        }\
\
    ],

    "created_at": "2020-09-18T04:12:10.236Z",

    "default_address": {

        "address1": "182 Lê Đại Hành",

        "address2": null,

        "city": null,

        "company": null,

        "country": "Vietnam",

        "first_name": "Haravan Demo",

        "id": 1056185840,

        "last_name": null,

        "phone": null,

        "province": "Hồ Chí Minh",

        "zip": null,

        "name": " Haravan Demo",

        "province_code": "HC",

        "country_code": "vn",

        "default": true,

        "district": "Quận 11",

        "district_code": "HC476",

        "ward": "Phường 15",

        "ward_code": "27208"

    },

    "email": "hello@haravan.com",

    "phone": null,

    "first_name": "Haravan Demo",

    "id": 1036847352,

    "multipass_identifier": null,

    "last_name": null,

    "last_order_id": 1138637123,

    "last_order_name": "#100027",

    "note": "Demo     ",

    "orders_count": 28,

    "state": "Disabled",

    "tags": null,

    "total_spent": 261380000.0000,

    "total_paid": 0.0,

    "updated_at": "2021-01-04T22:00:52.558Z",

    "verified_email": false,

    "send_email_invite": false,

    "send_email_welcome": false,

    "password": null,

    "password_confirmation": null,

    "group_name": null,

    "birthday": null,

    "gender": null,

    "last_order_date": null

}

```

Information about the customer. The order might not have a customer and apps should not depend on the existence of a `customer` object. This value might be null if the order was created through Haravan POS. For more information about the customer object, see the [Customer resource](https://docs.haravan.com/docs/omni-apis/customer/).

`discount_codes`: `array`

```codeBlockLines_e6Vv
"discount_codes": [\
\
    {\
\
        "code": "SPRING30",\
\
        "amount": 300000.0000,\
\
        "type": "fixed_amount"\
\
    }\
\
]

```

Applicable discount codes that can be applied to the order. If no codes exist the value will default to blank.A Discount code will include the following fields:

- **amount**: The amount of the discount.
- **code**: The discount code.
- **type**: The type of discount. Can be one of: "percentage", "shipping", "fixed\_amount" (default).

`email`: `string`

```codeBlockLines_e6Vv
"email": "hello@haravan.com"

```

The customer's email address.

`financial_status`: `string`

```codeBlockLines_e6Vv
"financial_status": "paid"

```

The status of payments associated with the order. Can only be set when the order is created. Valid values:

- **pending**: The payments are pending. Payment might fail in this state. Check again to confirm whether the payments have been paid successfully.
- **authorized**: The payments have been authorized.
- **partially\_paid**: The order has been partially paid.
- **paid**: The payments have been paid.
- **partially\_refunded**: The payments have been partially refunded.
- **refunded**: The payments have been refunded.
- **voided**: The payments have been voided.

`fulfillments`: `array`

```codeBlockLines_e6Vv
"fulfillments": []

```

An array of fulfillments associated with the order.

`fulfillment_status`: `string`

```codeBlockLines_e6Vv
"fulfillment_status": "partial"

```

The order's status in terms of fulfilled line items. Valid values:

- **fulfilled**: Every line item in the order has been fulfilled.
- **null**: None of the line items in the order have been fulfilled.
- **partial**: At least one line item in the order has been fulfilled.
- **restocked**: Every line item in the order has been restocked and the order canceled.

`tags`: `string`

```codeBlockLines_e6Vv
"tags": null

```

Tags are additional short descriptors, commonly used for filtering and searching, formatted as a string of comma-separated values. For example, if an order has three tags: tag1, tag2, tag3. Each individual tag is limited to 40 characters in length.

`gateway`: `string`

```codeBlockLines_e6Vv
"gateway": "Thanh toán khi giao hàng (COD)"

```

The payment gateway used.

`gateway_code`: `string`

```codeBlockLines_e6Vv
"gateway_code": "COD"

```

The unique identifier for the payment gateway used.

`id`: `number`

```codeBlockLines_e6Vv
"id": 632910392

```

The ID of the order, used for API purposes. This is different from the order\_number property, which is the ID used by the shop owner and customer.

`landing_site`: `string`

```codeBlockLines_e6Vv
"landing_site": "http://www.example.com?source=abc"

```

The URL for the page where the buyer landed when they entered the shop.

`landing_site_ref`: `string`

```codeBlockLines_e6Vv
"landing_site_ref": "haravan"

```

The ref for the page where the buyer landed when they entered the shop.

`line_items`: `array`

```codeBlockLines_e6Vv
"line_items": [\
\
    {\
\
        "fulfillable_quantity": 22,\
\
        "fulfillment_service": null,\
\
        "fulfillment_status": "notfulfilled",\
\
        "grams": 0.0000,\
\
        "id": 1160828322,\
\
        "price": 600000.0000,\
\
        "price_original": 600000.0000,\
\
        "price_promotion": 0.0,\
\
        "product_id": 1028183659,\
\
        "quantity": 22,\
\
        "requires_shipping": true,\
\
        "sku": null,\
\
        "title": "Đầm babydoll tay lỡ khoét lỗ",\
\
        "variant_id": 1061514693,\
\
        "variant_title": "Default Title",\
\
        "vendor": "Khác",\
\
        "type": "Khác",\
\
        "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
\
        "gift_card": false,\
\
        "taxable": true,\
\
        "tax_lines": null,\
\
        "product_exists": true,\
\
        "barcode": null,\
\
        "properties": null,\
\
        "total_discount": 0.0000,\
\
        "applied_discounts": [],\
\
        "image": {\
\
            "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
\
            "attactment": null,\
\
            "filename": null\
\
        },\
\
        "not_allow_promotion": false,\
\
        "ma_cost_amount": 0.00\
\
    }\
\
]

```

A list of line item objects, each containing information about an item in the order. Each object has the following properties:

- **fulfillable\_quantity**: The amount available to fulfill. This is the quantity - max(refunded\_quantity, fulfilled\_quantity) - pending\_fulfilled\_quantity.
- **fulfillment\_service**: Service provider who is doing the fulfillment. Valid values are either "manual" or the name of the provider. eg: "amazon", "shipwire", etc.
- **fulfillment\_status**: How far along an order is in terms line items fulfilled. Valid values are: fulfilled, null or partial.
- **grams**: The weight of the item in grams.
- **id**: The id of the line item.
- **price**: The price of the item before discounts have been applied.
- **product\_id**: The unique numeric identifier for the product in the fulfillment. Can be null if the original product associated with the order is deleted at a later date.
- **quantity**: The number of products that were purchased.
- **requires\_shipping**: States whether or not the fulfillment requires shipping. Values are: true or false.
- **sku**: A unique identifier of the item in the fulfillment.
- **title**: The title of the product.
- **variant\_id**: The id of the product variant.
- **variant\_title**: The title of the product variant.
- **vendor**: The name of the supplier of the item.
- **name**: The name of the product variant.
- **gift\_card**: States wether or not the line\_item is a gift card. If so, the item is not taxed or considered for shipping charges.
- **taxable**: States whether or not the product was taxable. Values are: true or false.
- **tax\_lines**: A list of tax\_line objects, each of which details the taxes applicable to this line\_item.
- **total\_discount**: The total discount amount applied to this line item. This value is not subtracted in the line item price.

`name`: `string`

```codeBlockLines_e6Vv
"name": "#100020"

```

The order name, generated by combining the order\_number property with the order prefix and suffix that are set in the merchant's general settings. This is different from the id property, which is the ID of the order used by the API. This field can also be set by the API to be any string value.

`note`: `string`

```codeBlockLines_e6Vv
"note":"Customer changed their mind."

```

An optional note that a shop owner can attach to the order.

`number`: `number`

```codeBlockLines_e6Vv
"number": 1138637099

```

The order's position in the shop's count of orders.

`order_number`: `string`

```codeBlockLines_e6Vv
"order_number": "#100020"

```

A unique numeric identifier for the order. This one is used by the shop owner and customer. This is different from the id property, which is also a unique numeric identifier for the order, but used for API purposes.

`processing_method`: `string`

```codeBlockLines_e6Vv
"processing_method": null

```

How the payment was processed. It has the following valid values:

- **checkout**: The order was processed using the Haravan checkout.
- **direct**: The order was processed using a direct payment provider.
- **manual**: The order was processed using a manual payment method.
- **offsite**: The order was processed by an external payment provider to the Haravan checkout.

`referring_site`: `array`

```codeBlockLines_e6Vv
"refunds":[]

```

A list of refunds applied to the order. For more information, see the Refund API.

`shipping_address`: `array`

```codeBlockLines_e6Vv
"shipping_address": {

    "address1": "182 Lê Đại Hành",

    "address2": null,

    "city": null,

    "company": null,

    "country": "Vietnam",

    "first_name": "Haravan Demo",

    "last_name": null,

    "latitude": 0.00000000,

    "longitude": 0.00000000,

    "phone": null,

    "province": "Hồ Chí Minh",

    "zip": null,

    "name": " Haravan Demo",

    "province_code": "HC",

    "country_code": "VN",

    "district_code": "HC476",

    "district": "Quận 11",

    "ward_code": "27208",

    "ward": "Phường 15"

}

```

The mailing address to where the order will be shipped. This address is optional and will not be available on orders that do not require shipping. It has the following properties:

- **address1**: The street address of the shipping address.
- **address2**: An optional additional field for the street address of the shipping address.
- **city**: The city, town, or village of the shipping address.
- **company**: The company of the person associated with the shipping address.
- **country**: The name of the country of the shipping address.
- **country\_code**: The two-letter code (ISO 3166-1 format) for the country of the shipping address.
- **first\_name**: The first name of the person associated with the shipping address.
- **last\_name**: The last name of the person associated with the shipping address.
- **latitude**: The latitude of the shipping address.
- **longitude**: The longitude of the shipping address.
- **name**: The full name of the person associated with the payment method.
- **phone**: The phone number at the shipping address.
- **province**: The name of the region (for example, province, state, or prefecture) of the shipping address.
- **province\_code**: The two-letter abbreviation of the region of the shipping address.
- **zip**: The postal code (for example, zip, postcode, or Eircode) of the shipping address.

`fishipping_lineseld`: `array`

```codeBlockLines_e6Vv

"shipping_lines": [\
\
    {\
\
        "code": null,\
\
        "price": 0.0000,\
\
        "source": null,\
\
        "title": null\
\
    }\
\
]

```

An array of objects, each of which details a shipping method used. Each object has the following properties:

- **code**: A reference to the shipping method.
- **price**: The price of this shipping method.
- **source**: The source of the shipping method.
- **title**: The title of the shipping method.
- **tax\_lines**: A list of tax\_line objects, each of which details the taxes applicable to this shipping\_line.

`source_name`: `string`

```codeBlockLines_e6Vv
"source_name":"web"

```

Where the order originated. Can be set only during order creation, and is not writeable afterwards. Values for haravan channels are protected and cannot be assigned by other API clients: web, pos, haravan\_draft\_order, iphone, and android. Orders created via the API can be assigned any other string of your choice. If unspecified, then new orders are assigned the value of your app's ID.

`subtotal_price`: `number`

```codeBlockLines_e6Vv
"subtotal_price":100000.0000

```

The price of the order in the shop currency after discounts but before shipping, duties, taxes, and tips.

`tax_lines`: `string`

```codeBlockLines_e6Vv
"tax_lines":null

```

An array of tax\_line objects, each of which details the total taxes applicable to the order. Each tax\_line has the following properties:

- **price**: The amount of tax to be charged.
- **rate**: The rate of tax to be applied.
- **title**: The name of the tax.

`taxes_included`: `string`

```codeBlockLines_e6Vv
"taxes_included":null

```

States whether or not taxes are included in the order subtotal. Valid values are "true" or "false".

`token`: `string`

```codeBlockLines_e6Vv
"token":"19627118f2e844ddb3a0c8d73f99a580"

```

A unique value when referencing the order.

`total_discounts`: `number`

```codeBlockLines_e6Vv
"total_discounts":0.0000

```

The total discounts applied to the price of the order in the shop currency.

`total_line_items_price`: `number`

```codeBlockLines_e6Vv
"total_line_items_price":13200000.0000

```

The sum of all line item prices in the shop currency.

`total_price`: `number`

```codeBlockLines_e6Vv
"total_price":13200000.0000

```

The sum of all line item prices, discounts, shipping, taxes, and tips in the shop currency. Must be positive.

`total_tax`: `number`

```codeBlockLines_e6Vv
"total_tax":0.0000

```

The sum of all the taxes applied to the order in the shop currency. Must be positive.

`image_id`: `number`

```codeBlockLines_e6Vv
"image_id":null

```

The unique numeric identifier for one of the product's images.

`total_weight`: `number`

```codeBlockLines_e6Vv
"total_weight":0.0000

```

The sum of all line item weights in grams. The sum is not adjusted as items are removed from the order.

`updated_at`: `string`

```codeBlockLines_e6Vv
"updated_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the order was updated.

`transactions`: `array`

```codeBlockLines_e6Vv
"transactions":[]

```

Information about the transaction. For more information about the transaction object, see the resource.

`note_attributes`: `array`

```codeBlockLines_e6Vv

"note_attributes": [\
\
  {\
\
    "name": "custom name",\
\
    "value": "custom value"\
\
  }\
\
]

```

Extra information that is added to the order. Appears in the Additional details section of an order details page. Each array entry must contain a hash with name and value keys.

`confirmed_at`: `string`

```codeBlockLines_e6Vv
"confirmed_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the order was confirmed.

`closed_status`: `string`

```codeBlockLines_e6Vv
"closed_status":"unclosed"

```

Status when order has been closed.

`cancelled_status`: `string`

```codeBlockLines_e6Vv
"cancelled_status":"uncancelled"

```

Status when order has been cancelled.

`confirmed_status`: `string`

```codeBlockLines_e6Vv
"confirmed_status":"unconfirmed"

```

Status when order has been confirmed.

`user_id`: `number`

```codeBlockLines_e6Vv
"user_id":31522279

```

The ID of the user logged into Haravan POS who processed the order, if applicable.

`location_id`: `number`

```codeBlockLines_e6Vv
"location_id":963414

```

The ID of the physical location where the order was processed.

`contact_email`: `string`

```codeBlockLines_e6Vv
"contact_email":hello@haravan.com

```

The contact email of the buyer.

### Retrieves a list of orders [​](https://docs.haravan.com/docs/omni-apis/orders/\#retrieves-a-list-of-orders "Direct link to heading")

GET

https://apis.haravan.com/com/orders.json

Retrieves a list of orders. You can filter resources by params.

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/orders/\#parameters "Direct link to heading")

* * *

`ids`

A comma-separated list of order ids.

* * *

`limit` `integer` `≤50` `default 50`

The maximum number of results to show on a page.

* * *

`page`

Page to show the result.

* * *

`since_id`

Restrict results to after the specified ID.

* * *

`created_at_min`

Show orders created after date. (format: 2021-10-20T14:07:45.084Z)

* * *

`created_at_max`

Show orders created before date. (format: 2021-10-20T14:07:45.084Z)

* * *

`updated_at_min`

Show orders last updated after date. (format: 2021-10-20T14:07:45.084Z)

* * *

`updated_at_max`

Show orders last updated before date. (format: 2021-10-20T14:07:45.084Z)

* * *

`processed_at_min`

Show orders imported after date. (format: 2021-10-20T14:07:45.084Z)

* * *

`processed_at_max`

Show orders imported before date. (format: 2021-10-20T14:07:45.084Z)

* * *

`financial_status`

The current payment status.

- **pending**: Show only pending orders.

- **paid**: Show only paid orders.

- **partially\_paid**: Show only partially paid orders.

- **refunded**: Show only refunded orders.

- **voided**: Show only voided orders.

- **partially\_refunded**: Show only partially refunded orders.


* * *

`fulfillment_status`

The current fulfillment status of the order.

- **unshipped**: Show orders that haven't been shipped.

- **shipped**: Show orders that have been shipped.

- **partial**: Show partially shipped orders.


* * *

`status`

The current orders status of the order.

- **open**: Show only open orders.

- **closed**: Show only closed orders.

- **cancelled**: Show only canceled orders.

- **any**: Show orders of any status, including archived orders.


* * *

`fields`

comma-separated list of fields to include in the response.

* * *

`order`

Sort response data. The fields that can sort by are `created_at` and `updated_at`

Sort ascending:

```codeBlockLines_e6Vv
  &order=created_at%20asc
  &order=updated_at%20asc

```

Sort descending:

```codeBlockLines_e6Vv
  &order=created_at%20desc
  &order=updated_at%20desc

```

* * *

Retrieve all orders by page number. By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/com/orders.json?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "orders": [\
        {\
            "billing_address": {\
                "address1": "182 Lê Đại Hành",\
                "address2": null,\
                "city": null,\
                "company": null,\
                "country": "Vietnam",\
                "first_name": "Haravan Demo",\
                "id": 1036847352,\
                "last_name": null,\
                "phone": null,\
                "province": "Hồ Chí Minh",\
                "zip": null,\
                "name": " Haravan Demo",\
                "province_code": "HC",\
                "country_code": "VN",\
                "default": true,\
                "district": "Quận 11",\
                "district_code": "HC476",\
                "ward": "Phường 15",\
                "ward_code": "27208"\
            },\
            "browser_ip": null,\
            "buyer_accepts_marketing": false,\
            "cancel_reason": null,\
            "cancelled_at": null,\
            "cart_token": "19627118f2e844ddb3a0c8d73f99a580",\
            "checkout_token": "19627118f2e844ddb3a0c8d73f99a580",\
            "client_details": {\
                "accept_language": null,\
                "browser_ip": null,\
                "session_hash": null,\
                "user_agent": null,\
                "browser_height": null,\
                "browser_width": null\
            },\
            "closed_at": null,\
            "created_at": "2020-09-19T01:12:10.062Z",\
            "currency": "VND",\
            "customer": {\
                "accepts_marketing": false,\
                "addresses": [\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185840,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": true,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185854,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185852,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185851,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185850,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185849,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185847,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185845,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185844,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185843,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    }\
                ],\
                "created_at": "2020-09-18T04:12:10.236Z",\
                "default_address": {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1056185840,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                "email": "hello@haravan.com",\
                "phone": null,\
                "first_name": "Haravan Demo",\
                "id": 1036847352,\
                "multipass_identifier": null,\
                "last_name": null,\
                "last_order_id": 1138637123,\
                "last_order_name": "#100027",\
                "note": "Demo     ",\
                "orders_count": 28,\
                "state": "Disabled",\
                "tags": null,\
                "total_spent": 261380000.0000,\
                "total_paid": 0.0,\
                "updated_at": "2021-01-04T22:00:52.558Z",\
                "verified_email": false,\
                "send_email_invite": false,\
                "send_email_welcome": false,\
                "password": null,\
                "password_confirmation": null,\
                "group_name": null,\
                "birthday": null,\
                "gender": null,\
                "last_order_date": null\
            },\
            "discount_codes": [],\
            "email": "hello@haravan.com",\
            "financial_status": "paid",\
            "fulfillments": [],\
            "fulfillment_status": "notfulfilled",\
            "tags": null,\
            "gateway": "COD",\
            "gateway_code": null,\
            "id": 1138637099,\
            "landing_site": null,\
            "landing_site_ref": null,\
            "source": "web",\
            "line_items": [\
                {\
                    "fulfillable_quantity": 22,\
                    "fulfillment_service": null,\
                    "fulfillment_status": "notfulfilled",\
                    "grams": 0.0000,\
                    "id": 1160828322,\
                    "price": 600000.0000,\
                    "price_original": 600000.0000,\
                    "price_promotion": 0.0,\
                    "product_id": 1028183659,\
                    "quantity": 22,\
                    "requires_shipping": true,\
                    "sku": null,\
                    "title": "Đầm babydoll tay lỡ khoét lỗ",\
                    "variant_id": 1061514693,\
                    "variant_title": "Default Title",\
                    "vendor": "Khác",\
                    "type": "Khác",\
                    "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                    "gift_card": false,\
                    "taxable": true,\
                    "tax_lines": null,\
                    "product_exists": true,\
                    "barcode": null,\
                    "properties": null,\
                    "total_discount": 0.0000,\
                    "applied_discounts": [],\
                    "image": {\
                        "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                        "attactment": null,\
                        "filename": null\
                    },\
                    "not_allow_promotion": false,\
                    "ma_cost_amount": 0.00\
                }\
            ],\
            "name": "#100020",\
            "note": null,\
            "number": 1138637099,\
            "order_number": "#100020",\
            "processing_method": null,\
            "referring_site": null,\
            "refunds": [],\
            "shipping_address": {\
                "address1": "182 Lê Đại Hành",\
                "address2": null,\
                "city": null,\
                "company": null,\
                "country": "Vietnam",\
                "first_name": "Haravan Demo",\
                "last_name": null,\
                "latitude": 0.00000000,\
                "longitude": 0.00000000,\
                "phone": null,\
                "province": "Hồ Chí Minh",\
                "zip": null,\
                "name": " Haravan Demo",\
                "province_code": "HC",\
                "country_code": "VN",\
                "district_code": "HC476",\
                "district": "Quận 11",\
                "ward_code": "27208",\
                "ward": "Phường 15"\
            },\
            "shipping_lines": [\
                {\
                    "code": null,\
                    "price": 0.0000,\
                    "source": null,\
                    "title": null\
                }\
            ],\
            "source_name": "web",\
            "subtotal_price": 13200000.0000,\
            "tax_lines": null,\
            "taxes_included": false,\
            "token": "19627118f2e844ddb3a0c8d73f99a580",\
            "total_discounts": 0.0000,\
            "total_line_items_price": 13200000.0000,\
            "total_price": 13200000.0000,\
            "total_tax": 0.0,\
            "total_weight": 0.0000,\
            "updated_at": "2020-09-18T04:12:21.837Z",\
            "transactions": [\
                {\
                    "amount": 13200000.0000,\
                    "authorization": null,\
                    "created_at": "2020-09-19T01:12:10.062Z",\
                    "device_id": null,\
                    "gateway": "COD",\
                    "id": 1055329694,\
                    "kind": "capture",\
                    "order_id": 1138637099,\
                    "receipt": null,\
                    "status": null,\
                    "test": false,\
                    "user_id": 0,\
                    "location_id": 963414,\
                    "payment_details": null,\
                    "parent_id": 1055329693,\
                    "currency": "VND",\
                    "haravan_transaction_id": null,\
                    "external_transaction_id": null,\
                    "send_email": false\
                },\
                {\
                    "amount": 13200000.0000,\
                    "authorization": null,\
                    "created_at": "2020-09-19T01:12:10.062Z",\
                    "device_id": null,\
                    "gateway": "COD",\
                    "id": 1055329693,\
                    "kind": "pending",\
                    "order_id": 1138637099,\
                    "receipt": null,\
                    "status": null,\
                    "test": false,\
                    "user_id": 0,\
                    "location_id": 963414,\
                    "payment_details": null,\
                    "parent_id": null,\
                    "currency": "VND",\
                    "haravan_transaction_id": null,\
                    "external_transaction_id": null,\
                    "send_email": false\
                }\
            ],\
            "note_attributes": [],\
            "confirmed_at": null,\
            "closed_status": "unclosed",\
            "cancelled_status": "uncancelled",\
            "confirmed_status": "unconfirmed",\
            "user_id": 0,\
            "device_id": null,\
            "location_id": 963414,\
            "ref_order_id": 0,\
            "ref_order_number": null,\
            "utm_source": null,\
            "utm_medium": null,\
            "utm_campaign": null,\
            "utm_term": null,\
            "utm_content": null,\
            "redeem_model": null,\
            "omni_order_status": 0,\
            "omni_order_status_name": null,\
            "location_assigned_at": null,\
            "in_stock_at": null,\
            "out_of_stock_at": null,\
            "export_at": null,\
            "complete_at": null,\
            "payment_url": null,\
            "contact_email": "hello@haravan.com"\
        }\
    ]
}

```

Retrieve orders last updated after 2021-01-04T00:00:00.000Z.

- GET `https://apis.haravan.com/com/orders.json?updated_at_min=2021-01-04T00:00:00.000Z`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "order": {
            "billing_address": {
                "address1": "182 Lê Đại Hành",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": "Haravan Demo",
                "id": 1036847352,
                "last_name": null,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": null,
                "name": " Haravan Demo",
                "province_code": "HC",
                "country_code": "VN",
                "default": true,
                "district": "Quận 11",
                "district_code": "HC476",
                "ward": "Phường 15",
                "ward_code": "27208"
            },
            "browser_ip": null,
            "buyer_accepts_marketing": false,
            "cancel_reason": null,
            "cancelled_at": null,
            "cart_token": "19627118f2e844ddb3a0c8d73f99a580",
            "checkout_token": "19627118f2e844ddb3a0c8d73f99a580",
            "client_details": {
                "accept_language": null,
                "browser_ip": null,
                "session_hash": null,
                "user_agent": null,
                "browser_height": null,
                "browser_width": null
            },
            "closed_at": null,
            "created_at": "2020-09-19T01:12:10.062Z",
            "currency": "VND",
            "customer": {
                "accepts_marketing": false,
                "addresses": [\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185840,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": true,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185854,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185852,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185851,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185850,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185849,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185847,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185845,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185844,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185843,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    }\
                ],
                "created_at": "2020-09-18T04:12:10.236Z",
                "default_address": {
                    "address1": "182 Lê Đại Hành",
                    "address2": null,
                    "city": null,
                    "company": null,
                    "country": "Vietnam",
                    "first_name": "Haravan Demo",
                    "id": 1056185840,
                    "last_name": null,
                    "phone": null,
                    "province": "Hồ Chí Minh",
                    "zip": null,
                    "name": " Haravan Demo",
                    "province_code": "HC",
                    "country_code": "vn",
                    "default": true,
                    "district": "Quận 11",
                    "district_code": "HC476",
                    "ward": "Phường 15",
                    "ward_code": "27208"
                },
                "email": "hello@haravan.com",
                "phone": null,
                "first_name": "Haravan Demo",
                "id": 1036847352,
                "multipass_identifier": null,
                "last_name": null,
                "last_order_id": 1138637123,
                "last_order_name": "#100027",
                "note": "Demo     ",
                "orders_count": 28,
                "state": "Disabled",
                "tags": null,
                "total_spent": 261380000.0000,
                "total_paid": 0.0,
                "updated_at": "2021-01-04T22:00:52.558Z",
                "verified_email": false,
                "send_email_invite": false,
                "send_email_welcome": false,
                "password": null,
                "password_confirmation": null,
                "group_name": null,
                "birthday": null,
                "gender": null,
                "last_order_date": null
            },
            "discount_codes": [],
            "email": "hello@haravan.com",
            "financial_status": "paid",
            "fulfillments": [],
            "fulfillment_status": "notfulfilled",
            "tags": null,
            "gateway": "COD",
            "gateway_code": null,
            "id": 1138637099,
            "landing_site": null,
            "landing_site_ref": null,
            "source": "web",
            "line_items": [\
                {\
                    "fulfillable_quantity": 22,\
                    "fulfillment_service": null,\
                    "fulfillment_status": "notfulfilled",\
                    "grams": 0.0000,\
                    "id": 1160828322,\
                    "price": 600000.0000,\
                    "price_original": 600000.0000,\
                    "price_promotion": 0.0,\
                    "product_id": 1028183659,\
                    "quantity": 22,\
                    "requires_shipping": true,\
                    "sku": null,\
                    "title": "Đầm babydoll tay lỡ khoét lỗ",\
                    "variant_id": 1061514693,\
                    "variant_title": "Default Title",\
                    "vendor": "Khác",\
                    "type": "Khác",\
                    "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                    "gift_card": false,\
                    "taxable": true,\
                    "tax_lines": null,\
                    "product_exists": true,\
                    "barcode": null,\
                    "properties": null,\
                    "total_discount": 0.0000,\
                    "applied_discounts": [],\
                    "image": {\
                        "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                        "attactment": null,\
                        "filename": null\
                    },\
                    "not_allow_promotion": false,\
                    "ma_cost_amount": 0.00\
                }\
            ],
            "name": "#100020",
            "note": null,
            "number": 1138637099,
            "order_number": "#100020",
            "processing_method": null,
            "referring_site": null,
            "refunds": [],
            "shipping_address": {
                "address1": "182 Lê Đại Hành",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": "Haravan Demo",
                "last_name": null,
                "latitude": 0.00000000,
                "longitude": 0.00000000,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": null,
                "name": " Haravan Demo",
                "province_code": "HC",
                "country_code": "VN",
                "district_code": "HC476",
                "district": "Quận 11",
                "ward_code": "27208",
                "ward": "Phường 15"
            },
            "shipping_lines": [\
                {\
                    "code": null,\
                    "price": 0.0000,\
                    "source": null,\
                    "title": null\
                }\
            ],
            "source_name": "web",
            "subtotal_price": 13200000.0000,
            "tax_lines": null,
            "taxes_included": false,
            "token": "19627118f2e844ddb3a0c8d73f99a580",
            "total_discounts": 0.0000,
            "total_line_items_price": 13200000.0000,
            "total_price": 13200000.0000,
            "total_tax": 0.0,
            "total_weight": 0.0000,
            "updated_at": "2020-09-18T04:12:21.837Z",
            "transactions": [\
                {\
                    "amount": 13200000.0000,\
                    "authorization": null,\
                    "created_at": "2020-09-19T01:12:10.062Z",\
                    "device_id": null,\
                    "gateway": "COD",\
                    "id": 1055329694,\
                    "kind": "capture",\
                    "order_id": 1138637099,\
                    "receipt": null,\
                    "status": null,\
                    "test": false,\
                    "user_id": 0,\
                    "location_id": 963414,\
                    "payment_details": null,\
                    "parent_id": 1055329693,\
                    "currency": "VND",\
                    "haravan_transaction_id": null,\
                    "external_transaction_id": null,\
                    "send_email": false\
                },\
                {\
                    "amount": 13200000.0000,\
                    "authorization": null,\
                    "created_at": "2020-09-19T01:12:10.062Z",\
                    "device_id": null,\
                    "gateway": "COD",\
                    "id": 1055329693,\
                    "kind": "pending",\
                    "order_id": 1138637099,\
                    "receipt": null,\
                    "status": null,\
                    "test": false,\
                    "user_id": 0,\
                    "location_id": 963414,\
                    "payment_details": null,\
                    "parent_id": null,\
                    "currency": "VND",\
                    "haravan_transaction_id": null,\
                    "external_transaction_id": null,\
                    "send_email": false\
                }\
            ],
            "note_attributes": [],
            "confirmed_at": null,
            "closed_status": "unclosed",
            "cancelled_status": "uncancelled",
            "confirmed_status": "unconfirmed",
            "user_id": 0,
            "device_id": null,
            "location_id": 963414,
            "ref_order_id": 0,
            "ref_order_number": null,
            "utm_source": null,
            "utm_medium": null,
            "utm_campaign": null,
            "utm_term": null,
            "utm_content": null,
            "redeem_model": null,
            "omni_order_status": 0,
            "omni_order_status_name": null,
            "location_assigned_at": null,
            "in_stock_at": null,
            "out_of_stock_at": null,
            "export_at": null,
            "complete_at": null,
            "payment_url": null,
            "contact_email": "hello@haravan.com"
      }
   ]
}

```

Retrieve all orders but show only certain properties

- GET `https://apis.haravan.com/com/orders.json?fields=id,name,created_at`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "orders": [\
        {\
        "created_at": "2020-09-19T01:12:10.062Z",\
        "id": 1138637099,\
        "name": "#100020"\
        }\
    ]
}

```

Retrieve all orders after the specified ID.

- GET `https://apis.haravan.com/com/orders.json?since_id=1138637000`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "order": {
            "billing_address": {
                "address1": "182 Lê Đại Hành",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": "Haravan Demo",
                "id": 1036847352,
                "last_name": null,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": null,
                "name": " Haravan Demo",
                "province_code": "HC",
                "country_code": "VN",
                "default": true,
                "district": "Quận 11",
                "district_code": "HC476",
                "ward": "Phường 15",
                "ward_code": "27208"
            },
            "browser_ip": null,
            "buyer_accepts_marketing": false,
            "cancel_reason": null,
            "cancelled_at": null,
            "cart_token": "19627118f2e844ddb3a0c8d73f99a580",
            "checkout_token": "19627118f2e844ddb3a0c8d73f99a580",
            "client_details": {
                "accept_language": null,
                "browser_ip": null,
                "session_hash": null,
                "user_agent": null,
                "browser_height": null,
                "browser_width": null
            },
            "closed_at": null,
            "created_at": "2020-09-19T01:12:10.062Z",
            "currency": "VND",
            "customer": {
                "accepts_marketing": false,
                "addresses": [\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185840,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": true,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185854,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185852,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185851,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185850,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185849,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185847,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185845,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185844,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    },\
                    {\
                        "address1": "182 Lê Đại Hành",\
                        "address2": null,\
                        "city": null,\
                        "company": null,\
                        "country": "Vietnam",\
                        "first_name": "Haravan Demo",\
                        "id": 1056185843,\
                        "last_name": null,\
                        "phone": null,\
                        "province": "Hồ Chí Minh",\
                        "zip": null,\
                        "name": " Haravan Demo",\
                        "province_code": "HC",\
                        "country_code": "vn",\
                        "default": false,\
                        "district": "Quận 11",\
                        "district_code": "HC476",\
                        "ward": "Phường 15",\
                        "ward_code": "27208"\
                    }\
                ],
                "created_at": "2020-09-18T04:12:10.236Z",
                "default_address": {
                    "address1": "182 Lê Đại Hành",
                    "address2": null,
                    "city": null,
                    "company": null,
                    "country": "Vietnam",
                    "first_name": "Haravan Demo",
                    "id": 1056185840,
                    "last_name": null,
                    "phone": null,
                    "province": "Hồ Chí Minh",
                    "zip": null,
                    "name": " Haravan Demo",
                    "province_code": "HC",
                    "country_code": "vn",
                    "default": true,
                    "district": "Quận 11",
                    "district_code": "HC476",
                    "ward": "Phường 15",
                    "ward_code": "27208"
                },
                "email": "hello@haravan.com",
                "phone": null,
                "first_name": "Haravan Demo",
                "id": 1036847352,
                "multipass_identifier": null,
                "last_name": null,
                "last_order_id": 1138637123,
                "last_order_name": "#100027",
                "note": "Demo     ",
                "orders_count": 28,
                "state": "Disabled",
                "tags": null,
                "total_spent": 261380000.0000,
                "total_paid": 0.0,
                "updated_at": "2021-01-04T22:00:52.558Z",
                "verified_email": false,
                "send_email_invite": false,
                "send_email_welcome": false,
                "password": null,
                "password_confirmation": null,
                "group_name": null,
                "birthday": null,
                "gender": null,
                "last_order_date": null
            },
            "discount_codes": [],
            "email": "hello@haravan.com",
            "financial_status": "paid",
            "fulfillments": [],
            "fulfillment_status": "notfulfilled",
            "tags": null,
            "gateway": "COD",
            "gateway_code": null,
            "id": 1138637099,
            "landing_site": null,
            "landing_site_ref": null,
            "source": "web",
            "line_items": [\
                {\
                    "fulfillable_quantity": 22,\
                    "fulfillment_service": null,\
                    "fulfillment_status": "notfulfilled",\
                    "grams": 0.0000,\
                    "id": 1160828322,\
                    "price": 600000.0000,\
                    "price_original": 600000.0000,\
                    "price_promotion": 0.0,\
                    "product_id": 1028183659,\
                    "quantity": 22,\
                    "requires_shipping": true,\
                    "sku": null,\
                    "title": "Đầm babydoll tay lỡ khoét lỗ",\
                    "variant_id": 1061514693,\
                    "variant_title": "Default Title",\
                    "vendor": "Khác",\
                    "type": "Khác",\
                    "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                    "gift_card": false,\
                    "taxable": true,\
                    "tax_lines": null,\
                    "product_exists": true,\
                    "barcode": null,\
                    "properties": null,\
                    "total_discount": 0.0000,\
                    "applied_discounts": [],\
                    "image": {\
                        "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                        "attactment": null,\
                        "filename": null\
                    },\
                    "not_allow_promotion": false,\
                    "ma_cost_amount": 0.00\
                }\
            ],
            "name": "#100020",
            "note": null,
            "number": 1138637099,
            "order_number": "#100020",
            "processing_method": null,
            "referring_site": null,
            "refunds": [],
            "shipping_address": {
                "address1": "182 Lê Đại Hành",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": "Haravan Demo",
                "last_name": null,
                "latitude": 0.00000000,
                "longitude": 0.00000000,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": null,
                "name": " Haravan Demo",
                "province_code": "HC",
                "country_code": "VN",
                "district_code": "HC476",
                "district": "Quận 11",
                "ward_code": "27208",
                "ward": "Phường 15"
            },
            "shipping_lines": [\
                {\
                    "code": null,\
                    "price": 0.0000,\
                    "source": null,\
                    "title": null\
                }\
            ],
            "source_name": "web",
            "subtotal_price": 13200000.0000,
            "tax_lines": null,
            "taxes_included": false,
            "token": "19627118f2e844ddb3a0c8d73f99a580",
            "total_discounts": 0.0000,
            "total_line_items_price": 13200000.0000,
            "total_price": 13200000.0000,
            "total_tax": 0.0,
            "total_weight": 0.0000,
            "updated_at": "2020-09-18T04:12:21.837Z",
            "transactions": [\
                {\
                    "amount": 13200000.0000,\
                    "authorization": null,\
                    "created_at": "2020-09-19T01:12:10.062Z",\
                    "device_id": null,\
                    "gateway": "COD",\
                    "id": 1055329694,\
                    "kind": "capture",\
                    "order_id": 1138637099,\
                    "receipt": null,\
                    "status": null,\
                    "test": false,\
                    "user_id": 0,\
                    "location_id": 963414,\
                    "payment_details": null,\
                    "parent_id": 1055329693,\
                    "currency": "VND",\
                    "haravan_transaction_id": null,\
                    "external_transaction_id": null,\
                    "send_email": false\
                },\
                {\
                    "amount": 13200000.0000,\
                    "authorization": null,\
                    "created_at": "2020-09-19T01:12:10.062Z",\
                    "device_id": null,\
                    "gateway": "COD",\
                    "id": 1055329693,\
                    "kind": "pending",\
                    "order_id": 1138637099,\
                    "receipt": null,\
                    "status": null,\
                    "test": false,\
                    "user_id": 0,\
                    "location_id": 963414,\
                    "payment_details": null,\
                    "parent_id": null,\
                    "currency": "VND",\
                    "haravan_transaction_id": null,\
                    "external_transaction_id": null,\
                    "send_email": false\
                }\
            ],
            "note_attributes": [],
            "confirmed_at": null,
            "closed_status": "unclosed",
            "cancelled_status": "uncancelled",
            "confirmed_status": "unconfirmed",
            "user_id": 0,
            "device_id": null,
            "location_id": 963414,
            "ref_order_id": 0,
            "ref_order_number": null,
            "utm_source": null,
            "utm_medium": null,
            "utm_campaign": null,
            "utm_term": null,
            "utm_content": null,
            "redeem_model": null,
            "omni_order_status": 0,
            "omni_order_status_name": null,
            "location_assigned_at": null,
            "in_stock_at": null,
            "out_of_stock_at": null,
            "export_at": null,
            "complete_at": null,
            "payment_url": null,
            "contact_email": "hello@haravan.com"
      }
   ]
}

```

### Retrieve a count of the orders [​](https://docs.haravan.com/docs/omni-apis/orders/\#retrieve-a-count-of-the-orders "Direct link to heading")

GET

https://apis.haravan.com/com/orders/count.json

Retrieve the count of resources of the orders.

- GET `https://apis.haravan.com/com/orders/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "count": 500
}

```

Retrieve the count of resources of the cancelled orders.

- GET `https://apis.haravan.com/com/orders/count.json?status=cancelled`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "count": 33
}

```

### Retrieves single the order [​](https://docs.haravan.com/docs/omni-apis/orders/\#retrieves-single-the-order "Direct link to heading")

GET

https://apis.haravan.com/com/orders/{order\_id}.json

Retrieves single the order by ID.

- GET `https://apis.haravan.com/com/orders/1075012798.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "order": {
        "billing_address": {
            "address1": "182 Lê Đại Hành",
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": "Haravan Demo",
            "id": 1036847352,
            "last_name": null,
            "phone": null,
            "province": "Hồ Chí Minh",
            "zip": null,
            "name": " Haravan Demo",
            "province_code": "HC",
            "country_code": "VN",
            "default": true,
            "district": "Quận 11",
            "district_code": "HC476",
            "ward": "Phường 15",
            "ward_code": "27208"
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": null,
        "cancelled_at": null,
        "cart_token": "19627118f2e844ddb3a0c8d73f99a580",
        "checkout_token": "19627118f2e844ddb3a0c8d73f99a580",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2020-09-19T01:12:10.062Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1056185840,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1056185854,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1056185852,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1056185851,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1056185850,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1056185849,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1056185847,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1056185845,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1056185844,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1056185843,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                }\
            ],
            "created_at": "2020-09-18T04:12:10.236Z",
            "default_address": {
                "address1": "182 Lê Đại Hành",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": "Haravan Demo",
                "id": 1056185840,
                "last_name": null,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": null,
                "name": " Haravan Demo",
                "province_code": "HC",
                "country_code": "vn",
                "default": true,
                "district": "Quận 11",
                "district_code": "HC476",
                "ward": "Phường 15",
                "ward_code": "27208"
            },
            "email": "hello@haravan.com",
            "phone": null,
            "first_name": "Haravan Demo",
            "id": 1036847352,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1138637123,
            "last_order_name": "#100027",
            "note": "Demo     ",
            "orders_count": 28,
            "state": "Disabled",
            "tags": null,
            "total_spent": 261380000.0000,
            "total_paid": 0.0,
            "updated_at": "2021-01-04T22:00:52.558Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [],
        "email": "hello@haravan.com",
        "financial_status": "paid",
        "fulfillments": [],
        "fulfillment_status": "notfulfilled",
        "tags": null,
        "gateway": "COD",
        "gateway_code": null,
        "id": 1138637099,
        "landing_site": null,
        "landing_site_ref": null,
        "source": "web",
        "line_items": [\
            {\
                "fulfillable_quantity": 22,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1160828322,\
                "price": 600000.0000,\
                "price_original": 600000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1028183659,\
                "quantity": 22,\
                "requires_shipping": true,\
                "sku": null,\
                "title": "Đầm babydoll tay lỡ khoét lỗ",\
                "variant_id": 1061514693,\
                "variant_title": "Default Title",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": null,\
                "properties": null,\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 0.00\
            }\
        ],
        "name": "#100020",
        "note": null,
        "number": 1138637099,
        "order_number": "#100020",
        "processing_method": null,
        "referring_site": null,
        "refunds": [],
        "shipping_address": {
            "address1": "182 Lê Đại Hành",
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": "Haravan Demo",
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": "Hồ Chí Minh",
            "zip": null,
            "name": " Haravan Demo",
            "province_code": "HC",
            "country_code": "VN",
            "district_code": "HC476",
            "district": "Quận 11",
            "ward_code": "27208",
            "ward": "Phường 15"
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": "web",
        "subtotal_price": 13200000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "19627118f2e844ddb3a0c8d73f99a580",
        "total_discounts": 0.0000,
        "total_line_items_price": 13200000.0000,
        "total_price": 13200000.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2020-09-18T04:12:21.837Z",
        "transactions": [\
            {\
                "amount": 13200000.0000,\
                "authorization": null,\
                "created_at": "2020-09-19T01:12:10.062Z",\
                "device_id": null,\
                "gateway": "COD",\
                "id": 1055329694,\
                "kind": "capture",\
                "order_id": 1138637099,\
                "receipt": null,\
                "status": null,\
                "test": false,\
                "user_id": 0,\
                "location_id": 963414,\
                "payment_details": null,\
                "parent_id": 1055329693,\
                "currency": "VND",\
                "haravan_transaction_id": null,\
                "external_transaction_id": null,\
                "send_email": false\
            },\
            {\
                "amount": 13200000.0000,\
                "authorization": null,\
                "created_at": "2020-09-19T01:12:10.062Z",\
                "device_id": null,\
                "gateway": "COD",\
                "id": 1055329693,\
                "kind": "pending",\
                "order_id": 1138637099,\
                "receipt": null,\
                "status": null,\
                "test": false,\
                "user_id": 0,\
                "location_id": 963414,\
                "payment_details": null,\
                "parent_id": null,\
                "currency": "VND",\
                "haravan_transaction_id": null,\
                "external_transaction_id": null,\
                "send_email": false\
            }\
        ],
        "note_attributes": [],
        "confirmed_at": null,
        "closed_status": "unclosed",
        "cancelled_status": "uncancelled",
        "confirmed_status": "unconfirmed",
        "user_id": 0,
        "device_id": null,
        "location_id": 963414,
        "ref_order_id": 0,
        "ref_order_number": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "omni_order_status": 0,
        "omni_order_status_name": null,
        "location_assigned_at": null,
        "in_stock_at": null,
        "out_of_stock_at": null,
        "export_at": null,
        "complete_at": null,
        "payment_url": null,
        "contact_email": "hello@haravan.com"
    }
}

```

### Create a new order [​](https://docs.haravan.com/docs/omni-apis/orders/\#create-a-new-order "Direct link to heading")

POST

https://apis.haravan.com/com/orders.json

Create a simple order with only a product variant ID and no optional parameters.

- POST `https://apis.haravan.com/com/orders.json`





```codeBlockLines_e6Vv
{
"order": {
     "line_items": [\
       {\
         "variant_id": 1061514693,\
         "quantity": 1\
       }\
     ]
}
}

```


Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created

{
    "order": {
        "billing_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "id": 1043680707,
            "last_name": null,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "default": true,
            "district": null,
            "district_code": null,
            "ward": null,
            "ward_code": null
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": null,
        "cancelled_at": null,
        "cart_token": "3340f74c1d084bf2a51e1c654ceeba25",
        "checkout_token": "3340f74c1d084bf2a51e1c654ceeba25",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2021-09-08T18:39:41.567Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": null,\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "---",\
                    "id": 1081844056,\
                    "last_name": null,\
                    "phone": null,\
                    "province": null,\
                    "zip": null,\
                    "name": " ---",\
                    "province_code": null,\
                    "country_code": "vn",\
                    "default": true,\
                    "district": null,\
                    "district_code": null,\
                    "ward": null,\
                    "ward_code": null\
                }\
            ],
            "created_at": "2021-03-21T11:23:42.56Z",
            "default_address": {
                "address1": null,
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": "---",
                "id": 1081844056,
                "last_name": null,
                "phone": null,
                "province": null,
                "zip": null,
                "name": " ---",
                "province_code": null,
                "country_code": "vn",
                "default": true,
                "district": null,
                "district_code": null,
                "ward": null,
                "ward_code": null
            },
            "email": "guest@haravan.com",
            "phone": null,
            "first_name": null,
            "id": 1043680707,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1221136952,
            "last_order_name": "#100512",
            "note": null,
            "orders_count": 13,
            "state": "Disabled",
            "tags": null,
            "total_spent": 103890000.0000,
            "total_paid": 0.0,
            "updated_at": "2021-08-14T11:29:07Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [],
        "email": "guest@haravan.com",
        "financial_status": "pending",
        "fulfillments": [],
        "fulfillment_status": "notfulfilled",
        "tags": null,
        "gateway": null,
        "gateway_code": null,
        "id": 1225410593,
        "landing_site": null,
        "landing_site_ref": null,
        "source": null,
        "line_items": [\
            {\
                "fulfillable_quantity": 1,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1292996509,\
                "price": 600000.0000,\
                "price_original": 600000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1028183659,\
                "quantity": 1,\
                "requires_shipping": true,\
                "sku": null,\
                "title": "Đầm babydoll tay lỡ khoét lỗ",\
                "variant_id": 1061514693,\
                "variant_title": "Default Title",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": null,\
                "properties": null,\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 0.00\
            }\
        ],
        "name": "#100522",
        "note": null,
        "number": 1225410593,
        "order_number": "#100522",
        "processing_method": null,
        "referring_site": null,
        "refunds": [],
        "shipping_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "district_code": null,
            "district": null,
            "ward_code": null,
            "ward": null
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": null,
        "subtotal_price": 600000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "3340f74c1d084bf2a51e1c654ceeba25",
        "total_discounts": 0.0000,
        "total_line_items_price": 600000.0000,
        "total_price": 600000.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2021-09-08T18:39:41.613Z",
        "transactions": [],
        "note_attributes": [],
        "confirmed_at": null,
        "closed_status": "unclosed",
        "cancelled_status": "uncancelled",
        "confirmed_status": "unconfirmed",
        "user_id": 200000497867,
        "device_id": null,
        "location_id": 963414,
        "ref_order_id": 0,
        "ref_order_number": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "omni_order_status": 0,
        "omni_order_status_name": null,
        "location_assigned_at": null,
        "in_stock_at": null,
        "out_of_stock_at": null,
        "export_at": null,
        "complete_at": null,
        "payment_url": null,
        "contact_email": "guest@haravan.com"
    }
}

```

Create a simple order, sending an order confirmation and a shipping confirmation to the customer.

- POST `https://apis.haravan.com/com/orders.json`

```codeBlockLines_e6Vv
{
  "order": {
    "email": "foo@example.com",
    "fulfillment_status": "fulfilled",
    "send_receipt": true,
    "send_fulfillment_receipt": true,
    "line_items": [\
      {\
        "variant_id": 1061514693,\
        "quantity": 1\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created

{
    "order": {
        "billing_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "id": 1038792095,
            "last_name": null,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "default": true,
            "district": null,
            "district_code": null,
            "ward": null,
            "ward_code": null
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": null,
        "cancelled_at": null,
        "cart_token": "4b269f2acc5f4545bae3a273b7d36f9d",
        "checkout_token": "4b269f2acc5f4545bae3a273b7d36f9d",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2021-09-08T18:42:00.767Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": null,\
                    "id": 1060106899,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " ",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": null,\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1061189728,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": null,\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": null,\
                    "country_code": "vn",\
                    "default": false,\
                    "district": null,\
                    "district_code": null,\
                    "ward": null,\
                    "ward_code": null\
                },\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1060107099,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                }\
            ],
            "created_at": "2020-11-19T06:53:12.246Z",
            "default_address": {
                "address1": "123 abc",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": null,
                "id": 1060106899,
                "last_name": null,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": null,
                "name": " ",
                "province_code": "HC",
                "country_code": "vn",
                "default": true,
                "district": "Quận 11",
                "district_code": "HC476",
                "ward": "Phường 15",
                "ward_code": "27208"
            },
            "email": "foo@example.com",
            "phone": null,
            "first_name": null,
            "id": 1038792095,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1196361656,
            "last_order_name": "#100358",
            "note": "vip",
            "orders_count": 15,
            "state": "Disabled",
            "tags": null,
            "total_spent": 36000000.0000,
            "total_paid": 0.0,
            "updated_at": "2021-05-10T03:55:26Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [],
        "email": "foo@example.com",
        "financial_status": "pending",
        "fulfillments": [\
            {\
                "created_at": "2021-09-08T18:42:00.809Z",\
                "id": 1052688901,\
                "order_id": 1225411478,\
                "receipt": null,\
                "status": "success",\
                "tracking_company": null,\
                "tracking_company_code": null,\
                "tracking_numbers": [],\
                "tracking_number": null,\
                "tracking_url": null,\
                "tracking_urls": [],\
                "updated_at": "2021-09-08T18:42:00.825Z",\
                "line_items": [\
                    {\
                        "fulfillable_quantity": 0,\
                        "fulfillment_service": "Thủ công",\
                        "fulfillment_status": "Chưa hoàn thành",\
                        "grams": 0.0000,\
                        "id": 1292997206,\
                        "price": 600000.0000,\
                        "product_id": 1028183659,\
                        "quantity": 1,\
                        "requires_shipping": true,\
                        "sku": null,\
                        "title": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_id": 1061514693,\
                        "variant_title": "Default Title",\
                        "vendor": "Khác",\
                        "name": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_inventory_management": null,\
                        "properties": null,\
                        "product_exists": false\
                    }\
                ],\
                "notify_customer": false,\
                "province": null,\
                "province_code": null,\
                "district": null,\
                "district_code": null,\
                "ward": null,\
                "ward_code": null,\
                "cod_amount": 0.0000,\
                "carrier_status_name": "Đã giao hàng",\
                "carrier_cod_status_name": "Không",\
                "carrier_status_code": "delivered",\
                "carrier_cod_status_code": "none",\
                "location_id": 963414,\
                "shipping_package": 0,\
                "note": null,\
                "carrier_service_package": 0,\
                "carrier_service_package_name": null,\
                "is_new_service_package": false,\
                "coupon_code": null,\
                "ready_to_pick_date": null,\
                "picking_date": null,\
                "delivering_date": null,\
                "delivered_date": null,\
                "return_date": null,\
                "not_meet_customer_date": null,\
                "waiting_for_return_date": null,\
                "cod_paid_date": null,\
                "cod_receipt_date": null,\
                "cod_pending_date": null,\
                "cod_not_receipt_date": null,\
                "cancel_date": null,\
                "is_view_before": null,\
                "country": null,\
                "country_code": null,\
                "zip_code": null,\
                "city": null,\
                "real_shipping_fee": 0.0000,\
                "shipping_notes": null,\
                "total_weight": 0.0,\
                "package_length": 0.00,\
                "package_width": 0.00,\
                "package_height": 0.00,\
                "boxme_servicecode": null,\
                "transport_type": 0,\
                "address": null,\
                "sender_phone": null,\
                "sender_name": null,\
                "carrier_service_code": null,\
                "from_longtitude": 0.0,\
                "from_latitude": 0.0,\
                "to_longtitude": 0.0,\
                "to_latitude": 0.0,\
                "sort_code": null,\
                "is_drop_off": false,\
                "is_insurance": false,\
                "insurance_price": 0.0,\
                "is_open_box": false,\
                "request_id": null,\
                "carrier_options": null,\
                "note_attributes": null,\
                "first_name": null,\
                "last_name": null,\
                "shipping_address": null,\
                "shipping_phone": null,\
                "carrier_shop_id": null\
            }\
        ],
        "fulfillment_status": "fulfilled",
        "tags": null,
        "gateway": null,
        "gateway_code": null,
        "id": 1225411478,
        "landing_site": null,
        "landing_site_ref": null,
        "source": null,
        "line_items": [\
            {\
                "fulfillable_quantity": 0,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1292997206,\
                "price": 600000.0000,\
                "price_original": 600000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1028183659,\
                "quantity": 1,\
                "requires_shipping": true,\
                "sku": null,\
                "title": "Đầm babydoll tay lỡ khoét lỗ",\
                "variant_id": 1061514693,\
                "variant_title": "Default Title",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": null,\
                "properties": null,\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 0.00\
            }\
        ],
        "name": "#100523",
        "note": null,
        "number": 1225411478,
        "order_number": "#100523",
        "processing_method": null,
        "referring_site": null,
        "refunds": [],
        "shipping_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "district_code": null,
            "district": null,
            "ward_code": null,
            "ward": null
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": null,
        "subtotal_price": 600000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "4b269f2acc5f4545bae3a273b7d36f9d",
        "total_discounts": 0.0000,
        "total_line_items_price": 600000.0000,
        "total_price": 600000.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2021-09-08T18:42:00.838Z",
        "transactions": [],
        "note_attributes": [],
        "confirmed_at": null,
        "closed_status": "unclosed",
        "cancelled_status": "uncancelled",
        "confirmed_status": "unconfirmed",
        "user_id": 200000497867,
        "device_id": null,
        "location_id": 963414,
        "ref_order_id": 0,
        "ref_order_number": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "omni_order_status": 0,
        "omni_order_status_name": null,
        "location_assigned_at": null,
        "in_stock_at": null,
        "out_of_stock_at": null,
        "export_at": null,
        "complete_at": null,
        "payment_url": null,
        "contact_email": "foo@example.com"
    }
}

```

Create a simple order without sending an order receipt or a fulfillment receipt.

- POST `https://apis.haravan.com/com/orders.json`

```codeBlockLines_e6Vv
{
  "order": {
    "email": "foo@example.com",
    "fulfillment_status": "fulfilled",
    "line_items": [\
      {\
        "variant_id": 1061514693,\
        "quantity": 1\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created

{
    "order": {
        "billing_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "id": 1038792095,
            "last_name": null,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "default": true,
            "district": null,
            "district_code": null,
            "ward": null,
            "ward_code": null
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": null,
        "cancelled_at": null,
        "cart_token": "bd427a1f10e44557bd6d44f5ccb34c27",
        "checkout_token": "bd427a1f10e44557bd6d44f5ccb34c27",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2021-09-08T18:50:16.53Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": null,\
                    "id": 1060106899,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " ",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": null,\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1061189728,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": null,\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": null,\
                    "country_code": "vn",\
                    "default": false,\
                    "district": null,\
                    "district_code": null,\
                    "ward": null,\
                    "ward_code": null\
                },\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1060107099,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                }\
            ],
            "created_at": "2020-11-19T06:53:12.246Z",
            "default_address": {
                "address1": "123 abc",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": null,
                "id": 1060106899,
                "last_name": null,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": null,
                "name": " ",
                "province_code": "HC",
                "country_code": "vn",
                "default": true,
                "district": "Quận 11",
                "district_code": "HC476",
                "ward": "Phường 15",
                "ward_code": "27208"
            },
            "email": "foo@example.com",
            "phone": null,
            "first_name": null,
            "id": 1038792095,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1225411478,
            "last_order_name": "#100523",
            "note": "vip",
            "orders_count": 16,
            "state": "Disabled",
            "tags": null,
            "total_spent": 36000000.0000,
            "total_paid": 0.0,
            "updated_at": "2021-09-08T18:42:01Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [],
        "email": "foo@example.com",
        "financial_status": "pending",
        "fulfillments": [\
            {\
                "created_at": "2021-09-08T18:50:16.607Z",\
                "id": 1052689465,\
                "order_id": 1225414307,\
                "receipt": null,\
                "status": "success",\
                "tracking_company": null,\
                "tracking_company_code": null,\
                "tracking_numbers": [],\
                "tracking_number": null,\
                "tracking_url": null,\
                "tracking_urls": [],\
                "updated_at": "2021-09-08T18:50:16.631Z",\
                "line_items": [\
                    {\
                        "fulfillable_quantity": 0,\
                        "fulfillment_service": "Thủ công",\
                        "fulfillment_status": "Chưa hoàn thành",\
                        "grams": 0.0000,\
                        "id": 1292999429,\
                        "price": 600000.0000,\
                        "product_id": 1028183659,\
                        "quantity": 1,\
                        "requires_shipping": true,\
                        "sku": null,\
                        "title": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_id": 1061514693,\
                        "variant_title": "Default Title",\
                        "vendor": "Khác",\
                        "name": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_inventory_management": null,\
                        "properties": null,\
                        "product_exists": false\
                    }\
                ],\
                "notify_customer": false,\
                "province": null,\
                "province_code": null,\
                "district": null,\
                "district_code": null,\
                "ward": null,\
                "ward_code": null,\
                "cod_amount": 0.0000,\
                "carrier_status_name": "Đã giao hàng",\
                "carrier_cod_status_name": "Không",\
                "carrier_status_code": "delivered",\
                "carrier_cod_status_code": "none",\
                "location_id": 963414,\
                "shipping_package": 0,\
                "note": null,\
                "carrier_service_package": 0,\
                "carrier_service_package_name": null,\
                "is_new_service_package": false,\
                "coupon_code": null,\
                "ready_to_pick_date": null,\
                "picking_date": null,\
                "delivering_date": null,\
                "delivered_date": null,\
                "return_date": null,\
                "not_meet_customer_date": null,\
                "waiting_for_return_date": null,\
                "cod_paid_date": null,\
                "cod_receipt_date": null,\
                "cod_pending_date": null,\
                "cod_not_receipt_date": null,\
                "cancel_date": null,\
                "is_view_before": null,\
                "country": null,\
                "country_code": null,\
                "zip_code": null,\
                "city": null,\
                "real_shipping_fee": 0.0000,\
                "shipping_notes": null,\
                "total_weight": 0.0,\
                "package_length": 0.00,\
                "package_width": 0.00,\
                "package_height": 0.00,\
                "boxme_servicecode": null,\
                "transport_type": 0,\
                "address": null,\
                "sender_phone": null,\
                "sender_name": null,\
                "carrier_service_code": null,\
                "from_longtitude": 0.0,\
                "from_latitude": 0.0,\
                "to_longtitude": 0.0,\
                "to_latitude": 0.0,\
                "sort_code": null,\
                "is_drop_off": false,\
                "is_insurance": false,\
                "insurance_price": 0.0,\
                "is_open_box": false,\
                "request_id": null,\
                "carrier_options": null,\
                "note_attributes": null,\
                "first_name": null,\
                "last_name": null,\
                "shipping_address": null,\
                "shipping_phone": null,\
                "carrier_shop_id": null\
            }\
        ],
        "fulfillment_status": "fulfilled",
        "tags": null,
        "gateway": null,
        "gateway_code": null,
        "id": 1225414307,
        "landing_site": null,
        "landing_site_ref": null,
        "source": null,
        "line_items": [\
            {\
                "fulfillable_quantity": 0,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1292999429,\
                "price": 600000.0000,\
                "price_original": 600000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1028183659,\
                "quantity": 1,\
                "requires_shipping": true,\
                "sku": null,\
                "title": "Đầm babydoll tay lỡ khoét lỗ",\
                "variant_id": 1061514693,\
                "variant_title": "Default Title",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": null,\
                "properties": null,\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 0.00\
            }\
        ],
        "name": "#100524",
        "note": null,
        "number": 1225414307,
        "order_number": "#100524",
        "processing_method": null,
        "referring_site": null,
        "refunds": [],
        "shipping_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "district_code": null,
            "district": null,
            "ward_code": null,
            "ward": null
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": null,
        "subtotal_price": 600000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "bd427a1f10e44557bd6d44f5ccb34c27",
        "total_discounts": 0.0000,
        "total_line_items_price": 600000.0000,
        "total_price": 600000.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2021-09-08T18:50:16.65Z",
        "transactions": [],
        "note_attributes": [],
        "confirmed_at": null,
        "closed_status": "unclosed",
        "cancelled_status": "uncancelled",
        "confirmed_status": "unconfirmed",
        "user_id": 200000497867,
        "device_id": null,
        "location_id": 963414,
        "ref_order_id": 0,
        "ref_order_number": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "omni_order_status": 0,
        "omni_order_status_name": null,
        "location_assigned_at": null,
        "in_stock_at": null,
        "out_of_stock_at": null,
        "export_at": null,
        "complete_at": null,
        "payment_url": null,
        "contact_email": "foo@example.com"
    }
}

```

Create a simple order and fulfill it.

- POST `https://apis.haravan.com/com/orders.json`

```codeBlockLines_e6Vv
{
  "order": {
    "email": "foo@example.com",
    "fulfillment_status": "fulfilled",
    "fulfillments": [\
      {\
        "location_id": 963414\
      }\
    ],
    "line_items": [\
      {\
        "variant_id": 1061514693,\
        "quantity": 1\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created

{
    "order": {
        "billing_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "id": 1038792095,
            "last_name": null,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "default": true,
            "district": null,
            "district_code": null,
            "ward": null,
            "ward_code": null
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": null,
        "cancelled_at": null,
        "cart_token": "ba672331ed7a459b91a04af2073914d0",
        "checkout_token": "ba672331ed7a459b91a04af2073914d0",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2021-09-08T18:52:25.332Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": null,\
                    "id": 1060106899,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " ",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": null,\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1061189728,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": null,\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": null,\
                    "country_code": "vn",\
                    "default": false,\
                    "district": null,\
                    "district_code": null,\
                    "ward": null,\
                    "ward_code": null\
                },\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1060107099,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                }\
            ],
            "created_at": "2020-11-19T06:53:12.246Z",
            "default_address": {
                "address1": "123 abc",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": null,
                "id": 1060106899,
                "last_name": null,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": null,
                "name": " ",
                "province_code": "HC",
                "country_code": "vn",
                "default": true,
                "district": "Quận 11",
                "district_code": "HC476",
                "ward": "Phường 15",
                "ward_code": "27208"
            },
            "email": "foo@example.com",
            "phone": null,
            "first_name": null,
            "id": 1038792095,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1225414307,
            "last_order_name": "#100524",
            "note": "vip",
            "orders_count": 17,
            "state": "Disabled",
            "tags": null,
            "total_spent": 36000000.0000,
            "total_paid": 0.0,
            "updated_at": "2021-09-08T18:50:18Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [],
        "email": "foo@example.com",
        "financial_status": "pending",
        "fulfillments": [\
            {\
                "created_at": "2021-09-08T18:52:25.422Z",\
                "id": 1052689551,\
                "order_id": 1225414919,\
                "receipt": null,\
                "status": "success",\
                "tracking_company": null,\
                "tracking_company_code": null,\
                "tracking_numbers": [],\
                "tracking_number": null,\
                "tracking_url": null,\
                "tracking_urls": [],\
                "updated_at": "2021-09-08T18:52:25.441Z",\
                "line_items": [\
                    {\
                        "fulfillable_quantity": 0,\
                        "fulfillment_service": "Thủ công",\
                        "fulfillment_status": "Chưa hoàn thành",\
                        "grams": 0.0000,\
                        "id": 1292999873,\
                        "price": 600000.0000,\
                        "product_id": 1028183659,\
                        "quantity": 1,\
                        "requires_shipping": true,\
                        "sku": null,\
                        "title": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_id": 1061514693,\
                        "variant_title": "Default Title",\
                        "vendor": "Khác",\
                        "name": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_inventory_management": null,\
                        "properties": null,\
                        "product_exists": false\
                    }\
                ],\
                "notify_customer": false,\
                "province": null,\
                "province_code": null,\
                "district": null,\
                "district_code": null,\
                "ward": null,\
                "ward_code": null,\
                "cod_amount": 0.0000,\
                "carrier_status_name": "Đã giao hàng",\
                "carrier_cod_status_name": "Không",\
                "carrier_status_code": "delivered",\
                "carrier_cod_status_code": "none",\
                "location_id": 963414,\
                "shipping_package": 0,\
                "note": null,\
                "carrier_service_package": 0,\
                "carrier_service_package_name": null,\
                "is_new_service_package": false,\
                "coupon_code": null,\
                "ready_to_pick_date": null,\
                "picking_date": null,\
                "delivering_date": null,\
                "delivered_date": null,\
                "return_date": null,\
                "not_meet_customer_date": null,\
                "waiting_for_return_date": null,\
                "cod_paid_date": null,\
                "cod_receipt_date": null,\
                "cod_pending_date": null,\
                "cod_not_receipt_date": null,\
                "cancel_date": null,\
                "is_view_before": null,\
                "country": null,\
                "country_code": null,\
                "zip_code": null,\
                "city": null,\
                "real_shipping_fee": 0.0000,\
                "shipping_notes": null,\
                "total_weight": 0.0,\
                "package_length": 0.00,\
                "package_width": 0.00,\
                "package_height": 0.00,\
                "boxme_servicecode": null,\
                "transport_type": 0,\
                "address": null,\
                "sender_phone": null,\
                "sender_name": null,\
                "carrier_service_code": null,\
                "from_longtitude": 0.0,\
                "from_latitude": 0.0,\
                "to_longtitude": 0.0,\
                "to_latitude": 0.0,\
                "sort_code": null,\
                "is_drop_off": false,\
                "is_insurance": false,\
                "insurance_price": 0.0,\
                "is_open_box": false,\
                "request_id": null,\
                "carrier_options": null,\
                "note_attributes": null,\
                "first_name": null,\
                "last_name": null,\
                "shipping_address": null,\
                "shipping_phone": null,\
                "carrier_shop_id": null\
            }\
        ],
        "fulfillment_status": "fulfilled",
        "tags": null,
        "gateway": null,
        "gateway_code": null,
        "id": 1225414919,
        "landing_site": null,
        "landing_site_ref": null,
        "source": null,
        "line_items": [\
            {\
                "fulfillable_quantity": 0,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1292999873,\
                "price": 600000.0000,\
                "price_original": 600000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1028183659,\
                "quantity": 1,\
                "requires_shipping": true,\
                "sku": null,\
                "title": "Đầm babydoll tay lỡ khoét lỗ",\
                "variant_id": 1061514693,\
                "variant_title": "Default Title",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": null,\
                "properties": null,\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 0.00\
            }\
        ],
        "name": "#100525",
        "note": null,
        "number": 1225414919,
        "order_number": "#100525",
        "processing_method": null,
        "referring_site": null,
        "refunds": [],
        "shipping_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "district_code": null,
            "district": null,
            "ward_code": null,
            "ward": null
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": null,
        "subtotal_price": 600000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "ba672331ed7a459b91a04af2073914d0",
        "total_discounts": 0.0000,
        "total_line_items_price": 600000.0000,
        "total_price": 600000.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2021-09-08T18:52:25.463Z",
        "transactions": [],
        "note_attributes": [],
        "confirmed_at": null,
        "closed_status": "unclosed",
        "cancelled_status": "uncancelled",
        "confirmed_status": "unconfirmed",
        "user_id": 200000497867,
        "device_id": null,
        "location_id": 963414,
        "ref_order_id": 0,
        "ref_order_number": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "omni_order_status": 0,
        "omni_order_status_name": null,
        "location_assigned_at": null,
        "in_stock_at": null,
        "out_of_stock_at": null,
        "export_at": null,
        "complete_at": null,
        "payment_url": null,
        "contact_email": "foo@example.com"
    }
}

```

Create an order and apply a discount.

- POST `https://apis.haravan.com/com/orders.json`

```codeBlockLines_e6Vv
{
  "order": {
    "email": "foo@example.com",
    "fulfillment_status": "fulfilled",
    "fulfillments": [\
      {\
        "location_id": 963414\
      }\
    ],
    "line_items": [\
      {\
        "variant_id": 1061514693,\
        "quantity": 1\
      }\
    ],
    "financial_status": "paid",
    "transactions": [\
      {\
        "kind": "capture"\
      }\
    ],
    "discount_codes": [\
      {\
        "code": "KM",\
        "amount": 100000,\
        "is_coupon_code": true\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created

{
    "order": {
        "billing_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "id": 1038792095,
            "last_name": null,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "default": true,
            "district": null,
            "district_code": null,
            "ward": null,
            "ward_code": null
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": null,
        "cancelled_at": null,
        "cart_token": "da3019409b794adf9aefbe0ba26d3f2d",
        "checkout_token": "da3019409b794adf9aefbe0ba26d3f2d",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2021-09-08T19:08:40.339Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": null,\
                    "id": 1060106899,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " ",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": null,\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1061189728,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": null,\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": null,\
                    "country_code": "vn",\
                    "default": false,\
                    "district": null,\
                    "district_code": null,\
                    "ward": null,\
                    "ward_code": null\
                },\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1060107099,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                }\
            ],
            "created_at": "2020-11-19T06:53:12.246Z",
            "default_address": {
                "address1": "123 abc",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": null,
                "id": 1060106899,
                "last_name": null,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": null,
                "name": " ",
                "province_code": "HC",
                "country_code": "vn",
                "default": true,
                "district": "Quận 11",
                "district_code": "HC476",
                "ward": "Phường 15",
                "ward_code": "27208"
            },
            "email": "foo@example.com",
            "phone": null,
            "first_name": null,
            "id": 1038792095,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1225418252,
            "last_order_name": "#100534",
            "note": "vip",
            "orders_count": 25,
            "state": "Disabled",
            "tags": null,
            "total_spent": 36000000.0000,
            "total_paid": 0.0,
            "updated_at": "2021-09-08T19:08:15Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [\
            {\
                "amount": 100000.0000,\
                "code": "KM",\
                "type": "fixed_amount",\
                "is_coupon_code": false\
            }\
        ],
        "email": "foo@example.com",
        "financial_status": "partiallypaid",
        "fulfillments": [\
            {\
                "created_at": "2021-09-08T19:08:40.422Z",\
                "id": 1052690695,\
                "order_id": 1225418351,\
                "receipt": null,\
                "status": "success",\
                "tracking_company": null,\
                "tracking_company_code": null,\
                "tracking_numbers": [],\
                "tracking_number": null,\
                "tracking_url": null,\
                "tracking_urls": [],\
                "updated_at": "2021-09-08T19:08:40.438Z",\
                "line_items": [\
                    {\
                        "fulfillable_quantity": 0,\
                        "fulfillment_service": "Thủ công",\
                        "fulfillment_status": "Chưa hoàn thành",\
                        "grams": 0.0000,\
                        "id": 1293002914,\
                        "price": 600000.0000,\
                        "product_id": 1028183659,\
                        "quantity": 1,\
                        "requires_shipping": true,\
                        "sku": null,\
                        "title": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_id": 1061514693,\
                        "variant_title": "Default Title",\
                        "vendor": "Khác",\
                        "name": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_inventory_management": null,\
                        "properties": null,\
                        "product_exists": false\
                    }\
                ],\
                "notify_customer": false,\
                "province": null,\
                "province_code": null,\
                "district": null,\
                "district_code": null,\
                "ward": null,\
                "ward_code": null,\
                "cod_amount": 0.0000,\
                "carrier_status_name": "Đã giao hàng",\
                "carrier_cod_status_name": "Không",\
                "carrier_status_code": "delivered",\
                "carrier_cod_status_code": "none",\
                "location_id": 963414,\
                "shipping_package": 0,\
                "note": null,\
                "carrier_service_package": 0,\
                "carrier_service_package_name": null,\
                "is_new_service_package": false,\
                "coupon_code": null,\
                "ready_to_pick_date": null,\
                "picking_date": null,\
                "delivering_date": null,\
                "delivered_date": null,\
                "return_date": null,\
                "not_meet_customer_date": null,\
                "waiting_for_return_date": null,\
                "cod_paid_date": null,\
                "cod_receipt_date": null,\
                "cod_pending_date": null,\
                "cod_not_receipt_date": null,\
                "cancel_date": null,\
                "is_view_before": null,\
                "country": null,\
                "country_code": null,\
                "zip_code": null,\
                "city": null,\
                "real_shipping_fee": 0.0000,\
                "shipping_notes": null,\
                "total_weight": 0.0,\
                "package_length": 0.00,\
                "package_width": 0.00,\
                "package_height": 0.00,\
                "boxme_servicecode": null,\
                "transport_type": 0,\
                "address": null,\
                "sender_phone": null,\
                "sender_name": null,\
                "carrier_service_code": null,\
                "from_longtitude": 0.0,\
                "from_latitude": 0.0,\
                "to_longtitude": 0.0,\
                "to_latitude": 0.0,\
                "sort_code": null,\
                "is_drop_off": false,\
                "is_insurance": false,\
                "insurance_price": 0.0,\
                "is_open_box": false,\
                "request_id": null,\
                "carrier_options": null,\
                "note_attributes": null,\
                "first_name": null,\
                "last_name": null,\
                "shipping_address": null,\
                "shipping_phone": null,\
                "carrier_shop_id": null\
            }\
        ],
        "fulfillment_status": "fulfilled",
        "tags": null,
        "gateway": null,
        "gateway_code": null,
        "id": 1225418351,
        "landing_site": null,
        "landing_site_ref": null,
        "source": null,
        "line_items": [\
            {\
                "fulfillable_quantity": 0,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1293002914,\
                "price": 600000.0000,\
                "price_original": 600000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1028183659,\
                "quantity": 1,\
                "requires_shipping": true,\
                "sku": null,\
                "title": "Đầm babydoll tay lỡ khoét lỗ",\
                "variant_id": 1061514693,\
                "variant_title": "Default Title",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": null,\
                "properties": null,\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 0.00\
            }\
        ],
        "name": "#100535",
        "note": null,
        "number": 1225418351,
        "order_number": "#100535",
        "processing_method": null,
        "referring_site": null,
        "refunds": [],
        "shipping_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "district_code": null,
            "district": null,
            "ward_code": null,
            "ward": null
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": null,
        "subtotal_price": 600000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "da3019409b794adf9aefbe0ba26d3f2d",
        "total_discounts": 100000.0000,
        "total_line_items_price": 600000.0000,
        "total_price": 500000.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2021-09-08T19:08:40.452Z",
        "transactions": [],
        "note_attributes": [],
        "confirmed_at": null,
        "closed_status": "unclosed",
        "cancelled_status": "uncancelled",
        "confirmed_status": "unconfirmed",
        "user_id": 200000497867,
        "device_id": null,
        "location_id": 963414,
        "ref_order_id": 0,
        "ref_order_number": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "omni_order_status": 0,
        "omni_order_status_name": null,
        "location_assigned_at": null,
        "in_stock_at": null,
        "out_of_stock_at": null,
        "export_at": null,
        "complete_at": null,
        "payment_url": null,
        "contact_email": "foo@example.com"
    }
}

```

Create an order with gateway is COD

- POST `https://apis.haravan.com/com/orders.json`

```codeBlockLines_e6Vv
{
  "order": {
    "email": "foo@example.com",
    "line_items": [\
      {\
        "variant_id": 1061514693,\
        "quantity": 1\
      }\
    ],
    "is_cod_gateway" : true
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created

{
    "order": {
        "billing_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "id": 1038792095,
            "last_name": null,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "default": true,
            "district": null,
            "district_code": null,
            "ward": null,
            "ward_code": null
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": null,
        "cancelled_at": null,
        "cart_token": "f512679381ad419380c2d429bec99f89",
        "checkout_token": "f512679381ad419380c2d429bec99f89",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2021-09-08T19:17:18.807Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": null,\
                    "id": 1060106899,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " ",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": null,\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1061189728,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": null,\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": null,\
                    "country_code": "vn",\
                    "default": false,\
                    "district": null,\
                    "district_code": null,\
                    "ward": null,\
                    "ward_code": null\
                },\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1060107099,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                }\
            ],
            "created_at": "2020-11-19T06:53:12.246Z",
            "default_address": {
                "address1": "123 abc",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": null,
                "id": 1060106899,
                "last_name": null,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": null,
                "name": " ",
                "province_code": "HC",
                "country_code": "vn",
                "default": true,
                "district": "Quận 11",
                "district_code": "HC476",
                "ward": "Phường 15",
                "ward_code": "27208"
            },
            "email": "foo@example.com",
            "phone": null,
            "first_name": null,
            "id": 1038792095,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1225418951,
            "last_order_name": "#100536",
            "note": "vip",
            "orders_count": 27,
            "state": "Disabled",
            "tags": null,
            "total_spent": 36000000.0000,
            "total_paid": 0.0,
            "updated_at": "2021-09-08T19:12:43Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [],
        "email": "foo@example.com",
        "financial_status": "pending",
        "fulfillments": [\
            {\
                "created_at": "2021-09-08T19:17:18.843Z",\
                "id": 1052691096,\
                "order_id": 1225419563,\
                "receipt": null,\
                "status": "success",\
                "tracking_company": null,\
                "tracking_company_code": null,\
                "tracking_numbers": [],\
                "tracking_number": null,\
                "tracking_url": null,\
                "tracking_urls": [],\
                "updated_at": "2021-09-08T19:17:18.86Z",\
                "line_items": [\
                    {\
                        "fulfillable_quantity": 0,\
                        "fulfillment_service": "Thủ công",\
                        "fulfillment_status": "Chưa hoàn thành",\
                        "grams": 0.0000,\
                        "id": 1293004126,\
                        "price": 600000.0000,\
                        "product_id": 1028183659,\
                        "quantity": 1,\
                        "requires_shipping": true,\
                        "sku": null,\
                        "title": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_id": 1061514693,\
                        "variant_title": "Default Title",\
                        "vendor": "Khác",\
                        "name": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_inventory_management": null,\
                        "properties": null,\
                        "product_exists": false\
                    }\
                ],\
                "notify_customer": false,\
                "province": null,\
                "province_code": null,\
                "district": null,\
                "district_code": null,\
                "ward": null,\
                "ward_code": null,\
                "cod_amount": 0.0000,\
                "carrier_status_name": "Đã giao hàng",\
                "carrier_cod_status_name": "Không",\
                "carrier_status_code": "delivered",\
                "carrier_cod_status_code": "none",\
                "location_id": 963414,\
                "shipping_package": 0,\
                "note": null,\
                "carrier_service_package": 0,\
                "carrier_service_package_name": null,\
                "is_new_service_package": false,\
                "coupon_code": null,\
                "ready_to_pick_date": null,\
                "picking_date": null,\
                "delivering_date": null,\
                "delivered_date": null,\
                "return_date": null,\
                "not_meet_customer_date": null,\
                "waiting_for_return_date": null,\
                "cod_paid_date": null,\
                "cod_receipt_date": null,\
                "cod_pending_date": null,\
                "cod_not_receipt_date": null,\
                "cancel_date": null,\
                "is_view_before": null,\
                "country": null,\
                "country_code": null,\
                "zip_code": null,\
                "city": null,\
                "real_shipping_fee": 0.0000,\
                "shipping_notes": null,\
                "total_weight": 0.0,\
                "package_length": 0.00,\
                "package_width": 0.00,\
                "package_height": 0.00,\
                "boxme_servicecode": null,\
                "transport_type": 0,\
                "address": null,\
                "sender_phone": null,\
                "sender_name": null,\
                "carrier_service_code": null,\
                "from_longtitude": 0.0,\
                "from_latitude": 0.0,\
                "to_longtitude": 0.0,\
                "to_latitude": 0.0,\
                "sort_code": null,\
                "is_drop_off": false,\
                "is_insurance": false,\
                "insurance_price": 0.0,\
                "is_open_box": false,\
                "request_id": null,\
                "carrier_options": null,\
                "note_attributes": null,\
                "first_name": null,\
                "last_name": null,\
                "shipping_address": null,\
                "shipping_phone": null,\
                "carrier_shop_id": null\
            }\
        ],
        "fulfillment_status": "fulfilled",
        "tags": null,
        "gateway": null,
        "gateway_code": "COD",
        "id": 1225419563,
        "landing_site": null,
        "landing_site_ref": null,
        "source": null,
        "line_items": [\
            {\
                "fulfillable_quantity": 0,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1293004126,\
                "price": 600000.0000,\
                "price_original": 600000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1028183659,\
                "quantity": 1,\
                "requires_shipping": true,\
                "sku": null,\
                "title": "Đầm babydoll tay lỡ khoét lỗ",\
                "variant_id": 1061514693,\
                "variant_title": "Default Title",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": null,\
                "properties": null,\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 0.00\
            }\
        ],
        "name": "#100537",
        "note": null,
        "number": 1225419563,
        "order_number": "#100537",
        "processing_method": null,
        "referring_site": null,
        "refunds": [],
        "shipping_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "district_code": null,
            "district": null,
            "ward_code": null,
            "ward": null
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": null,
        "subtotal_price": 600000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "f512679381ad419380c2d429bec99f89",
        "total_discounts": 0.0000,
        "total_line_items_price": 600000.0000,
        "total_price": 600000.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2021-09-08T19:17:18.876Z",
        "transactions": [],
        "note_attributes": [],
        "confirmed_at": null,
        "closed_status": "unclosed",
        "cancelled_status": "uncancelled",
        "confirmed_status": "unconfirmed",
        "user_id": 200000497867,
        "device_id": null,
        "location_id": 963414,
        "ref_order_id": 0,
        "ref_order_number": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "omni_order_status": 0,
        "omni_order_status_name": null,
        "location_assigned_at": null,
        "in_stock_at": null,
        "out_of_stock_at": null,
        "export_at": null,
        "complete_at": null,
        "payment_url": null,
        "contact_email": "foo@example.com"
    }
}

```

Create an order with custom gateway.

- POST `https://apis.haravan.com/com/orders.json`

```codeBlockLines_e6Vv
{
  "order": {
    "email": "foo@example.com",
    "line_items": [\
      {\
        "variant_id": 1061514693,\
        "quantity": 1\
      }\
    ],
    "is_cod_gateway": false,
    "gateway": "Bank transfer"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created

{
  "order": {
    "billing_address": {
      "address1": null,
      "address2": null,
      "city": null,
      "company": null,
      "country": "Vietnam",
      "first_name": null,
      "id": 1038792095,
      "last_name": null,
      "phone": null,
      "province": null,
      "zip": null,
      "name": " ",
      "province_code": null,
      "country_code": "VN",
      "default": true,
      "district": null,
      "district_code": null,
      "ward": null,
      "ward_code": null
    },
    "browser_ip": null,
    "buyer_accepts_marketing": false,
    "cancel_reason": null,
    "cancelled_at": null,
    "cart_token": "f512679381ad419380c2d429bec99f89",
    "checkout_token": "f512679381ad419380c2d429bec99f89",
    "client_details": {
      "accept_language": null,
      "browser_ip": null,
      "session_hash": null,
      "user_agent": null,
      "browser_height": null,
      "browser_width": null
    },
    "closed_at": null,
    "created_at": "2021-09-08T19:17:18.807Z",
    "currency": "VND",
    "customer": {
      "accepts_marketing": false,
      "addresses": [\
        {\
          "address1": "123 abc",\
          "address2": null,\
          "city": null,\
          "company": null,\
          "country": "Vietnam",\
          "first_name": null,\
          "id": 1060106899,\
          "last_name": null,\
          "phone": null,\
          "province": "Hồ Chí Minh",\
          "zip": null,\
          "name": " ",\
          "province_code": "HC",\
          "country_code": "vn",\
          "default": true,\
          "district": "Quận 11",\
          "district_code": "HC476",\
          "ward": "Phường 15",\
          "ward_code": "27208"\
        },\
        {\
          "address1": null,\
          "address2": null,\
          "city": null,\
          "company": null,\
          "country": "Vietnam",\
          "first_name": "abc",\
          "id": 1061189728,\
          "last_name": "xxx",\
          "phone": null,\
          "province": null,\
          "zip": null,\
          "name": "xxx abc",\
          "province_code": null,\
          "country_code": "vn",\
          "default": false,\
          "district": null,\
          "district_code": null,\
          "ward": null,\
          "ward_code": null\
        },\
        {\
          "address1": "123 abc",\
          "address2": null,\
          "city": null,\
          "company": null,\
          "country": "Vietnam",\
          "first_name": "abc",\
          "id": 1060107099,\
          "last_name": "xxx",\
          "phone": null,\
          "province": "Hồ Chí Minh",\
          "zip": null,\
          "name": "xxx abc",\
          "province_code": "HC",\
          "country_code": "vn",\
          "default": false,\
          "district": "Quận 11",\
          "district_code": "HC476",\
          "ward": "Phường 15",\
          "ward_code": "27208"\
        }\
      ],
      "created_at": "2020-11-19T06:53:12.246Z",
      "default_address": {
        "address1": "123 abc",
        "address2": null,
        "city": null,
        "company": null,
        "country": "Vietnam",
        "first_name": null,
        "id": 1060106899,
        "last_name": null,
        "phone": null,
        "province": "Hồ Chí Minh",
        "zip": null,
        "name": " ",
        "province_code": "HC",
        "country_code": "vn",
        "default": true,
        "district": "Quận 11",
        "district_code": "HC476",
        "ward": "Phường 15",
        "ward_code": "27208"
      },
      "email": "foo@example.com",
      "phone": null,
      "first_name": null,
      "id": 1038792095,
      "multipass_identifier": null,
      "last_name": null,
      "last_order_id": 1225418951,
      "last_order_name": "#100536",
      "note": "vip",
      "orders_count": 27,
      "state": "Disabled",
      "tags": null,
      "total_spent": 36000000,
      "total_paid": 0,
      "updated_at": "2021-09-08T19:12:43Z",
      "verified_email": false,
      "send_email_invite": false,
      "send_email_welcome": false,
      "password": null,
      "password_confirmation": null,
      "group_name": null,
      "birthday": null,
      "gender": null,
      "last_order_date": null
    },
    "discount_codes": [],
    "email": "foo@example.com",
    "financial_status": "pending",
    "fulfillments": [\
      {\
        "created_at": "2021-09-08T19:17:18.843Z",\
        "id": 1052691096,\
        "order_id": 1225419563,\
        "receipt": null,\
        "status": "success",\
        "tracking_company": null,\
        "tracking_company_code": null,\
        "tracking_numbers": [],\
        "tracking_number": null,\
        "tracking_url": null,\
        "tracking_urls": [],\
        "updated_at": "2021-09-08T19:17:18.86Z",\
        "line_items": [\
          {\
            "fulfillable_quantity": 0,\
            "fulfillment_service": "Thủ công",\
            "fulfillment_status": "Chưa hoàn thành",\
            "grams": 0,\
            "id": 1293004126,\
            "price": 600000,\
            "product_id": 1028183659,\
            "quantity": 1,\
            "requires_shipping": true,\
            "sku": null,\
            "title": "Đầm babydoll tay lỡ khoét lỗ",\
            "variant_id": 1061514693,\
            "variant_title": "Default Title",\
            "vendor": "Khác",\
            "name": "Đầm babydoll tay lỡ khoét lỗ",\
            "variant_inventory_management": null,\
            "properties": null,\
            "product_exists": false\
          }\
        ],\
        "notify_customer": false,\
        "province": null,\
        "province_code": null,\
        "district": null,\
        "district_code": null,\
        "ward": null,\
        "ward_code": null,\
        "cod_amount": 0,\
        "carrier_status_name": "Đã giao hàng",\
        "carrier_cod_status_name": "Không",\
        "carrier_status_code": "delivered",\
        "carrier_cod_status_code": "none",\
        "location_id": 963414,\
        "shipping_package": 0,\
        "note": null,\
        "carrier_service_package": 0,\
        "carrier_service_package_name": null,\
        "is_new_service_package": false,\
        "coupon_code": null,\
        "ready_to_pick_date": null,\
        "picking_date": null,\
        "delivering_date": null,\
        "delivered_date": null,\
        "return_date": null,\
        "not_meet_customer_date": null,\
        "waiting_for_return_date": null,\
        "cod_paid_date": null,\
        "cod_receipt_date": null,\
        "cod_pending_date": null,\
        "cod_not_receipt_date": null,\
        "cancel_date": null,\
        "is_view_before": null,\
        "country": null,\
        "country_code": null,\
        "zip_code": null,\
        "city": null,\
        "real_shipping_fee": 0,\
        "shipping_notes": null,\
        "total_weight": 0,\
        "package_length": 0,\
        "package_width": 0,\
        "package_height": 0,\
        "boxme_servicecode": null,\
        "transport_type": 0,\
        "address": null,\
        "sender_phone": null,\
        "sender_name": null,\
        "carrier_service_code": null,\
        "from_longtitude": 0,\
        "from_latitude": 0,\
        "to_longtitude": 0,\
        "to_latitude": 0,\
        "sort_code": null,\
        "is_drop_off": false,\
        "is_insurance": false,\
        "insurance_price": 0,\
        "is_open_box": false,\
        "request_id": null,\
        "carrier_options": null,\
        "note_attributes": null,\
        "first_name": null,\
        "last_name": null,\
        "shipping_address": null,\
        "shipping_phone": null,\
        "carrier_shop_id": null\
      }\
    ],
    "fulfillment_status": "fulfilled",
    "tags": null,
    "gateway": "Bank transfer",
    "gateway_code": "",
    "id": 1225419563,
    "landing_site": null,
    "landing_site_ref": null,
    "source": null,
    "line_items": [\
      {\
        "fulfillable_quantity": 0,\
        "fulfillment_service": null,\
        "fulfillment_status": "notfulfilled",\
        "grams": 0,\
        "id": 1293004126,\
        "price": 600000,\
        "price_original": 600000,\
        "price_promotion": 0,\
        "product_id": 1028183659,\
        "quantity": 1,\
        "requires_shipping": true,\
        "sku": null,\
        "title": "Đầm babydoll tay lỡ khoét lỗ",\
        "variant_id": 1061514693,\
        "variant_title": "Default Title",\
        "vendor": "Khác",\
        "type": "Khác",\
        "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
        "gift_card": false,\
        "taxable": true,\
        "tax_lines": null,\
        "product_exists": true,\
        "barcode": null,\
        "properties": null,\
        "total_discount": 0,\
        "applied_discounts": [],\
        "image": {\
          "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
          "attactment": null,\
          "filename": null\
        },\
        "not_allow_promotion": false,\
        "ma_cost_amount": 0\
      }\
    ],
    "name": "#100537",
    "note": null,
    "number": 1225419563,
    "order_number": "#100537",
    "processing_method": null,
    "referring_site": null,
    "refunds": [],
    "shipping_address": {
      "address1": null,
      "address2": null,
      "city": null,
      "company": null,
      "country": "Vietnam",
      "first_name": null,
      "last_name": null,
      "latitude": 0,
      "longitude": 0,
      "phone": null,
      "province": null,
      "zip": null,
      "name": " ",
      "province_code": null,
      "country_code": "VN",
      "district_code": null,
      "district": null,
      "ward_code": null,
      "ward": null
    },
    "shipping_lines": [\
      {\
        "code": null,\
        "price": 0,\
        "source": null,\
        "title": null\
      }\
    ],
    "source_name": null,
    "subtotal_price": 600000,
    "tax_lines": null,
    "taxes_included": false,
    "token": "f512679381ad419380c2d429bec99f89",
    "total_discounts": 0,
    "total_line_items_price": 600000,
    "total_price": 600000,
    "total_tax": 0,
    "total_weight": 0,
    "updated_at": "2021-09-08T19:17:18.876Z",
    "transactions": [],
    "note_attributes": [],
    "confirmed_at": null,
    "closed_status": "unclosed",
    "cancelled_status": "uncancelled",
    "confirmed_status": "unconfirmed",
    "user_id": 200000497867,
    "device_id": null,
    "location_id": 963414,
    "ref_order_id": 0,
    "ref_order_number": null,
    "utm_source": null,
    "utm_medium": null,
    "utm_campaign": null,
    "utm_term": null,
    "utm_content": null,
    "redeem_model": null,
    "omni_order_status": 0,
    "omni_order_status_name": null,
    "location_assigned_at": null,
    "in_stock_at": null,
    "out_of_stock_at": null,
    "export_at": null,
    "complete_at": null,
    "payment_url": null,
    "contact_email": "foo@example.com"
  }
}

```

Create an order with customer.

- POST `https://apis.haravan.com/com/orders.json`

```codeBlockLines_e6Vv
{
  "order": {
    "customer": {
      "id": 1085558958
    },
    "email": "example@haravan.com",
    "shipping_address": {
      "address1": "182 Lê Đại Hành",
      "company": "HRV",
      "country": "Vietnam",
      "first_name": "A",
      "last_name": "Nguyễn Văn",
      "phone": "0909090909",
      "province": "Hồ Chí Minh",
      "province_code": "HC",
      "country_code": "VN",
      "district_code": "HC476",
      "district": "Quận 11",
      "ward_code": "27208",
      "ward": "Phường 15"
    },
    "send_receipt": false,
    "send_fulfillment_receipt": false,
    "is_confirm": true,
    "source": "pos",
    "source_name": "pos",
    "line_items": [\
      {\
        "product_id": 1003148078,\
        "variant_id": 1008493211,\
        "quantity": 1,\
        "price": 110000,\
        "applied_discounts": [\
          {\
            "description": "Khuyến mãi sinh nhật",\
            "amount": 5000.0\
          }\
        ],\
        "total_discount": 5000.0,\
        "properties": [\
          {\
            "name": "Ghi chú sản phẩm",\
            "value": "Xuất xứ Vietnam"\
          }\
        ]\
      },\
      {\
        "price": 170000.0,\
        "quantity": 2,\
        "title": "Sản phầm ABC",\
        "sku": "ABC",\
        "barcode": "ABCDE",\
        "applied_discounts": [\
          {\
            "description": "Khuyến mãi sinh nhật",\
            "amount": 30000.0\
          }\
        ],\
        "total_discount": 30000.0,\
        "properties": [\
          {\
            "name": "Ghi chú sản phẩm",\
            "value": "Xuất xứ Hà Nội"\
          }\
        ]\
      }\
    ],
    "tags": "A1,A2",
    "gateway": "Tiền mặt",
    "note": "Ghi chú đơn hàng",
    "discount_codes": [\
      {\
        "amount": 10000.0,\
        "code": "Khuyến mãi mùa hè",\
        "is_coupon_code": false\
      }\
    ],
    "total_discounts": 10000,
    "shipping_lines": [\
      {\
        "code": "Giao hàng tận nơi",\
        "price": 15000.0,\
        "title": "Giao hàng tận nơi"\
      }\
    ],
    "landing_site_ref": "refabc",
    "location_id": 895636,
    "user_id": "1000374246",
    "note_attributes": [\
      {\
        "name": "Ghi chú khác",\
        "value": "thông tin khác"\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created

{
  "order": {
    "billing_address": {
      "address1": "182 Lê Đại Hành",
      "address2": null,
      "city": null,
      "company": "HRV",
      "country": "Vietnam",
      "first_name": "A",
      "id": 1085558958,
      "last_name": "Nguyễn Văn",
      "phone": "0909090909",
      "province": "Hồ Chí Minh",
      "zip": null,
      "name": "Nguyễn Văn A",
      "province_code": "HC",
      "country_code": "VN",
      "default": true,
      "district": "Quận 11",
      "district_code": "HC476",
      "ward": "Phường 15",
      "ward_code": "27208"
    },
    "browser_ip": null,
    "buyer_accepts_marketing": false,
    "cancel_reason": null,
    "cancelled_at": null,
    "cart_token": "09839b9c20044d97835218bdd8ba9c4c",
    "checkout_token": "09839b9c20044d97835218bdd8ba9c4c",
    "client_details": {
      "accept_language": null,
      "browser_ip": null,
      "session_hash": null,
      "user_agent": null,
      "browser_height": null,
      "browser_width": null
    },
    "closed_at": null,
    "created_at": "2023-06-10T12:19:26.027Z",
    "currency": "VND",
    "customer": {
      "accepts_marketing": false,
      "addresses": [\
        {\
          "address1": "182 Lê Đại Hành",\
          "address2": null,\
          "city": null,\
          "company": "HRV",\
          "country": "Vietnam",\
          "first_name": "A",\
          "id": 1131187607,\
          "last_name": "Nguyễn Văn",\
          "phone": "0909090909",\
          "province": "Hồ Chí Minh",\
          "zip": null,\
          "name": "Nguyễn Văn A",\
          "province_code": "HC",\
          "country_code": "vn",\
          "default": true,\
          "district": "Quận 11",\
          "district_code": "HC476",\
          "ward": "Phường 15",\
          "ward_code": "27208"\
        }\
      ],
      "created_at": "2023-06-10T12:19:26.011Z",
      "default_address": {
        "address1": "182 Lê Đại Hành",
        "address2": null,
        "city": null,
        "company": "HRV",
        "country": "Vietnam",
        "first_name": "A",
        "id": 1131187607,
        "last_name": "Nguyễn Văn",
        "phone": "0909090909",
        "province": "Hồ Chí Minh",
        "zip": null,
        "name": "Nguyễn Văn A",
        "province_code": "HC",
        "country_code": "vn",
        "default": true,
        "district": "Quận 11",
        "district_code": "HC476",
        "ward": "Phường 15",
        "ward_code": "27208"
      },
      "email": "example@haravan.com",
      "phone": "0909090909",
      "first_name": "A",
      "id": 1085558958,
      "multipass_identifier": null,
      "last_name": "Nguyễn Văn",
      "last_order_id": 1456389374,
      "last_order_name": "#100811",
      "note": null,
      "orders_count": 1,
      "state": "Disabled",
      "tags": null,
      "total_spent": 0.0,
      "total_paid": 0.0,
      "updated_at": "2023-06-10T12:19:26.055Z",
      "verified_email": false,
      "send_email_invite": false,
      "send_email_welcome": false,
      "password": null,
      "password_confirmation": null,
      "group_name": null,
      "birthday": null,
      "gender": null,
      "last_order_date": null
    },
    "discount_codes": [\
      {\
        "amount": 10000.0,\
        "code": "Khuyến mãi mùa hè",\
        "type": null,\
        "is_coupon_code": false\
      }\
    ],
    "email": "example@haravan.com",
    "financial_status": "pending",
    "fulfillments": [],
    "fulfillment_status": "notfulfilled",
    "tags": "A1,A2",
    "gateway": "Tiền mặt",
    "gateway_code": null,
    "id": 1456389374,
    "landing_site": null,
    "landing_site_ref": "refabc",
    "source": "pos",
    "line_items": [\
      {\
        "fulfillable_quantity": 1,\
        "fulfillment_service": null,\
        "fulfillment_status": "notfulfilled",\
        "grams": 0.0,\
        "id": 1615733005,\
        "price": 110000.0,\
        "price_original": 115000.0,\
        "price_promotion": 0.0,\
        "product_id": 1003148078,\
        "quantity": 1,\
        "requires_shipping": false,\
        "sku": "ABC",\
        "title": "Túi sưởi tay hình gấu siêu dễ thương.",\
        "variant_id": 1008493211,\
        "variant_title": "Default Title",\
        "vendor": "Khác",\
        "type": "Khác",\
        "name": "Túi sưởi tay hình gấu siêu dễ thương. - Default Title",\
        "gift_card": false,\
        "taxable": false,\
        "tax_lines": null,\
        "product_exists": true,\
        "barcode": "8934588063053",\
        "properties": [\
          {\
            "name": "Ghi chú sản phẩm",\
            "value": "Xuất xứ Vietnam"\
          }\
        ],\
        "total_discount": 5000.0,\
        "applied_discounts": [\
          {\
            "description": "Khuyến mãi sinh nhật",\
            "amount": 5000.0\
          }\
        ],\
        "image": {\
          "src": "http://hstatic.net/110/1000045110/1/2016/9-5/tui-suoi-da-nang-ts022-chomongcaionline-6.jpg",\
          "attactment": null,\
          "filename": null\
        },\
        "not_allow_promotion": false,\
        "ma_cost_amount": 0.0,\
        "actual_price": 0.0\
      },\
      {\
        "fulfillable_quantity": 2,\
        "fulfillment_service": null,\
        "fulfillment_status": "notfulfilled",\
        "grams": 0.0,\
        "id": 1615733006,\
        "price": 170000.0,\
        "price_original": 185000.0,\
        "price_promotion": 0.0,\
        "product_id": null,\
        "quantity": 2,\
        "requires_shipping": false,\
        "sku": "ABC",\
        "title": "Sản phầm ABC",\
        "variant_id": null,\
        "variant_title": "",\
        "vendor": null,\
        "type": null,\
        "name": "Sản phầm ABC",\
        "gift_card": false,\
        "taxable": false,\
        "tax_lines": null,\
        "product_exists": true,\
        "barcode": "ABCDE",\
        "properties": [\
          {\
            "name": "Ghi chú sản phẩm",\
            "value": "Xuất xứ Hà Nội"\
          }\
        ],\
        "total_discount": 15000.0,\
        "applied_discounts": [\
          {\
            "description": "Khuyến mãi sinh nhật",\
            "amount": 15000.0\
          }\
        ],\
        "image": null,\
        "not_allow_promotion": false,\
        "ma_cost_amount": 0.0,\
        "actual_price": 0.0\
      }\
    ],
    "name": "#100811",
    "note": "Ghi chú đơn hàng",
    "number": 1456389374,
    "order_number": "#100811",
    "processing_method": null,
    "referring_site": null,
    "refunds": [],
    "shipping_address": {
      "address1": "182 Lê Đại Hành",
      "address2": null,
      "city": null,
      "company": "HRV",
      "country": "Vietnam",
      "first_name": "A",
      "last_name": "Nguyễn Văn",
      "latitude": 0.0,
      "longitude": 0.0,
      "phone": "0909090909",
      "province": "Hồ Chí Minh",
      "zip": null,
      "name": "Nguyễn Văn A",
      "province_code": "HC",
      "country_code": "VN",
      "district_code": "HC476",
      "district": "Quận 11",
      "ward_code": "27208",
      "ward": "Phường 15"
    },
    "shipping_lines": [\
      {\
        "code": "Giao hàng tận nơi",\
        "price": 15000.0,\
        "source": null,\
        "title": "Giao hàng tận nơi"\
      }\
    ],
    "source_name": "pos",
    "subtotal_price": 450000.0,
    "tax_lines": null,
    "taxes_included": false,
    "token": "09839b9c20044d97835218bdd8ba9c4c",
    "total_discounts": 10000.0,
    "total_line_items_price": 450000.0,
    "total_price": 455000.0,
    "total_tax": 0.0,
    "total_weight": 0.0,
    "updated_at": "2023-06-10T12:19:26.059Z",
    "transactions": [],
    "note_attributes": [\
      {\
        "name": "Ghi chú khác",\
        "value": "thông tin khác"\
      }\
    ],
    "confirmed_at": "2023-06-10T12:19:26.055Z",
    "closed_status": "unclosed",
    "cancelled_status": "uncancelled",
    "confirmed_status": "confirmed",
    "user_id": 1000374246,
    "device_id": null,
    "location_id": 895636,
    "location_name": "Flemington",
    "ref_order_id": 0,
    "ref_order_number": null,
    "ref_order_date": null,
    "confirm_user": 200000500173,
    "utm_source": null,
    "utm_medium": null,
    "utm_campaign": null,
    "utm_term": null,
    "utm_content": null,
    "redeem_model": null,
    "payment_url": null,
    "contact_email": "example@haravan.com",
    "assigned_location_id": null,
    "assigned_location_name": null,
    "assigned_location_at": null,
    "exported_confirm_at": null,
    "order_processing_status": "confirmed",
    "prev_order_id": null,
    "prev_order_number": null,
    "prev_order_date": null
  }
}

```

### Confirm an order [​](https://docs.haravan.com/docs/omni-apis/orders/\#confirm-an-order "Direct link to heading")

POST

https://apis.haravan.com/com/orders/{order\_id}/confirm.json

Confirm an exist order.

- POST `https://apis.haravan.com/com/orders/1225410593/confirm.json`

```codeBlockLines_e6Vv
{}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "order": {
        "billing_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "id": 1043680707,
            "last_name": null,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "default": true,
            "district": null,
            "district_code": null,
            "ward": null,
            "ward_code": null
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": null,
        "cancelled_at": null,
        "cart_token": "3340f74c1d084bf2a51e1c654ceeba25",
        "checkout_token": "3340f74c1d084bf2a51e1c654ceeba25",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2021-09-08T18:39:41.567Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": null,\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "---",\
                    "id": 1081844056,\
                    "last_name": null,\
                    "phone": null,\
                    "province": null,\
                    "zip": null,\
                    "name": " ---",\
                    "province_code": null,\
                    "country_code": "vn",\
                    "default": true,\
                    "district": null,\
                    "district_code": null,\
                    "ward": null,\
                    "ward_code": null\
                }\
            ],
            "created_at": "2021-03-21T11:23:42.56Z",
            "default_address": {
                "address1": null,
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": "---",
                "id": 1081844056,
                "last_name": null,
                "phone": null,
                "province": null,
                "zip": null,
                "name": " ---",
                "province_code": null,
                "country_code": "vn",
                "default": true,
                "district": null,
                "district_code": null,
                "ward": null,
                "ward_code": null
            },
            "email": "guest@haravan.com",
            "phone": null,
            "first_name": null,
            "id": 1043680707,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1225410593,
            "last_order_name": "#100522",
            "note": null,
            "orders_count": 14,
            "state": "Disabled",
            "tags": null,
            "total_spent": 103890000.0000,
            "total_paid": 0.0,
            "updated_at": "2021-09-08T18:39:44Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [],
        "email": "guest@haravan.com",
        "financial_status": "pending",
        "fulfillments": [],
        "fulfillment_status": "notfulfilled",
        "tags": null,
        "gateway": null,
        "gateway_code": null,
        "id": 1225410593,
        "landing_site": null,
        "landing_site_ref": null,
        "source": null,
        "line_items": [\
            {\
                "fulfillable_quantity": 1,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1292996509,\
                "price": 600000.0000,\
                "price_original": 600000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1028183659,\
                "quantity": 1,\
                "requires_shipping": true,\
                "sku": null,\
                "title": "Đầm babydoll tay lỡ khoét lỗ",\
                "variant_id": 1061514693,\
                "variant_title": "Default Title",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": null,\
                "properties": null,\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 0.00\
            }\
        ],
        "name": "#100522",
        "note": null,
        "number": 1225410593,
        "order_number": "#100522",
        "processing_method": null,
        "referring_site": null,
        "refunds": [],
        "shipping_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "district_code": null,
            "district": null,
            "ward_code": null,
            "ward": null
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": null,
        "subtotal_price": 600000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "3340f74c1d084bf2a51e1c654ceeba25",
        "total_discounts": 0.0000,
        "total_line_items_price": 600000.0000,
        "total_price": 600000.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2021-09-08T19:25:54.69Z",
        "transactions": [\
            {\
                "amount": 600000.0000,\
                "authorization": null,\
                "created_at": "2021-09-08T18:39:41.567Z",\
                "device_id": null,\
                "gateway": "",\
                "id": 1091216100,\
                "kind": "pending",\
                "order_id": 1225410593,\
                "receipt": null,\
                "status": null,\
                "test": false,\
                "user_id": 200000497867,\
                "location_id": 963414,\
                "payment_details": null,\
                "parent_id": null,\
                "currency": "VND",\
                "haravan_transaction_id": null,\
                "external_transaction_id": null,\
                "send_email": false\
            }\
        ],
        "note_attributes": [],
        "confirmed_at": "2021-09-08T19:25:54.687Z",
        "closed_status": "unclosed",
        "cancelled_status": "uncancelled",
        "confirmed_status": "confirmed",
        "user_id": 200000497867,
        "device_id": null,
        "location_id": 963414,
        "ref_order_id": 0,
        "ref_order_number": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "omni_order_status": 0,
        "omni_order_status_name": null,
        "location_assigned_at": null,
        "in_stock_at": null,
        "out_of_stock_at": null,
        "export_at": null,
        "complete_at": null,
        "payment_url": null,
        "contact_email": "guest@haravan.com"
    }
}

```

### Close an order [​](https://docs.haravan.com/docs/omni-apis/orders/\#close-an-order "Direct link to heading")

POST

https://apis.haravan.com/com/orders/{order\_id}/close.json

Closes an order. A closed order is one that has no more work to be done. All items have been fulfilled or refunded.

- POST `https://apis.haravan.com/com/orders/1225410593/close.json`

```codeBlockLines_e6Vv
{}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "order": {
        "billing_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "id": 1043680707,
            "last_name": null,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "default": true,
            "district": null,
            "district_code": null,
            "ward": null,
            "ward_code": null
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": null,
        "cancelled_at": null,
        "cart_token": "3340f74c1d084bf2a51e1c654ceeba25",
        "checkout_token": "3340f74c1d084bf2a51e1c654ceeba25",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2021-09-08T18:39:41.567Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": null,\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "---",\
                    "id": 1081844056,\
                    "last_name": null,\
                    "phone": null,\
                    "province": null,\
                    "zip": null,\
                    "name": " ---",\
                    "province_code": null,\
                    "country_code": "vn",\
                    "default": true,\
                    "district": null,\
                    "district_code": null,\
                    "ward": null,\
                    "ward_code": null\
                }\
            ],
            "created_at": "2021-03-21T11:23:42.56Z",
            "default_address": {
                "address1": null,
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": "---",
                "id": 1081844056,
                "last_name": null,
                "phone": null,
                "province": null,
                "zip": null,
                "name": " ---",
                "province_code": null,
                "country_code": "vn",
                "default": true,
                "district": null,
                "district_code": null,
                "ward": null,
                "ward_code": null
            },
            "email": "guest@haravan.com",
            "phone": null,
            "first_name": null,
            "id": 1043680707,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1225410593,
            "last_order_name": "#100522",
            "note": null,
            "orders_count": 14,
            "state": "Disabled",
            "tags": null,
            "total_spent": 103890000.0000,
            "total_paid": 0.0,
            "updated_at": "2021-09-08T18:39:44Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [],
        "email": "guest@haravan.com",
        "financial_status": "pending",
        "fulfillments": [],
        "fulfillment_status": "notfulfilled",
        "tags": null,
        "gateway": null,
        "gateway_code": null,
        "id": 1225410593,
        "landing_site": null,
        "landing_site_ref": null,
        "source": null,
        "line_items": [\
            {\
                "fulfillable_quantity": 1,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1292996509,\
                "price": 600000.0000,\
                "price_original": 600000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1028183659,\
                "quantity": 1,\
                "requires_shipping": true,\
                "sku": null,\
                "title": "Đầm babydoll tay lỡ khoét lỗ",\
                "variant_id": 1061514693,\
                "variant_title": "Default Title",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": null,\
                "properties": null,\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 0.00\
            }\
        ],
        "name": "#100522",
        "note": null,
        "number": 1225410593,
        "order_number": "#100522",
        "processing_method": null,
        "referring_site": null,
        "refunds": [],
        "shipping_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "district_code": null,
            "district": null,
            "ward_code": null,
            "ward": null
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": null,
        "subtotal_price": 600000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "3340f74c1d084bf2a51e1c654ceeba25",
        "total_discounts": 0.0000,
        "total_line_items_price": 600000.0000,
        "total_price": 600000.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2021-09-08T19:25:54.69Z",
        "transactions": [\
            {\
                "amount": 600000.0000,\
                "authorization": null,\
                "created_at": "2021-09-08T18:39:41.567Z",\
                "device_id": null,\
                "gateway": "",\
                "id": 1091216100,\
                "kind": "pending",\
                "order_id": 1225410593,\
                "receipt": null,\
                "status": null,\
                "test": false,\
                "user_id": 200000497867,\
                "location_id": 963414,\
                "payment_details": null,\
                "parent_id": null,\
                "currency": "VND",\
                "haravan_transaction_id": null,\
                "external_transaction_id": null,\
                "send_email": false\
            }\
        ],
        "note_attributes": [],
        "confirmed_at": "2021-09-08T19:25:54.687Z",
        "closed_status": "unclosed",
        "cancelled_status": "uncancelled",
        "confirmed_status": "confirmed",
        "user_id": 200000497867,
        "device_id": null,
        "location_id": 963414,
        "ref_order_id": 0,
        "ref_order_number": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "omni_order_status": 0,
        "omni_order_status_name": null,
        "location_assigned_at": null,
        "in_stock_at": null,
        "out_of_stock_at": null,
        "export_at": null,
        "complete_at": null,
        "payment_url": null,
        "contact_email": "guest@haravan.com"
    }
}

```

### Re-open a closed order [​](https://docs.haravan.com/docs/omni-apis/orders/\#re-open-a-closed-order "Direct link to heading")

POST

https://apis.haravan.com/com/orders/{order\_id}/open.json

Re-open a closed order.

- POST `https://apis.haravan.com/com/orders/1225410593/open.json`

```codeBlockLines_e6Vv
{}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "order": {
        "billing_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "id": 1043680707,
            "last_name": null,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "default": true,
            "district": null,
            "district_code": null,
            "ward": null,
            "ward_code": null
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": null,
        "cancelled_at": null,
        "cart_token": "3340f74c1d084bf2a51e1c654ceeba25",
        "checkout_token": "3340f74c1d084bf2a51e1c654ceeba25",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2021-09-08T18:39:41.567Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": null,\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "---",\
                    "id": 1081844056,\
                    "last_name": null,\
                    "phone": null,\
                    "province": null,\
                    "zip": null,\
                    "name": " ---",\
                    "province_code": null,\
                    "country_code": "vn",\
                    "default": true,\
                    "district": null,\
                    "district_code": null,\
                    "ward": null,\
                    "ward_code": null\
                }\
            ],
            "created_at": "2021-03-21T11:23:42.56Z",
            "default_address": {
                "address1": null,
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": "---",
                "id": 1081844056,
                "last_name": null,
                "phone": null,
                "province": null,
                "zip": null,
                "name": " ---",
                "province_code": null,
                "country_code": "vn",
                "default": true,
                "district": null,
                "district_code": null,
                "ward": null,
                "ward_code": null
            },
            "email": "guest@haravan.com",
            "phone": null,
            "first_name": null,
            "id": 1043680707,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1225410593,
            "last_order_name": "#100522",
            "note": null,
            "orders_count": 14,
            "state": "Disabled",
            "tags": null,
            "total_spent": 103890000.0000,
            "total_paid": 0.0,
            "updated_at": "2021-09-08T18:39:44Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [],
        "email": "guest@haravan.com",
        "financial_status": "pending",
        "fulfillments": [],
        "fulfillment_status": "notfulfilled",
        "tags": null,
        "gateway": null,
        "gateway_code": null,
        "id": 1225410593,
        "landing_site": null,
        "landing_site_ref": null,
        "source": null,
        "line_items": [\
            {\
                "fulfillable_quantity": 1,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1292996509,\
                "price": 600000.0000,\
                "price_original": 600000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1028183659,\
                "quantity": 1,\
                "requires_shipping": true,\
                "sku": null,\
                "title": "Đầm babydoll tay lỡ khoét lỗ",\
                "variant_id": 1061514693,\
                "variant_title": "Default Title",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": null,\
                "properties": null,\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 0.00\
            }\
        ],
        "name": "#100522",
        "note": null,
        "number": 1225410593,
        "order_number": "#100522",
        "processing_method": null,
        "referring_site": null,
        "refunds": [],
        "shipping_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "district_code": null,
            "district": null,
            "ward_code": null,
            "ward": null
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": null,
        "subtotal_price": 600000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "3340f74c1d084bf2a51e1c654ceeba25",
        "total_discounts": 0.0000,
        "total_line_items_price": 600000.0000,
        "total_price": 600000.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2021-09-08T19:39:43.395Z",
        "transactions": [\
            {\
                "amount": 600000.0000,\
                "authorization": null,\
                "created_at": "2021-09-08T18:39:41.567Z",\
                "device_id": null,\
                "gateway": "",\
                "id": 1091216100,\
                "kind": "pending",\
                "order_id": 1225410593,\
                "receipt": null,\
                "status": null,\
                "test": false,\
                "user_id": 200000497867,\
                "location_id": 963414,\
                "payment_details": null,\
                "parent_id": null,\
                "currency": "VND",\
                "haravan_transaction_id": null,\
                "external_transaction_id": null,\
                "send_email": false\
            }\
        ],
        "note_attributes": [],
        "confirmed_at": "2021-09-08T19:25:54.687Z",
        "closed_status": "unclosed",
        "cancelled_status": "uncancelled",
        "confirmed_status": "confirmed",
        "user_id": 200000497867,
        "device_id": null,
        "location_id": 963414,
        "ref_order_id": 0,
        "ref_order_number": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "omni_order_status": 0,
        "omni_order_status_name": null,
        "location_assigned_at": null,
        "in_stock_at": null,
        "out_of_stock_at": null,
        "export_at": null,
        "complete_at": null,
        "payment_url": null,
        "contact_email": "guest@haravan.com"
    }
}

```

### Cancel an order [​](https://docs.haravan.com/docs/omni-apis/orders/\#cancel-an-order "Direct link to heading")

POST

https://apis.haravan.com/com/orders/{order\_id}/cancel.json

Cancels an order.

#### Request body [​](https://docs.haravan.com/docs/omni-apis/orders/\#request-body "Direct link to heading")

* * *

`order_id` : `string` `required`

Order id.

* * *

`amount`: `string`

The amount to refund. If set, Haravan attempts to refund the specified amount, depending on its status. Haravan refunds through a manual gateway in cases where the original transaction was not made in Haravan. Refunds through a manual gateway are recorded as a refund on Haravan, but the customer is not refunded.

* * *

`email` : `bool` `default false`

Whether to send an email to the customer notifying them of the cancellation.

* * *

`reason` : `string` `required`

The reason for the order cancellation. Valid values: customer, inventory, fraud, declined, and other.

* * *

`refund` : `refund`

The refund transactions to perform. Required for some more complex refund situations. For more information, see the [Refund API](https://docs.haravan.com/docs/omni-apis/refunds/).

* * *

`restock` : `boolean` `default false`

Whether to restock refunded items back to your store's inventory.

* * *

`note` : `string`

An optional note attached to a refund.

* * *

`ignore_cancel_fulfillment` : `bool` `default false`

if set, ignore cancel fulfillment.

* * *

Cancels an order.

- POST `https://apis.haravan.com/com/orders/1225422362/cancel.json`





```codeBlockLines_e6Vv
{}

```


Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "order": {
        "billing_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "id": 1038792095,
            "last_name": null,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "default": true,
            "district": null,
            "district_code": null,
            "ward": null,
            "ward_code": null
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": "customer",
        "cancelled_at": "2021-09-08T19:53:04.345Z",
        "cart_token": "5517f28bb3514d6e9ff5fe7e52e9eafa",
        "checkout_token": "5517f28bb3514d6e9ff5fe7e52e9eafa",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2021-09-08T19:43:27.733Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": null,\
                    "id": 1060106899,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " ",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": null,\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1061189728,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": null,\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": null,\
                    "country_code": "vn",\
                    "default": false,\
                    "district": null,\
                    "district_code": null,\
                    "ward": null,\
                    "ward_code": null\
                },\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1060107099,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                }\
            ],
            "created_at": "2020-11-19T06:53:12.246Z",
            "default_address": {
                "address1": "123 abc",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": null,
                "id": 1060106899,
                "last_name": null,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": null,
                "name": " ",
                "province_code": "HC",
                "country_code": "vn",
                "default": true,
                "district": "Quận 11",
                "district_code": "HC476",
                "ward": "Phường 15",
                "ward_code": "27208"
            },
            "email": "foo@example.com",
            "phone": null,
            "first_name": null,
            "id": 1038792095,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1225422362,
            "last_order_name": "#100538",
            "note": "vip",
            "orders_count": 29,
            "state": "Disabled",
            "tags": null,
            "total_spent": 36000000.0000,
            "total_paid": 0.0,
            "updated_at": "2021-09-08T19:43:28Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [],
        "email": "foo@example.com",
        "financial_status": "pending",
        "fulfillments": [],
        "fulfillment_status": "notfulfilled",
        "tags": null,
        "gateway": null,
        "gateway_code": "COD",
        "id": 1225422362,
        "landing_site": null,
        "landing_site_ref": null,
        "source": null,
        "line_items": [\
            {\
                "fulfillable_quantity": 1,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1293007037,\
                "price": 600000.0000,\
                "price_original": 600000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1028183659,\
                "quantity": 1,\
                "requires_shipping": true,\
                "sku": null,\
                "title": "Đầm babydoll tay lỡ khoét lỗ",\
                "variant_id": 1061514693,\
                "variant_title": "Default Title",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": null,\
                "properties": null,\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 0.00\
            }\
        ],
        "name": "#100538",
        "note": null,
        "number": 1225422362,
        "order_number": "#100538",
        "processing_method": null,
        "referring_site": null,
        "refunds": [\
            {\
                "created_at": "2021-09-08T19:53:04.347Z",\
                "id": 1010919760,\
                "note": "Khách hủy",\
                "refund_line_items": null,\
                "restock": null,\
                "user_id": 200000497867,\
                "order_id": 1225422362,\
                "transactions": []\
            }\
        ],
        "shipping_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "district_code": null,
            "district": null,
            "ward_code": null,
            "ward": null
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": null,
        "subtotal_price": 600000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "5517f28bb3514d6e9ff5fe7e52e9eafa",
        "total_discounts": 0.0000,
        "total_line_items_price": 600000.0000,
        "total_price": 600000.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2021-09-08T19:53:04.347Z",
        "transactions": [\
            {\
                "amount": 600000.0000,\
                "authorization": null,\
                "created_at": "2021-09-08T19:43:27.733Z",\
                "device_id": null,\
                "gateway": "Thanh toán khi giao hàng (COD)",\
                "id": 1091220954,\
                "kind": "pending",\
                "order_id": 1225422362,\
                "receipt": null,\
                "status": null,\
                "test": false,\
                "user_id": 200000497867,\
                "location_id": 963414,\
                "payment_details": null,\
                "parent_id": null,\
                "currency": "VND",\
                "haravan_transaction_id": null,\
                "external_transaction_id": null,\
                "send_email": false\
            }\
        ],
        "note_attributes": [],
        "confirmed_at": null,
        "closed_status": "unclosed",
        "cancelled_status": "cancelled",
        "confirmed_status": "unconfirmed",
        "user_id": 200000497867,
        "device_id": null,
        "location_id": 963414,
        "ref_order_id": 0,
        "ref_order_number": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "omni_order_status": 0,
        "omni_order_status_name": null,
        "location_assigned_at": null,
        "in_stock_at": null,
        "out_of_stock_at": null,
        "export_at": null,
        "complete_at": null,
        "payment_url": null,
        "contact_email": "foo@example.com"
    }
}

```

Cancel and refund an order using the amount property.

Order was paid.

- POST `https://apis.haravan.com/com/orders/1235723054/cancel.json`

```codeBlockLines_e6Vv
{
  "amount": "520000"
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "order": {
    ...
    "cancel_reason": "other",
    "cancelled_at": "2021-10-20T15:25:32.525Z",
    "currency": "VND",
    "email": "foo@example.com",
    "financial_status": "partially_refunded",
    "gateway": "Thanh toán khi giao hàng (COD)",
    "gateway_code": "COD",
    "id": 1235723054,
    "refunds": [\
      {\
        "created_at": "2021-10-20T15:25:32.532Z",\
        "id": 1011746477,\
        "note": "",\
        "refund_line_items": null,\
        "restock": null,\
        "user_id": 200000500173,\
        "order_id": 1235723054,\
        "location_id": 895636,\
        "transactions": [\
          {\
            "amount": -520000,\
            "authorization": null,\
            "created_at": "2021-10-20T15:25:32.519Z",\
            "device_id": null,\
            "gateway": "Thanh toán khi giao hàng (COD)",\
            "id": 1095773223,\
            "kind": "refund",\
            "order_id": 1235723054,\
            "receipt": null,\
            "status": "Thành công",\
            "test": false,\
            "user_id": 200000500173,\
            "location_id": 895636,\
            "payment_details": null,\
            "parent_id": null,\
            "currency": "VND",\
            "haravan_transaction_id": null,\
            "external_transaction_id": null,\
            "send_email": false\
          }\
        ]\
      }\
    ],
    "transactions": [\
      {\
        "amount": -520000,\
        "authorization": null,\
        "created_at": "2021-10-20T15:25:32.519Z",\
        "device_id": null,\
        "gateway": "Thanh toán khi giao hàng (COD)",\
        "id": 1095773223,\
        "kind": "refund",\
        "order_id": 1235723054,\
        "receipt": null,\
        "status": null,\
        "test": false,\
        "user_id": 200000500173,\
        "location_id": 895636,\
        "payment_details": null,\
        "parent_id": null,\
        "currency": "VND",\
        "haravan_transaction_id": null,\
        "external_transaction_id": null,\
        "send_email": false\
      },\
      {\
        "amount": 1458000,\
        "authorization": null,\
        "created_at": "2021-10-20T15:25:24.386Z",\
        "device_id": null,\
        "gateway": "Thanh toán khi giao hàng (COD)",\
        "id": 1095773214,\
        "kind": "capture",\
        "order_id": 1235723054,\
        "receipt": null,\
        "status": null,\
        "test": false,\
        "user_id": 1000374246,\
        "location_id": 895636,\
        "payment_details": null,\
        "parent_id": 1095766650,\
        "currency": "VND",\
        "haravan_transaction_id": null,\
        "external_transaction_id": null,\
        "send_email": false\
      },\
      {\
        "amount": 1458000,\
        "authorization": null,\
        "created_at": "2021-10-20T14:07:45.176Z",\
        "device_id": null,\
        "gateway": "Thanh toán khi giao hàng (COD)",\
        "id": 1095766650,\
        "kind": "pending",\
        "order_id": 1235723054,\
        "receipt": null,\
        "status": null,\
        "test": false,\
        "user_id": 1000374246,\
        "location_id": 895636,\
        "payment_details": null,\
        "parent_id": null,\
        "currency": "VND",\
        "haravan_transaction_id": null,\
        "external_transaction_id": null,\
        "send_email": false\
      }\
    ],
    "cancelled_status": "cancelled",
    ...
  }
}

```

Cancel and refund an order using the amount, reason, restock, email, note, ignore\_cancel\_fulfillment propertys.

Order was paid and have fulfillments.

- POST `https://apis.haravan.com/com/orders/1235745635/cancel.json`

```codeBlockLines_e6Vv
{
  "amount": "520000",
  "reason": "customer",
  "restock": true,
  "email": true,
  "note": "Customer made a mistake",
  "ignore_cancel_fulfillment": true
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "order": {
    ...
    "cancel_reason": "customer",
    "cancelled_at": "2021-10-20T15:44:16.635Z",
    "currency": "VND",
    "email": "foo@example.com",
    "financial_status": "partially_refunded",
    "fulfillments": [\
      {\
        "created_at": "2021-10-20T15:41:28.577Z",\
        "id": 1058608514,\
        "order_id": 1235745635,\
        "receipt": null,\
        "status": "success",\
        "tracking_company": "Carrier",\
        "tracking_company_code": "external",\
        "tracking_numbers": [\
          "327569"\
        ],\
        "tracking_number": "327569",\
        "tracking_url": "",\
        "tracking_urls": [\
        ],\
        "updated_at": "2021-10-20T15:41:31.947Z",\
        "line_items": [\
          {\
            "fulfillable_quantity": 0,\
            "fulfillment_service": "Thủ công",\
            "fulfillment_status": "Nhập kho",\
            "grams": 0,\
            "id": 1315875100,\
            "price": 729000,\
            "product_id": 1003346284,\
            "quantity": 2,\
            "requires_shipping": true,\
            "sku": "NAM006",\
            "title": "Áo sơ mi nam màu xanh",\
            "variant_id": 1008864403,\
            "variant_title": "Default Title",\
            "vendor": "Khác",\
            "name": "Áo sơ mi nam màu xanh",\
            "variant_inventory_management": "haravan",\
            "properties": null,\
            "product_exists": false\
          }\
        ],\
        "notify_customer": false,\
        "province": null,\
        "province_code": null,\
        "district": null,\
        "district_code": "HC466",\
        "ward": null,\
        "ward_code": null,\
        "cod_amount": 1458000,\
        "carrier_status_name": "Chờ lấy hàng",\
        "carrier_cod_status_name": "Chưa nhận",\
        "carrier_status_code": "readytopick",\
        "carrier_cod_status_code": "codpending",\
        "location_id": 895636,\
        "shipping_package": 0,\
        "note": null,\
        "carrier_service_package": "0",\
        "carrier_service_package_name": "Nội thành Hồ Chí Minh",\
        "is_new_service_package": false,\
        "coupon_code": "",\
        "ready_to_pick_date": "2021-10-20T15:41:29Z",\
        "picking_date": null,\
        "delivering_date": null,\
        "delivered_date": null,\
        "return_date": null,\
        "not_meet_customer_date": null,\
        "waiting_for_return_date": null,\
        "cod_paid_date": null,\
        "cod_receipt_date": null,\
        "cod_pending_date": null,\
        "cod_not_receipt_date": null,\
        "cancel_date": null,\
        "is_view_before": null,\
        "country": null,\
        "country_code": null,\
        "zip_code": null,\
        "city": null,\
        "real_shipping_fee": 5000,\
        "shipping_notes": null,\
        "total_weight": 0,\
        "package_length": 0,\
        "package_width": 0,\
        "package_height": 0,\
        "boxme_servicecode": null,\
        "transport_type": 0,\
        "address": null,\
        "sender_phone": null,\
        "sender_name": null,\
        "carrier_service_code": null,\
        "from_longtitude": 0,\
        "from_latitude": 0,\
        "to_longtitude": 0,\
        "to_latitude": 0,\
        "sort_code": null,\
        "is_drop_off": false,\
        "is_insurance": false,\
        "insurance_price": 0,\
        "is_open_box": false,\
        "request_id": null,\
        "carrier_options": null,\
        "note_attributes": null,\
        "first_name": "John",\
        "last_name": "",\
        "shipping_address": "39 Le Duan",\
        "shipping_phone": "00000000",\
        "carrier_shop_id": null,\
        "request_mode": null\
      }\
    ],
    "fulfillment_status": "fulfilled",
    "gateway": "Thanh toán khi giao hàng (COD)",
    "gateway_code": "COD",
    "id": 1235745635,
    "line_items": [\
      {\
        "fulfillable_quantity": 0,\
        "fulfillment_service": null,\
        "fulfillment_status": "restock",\
        "grams": 0,\
        "id": 1315875100,\
        "price": 729000,\
        "price_original": 749000,\
        "price_promotion": 0,\
        "product_id": 1003346284,\
        "quantity": 2,\
        "requires_shipping": true,\
        "sku": "NAM006",\
        "title": "Áo sơ mi nam màu xanh",\
        "variant_id": 1008864403,\
        "variant_title": "Default Title",\
        "vendor": "Khác",\
        "type": "Thời trang nam",\
        "name": "Áo sơ mi nam màu xanh - Default Title",\
        "gift_card": false,\
        "taxable": false,\
        "tax_lines": null,\
        "product_exists": true,\
        "barcode": "NAM006",\
        "properties": [\
          {\
            "name": "Khuyến mãi",\
            "value": "1017934710 - KM-MUAHE"\
          }\
        ],\
        "total_discount": 0,\
        "applied_discounts": [],\
        "image": {\
          "src": "http://sw001.hstatic.net/9/0b56e650d29162/2015-01-27_161935.png",\
          "attactment": null,\
          "filename": null\
        },\
        "not_allow_promotion": false,\
        "ma_cost_amount": 0\
      }\
    ],
    "name": "#100675",
    "note": null,
    "number": 1235745635,
    "order_number": "#100675",
    "refunds": [\
      {\
        "created_at": "2021-10-20T15:44:16.642Z",\
        "id": 1011746701,\
        "note": "Customer made a mistake",\
        "refund_line_items": [\
          {\
            "id": 1013444927,\
            "line_item": {\
              "fulfillment_service": null,\
              "fulfillment_status": null,\
              "grams": 0,\
              "price": 729000,\
              "product_id": 1003346284,\
              "quantity": 2,\
              "requires_shipping": true,\
              "sku": "NAM006",\
              "title": "Áo sơ mi nam màu xanh",\
              "variant_id": 1008864403,\
              "variant_title": "Default Title",\
              "vendor": "Khác",\
              "name": "Áo sơ mi nam màu xanh",\
              "id": 0,\
              "barcode": "NAM006",\
              "properties": null\
            },\
            "line_item_id": 1315875100,\
            "quantity": 2\
          }\
        ],\
        "restock": true,\
        "user_id": 200000500173,\
        "order_id": 1235745635,\
        "location_id": 895636,\
        "transactions": [\
          {\
            "amount": -520000,\
            "authorization": null,\
            "created_at": "2021-10-20T15:44:16.629Z",\
            "device_id": null,\
            "gateway": "Thanh toán khi giao hàng (COD)",\
            "id": 1095774511,\
            "kind": "refund",\
            "order_id": 1235745635,\
            "receipt": null,\
            "status": "Thành công",\
            "test": false,\
            "user_id": 200000500173,\
            "location_id": 895636,\
            "payment_details": null,\
            "parent_id": null,\
            "currency": "VND",\
            "haravan_transaction_id": null,\
            "external_transaction_id": null,\
            "send_email": false\
          }\
        ]\
      }\
    ],
    "transactions": [\
      {\
        "amount": -520000,\
        "authorization": null,\
        "created_at": "2021-10-20T15:44:16.629Z",\
        "device_id": null,\
        "gateway": "Thanh toán khi giao hàng (COD)",\
        "id": 1095774511,\
        "kind": "refund",\
        "order_id": 1235745635,\
        "receipt": null,\
        "status": null,\
        "test": false,\
        "user_id": 200000500173,\
        "location_id": 895636,\
        "payment_details": null,\
        "parent_id": null,\
        "currency": "VND",\
        "haravan_transaction_id": null,\
        "external_transaction_id": null,\
        "send_email": false\
      },\
      {\
        "amount": 1458000,\
        "authorization": null,\
        "created_at": "2021-10-20T15:41:37.354Z",\
        "device_id": null,\
        "gateway": "Thanh toán khi giao hàng (COD)",\
        "id": 1095774297,\
        "kind": "capture",\
        "order_id": 1235745635,\
        "receipt": null,\
        "status": null,\
        "test": false,\
        "user_id": 1000374246,\
        "location_id": 895636,\
        "payment_details": null,\
        "parent_id": 1095774289,\
        "currency": "VND",\
        "haravan_transaction_id": null,\
        "external_transaction_id": null,\
        "send_email": false\
      },\
      {\
        "amount": 1458000,\
        "authorization": null,\
        "created_at": "2021-10-20T15:41:22.385Z",\
        "device_id": null,\
        "gateway": "Thanh toán khi giao hàng (COD)",\
        "id": 1095774289,\
        "kind": "pending",\
        "order_id": 1235745635,\
        "receipt": null,\
        "status": null,\
        "test": false,\
        "user_id": 1000374246,\
        "location_id": 895636,\
        "payment_details": null,\
        "parent_id": null,\
        "currency": "VND",\
        "haravan_transaction_id": null,\
        "external_transaction_id": null,\
        "send_email": false\
      }\
    ],
    "cancelled_status": "cancelled",
    ...
  }
}

```

Cancel and refund an order using the refund property.

Order was paid and have fulfillments.

- POST `https://apis.haravan.com/com/orders/1235748629/cancel.json`

```codeBlockLines_e6Vv
{
  "reason": "customer",
  "note": "Customer made a mistake",
  "refund": {
    "refund_line_items": [\
      {\
        "line_item_id": 1315883217,\
        "quantity": 1\
      }\
    ],
    "transactions": [\
      {\
        "amount": "300000",\
        "kind": "refund"\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "order": {
    ...
    "cancel_reason": "customer",
    "cancelled_at": "2021-10-20T15:57:48.228Z",
    "currency": "VND",
    "email": "foo@example.com",
    "financial_status": "partially_refunded",
    "fulfillments": [\
      {\
        "created_at": "2021-10-20T15:55:46.228Z",\
        "id": 1058610847,\
        "order_id": 1235748629,\
        "receipt": null,\
        "status": "success",\
        "tracking_company": "Carrier",\
        "tracking_company_code": "external",\
        "tracking_numbers": [\
          "403943"\
        ],\
        "tracking_number": "403943",\
        "tracking_url": "",\
        "tracking_urls": [],\
        "updated_at": "2021-10-20T15:57:48.533Z",\
        "line_items": [\
          {\
            "fulfillable_quantity": 0,\
            "fulfillment_service": "Thủ công",\
            "fulfillment_status": "Nhập kho",\
            "grams": 0,\
            "id": 1315883217,\
            "price": 729000,\
            "product_id": 1003346284,\
            "quantity": 2,\
            "requires_shipping": true,\
            "sku": "NAM006",\
            "title": "Áo sơ mi nam màu xanh",\
            "variant_id": 1008864403,\
            "variant_title": "Default Title",\
            "vendor": "Khác",\
            "name": "Áo sơ mi nam màu xanh",\
            "variant_inventory_management": "haravan",\
            "properties": null,\
            "product_exists": false\
          }\
        ],\
        "notify_customer": false,\
        "province": null,\
        "province_code": null,\
        "district": null,\
        "district_code": "HC466",\
        "ward": null,\
        "ward_code": null,\
        "cod_amount": 1458000,\
        "carrier_status_name": "Hủy giao hàng",\
        "carrier_cod_status_name": "Chưa nhận",\
        "carrier_status_code": "cancel",\
        "carrier_cod_status_code": "codpending",\
        "location_id": 895636,\
        "shipping_package": 0,\
        "note": null,\
        "carrier_service_package": "0",\
        "carrier_service_package_name": "Nội thành Hồ Chí Minh",\
        "is_new_service_package": false,\
        "coupon_code": "",\
        "ready_to_pick_date": "2021-10-20T15:55:46Z",\
        "picking_date": null,\
        "delivering_date": null,\
        "delivered_date": null,\
        "return_date": null,\
        "not_meet_customer_date": null,\
        "waiting_for_return_date": null,\
        "cod_paid_date": null,\
        "cod_receipt_date": null,\
        "cod_pending_date": null,\
        "cod_not_receipt_date": null,\
        "cancel_date": "2021-10-20T15:57:48.523Z",\
        "is_view_before": null,\
        "country": null,\
        "country_code": null,\
        "zip_code": null,\
        "city": null,\
        "real_shipping_fee": 5000,\
        "shipping_notes": null,\
        "total_weight": 0,\
        "package_length": 0,\
        "package_width": 0,\
        "package_height": 0,\
        "boxme_servicecode": null,\
        "transport_type": 0,\
        "address": null,\
        "sender_phone": null,\
        "sender_name": null,\
        "carrier_service_code": null,\
        "from_longtitude": 0,\
        "from_latitude": 0,\
        "to_longtitude": 0,\
        "to_latitude": 0,\
        "sort_code": null,\
        "is_drop_off": false,\
        "is_insurance": false,\
        "insurance_price": 0,\
        "is_open_box": false,\
        "request_id": null,\
        "carrier_options": null,\
        "note_attributes": null,\
        "first_name": "John",\
        "last_name": "",\
        "shipping_address": "39 Le Duan",\
        "shipping_phone": "00000000",\
        "carrier_shop_id": null,\
        "request_mode": null\
      }\
    ],
    "fulfillment_status": "fulfilled",
    "gateway": "Thanh toán khi giao hàng (COD)",
    "gateway_code": "COD",
    "id": 1235748629,
    "line_items": [\
      {\
        "fulfillable_quantity": 0,\
        "fulfillment_service": null,\
        "fulfillment_status": "restock",\
        "grams": 0,\
        "id": 1315883217,\
        "price": 729000,\
        "price_original": 749000,\
        "price_promotion": 0,\
        "product_id": 1003346284,\
        "quantity": 2,\
        "requires_shipping": true,\
        "sku": "NAM006",\
        "title": "Áo sơ mi nam màu xanh",\
        "variant_id": 1008864403,\
        "variant_title": "Default Title",\
        "vendor": "Khác",\
        "type": "Thời trang nam",\
        "name": "Áo sơ mi nam màu xanh - Default Title",\
        "gift_card": false,\
        "taxable": false,\
        "tax_lines": null,\
        "product_exists": true,\
        "barcode": "NAM006",\
        "properties": [\
          {\
            "name": "Khuyến mãi",\
            "value": "1017934710 - KM-MUAHE"\
          }\
        ],\
        "total_discount": 0,\
        "applied_discounts": [],\
        "image": {\
          "src": "http://sw001.hstatic.net/9/0b56e650d29162/2015-01-27_161935.png",\
          "attactment": null,\
          "filename": null\
        },\
        "not_allow_promotion": false,\
        "ma_cost_amount": 0\
      }\
    ],
    "name": "#100676",
    "refunds": [\
      {\
        "created_at": "2021-10-20T15:57:48.232Z",\
        "id": 1011746826,\
        "note": "Customer made a mistake",\
        "refund_line_items": [\
          {\
            "id": 1013445035,\
            "line_item": {\
              "fulfillment_service": null,\
              "fulfillment_status": null,\
              "grams": 0,\
              "price": 729000,\
              "product_id": 1003346284,\
              "quantity": 2,\
              "requires_shipping": true,\
              "sku": "NAM006",\
              "title": "Áo sơ mi nam màu xanh",\
              "variant_id": 1008864403,\
              "variant_title": "Default Title",\
              "vendor": "Khác",\
              "name": "Áo sơ mi nam màu xanh",\
              "id": 0,\
              "barcode": "NAM006",\
              "properties": null\
            },\
            "line_item_id": 1315883217,\
            "quantity": 1\
          }\
        ],\
        "restock": true,\
        "user_id": 200000500173,\
        "order_id": 1235748629,\
        "location_id": 895636,\
        "transactions": [\
          {\
            "amount": -300000,\
            "authorization": null,\
            "created_at": "2021-10-20T15:57:48.224Z",\
            "device_id": null,\
            "gateway": "Thanh toán khi giao hàng (COD)",\
            "id": 1095775466,\
            "kind": "refund",\
            "order_id": 1235748629,\
            "receipt": null,\
            "status": "Thành công",\
            "test": false,\
            "user_id": 200000500173,\
            "location_id": 895636,\
            "payment_details": null,\
            "parent_id": null,\
            "currency": "VND",\
            "haravan_transaction_id": null,\
            "external_transaction_id": null,\
            "send_email": false\
          }\
        ]\
      }\
    ],
    "subtotal_price": 1458000,
    "total_discounts": 0,
    "total_line_items_price": 1458000,
    "total_price": 1458000,
    "transactions": [\
      {\
        "amount": -300000,\
        "authorization": null,\
        "created_at": "2021-10-20T15:57:48.224Z",\
        "device_id": null,\
        "gateway": "Thanh toán khi giao hàng (COD)",\
        "id": 1095775466,\
        "kind": "refund",\
        "order_id": 1235748629,\
        "receipt": null,\
        "status": null,\
        "test": false,\
        "user_id": 200000500173,\
        "location_id": 895636,\
        "payment_details": null,\
        "parent_id": null,\
        "currency": "VND",\
        "haravan_transaction_id": null,\
        "external_transaction_id": null,\
        "send_email": false\
      },\
      {\
        "amount": 1458000,\
        "authorization": null,\
        "created_at": "2021-10-20T15:55:55.643Z",\
        "device_id": null,\
        "gateway": "Thanh toán khi giao hàng (COD)",\
        "id": 1095775354,\
        "kind": "capture",\
        "order_id": 1235748629,\
        "receipt": null,\
        "status": null,\
        "test": false,\
        "user_id": 1000374246,\
        "location_id": 895636,\
        "payment_details": null,\
        "parent_id": 1095775335,\
        "currency": "VND",\
        "haravan_transaction_id": null,\
        "external_transaction_id": null,\
        "send_email": false\
      },\
      {\
        "amount": 1458000,\
        "authorization": null,\
        "created_at": "2021-10-20T15:55:28.965Z",\
        "device_id": null,\
        "gateway": "Thanh toán khi giao hàng (COD)",\
        "id": 1095775335,\
        "kind": "pending",\
        "order_id": 1235748629,\
        "receipt": null,\
        "status": null,\
        "test": false,\
        "user_id": 1000374246,\
        "location_id": 895636,\
        "payment_details": null,\
        "parent_id": null,\
        "currency": "VND",\
        "haravan_transaction_id": null,\
        "external_transaction_id": null,\
        "send_email": false\
      }\
    ],
    "cancelled_status": "cancelled",
    ...
  }
}

```

### Update an order [​](https://docs.haravan.com/docs/omni-apis/orders/\#update-an-order "Direct link to heading")

PUT

https://apis.haravan.com/com/orders/{order\_id}.json

Add a note to order.

- PUT `https://apis.haravan.com/com/orders/1225418252.json`

```codeBlockLines_e6Vv
{
  "order": {
    "id": 1225418252,
    "note": "Customer contacted us about a custom engraving on this iPod"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "order": {
        "billing_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "id": 1038792095,
            "last_name": null,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "default": true,
            "district": null,
            "district_code": null,
            "ward": null,
            "ward_code": null
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": null,
        "cancelled_at": null,
        "cart_token": "be096a3e0dc34d5f888aaacb71be03b1",
        "checkout_token": "be096a3e0dc34d5f888aaacb71be03b1",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2021-09-08T19:08:14.558Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": null,\
                    "id": 1060106899,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " ",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": null,\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1061189728,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": null,\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": null,\
                    "country_code": "vn",\
                    "default": false,\
                    "district": null,\
                    "district_code": null,\
                    "ward": null,\
                    "ward_code": null\
                },\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1060107099,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                }\
            ],
            "created_at": "2020-11-19T06:53:12.246Z",
            "default_address": {
                "address1": "123 abc",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": null,
                "id": 1060106899,
                "last_name": null,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": null,
                "name": " ",
                "province_code": "HC",
                "country_code": "vn",
                "default": true,
                "district": "Quận 11",
                "district_code": "HC476",
                "ward": "Phường 15",
                "ward_code": "27208"
            },
            "email": "foo@example.com",
            "phone": null,
            "first_name": null,
            "id": 1038792095,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1225422362,
            "last_order_name": "#100538",
            "note": "vip",
            "orders_count": 29,
            "state": "Disabled",
            "tags": null,
            "total_spent": 36000000.0000,
            "total_paid": 0.0,
            "updated_at": "2021-09-08T19:55:44Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [\
            {\
                "amount": 600000.0000,\
                "code": "KM",\
                "type": "fixed_amount",\
                "is_coupon_code": false\
            }\
        ],
        "email": "foo@example.com",
        "financial_status": "paid",
        "fulfillments": [\
            {\
                "created_at": "2021-09-08T19:08:14.637Z",\
                "id": 1052690678,\
                "order_id": 1225418252,\
                "receipt": null,\
                "status": "success",\
                "tracking_company": null,\
                "tracking_company_code": null,\
                "tracking_numbers": [],\
                "tracking_number": null,\
                "tracking_url": null,\
                "tracking_urls": [],\
                "updated_at": "2021-09-08T19:08:14.829Z",\
                "line_items": [\
                    {\
                        "fulfillable_quantity": 0,\
                        "fulfillment_service": "Thủ công",\
                        "fulfillment_status": "Chưa hoàn thành",\
                        "grams": 0.0000,\
                        "id": 1293002813,\
                        "price": 600000.0000,\
                        "product_id": 1028183659,\
                        "quantity": 1,\
                        "requires_shipping": true,\
                        "sku": null,\
                        "title": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_id": 1061514693,\
                        "variant_title": "Default Title",\
                        "vendor": "Khác",\
                        "name": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_inventory_management": null,\
                        "properties": null,\
                        "product_exists": false\
                    }\
                ],\
                "notify_customer": false,\
                "province": null,\
                "province_code": null,\
                "district": null,\
                "district_code": null,\
                "ward": null,\
                "ward_code": null,\
                "cod_amount": 0.0000,\
                "carrier_status_name": "Đã giao hàng",\
                "carrier_cod_status_name": "Không",\
                "carrier_status_code": "delivered",\
                "carrier_cod_status_code": "none",\
                "location_id": 963414,\
                "shipping_package": 0,\
                "note": null,\
                "carrier_service_package": 0,\
                "carrier_service_package_name": null,\
                "is_new_service_package": false,\
                "coupon_code": null,\
                "ready_to_pick_date": null,\
                "picking_date": null,\
                "delivering_date": null,\
                "delivered_date": null,\
                "return_date": null,\
                "not_meet_customer_date": null,\
                "waiting_for_return_date": null,\
                "cod_paid_date": null,\
                "cod_receipt_date": null,\
                "cod_pending_date": null,\
                "cod_not_receipt_date": null,\
                "cancel_date": null,\
                "is_view_before": null,\
                "country": null,\
                "country_code": null,\
                "zip_code": null,\
                "city": null,\
                "real_shipping_fee": 0.0000,\
                "shipping_notes": null,\
                "total_weight": 0.0,\
                "package_length": 0.00,\
                "package_width": 0.00,\
                "package_height": 0.00,\
                "boxme_servicecode": null,\
                "transport_type": 0,\
                "address": null,\
                "sender_phone": null,\
                "sender_name": null,\
                "carrier_service_code": null,\
                "from_longtitude": 0.0,\
                "from_latitude": 0.0,\
                "to_longtitude": 0.0,\
                "to_latitude": 0.0,\
                "sort_code": null,\
                "is_drop_off": false,\
                "is_insurance": false,\
                "insurance_price": 0.0,\
                "is_open_box": false,\
                "request_id": null,\
                "carrier_options": null,\
                "note_attributes": null,\
                "first_name": null,\
                "last_name": null,\
                "shipping_address": null,\
                "shipping_phone": null,\
                "carrier_shop_id": null\
            }\
        ],
        "fulfillment_status": "fulfilled",
        "tags": null,
        "gateway": null,
        "gateway_code": null,
        "id": 1225418252,
        "landing_site": null,
        "landing_site_ref": null,
        "source": null,
        "line_items": [\
            {\
                "fulfillable_quantity": 0,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1293002813,\
                "price": 600000.0000,\
                "price_original": 600000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1028183659,\
                "quantity": 1,\
                "requires_shipping": true,\
                "sku": null,\
                "title": "Đầm babydoll tay lỡ khoét lỗ",\
                "variant_id": 1061514693,\
                "variant_title": "Default Title",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": null,\
                "properties": null,\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 0.00\
            }\
        ],
        "name": "#100534",
        "note": "Customer contacted us about a custom engraving on this iPod",
        "number": 1225418252,
        "order_number": "#100534",
        "processing_method": null,
        "referring_site": null,
        "refunds": [],
        "shipping_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "district_code": null,
            "district": null,
            "ward_code": null,
            "ward": null
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": null,
        "subtotal_price": 600000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "be096a3e0dc34d5f888aaacb71be03b1",
        "total_discounts": 600000.0000,
        "total_line_items_price": 600000.0000,
        "total_price": 0.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2021-09-08T20:02:06.987Z",
        "transactions": [\
            {\
                "amount": 0.0000,\
                "authorization": null,\
                "created_at": "2021-09-08T19:08:14.558Z",\
                "device_id": null,\
                "gateway": "",\
                "id": 1091219306,\
                "kind": "capture",\
                "order_id": 1225418252,\
                "receipt": null,\
                "status": null,\
                "test": false,\
                "user_id": 200000497867,\
                "location_id": 963414,\
                "payment_details": null,\
                "parent_id": 1091219305,\
                "currency": "VND",\
                "haravan_transaction_id": null,\
                "external_transaction_id": null,\
                "send_email": false\
            },\
            {\
                "amount": 0.0000,\
                "authorization": null,\
                "created_at": "2021-09-08T19:08:14.558Z",\
                "device_id": null,\
                "gateway": "",\
                "id": 1091219305,\
                "kind": "pending",\
                "order_id": 1225418252,\
                "receipt": null,\
                "status": null,\
                "test": false,\
                "user_id": 200000497867,\
                "location_id": 963414,\
                "payment_details": null,\
                "parent_id": null,\
                "currency": "VND",\
                "haravan_transaction_id": null,\
                "external_transaction_id": null,\
                "send_email": false\
            }\
        ],
        "note_attributes": [],
        "confirmed_at": null,
        "closed_status": "unclosed",
        "cancelled_status": "uncancelled",
        "confirmed_status": "unconfirmed",
        "user_id": 200000497867,
        "device_id": null,
        "location_id": 963414,
        "ref_order_id": 0,
        "ref_order_number": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "omni_order_status": 0,
        "omni_order_status_name": null,
        "location_assigned_at": null,
        "in_stock_at": null,
        "out_of_stock_at": null,
        "export_at": null,
        "complete_at": null,
        "payment_url": null,
        "contact_email": "foo@example.com"
    }
}

```

Update note attributes to an order.

- PUT `https://apis.haravan.com/com/orders/1225418252.json`

```codeBlockLines_e6Vv
{
  "order": {
    "id": 1225418252,
    "note_attributes": [\
      {\
        "name": "colour",\
        "value": "red"\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "order": {
        "billing_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "id": 1038792095,
            "last_name": null,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "default": true,
            "district": null,
            "district_code": null,
            "ward": null,
            "ward_code": null
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": null,
        "cancelled_at": null,
        "cart_token": "be096a3e0dc34d5f888aaacb71be03b1",
        "checkout_token": "be096a3e0dc34d5f888aaacb71be03b1",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2021-09-08T19:08:14.558Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": null,\
                    "id": 1060106899,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " ",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                },\
                {\
                    "address1": null,\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1061189728,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": null,\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": null,\
                    "country_code": "vn",\
                    "default": false,\
                    "district": null,\
                    "district_code": null,\
                    "ward": null,\
                    "ward_code": null\
                },\
                {\
                    "address1": "123 abc",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "abc",\
                    "id": 1060107099,\
                    "last_name": "xxx",\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": "xxx abc",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                }\
            ],
            "created_at": "2020-11-19T06:53:12.246Z",
            "default_address": {
                "address1": "123 abc",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": null,
                "id": 1060106899,
                "last_name": null,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": null,
                "name": " ",
                "province_code": "HC",
                "country_code": "vn",
                "default": true,
                "district": "Quận 11",
                "district_code": "HC476",
                "ward": "Phường 15",
                "ward_code": "27208"
            },
            "email": "foo@example.com",
            "phone": null,
            "first_name": null,
            "id": 1038792095,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1225422362,
            "last_order_name": "#100538",
            "note": "vip",
            "orders_count": 29,
            "state": "Disabled",
            "tags": null,
            "total_spent": 36000000.0000,
            "total_paid": 0.0,
            "updated_at": "2021-09-08T19:55:44Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [\
            {\
                "amount": 600000.0000,\
                "code": "KM",\
                "type": "fixed_amount",\
                "is_coupon_code": false\
            }\
        ],
        "email": "a-different@email.com",
        "financial_status": "paid",
        "fulfillments": [\
            {\
                "created_at": "2021-09-08T19:08:14.637Z",\
                "id": 1052690678,\
                "order_id": 1225418252,\
                "receipt": null,\
                "status": "success",\
                "tracking_company": null,\
                "tracking_company_code": null,\
                "tracking_numbers": [],\
                "tracking_number": null,\
                "tracking_url": null,\
                "tracking_urls": [],\
                "updated_at": "2021-09-08T19:08:14.829Z",\
                "line_items": [\
                    {\
                        "fulfillable_quantity": 0,\
                        "fulfillment_service": "Thủ công",\
                        "fulfillment_status": "Chưa hoàn thành",\
                        "grams": 0.0000,\
                        "id": 1293002813,\
                        "price": 600000.0000,\
                        "product_id": 1028183659,\
                        "quantity": 1,\
                        "requires_shipping": true,\
                        "sku": null,\
                        "title": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_id": 1061514693,\
                        "variant_title": "Default Title",\
                        "vendor": "Khác",\
                        "name": "Đầm babydoll tay lỡ khoét lỗ",\
                        "variant_inventory_management": null,\
                        "properties": null,\
                        "product_exists": false\
                    }\
                ],\
                "notify_customer": false,\
                "province": null,\
                "province_code": null,\
                "district": null,\
                "district_code": null,\
                "ward": null,\
                "ward_code": null,\
                "cod_amount": 0.0000,\
                "carrier_status_name": "Đã giao hàng",\
                "carrier_cod_status_name": "Không",\
                "carrier_status_code": "delivered",\
                "carrier_cod_status_code": "none",\
                "location_id": 963414,\
                "shipping_package": 0,\
                "note": null,\
                "carrier_service_package": 0,\
                "carrier_service_package_name": null,\
                "is_new_service_package": false,\
                "coupon_code": null,\
                "ready_to_pick_date": null,\
                "picking_date": null,\
                "delivering_date": null,\
                "delivered_date": null,\
                "return_date": null,\
                "not_meet_customer_date": null,\
                "waiting_for_return_date": null,\
                "cod_paid_date": null,\
                "cod_receipt_date": null,\
                "cod_pending_date": null,\
                "cod_not_receipt_date": null,\
                "cancel_date": null,\
                "is_view_before": null,\
                "country": null,\
                "country_code": null,\
                "zip_code": null,\
                "city": null,\
                "real_shipping_fee": 0.0000,\
                "shipping_notes": null,\
                "total_weight": 0.0,\
                "package_length": 0.00,\
                "package_width": 0.00,\
                "package_height": 0.00,\
                "boxme_servicecode": null,\
                "transport_type": 0,\
                "address": null,\
                "sender_phone": null,\
                "sender_name": null,\
                "carrier_service_code": null,\
                "from_longtitude": 0.0,\
                "from_latitude": 0.0,\
                "to_longtitude": 0.0,\
                "to_latitude": 0.0,\
                "sort_code": null,\
                "is_drop_off": false,\
                "is_insurance": false,\
                "insurance_price": 0.0,\
                "is_open_box": false,\
                "request_id": null,\
                "carrier_options": null,\
                "note_attributes": null,\
                "first_name": null,\
                "last_name": null,\
                "shipping_address": null,\
                "shipping_phone": null,\
                "carrier_shop_id": null\
            }\
        ],
        "fulfillment_status": "fulfilled",
        "tags": null,
        "gateway": null,
        "gateway_code": null,
        "id": 1225418252,
        "landing_site": null,
        "landing_site_ref": null,
        "source": null,
        "line_items": [\
            {\
                "fulfillable_quantity": 0,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1293002813,\
                "price": 600000.0000,\
                "price_original": 600000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1028183659,\
                "quantity": 1,\
                "requires_shipping": true,\
                "sku": null,\
                "title": "Đầm babydoll tay lỡ khoét lỗ",\
                "variant_id": 1061514693,\
                "variant_title": "Default Title",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Đầm babydoll tay lỡ khoét lỗ - Default Title",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": null,\
                "properties": null,\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/200000219339/product/odette-baby-doll-dress-by-s.wallis-1_41912496455f423391fc4330cdf52dc3.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 0.00\
            }\
        ],
        "name": "#100534",
        "note": "Customer contacted us about a custom engraving on this iPod",
        "number": 1225418252,
        "order_number": "#100534",
        "processing_method": null,
        "referring_site": null,
        "refunds": [],
        "shipping_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "district_code": null,
            "district": null,
            "ward_code": null,
            "ward": null
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": null,
        "subtotal_price": 600000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "be096a3e0dc34d5f888aaacb71be03b1",
        "total_discounts": 600000.0000,
        "total_line_items_price": 600000.0000,
        "total_price": 0.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2021-09-08T20:21:30.046Z",
        "transactions": [\
            {\
                "amount": 0.0000,\
                "authorization": null,\
                "created_at": "2021-09-08T19:08:14.558Z",\
                "device_id": null,\
                "gateway": "",\
                "id": 1091219306,\
                "kind": "capture",\
                "order_id": 1225418252,\
                "receipt": null,\
                "status": null,\
                "test": false,\
                "user_id": 200000497867,\
                "location_id": 963414,\
                "payment_details": null,\
                "parent_id": 1091219305,\
                "currency": "VND",\
                "haravan_transaction_id": null,\
                "external_transaction_id": null,\
                "send_email": false\
            },\
            {\
                "amount": 0.0000,\
                "authorization": null,\
                "created_at": "2021-09-08T19:08:14.558Z",\
                "device_id": null,\
                "gateway": "",\
                "id": 1091219305,\
                "kind": "pending",\
                "order_id": 1225418252,\
                "receipt": null,\
                "status": null,\
                "test": false,\
                "user_id": 200000497867,\
                "location_id": 963414,\
                "payment_details": null,\
                "parent_id": null,\
                "currency": "VND",\
                "haravan_transaction_id": null,\
                "external_transaction_id": null,\
                "send_email": false\
            }\
        ],
        "note_attributes": [\
            {\
                "name": "colour",\
                "value": "red"\
            }\
        ],
        "confirmed_at": null,
        "closed_status": "unclosed",
        "cancelled_status": "uncancelled",
        "confirmed_status": "unconfirmed",
        "user_id": 200000497867,
        "device_id": null,
        "location_id": 963414,
        "ref_order_id": 0,
        "ref_order_number": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "omni_order_status": 0,
        "omni_order_status_name": null,
        "location_assigned_at": null,
        "in_stock_at": null,
        "out_of_stock_at": null,
        "export_at": null,
        "complete_at": null,
        "payment_url": null,
        "contact_email": "a-different@email.com"
    }
}

```

### Update tags for an order [​](https://docs.haravan.com/docs/omni-apis/orders/\#update-tags-for-an-order "Direct link to heading")

POST

https://apis.haravan.com/com/orders/{order\_id}/tags.json

Add order tags.

- GET `https://apis.haravan.com/com/orders/1050764416/tags.json`

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

### Delete tags for an order [​](https://docs.haravan.com/docs/omni-apis/orders/\#delete-tags-for-an-order "Direct link to heading")

DELETE

https://apis.haravan.com/com/orders/{order\_id}/tags.json

Delete order tags.

- DELETE `https://apis.haravan.com/com/orders/1050764416/tags.json`

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

### Assign handling user for an order (Support for advanced order processing only) [​](https://docs.haravan.com/docs/omni-apis/orders/\#assign-handling-user-for-an-order-support-for-advanced-order-processing-only "Direct link to heading")

POST

https://apis.haravan.com/com/orders/{order\_id}/assign.json

Delete order tags.

- POST `https://apis.haravan.com/com/orders/1272208520/assign.json`

```codeBlockLines_e6Vv
{
  "user_ids": [\
    200001038919\
  ],
  "group_user_ids": [\
    0\
  ],
  "location_id": 876530
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "order": {
        "billing_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "id": 1024510520,
            "last_name": null,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "default": true,
            "district": null,
            "district_code": null,
            "ward": null,
            "ward_code": null
        },
        "browser_ip": null,
        "buyer_accepts_marketing": false,
        "cancel_reason": null,
        "cancelled_at": null,
        "cart_token": "176a57e3d4af44e7b49bd0f9bac50972",
        "checkout_token": "176a57e3d4af44e7b49bd0f9bac50972",
        "client_details": {
            "accept_language": null,
            "browser_ip": null,
            "session_hash": null,
            "user_agent": null,
            "browser_height": null,
            "browser_width": null
        },
        "closed_at": null,
        "created_at": "2022-02-16T02:48:54.859Z",
        "currency": "VND",
        "customer": {
            "accepts_marketing": false,
            "addresses": [\
\
                {\
                    "address1": null,\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "---",\
                    "id": 1050398907,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": null,\
                    "name": " ---",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": false,\
                    "district": null,\
                    "district_code": null,\
                    "ward": null,\
                    "ward_code": null\
                }\
            ],
            "created_at": "2019-09-13T08:44:53.19Z",
            "default_address": {
                "address1": null,
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": "---",
                "id": 1045519900,
                "last_name": null,
                "phone": null,
                "province": null,
                "zip": null,
                "name": " ---",
                "province_code": null,
                "country_code": "vn",
                "default": true,
                "district": null,
                "district_code": null,
                "ward": null,
                "ward_code": null
            },
            "email": "guest@haravan.com",
            "phone": null,
            "first_name": null,
            "id": 1024510520,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1272208520,
            "last_order_name": "A-101757-B",
            "note": null,
            "orders_count": 290,
            "state": "Disabled",
            "tags": "chủ shop",
            "total_spent": 121981374.6222,
            "total_paid": 0.0,
            "updated_at": "2022-02-16T02:48:54.921Z",
            "verified_email": false,
            "send_email_invite": false,
            "send_email_welcome": false,
            "password": null,
            "password_confirmation": null,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": null
        },
        "discount_codes": [],
        "email": "guest@haravan.com",
        "financial_status": "pending",
        "fulfillments": [],
        "fulfillment_status": "notfulfilled",
        "tags": "test bún",
        "gateway": "Voucher",
        "gateway_code": "Custom",
        "id": 1272208520,
        "landing_site": null,
        "landing_site_ref": null,
        "source": "haravan_draft_order",
        "line_items": [\
            {\
                "fulfillable_quantity": 1,\
                "fulfillment_service": null,\
                "fulfillment_status": "notfulfilled",\
                "grams": 0.0000,\
                "id": 1393284139,\
                "price": 289000.0000,\
                "price_original": 340000.0000,\
                "price_promotion": 0.0,\
                "product_id": 1021334422,\
                "quantity": 1,\
                "requires_shipping": true,\
                "sku": "AN-007",\
                "title": "Áo Sơ mi Caro tay ngắn",\
                "variant_id": 1043103601,\
                "variant_title": "Kích thước",\
                "vendor": "Khác",\
                "type": "Khác",\
                "name": "Áo Sơ mi Caro tay ngắn - Kích thước",\
                "gift_card": false,\
                "taxable": true,\
                "tax_lines": null,\
                "product_exists": true,\
                "barcode": "00015",\
                "properties": [\
                    {\
                        "name": "Khuyến mãi",\
                        "value": "1022743973 - GIẢM 15%"\
                    }\
                ],\
                "total_discount": 0.0000,\
                "applied_discounts": [],\
                "image": {\
                    "src": "https://product.hstatic.net/1000393684/product/ben-sherman-ss-gingham-shirt-1_3beb2c18eda54de39b71d343fd311ca7.jpg",\
                    "attactment": null,\
                    "filename": null\
                },\
                "not_allow_promotion": false,\
                "ma_cost_amount": 220549.65,\
                "actual_price": 0.0\
            }\
        ],
        "name": "A-101757-B",
        "note": null,
        "number": 1272208520,
        "order_number": "A-101757-B",
        "processing_method": null,
        "referring_site": "haravan_draft_order",
        "refunds": [],
        "shipping_address": {
            "address1": null,
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": null,
            "last_name": null,
            "latitude": 0.00000000,
            "longitude": 0.00000000,
            "phone": null,
            "province": null,
            "zip": null,
            "name": " ",
            "province_code": null,
            "country_code": "VN",
            "district_code": null,
            "district": null,
            "ward_code": null,
            "ward": null
        },
        "shipping_lines": [\
            {\
                "code": null,\
                "price": 0.0000,\
                "source": null,\
                "title": null\
            }\
        ],
        "source_name": "haravan_draft_order",
        "subtotal_price": 289000.0000,
        "tax_lines": null,
        "taxes_included": false,
        "token": "176a57e3d4af44e7b49bd0f9bac50972",
        "total_discounts": 0.0000,
        "total_line_items_price": 289000.0000,
        "total_price": 289000.0000,
        "total_tax": 0.0,
        "total_weight": 0.0000,
        "updated_at": "2022-02-17T07:10:33.304Z",
        "transactions": [\
            {\
                "amount": 289000.0000,\
                "authorization": null,\
                "created_at": "2022-02-16T02:48:54.963Z",\
                "device_id": null,\
                "gateway": "Voucher",\
                "id": 1113418186,\
                "kind": "pending",\
                "order_id": 1272208520,\
                "receipt": null,\
                "status": null,\
                "test": false,\
                "user_id": 200000496639,\
                "location_id": 702473,\
                "payment_details": null,\
                "parent_id": null,\
                "currency": "VND",\
                "haravan_transaction_id": null,\
                "external_transaction_id": null,\
                "send_email": false\
            }\
        ],
        "note_attributes": [],
        "confirmed_at": "2022-02-16T02:48:55.123Z",
        "closed_status": "unclosed",
        "cancelled_status": "uncancelled",
        "confirmed_status": "confirmed",
        "user_id": 200000496639,
        "device_id": null,
        "location_id": 702473,
        "location_name": "Kho HCM2222",
        "ref_order_id": 0,
        "ref_order_number": null,
        "ref_order_date": null,
        "utm_source": null,
        "utm_medium": null,
        "utm_campaign": null,
        "utm_term": null,
        "utm_content": null,
        "redeem_model": null,
        "payment_url": null,
        "contact_email": "guest@haravan.com",
        "assigned_location_id": 876530,
        "assigned_location_name": "Kho New World",
        "assigned_location_at": "2022-02-17T07:05:36.913Z",
        "exported_confirm_at": null,
        "order_processing_status": "out_of_stock_confirm",
        "prev_order_id": 1271866649,
        "prev_order_number": "A-101747-B",
        "prev_order_date": "2022-02-15T02:32:41.665Z"
    }
}

```

[Previous\\
\\
Multipass](https://docs.haravan.com/docs/omni-apis/multipass/) [Next\\
\\
Order](https://docs.haravan.com/docs/omni-apis/orders/)

- [What you can do with Orders](https://docs.haravan.com/docs/omni-apis/orders/#what-you-can-do-with-orders)
- [Properties](https://docs.haravan.com/docs/omni-apis/orders/#properties)
- [Retrieves a list of orders](https://docs.haravan.com/docs/omni-apis/orders/#retrieves-a-list-of-orders)
- [Retrieve a count of the orders](https://docs.haravan.com/docs/omni-apis/orders/#retrieve-a-count-of-the-orders)
- [Retrieves single the order](https://docs.haravan.com/docs/omni-apis/orders/#retrieves-single-the-order)
- [Create a new order](https://docs.haravan.com/docs/omni-apis/orders/#create-a-new-order)
- [Confirm an order](https://docs.haravan.com/docs/omni-apis/orders/#confirm-an-order)
- [Close an order](https://docs.haravan.com/docs/omni-apis/orders/#close-an-order)
- [Re-open a closed order](https://docs.haravan.com/docs/omni-apis/orders/#re-open-a-closed-order)
- [Cancel an order](https://docs.haravan.com/docs/omni-apis/orders/#cancel-an-order)
- [Update an order](https://docs.haravan.com/docs/omni-apis/orders/#update-an-order)
- [Update tags for an order](https://docs.haravan.com/docs/omni-apis/orders/#update-tags-for-an-order)
- [Delete tags for an order](https://docs.haravan.com/docs/omni-apis/orders/#delete-tags-for-an-order)
- [Assign handling user for an order (Support for advanced order processing only)](https://docs.haravan.com/docs/omni-apis/orders/#assign-handling-user-for-an-order-support-for-advanced-order-processing-only)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.