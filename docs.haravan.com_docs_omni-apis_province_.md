---
url: "https://docs.haravan.com/docs/omni-apis/province/"
title: "Province | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/province/#)

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
- Province

On this page

# Province

Shop owners can specify which country or countries they will ship to and these countries are made available through the API using the province resource.

States and provinces are represented by the province resource. We use the term "province" to cover both.

**Authenticated access scopes**: `com.read_shop`

### What you can do with Province [​](https://docs.haravan.com/docs/omni-apis/province/\#what-you-can-do-with-province "Direct link to heading")

The Haravan API lets you do the following with the Province resource.

- GET `https://apis.haravan.com/com/countries/{country_id}/provinces.json`
  - **[Retrieves all province for a country](https://docs.haravan.com/docs/omni-apis/province/#retrieves-all-province-for-a-country)**
- GET `https://apis.haravan.com/com/countries/{country_id}/provinces/count.json`
  - **[Retrieve a count of all provinces for a country](https://docs.haravan.com/docs/omni-apis/province/#retrieve-a-count-of-all-provinces-for-a-country)**
- GET `https://apis.haravan.com/com/countries/{country_id}/provinces/{province_id}.json`
  - **[Retrieves single province](https://docs.haravan.com/docs/omni-apis/province/#retrieves-single-province)**

### Province properties [​](https://docs.haravan.com/docs/omni-apis/province/\#province-properties "Direct link to heading")

`code`: `string`

```codeBlockLines_e6Vv
"code": "VN"

```

The standard abbreviation for the state or province.

`country_id`: `int`

```codeBlockLines_e6Vv
"country_id": 241

```

The unique numeric identifier for the country.

`id`: `number`

```codeBlockLines_e6Vv
"id": 1

```

The unique numeric identifier for the state or province.

`name`: `string`

```codeBlockLines_e6Vv
"name": "Hà Nội"

```

The full name of the state or province.

`tax`: `decimal`

```codeBlockLines_e6Vv
"tax": 0.08

```

The national sales tax rate to be applied to orders made by customers from that province or state.

`tax_name`: `string`

```codeBlockLines_e6Vv
"tax_name": null

```

The name of the tax for that province or state.

`tax_type`: `string`

```codeBlockLines_e6Vv
"tax_type": null

```

Compounded sales tax.

`tax_percentage `: `string`

```codeBlockLines_e6Vv
"tax_percentage ": null

```

The province or state's tax in percent format.

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/province/\#endpoints "Direct link to heading")

### Retrieves all province for a country [​](https://docs.haravan.com/docs/omni-apis/province/\#retrieves-all-province-for-a-country "Direct link to heading")

GET

https://apis.haravan.com/com/countries/{country\_id}/provinces.json

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/province/\#parameters "Direct link to heading")

* * *

`country_id`

The id of the country the province belongs to.

* * *

`since_id`

Restrict results to after the specified ID

* * *

`fields`

comma-separated list of fields to include in the response.

* * *

**Retrieve all provinces for a country.**

- GET `https://apis.haravan.com/com/countries/241/provinces.json`

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "provinces": [\
        {\
            "code": "HI",\
            "country_id": 241,\
            "id": 1,\
            "name": "Hà Nội",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "HG",\
            "country_id": 241,\
            "id": 2,\
            "name": "Hà Giang",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "CB",\
            "country_id": 241,\
            "id": 3,\
            "name": "Cao Bằng",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "BK",\
            "country_id": 241,\
            "id": 4,\
            "name": "Bắc Kạn",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "TQ",\
            "country_id": 241,\
            "id": 5,\
            "name": "Tuyên Quang",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "LO",\
            "country_id": 241,\
            "id": 6,\
            "name": "Lào Cai",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "DB",\
            "country_id": 241,\
            "id": 7,\
            "name": "Điện Biên",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "LI",\
            "country_id": 241,\
            "id": 8,\
            "name": "Lai Châu",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "SL",\
            "country_id": 241,\
            "id": 9,\
            "name": "Sơn La",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "YB",\
            "country_id": 241,\
            "id": 10,\
            "name": "Yên Bái",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "HO",\
            "country_id": 241,\
            "id": 11,\
            "name": "Hòa Bình",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "TY",\
            "country_id": 241,\
            "id": 12,\
            "name": "Thái Nguyên",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "LS",\
            "country_id": 241,\
            "id": 13,\
            "name": "Lạng Sơn",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "QN",\
            "country_id": 241,\
            "id": 14,\
            "name": "Quảng Ninh",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "BG",\
            "country_id": 241,\
            "id": 15,\
            "name": "Bắc Giang",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "PT",\
            "country_id": 241,\
            "id": 16,\
            "name": "Phú Thọ",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "VT",\
            "country_id": 241,\
            "id": 17,\
            "name": "Vĩnh Phúc",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "BN",\
            "country_id": 241,\
            "id": 18,\
            "name": "Bắc Ninh",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "HD",\
            "country_id": 241,\
            "id": 19,\
            "name": "Hải Dương",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "HP",\
            "country_id": 241,\
            "id": 20,\
            "name": "Hải Phòng",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "HY",\
            "country_id": 241,\
            "id": 21,\
            "name": "Hưng Yên",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "TB",\
            "country_id": 241,\
            "id": 22,\
            "name": "Thái Bình",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "HM",\
            "country_id": 241,\
            "id": 23,\
            "name": "Hà Nam",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "ND",\
            "country_id": 241,\
            "id": 24,\
            "name": "Nam Định",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "NB",\
            "country_id": 241,\
            "id": 25,\
            "name": "Ninh Bình",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "TH",\
            "country_id": 241,\
            "id": 26,\
            "name": "Thanh Hóa",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "NA",\
            "country_id": 241,\
            "id": 27,\
            "name": "Nghệ An",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "HT",\
            "country_id": 241,\
            "id": 28,\
            "name": "Hà Tĩnh",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "QB",\
            "country_id": 241,\
            "id": 29,\
            "name": "Quảng Bình",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "QT",\
            "country_id": 241,\
            "id": 30,\
            "name": "Quảng Trị",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "TT",\
            "country_id": 241,\
            "id": 31,\
            "name": "Thừa Thiên Huế",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "DA",\
            "country_id": 241,\
            "id": 32,\
            "name": "Đà Nẵng",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "QM",\
            "country_id": 241,\
            "id": 33,\
            "name": "Quảng Nam",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "QG",\
            "country_id": 241,\
            "id": 34,\
            "name": "Quảng Ngãi",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "BD",\
            "country_id": 241,\
            "id": 35,\
            "name": "Bình Định",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "PY",\
            "country_id": 241,\
            "id": 36,\
            "name": "Phú Yên",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "KH",\
            "country_id": 241,\
            "id": 37,\
            "name": "Khánh Hòa",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "NT",\
            "country_id": 241,\
            "id": 38,\
            "name": "Ninh Thuận",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "BU",\
            "country_id": 241,\
            "id": 39,\
            "name": "Bình Thuận",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "KT",\
            "country_id": 241,\
            "id": 40,\
            "name": "Kon Tum",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "GL",\
            "country_id": 241,\
            "id": 41,\
            "name": "Gia Lai",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "DC",\
            "country_id": 241,\
            "id": 42,\
            "name": "Đắk Lắk",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "DO",\
            "country_id": 241,\
            "id": 43,\
            "name": "Đắk Nông",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "LD",\
            "country_id": 241,\
            "id": 44,\
            "name": "Lâm Đồng",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "BP",\
            "country_id": 241,\
            "id": 45,\
            "name": "Bình Phước",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "TN",\
            "country_id": 241,\
            "id": 46,\
            "name": "Tây Ninh",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "BI",\
            "country_id": 241,\
            "id": 47,\
            "name": "Bình Dương",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "DN",\
            "country_id": 241,\
            "id": 48,\
            "name": "Đồng Nai",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "BV",\
            "country_id": 241,\
            "id": 49,\
            "name": "Bà Rịa - Vũng Tàu",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "HC",\
            "country_id": 241,\
            "id": 50,\
            "name": "Hồ Chí Minh",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "LA",\
            "country_id": 241,\
            "id": 51,\
            "name": "Long An",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "TG",\
            "country_id": 241,\
            "id": 52,\
            "name": "Tiền Giang",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "BT",\
            "country_id": 241,\
            "id": 53,\
            "name": "Bến Tre",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "TV",\
            "country_id": 241,\
            "id": 54,\
            "name": "Trà Vinh",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "VL",\
            "country_id": 241,\
            "id": 55,\
            "name": "Vĩnh Long",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "DT",\
            "country_id": 241,\
            "id": 56,\
            "name": "Đồng Tháp",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "AG",\
            "country_id": 241,\
            "id": 57,\
            "name": "An Giang",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "KG",\
            "country_id": 241,\
            "id": 58,\
            "name": "Kiên Giang",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "CN",\
            "country_id": 241,\
            "id": 59,\
            "name": "Cần Thơ",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "HU",\
            "country_id": 241,\
            "id": 60,\
            "name": "Hậu Giang",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "ST",\
            "country_id": 241,\
            "id": 61,\
            "name": "Sóc Trăng",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "BL",\
            "country_id": 241,\
            "id": 62,\
            "name": "Bạc Liêu",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        },\
        {\
            "code": "CM",\
            "country_id": 241,\
            "id": 63,\
            "name": "Cà Mau",\
            "tax": null,\
            "tax_name": null,\
            "tax_type": null,\
            "tax_percentage": null\
        }\
    ]
}

```

### Retrieve a count of all provinces for a country [​](https://docs.haravan.com/docs/omni-apis/province/\#retrieve-a-count-of-all-provinces-for-a-country "Direct link to heading")

GET

https://apis.haravan.com/com/countries/{country\_id}/provinces/count.json

**Retrieve a count all provinces for a country.**

- GET `https://apis.haravan.com/com/countries/241/provinces/count.json`

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 63
}

```

### Retrieves single province [​](https://docs.haravan.com/docs/omni-apis/province/\#retrieves-single-province "Direct link to heading")

GET

https://apis.haravan.com/com/countries/{country\_id}/provinces/{province\_id}.json

**Retrieves a single province for a country.**

- GET `https://apis.haravan.com/com/countries/241/provinces/1.json`

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "province": {
        "code": "HI",
        "country_id": 241,
        "id": 1,
        "name": "Hà Nội",
        "tax": null,
        "tax_name": null,
        "tax_type": null,
        "tax_percentage": null
    }
}

```

[Previous\\
\\
Policy](https://docs.haravan.com/docs/omni-apis/policy/) [Next\\
\\
Shop](https://docs.haravan.com/docs/omni-apis/shop/)

- [What you can do with Province](https://docs.haravan.com/docs/omni-apis/province/#what-you-can-do-with-province)
- [Province properties](https://docs.haravan.com/docs/omni-apis/province/#province-properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/province/#endpoints)
- [Retrieves all province for a country](https://docs.haravan.com/docs/omni-apis/province/#retrieves-all-province-for-a-country)
- [Retrieve a count of all provinces for a country](https://docs.haravan.com/docs/omni-apis/province/#retrieve-a-count-of-all-provinces-for-a-country)
- [Retrieves single province](https://docs.haravan.com/docs/omni-apis/province/#retrieves-single-province)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.