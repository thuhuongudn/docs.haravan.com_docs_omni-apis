---
url: "https://docs.haravan.com/docs/omni-apis/country/"
title: "Country | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/country/#)

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
- Store properties

On this page

# Country

Shop owners can specify the country or countries they will ship their products to. Shop owners are able to do this through their shop admin dashboard in the "

These countries are made available through the API using the country resource. The countries list resource represents the set of countries that have been specified as shipping destinations, including an additional default 'country' called 'Rest of World', which represents the non-specified countries. An important piece of information included with each country is the country's national sales tax rate, which you can modify to account for surtaxes or exemptions that apply to the shop.

**Authenticated access scopes**: `com.read_shop`

### What you can do with Country [​](https://docs.haravan.com/docs/omni-apis/country/\#what-you-can-do-with-country "Direct link to heading")

The Haravan API lets you do the following with the Product resource.

- GET `https://apis.haravan.com/com/countries.json`
  - **[Retrieves all countries](https://docs.haravan.com/docs/omni-apis/country/#retrieves-all-countries)**
- GET `https://apis.haravan.com/com/countries/count.json`
  - **[Retrieve a count of all countries](https://docs.haravan.com/docs/omni-apis/country/#retrieve-a-count-of-all-countries)**
- GET `https://apis.haravan.com/com/countries/{country_id}.json`
  - **[Retrieves single country](https://docs.haravan.com/docs/omni-apis/country/#retrieves-single-country)**

### Country properties [​](https://docs.haravan.com/docs/omni-apis/country/\#country-properties "Direct link to heading")

`carrier_shipping_rate_providers`: `object`

```codeBlockLines_e6Vv
"carrier_shipping_rate_providers": null

```

Information about carrier shipping providers and the rates used.

`country_id`: `int`

```codeBlockLines_e6Vv
"country_id": 241

```

The unique numeric identifier for the country.

`code`: `string`

```codeBlockLines_e6Vv
"code": "VN"

```

The ISO 3166-1 alpha-2 two-letter country code for the country. The code for a given country will be the same as the code for the same country in another shop.

`id`: `number`

```codeBlockLines_e6Vv
"id": 1

```

The unique numeric identifier for the country. It is important to note that the id for a given country in one shop will not be the same as the id for the same country in another shop.

`name`: `string`

```codeBlockLines_e6Vv
"name": "VietNam"

```

The full name of the country, in English.

`tax_name`: `string`

```codeBlockLines_e6Vv
"tax_name": null

```

The name of the tax for that province or state.

`price_based_shipping_rates`: `object`

```codeBlockLines_e6Vv
"price_based_shipping_rates": null

```

Information about price based shipping rates used.

`provinces `: `object`

```codeBlockLines_e6Vv
"provinces ": null

```

The list of provinces involved in the country. References to object properties in [Province API](https://docs.haravan.com/docs/omni-apis/province/)

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/country/\#endpoints "Direct link to heading")

### Retrieves all countries [​](https://docs.haravan.com/docs/omni-apis/country/\#retrieves-all-countries "Direct link to heading")

GET

https://apis.haravan.com/com/countries.json

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/country/\#parameters "Direct link to heading")

* * *

`fields`

comma-separated list of fields to include in the response.

* * *

**Retrieve all countries.**

- GET `https://apis.haravan.com/com/countries.json`

Response:

Details

```codeBlockLines_e6Vv
{
    "countries": [\
        {\
            "carrier_shipping_rate_providers": null,\
            "code": "TH",\
            "id": 243,\
            "name": "Thailand",\
            "price_based_shipping_rates": null,\
            "provinces": [\
                {\
                    "code": "TH-37",\
                    "country_id": 243,\
                    "id": 126,\
                    "name": "Amnat Charoen",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-15",\
                    "country_id": 243,\
                    "id": 127,\
                    "name": "Ang Thong",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-10",\
                    "country_id": 243,\
                    "id": 128,\
                    "name": "Bangkok",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-38",\
                    "country_id": 243,\
                    "id": 129,\
                    "name": "Bueng Kan",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-31",\
                    "country_id": 243,\
                    "id": 130,\
                    "name": "Buriram",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-24",\
                    "country_id": 243,\
                    "id": 131,\
                    "name": "Chachoengsao",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-18",\
                    "country_id": 243,\
                    "id": 132,\
                    "name": "Chai Nat",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-36",\
                    "country_id": 243,\
                    "id": 133,\
                    "name": "Chaiyaphum",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-22",\
                    "country_id": 243,\
                    "id": 134,\
                    "name": "Chanthaburi",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-50",\
                    "country_id": 243,\
                    "id": 135,\
                    "name": "Chiang Mai",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-57",\
                    "country_id": 243,\
                    "id": 136,\
                    "name": "Chiang Rai",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-20",\
                    "country_id": 243,\
                    "id": 137,\
                    "name": "Chon Buri",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-86",\
                    "country_id": 243,\
                    "id": 138,\
                    "name": "Chumphon",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-46",\
                    "country_id": 243,\
                    "id": 139,\
                    "name": "Kalasin",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-62",\
                    "country_id": 243,\
                    "id": 140,\
                    "name": "Kamphaeng Phet",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-71",\
                    "country_id": 243,\
                    "id": 141,\
                    "name": "Kanchanaburi",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-40",\
                    "country_id": 243,\
                    "id": 142,\
                    "name": "Khon Kaen",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-81",\
                    "country_id": 243,\
                    "id": 143,\
                    "name": "Krabi",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-52",\
                    "country_id": 243,\
                    "id": 144,\
                    "name": "Lampang",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-51",\
                    "country_id": 243,\
                    "id": 145,\
                    "name": "Lamphun",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-42",\
                    "country_id": 243,\
                    "id": 146,\
                    "name": "Loei",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-16",\
                    "country_id": 243,\
                    "id": 147,\
                    "name": "Lopburi",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-58",\
                    "country_id": 243,\
                    "id": 148,\
                    "name": "Mae Hong Son",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-44",\
                    "country_id": 243,\
                    "id": 149,\
                    "name": "Maha Sarakham",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-49",\
                    "country_id": 243,\
                    "id": 150,\
                    "name": "Mukdahan",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-26",\
                    "country_id": 243,\
                    "id": 151,\
                    "name": "Nakhon Nayok",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-73",\
                    "country_id": 243,\
                    "id": 152,\
                    "name": "Nakhon Pathom",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-48",\
                    "country_id": 243,\
                    "id": 153,\
                    "name": "Nakhon Phanom",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-30",\
                    "country_id": 243,\
                    "id": 154,\
                    "name": "Nakhon Ratchasima",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-60",\
                    "country_id": 243,\
                    "id": 155,\
                    "name": "Nakhon Sawan",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-80",\
                    "country_id": 243,\
                    "id": 156,\
                    "name": "Nakhon Si Thammarat",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-55",\
                    "country_id": 243,\
                    "id": 157,\
                    "name": "Nan",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-96",\
                    "country_id": 243,\
                    "id": 158,\
                    "name": "Narathiwat",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-39",\
                    "country_id": 243,\
                    "id": 159,\
                    "name": "Nong Bua Lam Phu",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-43",\
                    "country_id": 243,\
                    "id": 160,\
                    "name": "Nong Khai",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-12",\
                    "country_id": 243,\
                    "id": 161,\
                    "name": "Nonthaburi",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-13",\
                    "country_id": 243,\
                    "id": 162,\
                    "name": "Pathum Thani",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-94",\
                    "country_id": 243,\
                    "id": 163,\
                    "name": "Pattani",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-S",\
                    "country_id": 243,\
                    "id": 164,\
                    "name": "Pattaya",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-82",\
                    "country_id": 243,\
                    "id": 165,\
                    "name": "Phangnga",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-93",\
                    "country_id": 243,\
                    "id": 166,\
                    "name": "Phatthalung",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-56",\
                    "country_id": 243,\
                    "id": 167,\
                    "name": "Phayao",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-67",\
                    "country_id": 243,\
                    "id": 168,\
                    "name": "Phetchabun",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-76",\
                    "country_id": 243,\
                    "id": 169,\
                    "name": "Phetchaburi",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-66",\
                    "country_id": 243,\
                    "id": 170,\
                    "name": "Phichit",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-65",\
                    "country_id": 243,\
                    "id": 171,\
                    "name": "Phitsanulok",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-14",\
                    "country_id": 243,\
                    "id": 172,\
                    "name": "Phra Nakhon Si Ayutthaya",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-54",\
                    "country_id": 243,\
                    "id": 173,\
                    "name": "Phrae",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-83",\
                    "country_id": 243,\
                    "id": 174,\
                    "name": "Phuket",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-25",\
                    "country_id": 243,\
                    "id": 175,\
                    "name": "Prachin Buri",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-77",\
                    "country_id": 243,\
                    "id": 176,\
                    "name": "Prachuap Khiri Khan",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-85",\
                    "country_id": 243,\
                    "id": 177,\
                    "name": "Ranong",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-70",\
                    "country_id": 243,\
                    "id": 178,\
                    "name": "Ratchaburi",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-21",\
                    "country_id": 243,\
                    "id": 179,\
                    "name": "Rayong",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-45",\
                    "country_id": 243,\
                    "id": 180,\
                    "name": "Roi Et",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-27",\
                    "country_id": 243,\
                    "id": 181,\
                    "name": "Sa Kaeo",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-47",\
                    "country_id": 243,\
                    "id": 182,\
                    "name": "Sakon Nakhon",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-11",\
                    "country_id": 243,\
                    "id": 183,\
                    "name": "Samut Prakan",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-74",\
                    "country_id": 243,\
                    "id": 184,\
                    "name": "Samut Sakhon",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-75",\
                    "country_id": 243,\
                    "id": 185,\
                    "name": "Samut Songkhram",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-19",\
                    "country_id": 243,\
                    "id": 186,\
                    "name": "Saraburi",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-91",\
                    "country_id": 243,\
                    "id": 187,\
                    "name": "Satun",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-17",\
                    "country_id": 243,\
                    "id": 188,\
                    "name": "Sing Buri",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-33",\
                    "country_id": 243,\
                    "id": 189,\
                    "name": "Sisaket",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-90",\
                    "country_id": 243,\
                    "id": 190,\
                    "name": "Songkhla",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-64",\
                    "country_id": 243,\
                    "id": 191,\
                    "name": "Sukhothai",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-72",\
                    "country_id": 243,\
                    "id": 192,\
                    "name": "Suphan Buri",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-84",\
                    "country_id": 243,\
                    "id": 193,\
                    "name": "Surat Thani",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-32",\
                    "country_id": 243,\
                    "id": 194,\
                    "name": "Surin",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-63",\
                    "country_id": 243,\
                    "id": 195,\
                    "name": "Tak",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-92",\
                    "country_id": 243,\
                    "id": 196,\
                    "name": "Trang",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-23",\
                    "country_id": 243,\
                    "id": 197,\
                    "name": "Trat",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-34",\
                    "country_id": 243,\
                    "id": 198,\
                    "name": "Ubon Ratchathani",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-41",\
                    "country_id": 243,\
                    "id": 199,\
                    "name": "Udon Thani",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-61",\
                    "country_id": 243,\
                    "id": 200,\
                    "name": "Uthai Thani",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-53",\
                    "country_id": 243,\
                    "id": 201,\
                    "name": "Uttaradit",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-95",\
                    "country_id": 243,\
                    "id": 202,\
                    "name": "Yala",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TH-35",\
                    "country_id": 243,\
                    "id": 203,\
                    "name": "Yasothon",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                }\
            ],\
            "tax": null,\
            "weight_based_shipping_rates": null\
        },\
        {\
            "carrier_shipping_rate_providers": null,\
            "code": "USA",\
            "id": 242,\
            "name": "United States",\
            "price_based_shipping_rates": null,\
            "provinces": [\
                {\
                    "code": "AL",\
                    "country_id": 242,\
                    "id": 64,\
                    "name": "Alabama",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "AK",\
                    "country_id": 242,\
                    "id": 65,\
                    "name": "Alaska",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "AS",\
                    "country_id": 242,\
                    "id": 66,\
                    "name": "American Samoa",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "AZ",\
                    "country_id": 242,\
                    "id": 67,\
                    "name": "Arizona",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "AR",\
                    "country_id": 242,\
                    "id": 68,\
                    "name": "Arkansas",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "AA",\
                    "country_id": 242,\
                    "id": 69,\
                    "name": "Armed Forces Americas",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "AE",\
                    "country_id": 242,\
                    "id": 70,\
                    "name": "Armed Forces Europe",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "AP",\
                    "country_id": 242,\
                    "id": 71,\
                    "name": "Armed Forces Pacific",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "CA",\
                    "country_id": 242,\
                    "id": 72,\
                    "name": "California",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "CO",\
                    "country_id": 242,\
                    "id": 73,\
                    "name": "Colorado",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "CT",\
                    "country_id": 242,\
                    "id": 74,\
                    "name": "Connecticut",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "DE",\
                    "country_id": 242,\
                    "id": 75,\
                    "name": "Delaware",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "DC",\
                    "country_id": 242,\
                    "id": 76,\
                    "name": "District of Columbia",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "FM",\
                    "country_id": 242,\
                    "id": 77,\
                    "name": "Federated States of Micronesia",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "FL",\
                    "country_id": 242,\
                    "id": 78,\
                    "name": "Florida",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "GA",\
                    "country_id": 242,\
                    "id": 79,\
                    "name": "Georgia",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "GU",\
                    "country_id": 242,\
                    "id": 80,\
                    "name": "Guam",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "HI",\
                    "country_id": 242,\
                    "id": 81,\
                    "name": "Hawaii",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "ID",\
                    "country_id": 242,\
                    "id": 82,\
                    "name": "Idaho",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "IL",\
                    "country_id": 242,\
                    "id": 83,\
                    "name": "Illinois",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "IN",\
                    "country_id": 242,\
                    "id": 84,\
                    "name": "Indiana",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "IA",\
                    "country_id": 242,\
                    "id": 85,\
                    "name": "Iowa",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "KS",\
                    "country_id": 242,\
                    "id": 86,\
                    "name": "Kansas",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "KY",\
                    "country_id": 242,\
                    "id": 87,\
                    "name": "Kentucky",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "LA",\
                    "country_id": 242,\
                    "id": 88,\
                    "name": "Louisiana",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "ME",\
                    "country_id": 242,\
                    "id": 89,\
                    "name": "Maine",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "MH",\
                    "country_id": 242,\
                    "id": 90,\
                    "name": "Marshall Islands",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "MD",\
                    "country_id": 242,\
                    "id": 91,\
                    "name": "Maryland",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "MA",\
                    "country_id": 242,\
                    "id": 92,\
                    "name": "Massachusetts",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "MI",\
                    "country_id": 242,\
                    "id": 93,\
                    "name": "Michigan",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "MN",\
                    "country_id": 242,\
                    "id": 94,\
                    "name": "Minnesota",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "MS",\
                    "country_id": 242,\
                    "id": 95,\
                    "name": "Mississippi",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "MO",\
                    "country_id": 242,\
                    "id": 96,\
                    "name": "Missouri",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "MT",\
                    "country_id": 242,\
                    "id": 97,\
                    "name": "Montana",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "NE",\
                    "country_id": 242,\
                    "id": 98,\
                    "name": "Nebraska",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "NV",\
                    "country_id": 242,\
                    "id": 99,\
                    "name": "Nevada",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "NH",\
                    "country_id": 242,\
                    "id": 100,\
                    "name": "New Hampshire",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "NJ",\
                    "country_id": 242,\
                    "id": 101,\
                    "name": "New Jersey",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "NM",\
                    "country_id": 242,\
                    "id": 102,\
                    "name": "New Mexico",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "NY",\
                    "country_id": 242,\
                    "id": 103,\
                    "name": "New York",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "NC",\
                    "country_id": 242,\
                    "id": 104,\
                    "name": "North Carolina",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "ND",\
                    "country_id": 242,\
                    "id": 105,\
                    "name": "North Dakota",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "MP",\
                    "country_id": 242,\
                    "id": 106,\
                    "name": "Northern Mariana Islands",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "OH",\
                    "country_id": 242,\
                    "id": 107,\
                    "name": "Ohio",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "OK",\
                    "country_id": 242,\
                    "id": 108,\
                    "name": "Oklahoma",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "OR",\
                    "country_id": 242,\
                    "id": 109,\
                    "name": "Oregon",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "PW",\
                    "country_id": 242,\
                    "id": 110,\
                    "name": "Palau",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "PA",\
                    "country_id": 242,\
                    "id": 111,\
                    "name": "Pennsylvania",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "PR",\
                    "country_id": 242,\
                    "id": 112,\
                    "name": "Puerto Rico",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "RI",\
                    "country_id": 242,\
                    "id": 113,\
                    "name": "Rhode Island",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "SC",\
                    "country_id": 242,\
                    "id": 114,\
                    "name": "South Carolina",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "SD",\
                    "country_id": 242,\
                    "id": 115,\
                    "name": "South Dakota",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TN",\
                    "country_id": 242,\
                    "id": 116,\
                    "name": "Tennessee",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "TX",\
                    "country_id": 242,\
                    "id": 117,\
                    "name": "Texas",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "UT",\
                    "country_id": 242,\
                    "id": 118,\
                    "name": "Utah",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "VT",\
                    "country_id": 242,\
                    "id": 119,\
                    "name": "Vermont",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "VI",\
                    "country_id": 242,\
                    "id": 120,\
                    "name": "Virgin Islands",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "VA",\
                    "country_id": 242,\
                    "id": 121,\
                    "name": "Virginia",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "WA",\
                    "country_id": 242,\
                    "id": 122,\
                    "name": "Washington",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "WV",\
                    "country_id": 242,\
                    "id": 123,\
                    "name": "West Virginia",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "WI",\
                    "country_id": 242,\
                    "id": 124,\
                    "name": "Wisconsin",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                },\
                {\
                    "code": "WY",\
                    "country_id": 242,\
                    "id": 125,\
                    "name": "Wyoming",\
                    "tax": null,\
                    "tax_name": null,\
                    "tax_type": null,\
                    "tax_percentage": null\
                }\
            ],\
            "tax": null,\
            "weight_based_shipping_rates": null\
        },\
        {\
            "carrier_shipping_rate_providers": null,\
            "code": "VN",\
            "id": 241,\
            "name": "Vietnam",\
            "price_based_shipping_rates": null,\
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
            ],\
            "tax": null,\
            "weight_based_shipping_rates": null\
        }\
    ]
}

```

### Retrieve a count of all countries [​](https://docs.haravan.com/docs/omni-apis/country/\#retrieve-a-count-of-all-countries "Direct link to heading")

GET

https://apis.haravan.com/com/countries/count.json

**Retrieve a count all countries.**

- GET `https://apis.haravan.com/com/countries/count.json`

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 3
}

```

### Retrieves single country [​](https://docs.haravan.com/docs/omni-apis/country/\#retrieves-single-country "Direct link to heading")

GET

https://apis.haravan.com/com/countries/{country\_id}.json

**Retrieves a single country.**

- GET `https://apis.haravan.com/com/countries/241.json`

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "country": {
        "carrier_shipping_rate_providers": null,
        "code": "VN",
        "id": 241,
        "name": "Vietnam",
        "price_based_shipping_rates": null,
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
        ],
        "tax": null,
        "weight_based_shipping_rates": null
    }
}

```

[Previous\\
\\
ShippingRate](https://docs.haravan.com/docs/omni-apis/shipping-rates/) [Next\\
\\
Country](https://docs.haravan.com/docs/omni-apis/country/)

- [What you can do with Country](https://docs.haravan.com/docs/omni-apis/country/#what-you-can-do-with-country)
- [Country properties](https://docs.haravan.com/docs/omni-apis/country/#country-properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/country/#endpoints)
- [Retrieves all countries](https://docs.haravan.com/docs/omni-apis/country/#retrieves-all-countries)
- [Retrieve a count of all countries](https://docs.haravan.com/docs/omni-apis/country/#retrieve-a-count-of-all-countries)
- [Retrieves single country](https://docs.haravan.com/docs/omni-apis/country/#retrieves-single-country)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.