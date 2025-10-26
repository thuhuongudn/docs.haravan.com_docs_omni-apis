---
url: "https://docs.haravan.com/docs/omni-apis/shipping-rates/"
title: "ShippingRate | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/shipping-rates/#)

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

    - [ShippingRate](https://docs.haravan.com/docs/omni-apis/shipping-rates/)
  - [Store properties](https://docs.haravan.com/docs/omni-apis/country/)

  - [Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [Home page](https://docs.haravan.com/)
- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)
- Shipping

On this page

# ShippingRate

`Version: 1.0`

This is used to view shipping zones, their countries, provinces, and shipping rates.

**Authenticated access scopes**: `com.read_orders`, `com.write_orders`

### What you can do with Shipping Rate [​](https://docs.haravan.com/docs/omni-apis/shipping-rates/\#what-you-can-do-with-shipping-rate "Direct link to heading")

The Haravan API lets you do the following with the Shipping Rate resource.

- GET `https://apis.haravan.com/com/shipping_rates.json?country_id={country_id}&province_id={province_id}`
  - **[Retrieves a list of shipping rates by parameters](https://docs.haravan.com/docs/omni-apis/shipping-rates/#retrieves-a-list-of-shipping-rates-by-parameters)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/shipping-rates/\#properties "Direct link to heading")

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id": 16629518

```

A unique identifier for the shipping rate.

* * *

`title` : `string`

```codeBlockLines_e6Vv
"title": "Giao hàng tận nơi"

```

The title for the shipping rate.

* * *

`price` : `number`

```codeBlockLines_e6Vv
"price ": 10000.0000

```

The price for the shipping rate.

* * *

### Retrieves a list of shipping rates by parameters [​](https://docs.haravan.com/docs/omni-apis/shipping-rates/\#retrieves-a-list-of-shipping-rates-by-parameters "Direct link to heading")

GET

https://apis.haravan.com/com/shipping\_rates.json?country\_id=241&province\_id=50&district\_id=478

### Parameters [​](https://docs.haravan.com/docs/omni-apis/shipping-rates/\#parameters "Direct link to heading")

* * *

`country_id`

Country of shipping rates. Get country\_id at [country API](https://docs.haravan.com/docs/omni-apis/country/).

* * *

`province_id`

Province of shipping rates. Get province\_id at [province API](https://docs.haravan.com/docs/omni-apis/province/).

* * *

`district_id`

District of shipping rates. Get district\_id at [district API](https://docs.haravan.com/docs/omni-apis/district/).

* * *

`total_price`

The total price of the order.

* * *

`total_weight`

The total weight of the package.

* * *

Retrieves a list of shipping rates by district.

- GET: `https://apis.haravan.com/com/shipping_rates.json?country_id=241&province_id=50&district_id=478`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "shipping_rates": [\
        {\
            "id": 1607492,\
            "title": "Giao hàng tận nơi",\
            "price": 20000.0000\
        }\
    ]
}

```

[Previous\\
\\
SmartCollection](https://docs.haravan.com/docs/omni-apis/smart-collections/) [Next\\
\\
ShippingRate](https://docs.haravan.com/docs/omni-apis/shipping-rates/)

- [What you can do with Shipping Rate](https://docs.haravan.com/docs/omni-apis/shipping-rates/#what-you-can-do-with-shipping-rate)
- [Properties](https://docs.haravan.com/docs/omni-apis/shipping-rates/#properties)
- [Retrieves a list of shipping rates by parameters](https://docs.haravan.com/docs/omni-apis/shipping-rates/#retrieves-a-list-of-shipping-rates-by-parameters)
- [Parameters](https://docs.haravan.com/docs/omni-apis/shipping-rates/#parameters)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.