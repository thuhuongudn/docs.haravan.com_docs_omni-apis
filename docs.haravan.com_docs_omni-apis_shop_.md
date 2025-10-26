---
url: "https://docs.haravan.com/docs/omni-apis/shop/"
title: "Shop | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/shop/#)

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

    - [Country](https://docs.haravan.com/docs/omni-apis/country/)
    - [District](https://docs.haravan.com/docs/omni-apis/district/)
    - [Location](https://docs.haravan.com/docs/omni-apis/location/)
    - [Policy](https://docs.haravan.com/docs/omni-apis/policy/)
    - [Province](https://docs.haravan.com/docs/omni-apis/province/)
    - [Shop](https://docs.haravan.com/docs/omni-apis/shop/)
    - [User](https://docs.haravan.com/docs/omni-apis/user/)
    - [Ward](https://docs.haravan.com/docs/omni-apis/ward/)
  - [Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [Home page](https://docs.haravan.com/)
- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)
- [Store properties](https://docs.haravan.com/docs/omni-apis/country/)
- Shop

On this page

# Shop

Only the shop owner can edit this information from inside their shop admin dashboard by navigating to the "Settings" tab and selecting the "General" tab. The API doesn't let you do anything other than retrieving information about a shop.

**Authenticated access scopes**: `com.read_shop`

### What you can do with Shop [​](https://docs.haravan.com/docs/omni-apis/shop/\#what-you-can-do-with-shop "Direct link to heading")

The haravan API lets you do the following with the Shop resource.

- GET `https://apis.haravan.com/com/shop.json`
  - **[Retrieves a single shop](https://docs.haravan.com/docs/omni-apis/shop/#retrieves-a-single-shop)**

### Shop properties [​](https://docs.haravan.com/docs/omni-apis/shop/\#shop-properties "Direct link to heading")

* * *

`address1`: `string`

```codeBlockLines_e6Vv
{"address1": "1 Infinite"}

```

The shop's street address.

`city`: `string`

```codeBlockLines_e6Vv
{"city": "Hồ Chí Minh"}

```

The date and time [(ISO 8601 format)](https://en.wikipedia.org/wiki/ISO_8601) when the shop was created.

`city`: `string`

```codeBlockLines_e6Vv
{"city": "Hồ Chí Minh"}

```

The shop's country (by default equal to the two-letter country code).

`country`: `string`

```codeBlockLines_e6Vv
{"country": "VN"}

```

The shop's country (by default equal to the two-letter country code).

`country_code`: `string`

```codeBlockLines_e6Vv
{"country_code":"VN"}

```

The two-letter country code corresponding to the shop's country.

`country_name`: `string`

```codeBlockLines_e6Vv
{"country_name": "Vietnam"}

```

The shop's normalized country name.

`created_at`: `string`

```codeBlockLines_e6Vv
{"created_at": "2021-05-13T07:29:20.1Z"}

```

The date and time when the shop was created. The API returns this value in [(ISO 8601 format)](https://en.wikipedia.org/wiki/ISO_8601).

`customer_email`: `string`

```codeBlockLines_e6Vv
{"customer_email": "hi@gmail.com"}

```

The customer's email.

`currency`: `string`

```codeBlockLines_e6Vv
{"currency": "VND"}

```

The three-letter code for the currency that the shop accepts.

`domain`: `string`

```codeBlockLines_e6Vv
{"domain":"https://shop.com"}

```

The shop's domain.

`email`: `string`

```codeBlockLines_e6Vv
{"email" : "steve@gmail.com" }

```

The contact email address for the shop.

`google_apps_domain`: `string`

```codeBlockLines_e6Vv
{"google_apps_domain": null}

```

Feature is present when a shop has a google app domain. It will be returned as a URL. If the shop does not have this feature enabled it will default to "null.".

`google_apps_login_enabled`: `string`

```codeBlockLines_e6Vv
{"google_apps_login_enabled":null}

```

Feature is present if a shop has google apps enabled. Those shops with this feature will be able to login to the google apps login. Shops without this feature enabled will default to "null".

`total_cost`: `number`

```codeBlockLines_e6Vv
{"total_cost": 150000000000.00}

```

Total amount cost product of the inventory adjustment.

`id`: `number`

```codeBlockLines_e6Vv
{"id": 690933842}

```

A unique numeric identifier for the shop.

`latitude`: `string`

```codeBlockLines_e6Vv
{"latitude": "45.427408"}

```

Geographic coordinate specifying the north/south location of a shop.

`longitude`: `string`

```codeBlockLines_e6Vv
{"longitude": "690933842"}

```

Geographic coordinate specifying the east/west location of a shop.

`money_format`: `string`

```codeBlockLines_e6Vv
{"money_format": "đ"}

```

A string representing the way currency is formatted when the currency isn't specified.

`money_with_currency_format`: `string`

```codeBlockLines_e6Vv
{"money_with_currency_format": "-n $;n $"}

```

A string representing the way currency is formatted when the currency is specified.

`longitude`: `string`

```codeBlockLines_e6Vv
{"longitude": "690933842"}

```

Geographic coordinate specifying the east/west location of a shop.

`myharavan_domain`: `string`

```codeBlockLines_e6Vv
{"myharavan_domain": "https:shop.myharavan.com"}

```

The shop's 'myharavan.com' domain.

`name`: `string`

```codeBlockLines_e6Vv
{"name": "shop"}

```

The name of the shop.

`plan_name`: `string`

```codeBlockLines_e6Vv
{"plan_name": "enterprise"}

```

The name of the haravan plan the shop is on.

`display_plan_name`: `string`

```codeBlockLines_e6Vv
{"display_plan_name": "enterprise"}

```

The display name of the haravan plan the shop is on.

`password_enabled`: `boolean`

```codeBlockLines_e6Vv
{"password_enabled": false}

```

Indicates whether the Storefront password protection is enabled.

`phone`: `string`

```codeBlockLines_e6Vv
{"phone": null}

```

Geographic coordinate specifying the east/west location of a shop.

`longitude`: `string`

```codeBlockLines_e6Vv
{"longitude": "690933842"}

```

The contact phone number for the shop.

`primary_locale`: `string`

```codeBlockLines_e6Vv
{"primary_locale": "fr"}

```

The shop's primary locale.

`province`: `string`

```codeBlockLines_e6Vv
{"province": "Hồ Chí Minh"}

```

The shop's normalized province or state name.

`province_code`: `string`

```codeBlockLines_e6Vv
{"province_code": "HC"}

```

The two-letter code for the shop's province or state.

`shop_owner`: `string`

```codeBlockLines_e6Vv
{"shop_owner": "steve"}

```

The username of the shop owner.

`source`: `string`

```codeBlockLines_e6Vv
{"source": null}

```

The handle of the partner account that referred the merchant to Haravan, if applicable.

`tax_shipping`: `boolean`

```codeBlockLines_e6Vv
{"tax_shipping": false}

```

Whether taxes are charged for shipping. Valid values: true or false.

`taxes_included`: `string`

```codeBlockLines_e6Vv
{"taxes_included": null}

```

Whether applicable taxes are included in product prices. Valid values: true or null.

`county_taxes`: `boolean`

```codeBlockLines_e6Vv
{"county_taxes": null}

```

The setting for whether the shop is applying taxes on a per-county basis or not (US-only). Valid values are: "true" or "null.".

`timezone`: `string`

```codeBlockLines_e6Vv
{"timezone": "(GMT+07:00) Hanoi"}

```

The name of the timezone the shop is in.

`timezone`: `number`

```codeBlockLines_e6Vv
{"zip": 7000}

```

The zip or postal code of the shop's address.

`has_storefront`: `boolean`

```codeBlockLines_e6Vv
{"has_storefront": true}

```

Indicates whether the shop has a web-based storefront or not.

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/shop/\#endpoints "Direct link to heading")

### Retrieves a single shop. [​](https://docs.haravan.com/docs/omni-apis/shop/\#retrieves-a-single-shop "Direct link to heading")

GET

https://apis.haravan.com/com/shop.json

**Retrieve a single shop.**

- GET `https://apis.haravan.com/com/shop.json`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK
{
    "shop": {
        "address1": "123 Nguyễn Dình Chiểu",
        "city": null,
        "country": "VN",
        "country_code": "VN",
        "country_name": "Vietnam",
        "created_at": "2020-10-22T03:35:37.455Z",
        "customer_email": "shop@gmail.com",
        "currency": "VND",
        "domain": "https://shop-2.myharavan.com/",
        "email": "shop@gmail.com",
        "google_apps_domain": null,
        "google_apps_login_enabled": null,
        "id": 200000244883,
        "latitude": 0.0,
        "longitude": 0.0,
        "money_format": "₫",
        "money_with_currency_format": "-n $;n $",
        "myharavan_domain": "https://shop-2.myharavan.com",
        "name": "shop-2",
        "plan_name": null,
        "display_plan_name": null,
        "password_enabled": true,
        "phone": "0332456789",
        "province": "Hồ Chí Minh",
        "province_code": "HC",
        "public": null,
        "shop_owner": "shop-2",
        "source": null,
        "tax_shipping": false,
        "taxes_included": null,
        "county_taxes": null,
        "timezone": "(GMT+07:00) Hanoi",
        "zip": "700000",
        "has_storefront": false,
        "shop_plan_id": -1,
        "inventory_method": "default",
        "fullname_checkout_behavior": "optional",
        "email_checkout_behavior": "optional",
        "phone_checkout_behavior": "required",
        "address_checkout_behavior": "optional",
        "district_checkout_behavior": "optional",
        "ward_checkout_behavior": "disabled",
        "primary_locale": ""
    }
}

```

[Previous\\
\\
Province](https://docs.haravan.com/docs/omni-apis/province/) [Next\\
\\
User](https://docs.haravan.com/docs/omni-apis/user/)

- [What you can do with Shop](https://docs.haravan.com/docs/omni-apis/shop/#what-you-can-do-with-shop)
- [Shop properties](https://docs.haravan.com/docs/omni-apis/shop/#shop-properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/shop/#endpoints)
- [Retrieves a single shop.](https://docs.haravan.com/docs/omni-apis/shop/#retrieves-a-single-shop)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.