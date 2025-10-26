---
url: "https://docs.haravan.com/docs/omni-apis/redirects/"
title: "Redirect | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/redirects/#)

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

    - [Article](https://docs.haravan.com/docs/omni-apis/articles/)
    - [Asset](https://docs.haravan.com/docs/omni-apis/assets/)
    - [Blog](https://docs.haravan.com/docs/omni-apis/blogs/)
    - [Comment](https://docs.haravan.com/docs/omni-apis/comments/)
    - [Page](https://docs.haravan.com/docs/omni-apis/pages/)
    - [Redirect](https://docs.haravan.com/docs/omni-apis/redirects/)
    - [ScriptTag](https://docs.haravan.com/docs/omni-apis/script_tags/)
    - [Theme](https://docs.haravan.com/docs/omni-apis/themes/)
    - [Multipass](https://docs.haravan.com/docs/omni-apis/multipass/)
  - [Orders](https://docs.haravan.com/docs/omni-apis/orders/)

  - [Products](https://docs.haravan.com/docs/omni-apis/collects/)

  - [Shipping](https://docs.haravan.com/docs/omni-apis/shipping-rates/)

  - [Store properties](https://docs.haravan.com/docs/omni-apis/country/)

  - [Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [Home page](https://docs.haravan.com/)
- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)
- [Online store](https://docs.haravan.com/docs/omni-apis/articles/)
- Redirect

On this page

# Redirect

`Version: 1.0`

A redirect causes a visitor on a specific path on the shop's site to be automatically sent to a target (different location). The target can be a new location on the shop's site, or a full URL, even one on a completely different domain. Redirect paths are unique; a shop cannot have more than one redirect with the same path.

**Authenticated access scopes**: `com.read_contents`, `com.write_contents`

### What you can do with Redirect? [​](https://docs.haravan.com/docs/omni-apis/redirects/\#what-you-can-do-with-redirect "Direct link to heading")

The haravan API lets you do the following with the Redirect resource. More detailed versions of these general actions may be available:

- GET `https://apis.haravan.com/web/redirects.json`
  - **[Receive a list of all Redirects](https://docs.haravan.com/docs/omni-apis/redirects/#receive-a-list-of-all-redirects)**
- GET `https://apis.haravan.com/web/redirects/count.json`
  - **[Receive a count of all Redirects](https://docs.haravan.com/docs/omni-apis/redirects/#receive-a-count-of-all-redirects)**
- GET `https://apis.haravan.com/web/redirects/{redirect_id}.json`
  - **[Receive a single Redirect](https://docs.haravan.com/docs/omni-apis/redirects/#receive-a-single-redirect)**
- POST `https://apis.haravan.com/web/redirects.json`
  - **[Create a new Redirect](https://docs.haravan.com/docs/omni-apis/redirects/#create-a-new-redirect)**
- PUT `https://apis.haravan.com/web/redirects/{redirect_id}.json`
  - **[Modify an existing Redirect](https://docs.haravan.com/docs/omni-apis/redirects/#modify-an-existing-redirect)**
- DELETE `https://apis.haravan.com/web/redirects/{redirect_id}.json`
  - **[Remove a Redirect from the database](https://docs.haravan.com/docs/omni-apis/redirects/#remove-a-redirect-from-the-database)**

### Redirect Properties [​](https://docs.haravan.com/docs/omni-apis/redirects/\#redirect-properties "Direct link to heading")

* * *

`id` : `string`

```codeBlockLines_e6Vv
"id": 304339089

```

The unique numeric identifier for the redirect.

`path` : `string`

```codeBlockLines_e6Vv
"path": "/products.php"

```

The "before" path to be redirected. When the user this path, s/he will be redirected to the path specified by target.

`target` : `string`

```codeBlockLines_e6Vv
"target": "/products"

```

The "after" path or URL to be redirected to. When the user visits the path specified by path, s/he will be redirected to this path or URL. This property can be set to any path on the shop's site, or any URL, even one on a completely different domain.

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/redirects/\#endpoints "Direct link to heading")

### Receive a list of all Redirects [​](https://docs.haravan.com/docs/omni-apis/redirects/\#receive-a-list-of-all-redirects "Direct link to heading")

GET

https://apis.haravan.com/web/redirects.json

**Get a list of all URL redirects for your shop.**

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/redirects/\#parameters "Direct link to heading")

* * *

`limit` default: 50 maximum: 250

Amount of results

* * *

`page` default: 1

Page to show

* * *

`since_id`

Restrict results to after the specified ID

* * *

`path`

Show Redirects with given target

* * *

`target`

Show Redirects with given target

* * *

`fields`

comma-separated list of fields to include in the response

* * *

**A redirect's "path" attribute is the path which activates this redirect when visited, and a shop cannot have more than one redirect with the same path. The "target" attribute is the URL which the visitor is redirected to when they try to access the associated path. The target could either be a path or a full URL, possibly even for a different domain.**

- GET `https://apis.haravan.com/web/redirects.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "redirects": [\
    {\
      "id": 304339089,\
      "path": "\/products.php",\
      "target": "\/products"\
    },\
    {\
      "id": 668809255,\
      "path": "\/leopard",\
      "target": "\/pages\/macosx"\
    },\
    {\
      "id": 950115854,\
      "path": "\/ibook",\
      "target": "\/products\/macbook"\
    }\
  ]
}

```

**Get a list of all URL redirects for your shop after a specified ID**

- GET `https://apis.haravan.com/web/redirects.json?since_id=668809255`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "redirects": [\
    {\
      "id": 950115854,\
      "path": "\/ibook",\
      "target": "\/products\/macbook"\
    }\
  ]
}

```

### Receive a count of all Redirects [​](https://docs.haravan.com/docs/omni-apis/redirects/\#receive-a-count-of-all-redirects "Direct link to heading")

GET

https://apis.haravan.com/web/redirects/count.json

**Get a count of all URL redirects for your shop.**

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/redirects/\#parameters-1 "Direct link to heading")

* * *

`path`

Count Redirects with given path

* * *

`target`

Count Redirects with given target

* * *

**A redirect’s “path” attribute is the path which activates this redirect when visited, and a shop cannot have more than one redirect with the same path. The “target” attribute is the URL which the visitor is redirected to when they try to access the associated path. The target could either be a path or a full URL, possibly even for a different domain.**

- GET `https://apis.haravan.com/web/redirects/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "count": 3
}

```

### Receive a single Redirect [​](https://docs.haravan.com/docs/omni-apis/redirects/\#receive-a-single-redirect "Direct link to heading")

GET

https://apis.haravan.com/web/redirects/{redirect\_id}.json

**Get a single redirect.**

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/redirects/\#parameters-2 "Direct link to heading")

* * *

`fields`

comma-separated list of fields to include in the response

* * *

**Get a single redirect by its ID.**

- GET `https://apis.haravan.com/web/redirects/668809255.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "redirect": {
    "id": 668809255,
    "path": "\/leopard",
    "target": "\/pages\/macosx"
  }
}

```

### Create a new Redirect [​](https://docs.haravan.com/docs/omni-apis/redirects/\#create-a-new-redirect "Direct link to heading")

POST

https://apis.haravan.com/web/redirects.json

**Create a new redirect.**

**We expect users might try going to /ipod in order to find about one of our popular products, but we want to redirect them to /itunes because that's where we have the information they're looking for.**

- POST `https://apis.haravan.com/web/redirects.json`

```codeBlockLines_e6Vv
{
  "redirect": {
    "path": "\/ipod",
    "target": "\/pages\/itunes"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "redirect": {
    "id": 979034144,
    "path": "\/ipod",
    "target": "\/pages\/itunes"
  }
}

```

**We have a separate forums site that is on a different subdomain. The "path" is always converted to an absolute path without a domain, but the "target" can be a full URL.**

- POST `https://apis.haravan.com/web/redirects.json`

```codeBlockLines_e6Vv
{
  "redirect": {
    "path": "http:\/\/www.apple.com\/forums",
    "target": "http:\/\/forums.apple.com"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "redirect": {
    "id": 979034145,
    "path": "\/forums",
    "target": "http:\/\/forums.apple.com"
  }
}

```

**Trying to create a redirect without a path and target will return an error**

- POST `https://apis.haravan.com/web/redirects.json`

```codeBlockLines_e6Vv
{
  "redirect": {
    "body": "foobar"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 422 Unprocessable Entity
{
  "errors": {
    "path": [\
      "can't be blank"\
    ],
    "target": [\
      "can't be blank",\
      "URI is invalid"\
    ]
  }
}

```

### Modify an existing Redirect [​](https://docs.haravan.com/docs/omni-apis/redirects/\#modify-an-existing-redirect "Direct link to heading")

PUT

https://apis.haravan.com/web/redirects/{redirect\_id}.json

**Update a redirect's path and/or target URIs.**

**Change a redirect so that it activates for a different request path:**

- PUT `https://apis.haravan.com/web/redirects/668809255.json`

```codeBlockLines_e6Vv
{
  "redirect": {
    "id": 668809255,
    "path": "\/tiger"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "redirect": {
    "id": 668809255,
    "path": "\/tiger",
    "target": "\/pages\/macosx"
  }
}

```

**Change both the path and target URIs for an existing redirect**

- PUT `https://apis.haravan.com/web/redirects/950115854.json`

```codeBlockLines_e6Vv
{
  "redirect": {
    "id": 950115854,
    "path": "\/powermac",
    "target": "\/pages\/macpro"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "redirect": {
    "id": 950115854,
    "path": "\/powermac",
    "target": "\/pages\/macpro"
  }
}

```

### Remove a Redirect from the database [​](https://docs.haravan.com/docs/omni-apis/redirects/\#remove-a-redirect-from-the-database "Direct link to heading")

DELETE

https://apis.haravan.com/web/redirects/{redirect\_id}.json

**Delete a redirect**

**Remove an existing redirect from a shop**

- DELETE `https://apis.haravan.com/web/redirects/668809255.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{}

```

[Previous\\
\\
Page](https://docs.haravan.com/docs/omni-apis/pages/) [Next\\
\\
ScriptTag](https://docs.haravan.com/docs/omni-apis/script_tags/)

- [What you can do with Redirect?](https://docs.haravan.com/docs/omni-apis/redirects/#what-you-can-do-with-redirect)
- [Redirect Properties](https://docs.haravan.com/docs/omni-apis/redirects/#redirect-properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/redirects/#endpoints)
- [Receive a list of all Redirects](https://docs.haravan.com/docs/omni-apis/redirects/#receive-a-list-of-all-redirects)
- [Receive a count of all Redirects](https://docs.haravan.com/docs/omni-apis/redirects/#receive-a-count-of-all-redirects)
- [Receive a single Redirect](https://docs.haravan.com/docs/omni-apis/redirects/#receive-a-single-redirect)
- [Create a new Redirect](https://docs.haravan.com/docs/omni-apis/redirects/#create-a-new-redirect)
- [Modify an existing Redirect](https://docs.haravan.com/docs/omni-apis/redirects/#modify-an-existing-redirect)
- [Remove a Redirect from the database](https://docs.haravan.com/docs/omni-apis/redirects/#remove-a-redirect-from-the-database)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.