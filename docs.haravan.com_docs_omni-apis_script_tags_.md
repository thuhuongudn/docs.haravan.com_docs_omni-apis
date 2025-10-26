---
url: "https://docs.haravan.com/docs/omni-apis/script_tags/"
title: "ScriptTag | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/script_tags/#)

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
- ScriptTag

On this page

# ScriptTag

`Version: 1.0`

The **ScriptTag** resource represents remote javascript which is loaded into the pages of a shop's storefront and in the final "Thank You" page of checkout. This makes it easy to add functionality to those pages without touching any theme templates. A script tag has two main attributes:

- **src**: The URL of the remote script.
- **event**: The DOM event which triggers the loading of the script. Currently, "onload" is the only supported event.

When an app is uninstalled from a shop, all of the script tags which it created are automatically removed along with it.

Reminder A ScriptTag will only appear in checkout if the src starts with 'https://' in order not to break the SSL lock.

**Authenticated access scopes**: `web.read_script_tags`, `com.write_script_tags`

### What you can do with ScriptTag [​](https://docs.haravan.com/docs/omni-apis/script_tags/\#what-you-can-do-with-scripttag "Direct link to heading")

The Haravan API lets you do the following with the ScriptTag resource.

- GET `https://apis.haravan.com/web/script_tags.json`
  - **[Receive a list of all ScriptTags.](https://docs.haravan.com/docs/omni-apis/script_tags/#receive-a-list-of-all-scripttags)**
- GET `https://apis.haravan.com/web/script_tags/count.json`
  - **[Receive a count of all ScriptTags.](https://docs.haravan.com/docs/omni-apis/script_tags/#receive-a-count-of-all-scripttags)**
- GET `https://apis.haravan.com/web/script_tags/{script_tags_id}.json`
  - **[Receive a single ScriptTag.](https://docs.haravan.com/docs/omni-apis/script_tags/#receive-a-single-scripttag)**
- POST `https://apis.haravan.com/web/script_tags.json`
  - **[Create a new ScriptTag.](https://docs.haravan.com/docs/omni-apis/script_tags/#create-a-new-scripttag)**
- PUT `https://apis.haravan.com/web/script_tags/{script_tags_id}.json`
  - **[Modify an existing ScriptTag.](https://docs.haravan.com/docs/omni-apis/script_tags/#modify-an-existing-scripttag)**
- DELETE `https://apis.haravan.com/web/script_tags/{script_tags_id}.json`
  - **[Remove a ScriptTag.](https://docs.haravan.com/docs/omni-apis/script_tags/#remove-a-scripttag)**

### ScriptTag properties [​](https://docs.haravan.com/docs/omni-apis/script_tags/\#scripttag-properties "Direct link to heading")

* * *

`created_at`: `string`

```codeBlockLines_e6Vv
{"created_at": "2021-05-13T07:29:20.1Z"}

```

The date and time [(ISO 8601 format)](http://en.wikipedia.org/wiki/ISO_8601) when the ScriptTag was created.

`event`: `string`

```codeBlockLines_e6Vv
{"event": "onload"}

```

DOM event which triggers the loading of the script. Valid values are: "onload".

`id`: `number`

```codeBlockLines_e6Vv
{"id": 1206854680}

```

The unique numeric identifier for the ScriptTag.

`src`: `string`

```codeBlockLines_e6Vv
{"src": "http://yourapp.com/foo.js"}

```

Specifies the location of the ScriptTag.

`updated_at`: `string`

```codeBlockLines_e6Vv
{"updated_at": "2021-05-13T07:29:20.808Z"}

```

The date and time [(ISO 8601 format)](http://en.wikipedia.org/wiki/ISO_8601) when the ScriptTag was last updated.

`display_scope`: `string`

```codeBlockLines_e6Vv
{"display_scope": "all"}

```

Specifies where the file should be included. Valid values are: "all".

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/script_tags/\#endpoints "Direct link to heading")

### Receive a list of all ScriptTags. [​](https://docs.haravan.com/docs/omni-apis/script_tags/\#receive-a-list-of-all-scripttags "Direct link to heading")

GET

https://apis.haravan.com/web/script\_tags.json

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/script_tags/\#parameters "Direct link to heading")

* * *

`limit` (default: 50) (maximum: 50)

Limit of the result.

* * *

`page` (default: 1)

Page to show the result.

* * *

`since_id`

Restrict results to after the specified ID

* * *

`created_at_min`

Show script\_tags created after date (format: 2008-12-31 03:00).

* * *

`created_at_max`

Show script\_tags created before date (format: 2008-12-31 03:00).

* * *

`updated_at_min`

Show script\_tags created after date (format: 2008-12-31 03:00).

* * *

`updated_at_max`

Show script\_tags updated after date (format: 2008-12-31 03:00).

* * *

`fields`

Comma-separated list of fields to include in the response.

* * *

`src`

Show script tags with a given URL.

* * *

**Retrieves a list of enabling script\_tag by page number. By default, the number of resources on the page is 50.**

GET `https://apis.haravan.com/web/script_tags.json?page=2`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "script_tags": [\
        {\
            "created_at": "2022-02-09T03:13:35.224Z",\
            "event": "onload",\
            "id": 1000132951,\
            "src": "https:your-app.com/foo.js",\
            "updated_at": "2022-02-09T03:13:35.224Z",\
            "display_scope": "all"\
        }\
    ]
}

```

**Get script tags with a particular URL.**

GET `https://apis.haravan.com/web/script_tags.json?src=http://your-app-combo/foo.js`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "script_tags": [\
        {\
            "created_at": "2022-02-09T03:13:35.224Z",\
            "event": "onload",\
            "id": 1000132951,\
            "src": "https:your-app.com/foo.js",\
            "updated_at": "2022-02-09T03:13:35.224Z",\
            "display_scope": "all"\
        }\
    ]
}

```

### Receive a count of all ScriptTags. [​](https://docs.haravan.com/docs/omni-apis/script_tags/\#receive-a-count-of-all-scripttags "Direct link to heading")

GET

https://apis.haravan.com/web/script\_tags/count.json

**Receive a count of all ScriptTags.**

GET `https://apis.haravan.com/web/script_tags/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 1
}

```

### Receive a single ScriptTag. [​](https://docs.haravan.com/docs/omni-apis/script_tags/\#receive-a-single-scripttag "Direct link to heading")

GET

https://apis.haravan.com/web/script\_tags/{script\_tags\_id}.json

**Get a single script tag by its ID.**

GET `https://apis.haravan.com/web/script_tags/1000132953.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "script_tag": {
        "created_at": "2022-02-09T03:48:55.204Z",
        "event": "onload",
        "id": 1000132953,
        "src": "http://your-app.com/foo.js",
        "updated_at": "2022-02-09T03:48:55.204Z",
        "display_scope": "all"
    }
}

```

### Create a new ScriptTag. [​](https://docs.haravan.com/docs/omni-apis/script_tags/\#create-a-new-scripttag "Direct link to heading")

POST

https://apis.haravan.com/web/script\_tags.json

**Create a new ScriptTag.**

POST `https://apis.haravan.com/web/script_tags.json`

```codeBlockLines_e6Vv
{
  "script_tag": {
    "event": "onload",
    "src": "http://your-app.com/foo.js"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "script_tag": {
        "created_at": "2022-02-09T03:48:55.204Z",
        "event": "onload",
        "id": 1000132953,
        "src": "http://your-app.com/foo.js",
        "updated_at": "2022-02-09T03:48:55.204Z",
        "display_scope": "all"
    }
}

```

### Modify an existing ScriptTag. [​](https://docs.haravan.com/docs/omni-apis/script_tags/\#modify-an-existing-scripttag "Direct link to heading")

PUT

https://apis.haravan.com/web/script\_tags/{script\_tags\_id}.json

**Update a script tags's URL.**

PUT `https://apis.haravan.com/web/script_tags/1000132953.json`

```codeBlockLines_e6Vv
{
  "script_tag": {
    "id": 1000132953,
    "src": "http://your-app.com/another.js"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "script_tag": {
        "created_at": "2022-02-09T03:48:55.204Z",
        "event": "onload",
        "id": 1000132953,
        "src": "http://your-app.com/another.js",
        "updated_at": "2022-02-09T03:59:46.094Z",
        "display_scope": "all"
    }
}

```

### Remove a ScriptTag. [​](https://docs.haravan.com/docs/omni-apis/script_tags/\#remove-a-scripttag "Direct link to heading")

DELETE

https://apis.haravan.com/web/script\_tags/{script\_tags\_id}.json

**Remove an existing script tag from a shop.**

DELETE `https://apis.haravan.com/web/script_tags/1000132953.json`

```codeBlockLines_e6Vv
{ }

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
[]

```

[Previous\\
\\
Redirect](https://docs.haravan.com/docs/omni-apis/redirects/) [Next\\
\\
Theme](https://docs.haravan.com/docs/omni-apis/themes/)

- [What you can do with ScriptTag](https://docs.haravan.com/docs/omni-apis/script_tags/#what-you-can-do-with-scripttag)
- [ScriptTag properties](https://docs.haravan.com/docs/omni-apis/script_tags/#scripttag-properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/script_tags/#endpoints)
- [Receive a list of all ScriptTags.](https://docs.haravan.com/docs/omni-apis/script_tags/#receive-a-list-of-all-scripttags)
- [Receive a count of all ScriptTags.](https://docs.haravan.com/docs/omni-apis/script_tags/#receive-a-count-of-all-scripttags)
- [Receive a single ScriptTag.](https://docs.haravan.com/docs/omni-apis/script_tags/#receive-a-single-scripttag)
- [Create a new ScriptTag.](https://docs.haravan.com/docs/omni-apis/script_tags/#create-a-new-scripttag)
- [Modify an existing ScriptTag.](https://docs.haravan.com/docs/omni-apis/script_tags/#modify-an-existing-scripttag)
- [Remove a ScriptTag.](https://docs.haravan.com/docs/omni-apis/script_tags/#remove-a-scripttag)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.