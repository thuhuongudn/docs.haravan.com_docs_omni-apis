---
url: "https://docs.haravan.com/docs/omni-apis/policy/"
title: "Policy | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/policy/#)

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
- Policy

On this page

# Policy

`Version: 1.0`

The list of policies that a merchant has configured for their store, such as their refund or privacy policies.

Only the shop owner can edit this information from inside their shop admin dashboard by navigating to the "Settings" tab and selecting the "General" tab. The API doesn't let you do anything other than retrieve information about a shop.

**Authenticated access scopes**: `com.read_shop`

### What can you do with Policy? [​](https://docs.haravan.com/docs/omni-apis/policy/\#what-can-you-do-with-policy "Direct link to heading")

The haravan API lets you do the following with the Policy resource. More detailed versions of these general actions may be available:

- GET `https://apis.haravan.com/com/policies.json`
  - **[Receive a list of all Policies](https://docs.haravan.com/docs/omni-apis/policy/#receive-a-list-of-all-policies)**

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/policy/\#endpoints "Direct link to heading")

### Receive a list of all Policies [​](https://docs.haravan.com/docs/omni-apis/policy/\#receive-a-list-of-all-policies "Direct link to heading")

GET

https://apis.haravan.com/com/policies.json

Get the policies and their contents for a shop

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/policy/\#parameters "Direct link to heading")

* * *

`title`

Name of the policy

* * *

`body`

Contents of the policy

* * *

`url`

Public URL to policy

* * *

**Getting the shops policies**

- GET `https://apis.haravan.com/com/policies.json`

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "policies": [\
    {\
      "body": "You have 30 days to get a refund",\
      "created_at": "2015-03-28T13:31:32-04:00",\
      "title": "Refund Policy",\
      "updated_at": "2015-03-28T13:31:32-04:00",\
      "url": "https:\/\/apple.myharavan.com\/690933842\/policies\/878590288"\
    }\
  ]
}

```

[Previous\\
\\
Location](https://docs.haravan.com/docs/omni-apis/location/) [Next\\
\\
Province](https://docs.haravan.com/docs/omni-apis/province/)

- [What can you do with Policy?](https://docs.haravan.com/docs/omni-apis/policy/#what-can-you-do-with-policy)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/policy/#endpoints)
- [Receive a list of all Policies](https://docs.haravan.com/docs/omni-apis/policy/#receive-a-list-of-all-policies)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.