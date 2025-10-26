---
url: "https://docs.haravan.com/docs/omni-apis/ward/"
title: "Ward | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/ward/#)

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
- Ward

On this page

# Ward

`Version: 1.0`

Shop owners can specify which country or countries they will ship to and these countries are made available through the API using the country resource. Shop owners can do this by navigating to the "Preferences" tab under "Regions & Taxes." If any of those countries have states or provinces, those states or provinces are also registered as shipping destinations, each of which can have its own state or provincial sales tax.

States and provinces are represented by the province resource. We use the term "province" to cover both.

**Authenticated access scopes**: `com.read_shop`

### What you can do with Ward [​](https://docs.haravan.com/docs/omni-apis/ward/\#what-you-can-do-with-ward "Direct link to heading")

- GET `https://apis.haravan.com/com/districts/{district_id}/wards.json`
  - **[Retrieves all wards for a district](https://docs.haravan.com/docs/omni-apis/ward/#retrieves-all-wards-for-a-district)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/ward/\#properties "Direct link to heading")

* * *

`code` : `string`

```codeBlockLines_e6Vv
"code": "26734"

```

The standard abbreviation for the state or ward.

* * *

`district_id` : `number`

```codeBlockLines_e6Vv
"country_id":  241

```

The unique numeric identifier for the district.

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id": 26734

```

The unique numeric identifier for the state or ward.

* * *

`name` : `string`

```codeBlockLines_e6Vv
"name": "Phường Tân Định"

```

The full name of the state or ward.

* * *

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/ward/\#endpoints "Direct link to heading")

### Retrieves all wards for a district [​](https://docs.haravan.com/docs/omni-apis/ward/\#retrieves-all-wards-for-a-district "Direct link to heading")

GET

https://apis.haravan.com/com/districts/{district\_id}/wards.json

Retrieves all wards for a district.

- GET `https://apis.haravan.com/com/districts/466/wards.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "wards": [\
        {\
            "id": 26734,\
            "name": "Phường Tân Định",\
            "code": "26734",\
            "district_id": 466\
        },\
        {\
            "id": 26737,\
            "name": "Phường Đa Kao",\
            "code": "26737",\
            "district_id": 466\
        },\
        {\
            "id": 26740,\
            "name": "Phường Bến Nghé",\
            "code": "26740",\
            "district_id": 466\
        },\
        {\
            "id": 26743,\
            "name": "Phường Bến Thành",\
            "code": "26743",\
            "district_id": 466\
        },\
        {\
            "id": 26746,\
            "name": "Phường Nguyễn Thái Bình",\
            "code": "26746",\
            "district_id": 466\
        },\
        {\
            "id": 26749,\
            "name": "Phường Phạm Ngũ Lão",\
            "code": "26749",\
            "district_id": 466\
        },\
        {\
            "id": 26752,\
            "name": "Phường Cầu Ông Lãnh",\
            "code": "26752",\
            "district_id": 466\
        },\
        {\
            "id": 26755,\
            "name": "Phường Cô Giang",\
            "code": "26755",\
            "district_id": 466\
        },\
        {\
            "id": 26758,\
            "name": "Phường Nguyễn Cư Trinh",\
            "code": "26758",\
            "district_id": 466\
        },\
        {\
            "id": 26761,\
            "name": "Phường Cầu Kho",\
            "code": "26761",\
            "district_id": 466\
        }\
    ]
}

```

[Previous\\
\\
User](https://docs.haravan.com/docs/omni-apis/user/) [Next\\
\\
Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [What you can do with Ward](https://docs.haravan.com/docs/omni-apis/ward/#what-you-can-do-with-ward)
- [Properties](https://docs.haravan.com/docs/omni-apis/ward/#properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/ward/#endpoints)
- [Retrieves all wards for a district](https://docs.haravan.com/docs/omni-apis/ward/#retrieves-all-wards-for-a-district)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.