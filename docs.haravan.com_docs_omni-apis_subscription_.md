---
url: "https://docs.haravan.com/docs/omni-apis/subscription/"
title: "Subscription | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/subscription/#)

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

  - [Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [Home page](https://docs.haravan.com/)
- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)
- Subscription

On this page

# Subscription

`Version: 1.0`

Get paid for your app by collecting a one time charge.

### Webhooks for Subscription [​](https://docs.haravan.com/docs/omni-apis/subscription/\#webhooks-for-subscription "Direct link to heading")

You can register [webhooks](https://docs.haravan.com/docs/tutorials/webhooks/) for specific shop events. For Subscription, the following webhook topic is available:

- `app_subscriptions/update`: Triggered when the status of an app purchase one time is changed.

### What you can do with Subscription [​](https://docs.haravan.com/docs/omni-apis/subscription/\#what-you-can-do-with-subscription "Direct link to heading")

**Authenticated access scopes**: `com.read_shop`

The Haravan API lets you do the following with the Subscription resource.

- GET `https://apis.haravan.com/com/apps/app_subscriptions.json`
  - **[Retrieves a list of subscriptions](https://docs.haravan.com/docs/omni-apis/subscription/#retrieves-a-list-of-subscriptions)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/subscription/\#properties "Direct link to heading")

* * *

`id` : `string`

```codeBlockLines_e6Vv
"id": "6141d6266e269fed5b515c89"

```

The subscription ID of the application charge.

* * *

`client_id` : `string`

```codeBlockLines_e6Vv
"client_id": "9ca6a90a2f50d894e6a123f5cd7ffa62"

```

The Client ID of the application.

* * *

`created_at` : `string`

```codeBlockLines_e6Vv
"created_at": "2021-09-15T11:17:03.458Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.263581903.2138857477.1661683799-1362597417.1649044980) format) when the application charge was created.

* * *

`updated_at` : `string`

```codeBlockLines_e6Vv
"updated_at": "2021-09-15T11:17:03.458Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.263581903.2138857477.1661683799-1362597417.1649044980) format) when the application charge was last updated.

* * *

`expired_at` : `string`

```codeBlockLines_e6Vv
"expired_at": "2024-08-29T11:17:00Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.263581903.2138857477.1661683799-1362597417.1649044980) format) when the application charge ends.

* * *

`cancelled_at` : `string`

```codeBlockLines_e6Vv
"cancelled_at": null

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.263581903.2138857477.1661683799-1362597417.1649044980) format) when the merchant canceled their application charge.

**Note**: Returns `null` value when the application has not been canceled.

* * *

`name` : `string`

```codeBlockLines_e6Vv
"name": "Promotion Bar"

```

The application name.

* * *

`price` : `number`

```codeBlockLines_e6Vv
"price": 1200000

```

The price of the application.

* * *

`plan_id` : `string`

```codeBlockLines_e6Vv
"plan_id": "plan_app_449_1713"

```

The plan id of the application.

* * *

`quantity` : `number`

```codeBlockLines_e6Vv
"quantity": 1

```

The quantity of plan.

* * *

`discount_amounts` : `number`

```codeBlockLines_e6Vv
"discount_amounts": 0

```

The discount applied to the price of the application.

* * *

`total` : `number`

```codeBlockLines_e6Vv
"total": 1200000

```

The value of: price \* quantity

* * *

`amount_paid` : `number`

```codeBlockLines_e6Vv
"amount_paid": 1200000

```

The value of: total - discount\_amounts

* * *

`status` : `string`

```codeBlockLines_e6Vv
"status": "active"

```

The status of the application. Valid values:

- **active**: Application fee has been paid.

- **canceled**: The application has been canceled.


* * *

### Example webhook: [​](https://docs.haravan.com/docs/omni-apis/subscription/\#example-webhook "Direct link to heading")

```codeBlockLines_e6Vv
POST HTTP/1.1

Headers:
  Content-Type: application/json; charset=utf-8
  X-Haravan-HmacSha256: t4mhmjWKTfHND1kC9nWFXtvKyOCYj3rUUycIfkKl6Cw=
  X-Haravan-Topic: app_subscriptions/update
  X-Haravan-Org-Id: 1000114691
  X-Haravan-Subscription-Id: 6141d6266e269fed5b515c89

Body:
  {
    "id": "6141d6266e269fed5b515c89",
    "client_id": "9ca6a90a2f50d894e6a123f5cd7ffa62",
    "created_at": "2021-09-15T11:17:03.458Z",
    "updated_at": "2021-09-15T11:17:03.458Z",
    "expired_at": "2024-08-29T11:17:00Z",
    "cancelled_at": null,
    "name": "Promotion Bar",
    "price": 1200000,
    "plan_id": "plan_app_449_1713",
    "quantity": 1,
    "discount_amounts": 0,
    "total": 1200000,
    "amount_paid": 1200000,
    "status": "active"
  }

```

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/subscription/\#endpoints "Direct link to heading")

### Retrieves a list of subscriptions [​](https://docs.haravan.com/docs/omni-apis/subscription/\#retrieves-a-list-of-subscriptions "Direct link to heading")

GET

https://apis.haravan.com/com/apps/app\_subscriptions.json

Retrieves a list of subscriptions.

- GET `https://apis.haravan.com/com/apps/app_subscriptions.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
  "app_subscriptions": [\
    {\
      "id": "61cec21e84b87c000192ec49",\
      "client_id": "6e6d****30a4",\
      "created_at": "2021-12-29T05:46:11.623Z",\
      "expired_at": "2022-01-13T05:46:11.623Z",\
      "updated_at": "2021-12-29T05:46:11.623Z",\
      "cancelled_at": null,\
      "total": 200000,\
      "amount_discount": 0,\
      "amount_paid": 200000,\
      "quantity": 1,\
      "status": "active",\
      "plan_id": "plan_app_2209_1793",\
      "name": "Hara Multi-language",\
      "price": 200000\
    }\
  ]
}

```

[Previous\\
\\
Ward](https://docs.haravan.com/docs/omni-apis/ward/)

- [Webhooks for Subscription](https://docs.haravan.com/docs/omni-apis/subscription/#webhooks-for-subscription)
- [What you can do with Subscription](https://docs.haravan.com/docs/omni-apis/subscription/#what-you-can-do-with-subscription)
- [Properties](https://docs.haravan.com/docs/omni-apis/subscription/#properties)
- [Example webhook:](https://docs.haravan.com/docs/omni-apis/subscription/#example-webhook)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/subscription/#endpoints)
- [Retrieves a list of subscriptions](https://docs.haravan.com/docs/omni-apis/subscription/#retrieves-a-list-of-subscriptions)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.