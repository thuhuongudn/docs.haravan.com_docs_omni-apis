---
url: "https://docs.haravan.com/docs/omni-apis/location/"
title: "Location | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/location/#)

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
- Location

On this page

# Location

`Version: 1.0`

A Location represents a geographical location where your stores, headquarters, and/or pop-up shops exist. These locations can be used to track sales and to help Haravan configure the tax rates to charge when selling products.

**Authenticated access scopes**: `com.read_shop`

### What you can do with Location [​](https://docs.haravan.com/docs/omni-apis/location/\#what-you-can-do-with-location "Direct link to heading")

The Haravan API lets you do the following with the Location resource.

- GET `https://apis.haravan.com/com/locations.json`
  - **[Retrieves a list of locations](https://docs.haravan.com/docs/omni-apis/location/#retrieves-a-list-of-locations)**
- GET `https://apis.haravan.com/com/locations/{location_id}.json`
  - **[Retrieves single the location](https://docs.haravan.com/docs/omni-apis/location/#retrieves-single-the-location)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/location/\#properties "Direct link to heading")

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id": 1206854680

```

A unique numeric identifier for the location.

`name` : `string`

```codeBlockLines_e6Vv
"name": "Ottawa Store"

```

The name of the location.

`location_type` : `string`

```codeBlockLines_e6Vv
"location_type":"null"

```

The kind of location type:

- **default**: default warehouse.
- **ontheroad**: transit warehouse.

`address1` : `string`

```codeBlockLines_e6Vv
"address1":"126 york street"

```

The first line of the address.

`address2` : `string`

```codeBlockLines_e6Vv
"address2": "second and third floor"

```

The second line of the address.

`zip` : `string`

```codeBlockLines_e6Vv
"zip": "7000"

```

The zip or postal code.

`city` : `string`

```codeBlockLines_e6Vv
"city": "Ottawa"

```

The city the location is in.

`province` : `string`

```codeBlockLines_e6Vv
"province": "Ontario"

```

The province the location is in.

`country` : `string`

```codeBlockLines_e6Vv
"country": "CA"

```

The country the location is in.

`phone` : `string`

```codeBlockLines_e6Vv
"phone": "18883290139"

```

The phone number of the location.

`created_at` : `string`

```codeBlockLines_e6Vv
"created_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the location was created.

`updated_at` : `string`

```codeBlockLines_e6Vv
"updated_at": "2021-05-13T07:29:20.808Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.265662026.432268510.1660477111-1472584803.1593074357) format) when the location was last updated.

### Retrieves a list of locations [​](https://docs.haravan.com/docs/omni-apis/location/\#retrieves-a-list-of-locations "Direct link to heading")

GET

https://apis.haravan.com/com/locations.json

Retrieves a list of all locations for a shop.

- GET `https://apis.haravan.com/com/locations.json`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK
{
    "locations": [\
        {\
            "id": 991324,\
            "name": "Địa điểm mặc định",\
            "location_type": null,\
            "email": null,\
            "address1": "123 Nguyễn Dình Chiểu",\
            "address2": null,\
            "zip": "700000",\
            "city": null,\
            "province": "Hồ Chí Minh",\
            "country": "Vietnam",\
            "phone": "0332456789",\
            "country_code": "VN",\
            "country_name": "Vietnam",\
            "province_code": "HC",\
            "district": "Quận Phú Nhuận",\
            "district_code": "HC481",\
            "ward": "Phường 03",\
            "ward_code": "27055",\
            "created_at": "2020-10-22T03:35:39.461Z",\
            "updated_at": "2021-05-24T03:17:54.555Z",\
            "is_primary": true,\
            "is_unavailable_quantity": false,\
            "type": "default"\
        }\
    ]
}

```

### Retrieves single the location [​](https://docs.haravan.com/docs/omni-apis/location/\#retrieves-single-the-location "Direct link to heading")

GET

https://apis.haravan.com/com/locations/{location\_id}.json

Retrieves single the location by ID.

- GET `https://apis.haravan.com/com/locations/487838322.json`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK
{
    "location": {
        "id": 991324,
        "name": "Địa điểm mặc định",
        "location_type": null,
        "email": null,
        "address1": "123 Nguyễn Dình Chiểu",
        "address2": null,
        "zip": "700000",
        "city": null,
        "province": "Hồ Chí Minh",
        "country": "Vietnam",
        "phone": "0332456789",
        "country_code": "VN",
        "country_name": "Vietnam",
        "province_code": "HC",
        "district": "Quận Phú Nhuận",
        "district_code": "HC481",
        "ward": "Phường 03",
        "ward_code": "27055",
        "created_at": "2020-10-22T03:35:39.461Z",
        "updated_at": "2021-05-24T03:17:54.555Z",
        "is_primary": true,
        "is_unavailable_quantity": false,
        "type": "default"
    }
}

```

[Previous\\
\\
District](https://docs.haravan.com/docs/omni-apis/district/) [Next\\
\\
Policy](https://docs.haravan.com/docs/omni-apis/policy/)

- [What you can do with Location](https://docs.haravan.com/docs/omni-apis/location/#what-you-can-do-with-location)
- [Properties](https://docs.haravan.com/docs/omni-apis/location/#properties)
- [Retrieves a list of locations](https://docs.haravan.com/docs/omni-apis/location/#retrieves-a-list-of-locations)
- [Retrieves single the location](https://docs.haravan.com/docs/omni-apis/location/#retrieves-single-the-location)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.