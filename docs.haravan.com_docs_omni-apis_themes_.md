---
url: "https://docs.haravan.com/docs/omni-apis/themes/"
title: "Theme | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/themes/#)

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
- Theme

On this page

# Theme

`Version: 1.0`

A **theme** is the look and feel template for your haravan shop.

![omni_api_theme](https://docs.haravan.com/assets/images/omni_api_theme-fbbb7816ee7aacf93eaa3bfbcc3cb306.png)

A shop can have multiple themes which take the role of either "published" or "unpublished". Each shop can have 20 themes total, including one main theme, and a max of 19 unpublished themes. The published theme is the one customers see when visiting the shop in a desktop browser. Unpublished themes are themes that customers cannot currently see. When you publish a theme, the previously published theme will become unpublished.

**Authenticated access scopes**: `web.read_themes`, `web.write_themes`

### What you can do with Theme? [​](https://docs.haravan.com/docs/omni-apis/themes/\#what-you-can-do-with-theme "Direct link to heading")

The haravan API lets you do the following with the Theme resource. More detailed versions of these general actions may be available:

- GET `https://apis.haravan.com/web/themes.json`
  - **[Receive a list of all Themes](https://docs.haravan.com/docs/omni-apis/themes/#receive-a-list-of-all-themes)**
- GET `https://apis.haravan.com/web/themes/{theme_id}.json`
  - **[Receive a single Theme](https://docs.haravan.com/docs/omni-apis/themes/#receive-a-single-theme)**
- POST `https://apis.haravan.com/web/themes.json`
  - **[Create a new Theme](https://docs.haravan.com/docs/omni-apis/themes/#create-a-new-theme)**
- PUT `https://apis.haravan.com/web/themes/{theme_id}.json`
  - **[Modify an existing Theme](https://docs.haravan.com/docs/omni-apis/themes/#modify-an-existing-theme)**
- DELETE `https://apis.haravan.com/web/themes/{theme_id}.json`
  - **[Remove a Theme from the database](https://docs.haravan.com/docs/omni-apis/themes/#remove-a-theme-from-the-database)**

### Theme Properties [​](https://docs.haravan.com/docs/omni-apis/themes/\#theme-properties "Direct link to heading")

* * *

`created_at`: `string`

```codeBlockLines_e6Vv
{ "created_at" : "2012-08-24T14:01:47-04:00" }

```

The date and time when the theme was created. The API returns this value in [ISO 8601 format](http://en.wikipedia.org/wiki/ISO_8601).

`id`: `number`

```codeBlockLines_e6Vv
{ "id" : 828155753 }

```

TA unique numeric identifier for the theme.

`name`: `string`

```codeBlockLines_e6Vv
{ "name" : "Comfort" }

```

The name of the theme.

`role`: `string`

```codeBlockLines_e6Vv
{ "role" : "main" }

```

Specifies how the theme is being used within the shop. Valid values are:

- **main**: the theme customers see when visiting the shop in a desktop browser.
- **mobile**: the theme customers see when visiting the shop in a mobile browser.
- **unpublished**: the theme that customers cannot currently see.

`updated_at`: `string`

```codeBlockLines_e6Vv
{ "updated_at" : "2012-08-24T14:01:47-04:00" }

```

The date and time when the theme was last updated. The API returns this value in [ISO 8601 format](http://en.wikipedia.org/wiki/ISO_8601).

`previewable`: `boolean`

```codeBlockLines_e6Vv
{ "previewable" : true }

```

Indicates if the theme can currently be previewed.

`processing`: `boolean`

```codeBlockLines_e6Vv
{ "processing" : true }

```

Indicates if files are still being copied into place for this theme.

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/themes/\#endpoints "Direct link to heading")

### Receive a list of all Themes [​](https://docs.haravan.com/docs/omni-apis/themes/\#receive-a-list-of-all-themes "Direct link to heading")

GET

https://apis.haravan.com/web/themes.json

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/themes/\#parameters "Direct link to heading")

* * *

`fields`

comma-separated list of fields to include in the response

* * *

**Get a list of a shop's themes**

- GET `https://apis.haravan.com/web/themes.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "themes": [\
    {\
      "created_at": "2015-03-28T13:31:19-04:00",\
      "id": 828155753,\
      "name": "Comfort",\
      "role": "main",\
      "theme_store_id": null,\
      "updated_at": "2015-03-28T13:33:30-04:00",\
      "previewable": true,\
      "processing": false\
    },\
    {\
      "created_at": "2015-03-28T13:31:19-04:00",\
      "id": 976877075,\
      "name": "Speed",\
      "role": "mobile",\
      "theme_store_id": null,\
      "updated_at": "2015-03-28T13:33:30-04:00",\
      "previewable": true,\
      "processing": false\
    },\
    {\
      "created_at": "2015-03-28T13:31:19-04:00",\
      "id": 752253240,\
      "name": "Sandbox",\
      "role": "unpublished",\
      "theme_store_id": null,\
      "updated_at": "2015-03-28T13:31:19-04:00",\
      "previewable": true,\
      "processing": false\
    }\
  ]
}

```

### Receive a single Theme [​](https://docs.haravan.com/docs/omni-apis/themes/\#receive-a-single-theme "Direct link to heading")

GET

https://apis.haravan.com/web/themes/{theme\_id}.json

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/themes/\#parameters-1 "Direct link to heading")

* * *

`fields`

comma-separated list of fields to include in the response

* * *

**Get a single theme**

- GET `https://apis.haravan.com/web/themes/828155753.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "theme": {
    "created_at": "2015-03-28T13:31:19-04:00",
    "id": 828155753,
    "name": "Comfort",
    "role": "main",
    "theme_store_id": null,
    "updated_at": "2015-03-28T13:31:19-04:00",
    "previewable": true,
    "processing": false
  }
}

```

### Create a new Theme [​](https://docs.haravan.com/docs/omni-apis/themes/\#create-a-new-theme "Direct link to heading")

POST

https://apis.haravan.com/web/themes.json

Create a theme by providing the public URL of a .zip containing the theme. The theme always starts out with a role of "unpublished." If a different role is provided in the POST request, the theme will be given that role only after all its files have been extracted and stored by haravan (which might take a couple of minutes).

**Create a theme from a URL and give it a custom name and role.**

- POST `https://apis.haravan.com/web/themes.json`

```codeBlockLines_e6Vv
{
  "theme": {
    "name": "Lemongrass",
    "src": "http:\/\/themes.haravan.com\/theme.zip",
    "role": "main"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "theme": {
    "created_at": "2015-03-28T13:33:29-04:00",
    "id": 1049083723,
    "name": "Lemongrass",
    "role": "unpublished",
    "theme_store_id": null,
    "updated_at": "2015-03-28T13:33:29-04:00",
    "previewable": false,
    "processing": false
  }
}

```

**Trying to create a theme without a name will return an error**

- POST `https://apis.haravan.com/web/themes.json`

```codeBlockLines_e6Vv
{
  "theme": {
    "body": "foobar"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 422 Unprocessable Entity
{
  "errors": {
    "name": [\
      "can't be blank"\
    ]
  }
}

```

### Modify an existing Theme [​](https://docs.haravan.com/docs/omni-apis/themes/\#modify-an-existing-theme "Direct link to heading")

PUT

https://apis.haravan.com/web/themes/{theme\_id}.json

**Change the theme's name**

- PUT `https://apis.haravan.com/web/themes/752253240.json`

```codeBlockLines_e6Vv
{
  "theme": {
    "id": 752253240,
    "name": "Experimental"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "theme": {
    "created_at": "2015-03-28T13:31:19-04:00",
    "id": 752253240,
    "name": "Experimental",
    "role": "unpublished",
    "theme_store_id": null,
    "updated_at": "2015-03-28T13:33:30-04:00",
    "previewable": true,
    "processing": false
  }
}

```

**Changing the theme's role to main or mobile will publish the theme to that role**

- PUT `https://apis.haravan.com/web/themes/752253240.json`

```codeBlockLines_e6Vv
{
  "theme": {
    "id": 752253240,
    "role": "main"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "theme": {
    "created_at": "2015-03-28T13:31:19-04:00",
    "id": 752253240,
    "name": "Sandbox",
    "role": "main",
    "theme_store_id": null,
    "updated_at": "2015-03-28T13:33:30-04:00",
    "previewable": true,
    "processing": false
  }
}

```

### Remove a Theme from the database [​](https://docs.haravan.com/docs/omni-apis/themes/\#remove-a-theme-from-the-database "Direct link to heading")

DELETE

https://apis.haravan.com/web/themes/{theme\_id}.json

**Remove a theme**

- DELETE `https://apis.haravan.com/web/themes/752253240.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "created_at": "2015-03-28T13:31:19-04:00",
  "id": 752253240,
  "name": "Sandbox",
  "role": "unpublished",
  "theme_store_id": null,
  "updated_at": "2015-03-28T13:31:19-04:00",
  "previewable": true,
  "processing": false
}

```

[Previous\\
\\
ScriptTag](https://docs.haravan.com/docs/omni-apis/script_tags/) [Next\\
\\
Multipass](https://docs.haravan.com/docs/omni-apis/multipass/)

- [What you can do with Theme?](https://docs.haravan.com/docs/omni-apis/themes/#what-you-can-do-with-theme)
- [Theme Properties](https://docs.haravan.com/docs/omni-apis/themes/#theme-properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/themes/#endpoints)
- [Receive a list of all Themes](https://docs.haravan.com/docs/omni-apis/themes/#receive-a-list-of-all-themes)
- [Receive a single Theme](https://docs.haravan.com/docs/omni-apis/themes/#receive-a-single-theme)
- [Create a new Theme](https://docs.haravan.com/docs/omni-apis/themes/#create-a-new-theme)
- [Modify an existing Theme](https://docs.haravan.com/docs/omni-apis/themes/#modify-an-existing-theme)
- [Remove a Theme from the database](https://docs.haravan.com/docs/omni-apis/themes/#remove-a-theme-from-the-database)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.