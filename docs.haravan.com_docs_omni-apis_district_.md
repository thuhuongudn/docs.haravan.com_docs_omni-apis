---
url: "https://docs.haravan.com/docs/omni-apis/district/"
title: "District | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/district/#)

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
- District

On this page

# District

`Version: 1.0`

Shop owners can specify which country or countries they will ship to and these countries are made available through the API using the country resource. Shop owners can do this by navigating to the "Preferences" tab under "Regions & Taxes." If any of those countries have states or provinces, those states or provinces are also registered as shipping destinations, each of which can have its own state or provincial sales tax.

States and provinces are represented by the province resource. We use the term "province" to cover both.

**Authenticated access scopes**: `com.read_shop`

### What you can do with Disctrict [​](https://docs.haravan.com/docs/omni-apis/district/\#what-you-can-do-with-disctrict "Direct link to heading")

The Haravan API lets you do the following with the Disctrict resource.

- GET `https://apis.haravan.com/com/provinces/{province_id}/districts.json`
  - **[Retrieves all district for a province](https://docs.haravan.com/docs/omni-apis/district/#retrieves-all-district-for-a-province)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/district/\#properties "Direct link to heading")

* * *

`code` : `string`

```codeBlockLines_e6Vv
"code": "HC466"

```

The standard abbreviation for the state or district.

* * *

`district_id` : `number`

```codeBlockLines_e6Vv
"province_id":  50

```

The unique numeric identifier for the district.

* * *

`id` : `number`

```codeBlockLines_e6Vv
"id": 466

```

The unique numeric identifier for the state or district.

* * *

`name` : `string`

```codeBlockLines_e6Vv
"name": "Quận 1"

```

The full name of the state or district.

* * *

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/district/\#endpoints "Direct link to heading")

### Retrieves all district for a province [​](https://docs.haravan.com/docs/omni-apis/district/\#retrieves-all-district-for-a-province "Direct link to heading")

GET

https://apis.haravan.com/com/provinces/{province\_id}/districts.json

Retrieves all district for a province.

- GET `https://apis.haravan.com/com/provinces/50/districts.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "districts": [\
        {\
            "id": 466,\
            "name": "Quận 1",\
            "code": "HC466",\
            "province_id": 50\
        },\
        {\
            "id": 467,\
            "name": "Quận 2",\
            "code": "HC467",\
            "province_id": 50\
        },\
        {\
            "id": 468,\
            "name": "Quận 3",\
            "code": "HC468",\
            "province_id": 50\
        },\
        {\
            "id": 469,\
            "name": "Quận 4",\
            "code": "HC469",\
            "province_id": 50\
        },\
        {\
            "id": 470,\
            "name": "Quận 5",\
            "code": "HC470",\
            "province_id": 50\
        },\
        {\
            "id": 471,\
            "name": "Quận 6",\
            "code": "HC471",\
            "province_id": 50\
        },\
        {\
            "id": 472,\
            "name": "Quận 7",\
            "code": "HC472",\
            "province_id": 50\
        },\
        {\
            "id": 473,\
            "name": "Quận 8",\
            "code": "HC473",\
            "province_id": 50\
        },\
        {\
            "id": 474,\
            "name": "Quận 9",\
            "code": "HC474",\
            "province_id": 50\
        },\
        {\
            "id": 475,\
            "name": "Quận 10",\
            "code": "HC475",\
            "province_id": 50\
        },\
        {\
            "id": 476,\
            "name": "Quận 11",\
            "code": "HC476",\
            "province_id": 50\
        },\
        {\
            "id": 477,\
            "name": "Quận 12",\
            "code": "HC477",\
            "province_id": 50\
        },\
        {\
            "id": 478,\
            "name": "Quận Gò Vấp",\
            "code": "HC478",\
            "province_id": 50\
        },\
        {\
            "id": 479,\
            "name": "Quận Tân Bình",\
            "code": "HC479",\
            "province_id": 50\
        },\
        {\
            "id": 480,\
            "name": "Quận Bình Thạnh",\
            "code": "HC480",\
            "province_id": 50\
        },\
        {\
            "id": 481,\
            "name": "Quận Phú Nhuận",\
            "code": "HC481",\
            "province_id": 50\
        },\
        {\
            "id": 482,\
            "name": "Quận Thủ Đức",\
            "code": "HC482",\
            "province_id": 50\
        },\
        {\
            "id": 483,\
            "name": "Huyện Củ Chi",\
            "code": "HC483",\
            "province_id": 50\
        },\
        {\
            "id": 484,\
            "name": "Huyện Hóc Môn",\
            "code": "HC484",\
            "province_id": 50\
        },\
        {\
            "id": 485,\
            "name": "Huyện Bình Chánh",\
            "code": "HC485",\
            "province_id": 50\
        },\
        {\
            "id": 486,\
            "name": "Huyện Nhà Bè",\
            "code": "HC486",\
            "province_id": 50\
        },\
        {\
            "id": 487,\
            "name": "Huyện Cần Giờ",\
            "code": "HC487",\
            "province_id": 50\
        },\
        {\
            "id": 679,\
            "name": "Quận Bình Tân",\
            "code": "HC679",\
            "province_id": 50\
        },\
        {\
            "id": 680,\
            "name": "Quận Tân Phú",\
            "code": "HC680",\
            "province_id": 50\
        },\
        {\
            "id": 2670,\
            "name": "Thành phố Thủ Đức",\
            "code": "HC2670",\
            "province_id": 50\
        }\
    ]
}

```

[Previous\\
\\
Country](https://docs.haravan.com/docs/omni-apis/country/) [Next\\
\\
Location](https://docs.haravan.com/docs/omni-apis/location/)

- [What you can do with Disctrict](https://docs.haravan.com/docs/omni-apis/district/#what-you-can-do-with-disctrict)
- [Properties](https://docs.haravan.com/docs/omni-apis/district/#properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/district/#endpoints)
- [Retrieves all district for a province](https://docs.haravan.com/docs/omni-apis/district/#retrieves-all-district-for-a-province)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.