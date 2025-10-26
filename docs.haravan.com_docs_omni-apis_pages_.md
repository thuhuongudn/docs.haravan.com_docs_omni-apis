---
url: "https://docs.haravan.com/docs/omni-apis/pages/"
title: "Page | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/pages/#)

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
- Page

On this page

# Page

`Version: 1.0`

In addition to an online storefront, Haravan shops come with a web **page** creation tool, allowing a shop to have one or more pages. Shop owners are encouraged to use pages for information that customers will use often, such as an 'About Us' page, a 'Contact Us' page, a page with customer testimonials etc.

#### Reminder [​](https://docs.haravan.com/docs/omni-apis/pages/\#reminder "Direct link to heading")

Pages are meant to be used for static content. If the shop needs a page for content that is created on a regular basis, we recommend that you use the [blog](https://docs.haravan.com/docs/omni-apis/blogs/) feature instead.

**Authenticated access scopes**: `com.read_contents`, `com.write_contents`

### What you can do with Page [​](https://docs.haravan.com/docs/omni-apis/pages/\#what-you-can-do-with-page "Direct link to heading")

The Haravan API lets you do the following with the Page resource. More detailed versions of these general actions may be available:

- GET `https://apis.haravan.com/web/pages.json`
  - **[Receive a list of all Pages.](https://docs.haravan.com/docs/omni-apis/pages/#receive-a-list-of-all-pages)**
- GET `https://apis.haravan.com/web/pages/count.json`
  - **[Receive a count of all Pages.](https://docs.haravan.com/docs/omni-apis/pages/#receive-a-count-of-all-pages)**
- GET `https://apis.haravan.com/web/pages/{page_id}.json`
  - **[Receive a single Page.](https://docs.haravan.com/docs/omni-apis/pages/#receive-a-single-page)**
- POST `https://apis.haravan.com/web/pages.json`
  - **[Create a new Page.](https://docs.haravan.com/docs/omni-apis/pages/#create-a-new-page)**
- PUT `https://apis.haravan.com/web/pages/{page_id}.json`
  - **[Modify an existing Page.](https://docs.haravan.com/docs/omni-apis/pages/#modify=an-existing-page)**
- DELETE `https://apis.haravan.com/web/pages/{page_id}.json`
  - **[Remove a Page from the database.](https://docs.haravan.com/docs/omni-apis/pages/#remove-a-page-from-the-database)**

### Page properties [​](https://docs.haravan.com/docs/omni-apis/pages/\#page-properties "Direct link to heading")

* * *

`author` : `string`

```codeBlockLines_e6Vv
"author": "Lydia"

```

The name of the person who created the page.

`body_html` : `string`

```codeBlockLines_e6Vv
"body_html": "We don't need a warranty"

```

Text content of the page, complete with HTML markup.

`created_at` : `string`

```codeBlockLines_e6Vv
"created_at": "2008-07-15T20:00:00-04:00"

```

The date and time when the page was created. The API returns this value in [ISO 8601 format](http://en.wikipedia.org/wiki/ISO_8601).

`handle` : `string`

```codeBlockLines_e6Vv
"handle": "tos"

```

A human-friendly unique string for the page automatically generated from its title. This is used in shop themes by the Liquid templating language to refer to the page.

`id` : `number`

```codeBlockLines_e6Vv
"id": 131092082

```

The unique numeric identifier for the page.

`metafield` : `json`

```codeBlockLines_e6Vv
"metafield": [\
  {"key": "new",\
  "value": "newvalue",\
  "value_type": "string",\
  "namespace": "global"\
  }\
]

```

Attaches additional information to a shop's resources:

- **key (required)**: Identifier for the metafield (maximum of 30 characters).
- **namespace (required)**: Container for a set of metadata. Namespaces help distinguish between metadata you created and metadata created by another individual with a similar namespace (maximum of 20 characters).
- **value (required)**: Information to be stored as metadata.
- **value\_type (required)**: States whether the information in the value is stored as a 'string' or 'integer.'
- **description (optional)**: Additional information about the metafield.

`published_at` : `string`

```codeBlockLines_e6Vv
"published_at": "2014-07-16T20:00:00-04:00"

```

This can have two different types of values, depending on whether the page has been published (i.e., made visible to the blog's readers).

If the page is **published**, this value is the date and time when it was published. The API returns this value in [ISO 8601 format](http://en.wikipedia.org/wiki/ISO_8601)

If the page is a **hidden**, this value is null. Changing an page's status from published to hidden changes its published\_at property to null.

`shop_id` : `number`

```codeBlockLines_e6Vv
"shop_id": 690933842

```

The id of the shop to which the page belongs.

`template_suffix` : `string`

```codeBlockLines_e6Vv
"template_suffix": "template_suffix"

```

The suffix of the liquid template being used. By default, the original template is called page.liquid, without any suffix. Any additional templates will be: page.suffix.liquid.

`title` : `string`

```codeBlockLines_e6Vv
"title": "Terms of Services"

```

The title of the page.

`updated_at` : `string`

```codeBlockLines_e6Vv
"updated_at": "2008-07-16T20:00:00-04:00"

```

The date and time when the page was last updated. The API returns this value in [ISO 8601 format](http://en.wikipedia.org/wiki/ISO_8601).

### Receive a list of all Pages. [​](https://docs.haravan.com/docs/omni-apis/pages/\#receive-a-list-of-all-pages "Direct link to heading")

GET

https://apis.haravan.com/web/pages.json

Get a list of all pages

* * *

`limit`

Amount of results(default: 50) (maximum: 250)

* * *

`page`

Page to show(default: 1)

* * *

`since_id`

Restrict results to after the specified ID

* * *

`title`

Show pages by Title

* * *

`handle`

Filter by Page handle

* * *

`created_at_min`

Show pages created after date (format: 2008-12-31)

* * *

`created_at_max`

Show pages created before date (format: 2008-12-31)

* * *

`updated_at_min`

Show pages last updated after date (format: 2008-12-31)

* * *

`updated_at_max`

Show pages last updated before date (format: 2008-12-31)

* * *

`published_at_min`

Show pages published after date (format: 2014-04-25T16:15:47-04:00)

* * *

`published_at_max`

Show pages published before date (format: 2014-04-25T16:15:47-04:00)

* * *

`fields`

comma-separated list of fields to include in the response

* * *

`published_status`

published - Show only published pages

unpublished - Show only unpublished pages

any - Show all pages (default)

Get all pages for a shop

- GET `https://apis.haravan.com/web/pages.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "pages": [\
    {\
      "id": 322471,\
      "title": "Support",\
      "shop_id": 690933842,\
      "handle": "support",\
      "body_html": "<p>Come in store for support.<\/p>",\
      "author": "Dennis",\
      "created_at": "2009-07-15T20:00:00-04:00",\
      "updated_at": "2009-07-16T20:00:00-04:00",\
      "published_at": null,\
      "template_suffix": null\
    },\
    {\
      "id": 108828309,\
      "title": "Sample Page",\
      "shop_id": 690933842,\
      "handle": "sample",\
      "body_html": "<p>this is a <strong>sample<\/strong> page.<\/p>",\
      "author": "Dennis",\
      "created_at": "2008-07-15T20:00:00-04:00",\
      "updated_at": "2008-07-16T20:00:00-04:00",\
      "published_at": null,\
      "template_suffix": null\
    },\
    {\
      "id": 131092082,\
      "title": "Terms of Services",\
      "shop_id": 690933842,\
      "handle": "tos",\
      "body_html": "<p>We make <strong>perfect<\/strong> stuff, we don't need a warranty.<\/p>",\
      "author": "Dennis",\
      "created_at": "2008-07-15T20:00:00-04:00",\
      "updated_at": "2008-07-16T20:00:00-04:00",\
      "published_at": "2008-07-15T20:00:00-04:00",\
      "template_suffix": null\
    },\
    {\
      "id": 169524623,\
      "title": "Store hours",\
      "shop_id": 690933842,\
      "handle": "store-hours",\
      "body_html": "<p>We never close.<\/p>",\
      "author": "Jobs",\
      "created_at": "2013-12-31T19:00:00-05:00",\
      "updated_at": "2013-12-31T19:00:00-05:00",\
      "published_at": "2014-02-01T19:00:00-05:00",\
      "template_suffix": null\
    }\
  ]
}

```

Get a list of all pages after the specified ID

- GET `https://apis.haravan.com/web/pages.json?since_id=108828309`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "pages": [\
    {\
      "id": 131092082,\
      "title": "Terms of Services",\
      "shop_id": 690933842,\
      "handle": "tos",\
      "body_html": "<p>We make <strong>perfect<\/strong> stuff, we don't need a warranty.<\/p>",\
      "author": "Dennis",\
      "created_at": "2008-07-15T20:00:00-04:00",\
      "updated_at": "2008-07-16T20:00:00-04:00",\
      "published_at": "2008-07-15T20:00:00-04:00",\
      "template_suffix": null\
    },\
    {\
      "id": 169524623,\
      "title": "Store hours",\
      "shop_id": 690933842,\
      "handle": "store-hours",\
      "body_html": "<p>We never close.<\/p>",\
      "author": "Jobs",\
      "created_at": "2013-12-31T19:00:00-05:00",\
      "updated_at": "2013-12-31T19:00:00-05:00",\
      "published_at": "2014-02-01T19:00:00-05:00",\
      "template_suffix": null\
    }\
  ]
}

```

### Receive a count of all Pages. [​](https://docs.haravan.com/docs/omni-apis/pages/\#receive-a-count-of-all-pages "Direct link to heading")

GET

https://apis.haravan.com/web/pages/count.json

Get a count of all pages

* * *

`title`

Pages with a given title

* * *

`created_at_min`

Pages created after date (format: 2008-12-31)

* * *

`created_at_max`

Pages created before date (format: 2008-12-31)

* * *

`updated_at_min`

Pages last updated after date (format: 2008-12-31)

* * *

`updated_at_max`

Pages last updated before date (format: 2008-12-31)

* * *

`published_at_min`

Show pages published after date (format: 2014-04-25T16:15:47-04:00)

* * *

`published_at_max`

Show pages published before date (format: 2014-04-25T16:15:47-04:00)

* * *

`published_status`

published - Only published pages

unpublished - Only unpublished pages

any - All pages (default)

Count all pages for a shop

- GET `https://apis.haravan.com/web/pages/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "count": 4
}

```

### Receive a single Page. [​](https://docs.haravan.com/docs/omni-apis/pages/\#receive-a-single-page "Direct link to heading")

GET

https://apis.haravan.com/web/pages/{page\_id}.json

Get a single page by its ID

* * *

`fields`

comma-separated list of fields to include in the response

* * *

Get a single page

- GET `https://apis.haravan.com/web/pages/131092082.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "page": {
    "id": 131092082,
    "title": "Terms of Services",
    "shop_id": 690933842,
    "handle": "tos",
    "body_html": "<p>We make <strong>perfect<\/strong> stuff, we don't need a warranty.<\/p>",
    "author": "Dennis",
    "created_at": "2008-07-15T20:00:00-04:00",
    "updated_at": "2008-07-16T20:00:00-04:00",
    "published_at": "2008-07-15T20:00:00-04:00",
    "template_suffix": null
  }
}

```

### Create a new Page. [​](https://docs.haravan.com/docs/omni-apis/pages/\#create-a-new-page "Direct link to heading")

POST

https://apis.haravan.com/web/pages.json

Create a new page

Create a new, but unpublished page

- POST `https://apis.haravan.com/web/pages.json`

```codeBlockLines_e6Vv
{
  "page": {
    "title": "Warranty information",
    "body_html": "<h1>Warranty<\/h1>
<p><strong>Forget it<\/strong>, we aint giving you nothing<\/p>",
    "published": false
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "page": {
    "id": 905192171,
    "title": "Warranty information",
    "shop_id": 690933842,
    "handle": "warranty-information",
    "body_html": "<h1>Warranty<\/h1>
<p><strong>Forget it<\/strong>, we aint giving you nothing<\/p>",
    "author": "Haravan API",
    "created_at": "2017-01-05T15:42:18-05:00",
    "updated_at": "2017-01-05T15:42:18-05:00",
    "published_at": null,
    "template_suffix": null
  }
}

```

Trying to create a page without a title will return an error

- POST `https://apis.haravan.com/web/pages.json`

```codeBlockLines_e6Vv
{
  "page": {
    "body": "foobar"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 422 Unprocessable Entity
{
  "errors": {
    "title": [\
      "can't be blank"\
    ]
  }
}

```

Create a page with a metafield

- POST `https://apis.haravan.com/web/pages.json`

```codeBlockLines_e6Vv
{
  "page": {
    "title": "Warranty information",
    "body_html": "<h1>Warranty<\/h1>
<p><strong>Forget it<\/strong>, we aint giving you nothing<\/p>",
    "metafields": [\
      {\
        "key": "new",\
        "value": "newvalue",\
        "value_type": "string",\
        "namespace": "global"\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "page": {
    "id": 905192172,
    "title": "Warranty information",
    "shop_id": 690933842,
    "handle": "warranty-information",
    "body_html": "<h1>Warranty<\/h1>
<p><strong>Forget it<\/strong>, we aint giving you nothing<\/p>",
    "author": "Haravan API",
    "created_at": "2017-01-05T15:42:20-05:00",
    "updated_at": "2017-01-05T15:42:20-05:00",
    "published_at": "2017-01-05T15:42:20-05:00",
    "template_suffix": null
  }
}

```

Create a new page with html markup and upload it to the shop

- POST `https://apis.haravan.com/web/pages.json`

```codeBlockLines_e6Vv
{
  "page": {
    "title": "Warranty information",
    "body_html": "<h1>Warranty<\/h1>
<p><strong>Forget it<\/strong>, we aint giving you nothing<\/p>"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "page": {
    "id": 905192173,
    "title": "Warranty information",
    "shop_id": 690933842,
    "handle": "warranty-information",
    "body_html": "<h1>Warranty<\/h1>
<p><strong>Forget it<\/strong>, we aint giving you nothing<\/p>",
    "author": "Haravan API",
    "created_at": "2017-01-05T15:42:20-05:00",
    "updated_at": "2017-01-05T15:42:20-05:00",
    "published_at": "2017-01-05T15:42:20-05:00",
    "template_suffix": null
  }
}

```

### Modify an existing Page. [​](https://docs.haravan.com/docs/omni-apis/pages/\#modify-an-existing-page "Direct link to heading")

PUT

https://apis.haravan.com/web/pages/{page\_id}.json

Update a page

Show a hidden page by changing the published attribute to true

- PUT `https://apis.haravan.com/web/pages/131092082.json`

```codeBlockLines_e6Vv
{
  "page": {
    "id": 131092082,
    "published": true
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "page": {
    "shop_id": 690933842,
    "id": 131092082,
    "published_at": "2017-01-05T15:42:15-05:00",
    "title": "Terms of Services",
    "handle": "tos",
    "body_html": "<p>We make <strong>perfect<\/strong> stuff, we don't need a warranty.<\/p>",
    "author": "Dennis",
    "created_at": "2008-07-15T20:00:00-04:00",
    "updated_at": "2017-01-05T15:42:15-05:00",
    "template_suffix": null
  }
}

```

Update an existing page body

- PUT `https://apis.haravan.com/web/pages/131092082.json`

```codeBlockLines_e6Vv
{
  "page": {
    "id": 131092082,
    "body_html": "<p>Okay, maybe we will give you a warranty.<\/p>"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "page": {
    "shop_id": 690933842,
    "id": 131092082,
    "title": "Terms of Services",
    "handle": "tos",
    "body_html": "<p>Okay, maybe we will give you a warranty.<\/p>",
    "author": "Dennis",
    "created_at": "2008-07-15T20:00:00-04:00",
    "updated_at": "2017-01-05T15:42:16-05:00",
    "published_at": "2008-07-15T20:00:00-04:00",
    "template_suffix": null
  }
}

```

Hide a published page by changing the published attribute to false

- PUT `https://apis.haravan.com/web/pages/131092082.json`

```codeBlockLines_e6Vv
{
  "page": {
    "id": 131092082,
    "published": false
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "page": {
    "shop_id": 690933842,
    "id": 131092082,
    "title": "Terms of Services",
    "handle": "tos",
    "body_html": "<p>We make <strong>perfect<\/strong> stuff, we don't need a warranty.<\/p>",
    "author": "Dennis",
    "created_at": "2008-07-15T20:00:00-04:00",
    "updated_at": "2017-01-05T15:42:17-05:00",
    "published_at": null,
    "template_suffix": null
  }
}

```

Add a metafield to an existing page

- PUT `https://apis.haravan.com/web/pages/131092082.json`

```codeBlockLines_e6Vv
{
  "page": {
    "id": 131092082,
    "metafields": [\
      {\
        "key": "new",\
        "value": "newvalue",\
        "value_type": "string",\
        "namespace": "global"\
      }\
    ]
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "page": {
    "shop_id": 690933842,
    "id": 131092082,
    "title": "Terms of Services",
    "handle": "tos",
    "body_html": "<p>We make <strong>perfect<\/strong> stuff, we don't need a warranty.<\/p>",
    "author": "Dennis",
    "created_at": "2008-07-15T20:00:00-04:00",
    "updated_at": "2017-01-05T15:42:20-05:00",
    "published_at": "2008-07-15T20:00:00-04:00",
    "template_suffix": null
  }
}

```

Update an existing page completely

- PUT `https://apis.haravan.com/web/pages/131092082.json`

```codeBlockLines_e6Vv
{
  "page": {
    "id": 131092082,
    "body_html": "<p>Okay, maybe we will give you a warranty.<\/p>",
    "author": "Your name",
    "title": "My new Title",
    "handle": "new-title"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "page": {
    "shop_id": 690933842,
    "id": 131092082,
    "title": "My new Title",
    "handle": "new-title",
    "body_html": "<p>Okay, maybe we will give you a warranty.<\/p>",
    "author": "Your name",
    "created_at": "2008-07-15T20:00:00-04:00",
    "updated_at": "2017-01-05T15:42:20-05:00",
    "published_at": "2008-07-15T20:00:00-04:00",
    "template_suffix": null
  }
}

```

### Remove a Page from the database. [​](https://docs.haravan.com/docs/omni-apis/pages/\#remove-a-page-from-the-database "Direct link to heading")

DELETE

https://apis.haravan.com/web/pages/{page\_id}.json

Delete a page

Remove an existing page from a shop

- DELETE `https://apis.haravan.com/web/pages/131092082.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{}

```

[Previous\\
\\
Comment](https://docs.haravan.com/docs/omni-apis/comments/) [Next\\
\\
Redirect](https://docs.haravan.com/docs/omni-apis/redirects/)

- [What you can do with Page](https://docs.haravan.com/docs/omni-apis/pages/#what-you-can-do-with-page)
- [Page properties](https://docs.haravan.com/docs/omni-apis/pages/#page-properties)
- [Receive a list of all Pages.](https://docs.haravan.com/docs/omni-apis/pages/#receive-a-list-of-all-pages)
- [Receive a count of all Pages.](https://docs.haravan.com/docs/omni-apis/pages/#receive-a-count-of-all-pages)
- [Receive a single Page.](https://docs.haravan.com/docs/omni-apis/pages/#receive-a-single-page)
- [Create a new Page.](https://docs.haravan.com/docs/omni-apis/pages/#create-a-new-page)
- [Modify an existing Page.](https://docs.haravan.com/docs/omni-apis/pages/#modify-an-existing-page)
- [Remove a Page from the database.](https://docs.haravan.com/docs/omni-apis/pages/#remove-a-page-from-the-database)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.