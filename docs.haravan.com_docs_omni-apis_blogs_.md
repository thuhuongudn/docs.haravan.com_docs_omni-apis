---
url: "https://docs.haravan.com/docs/omni-apis/blogs/"
title: "Blog | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/blogs/#)

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
- Blog

On this page

# Blog

`Version: 1.0`

In addition to an online storefront, haravan shops come with a built-in blogging engine, allowing a shop to have one or more blogs.

Shop owners are encouraged to use blogs to:

- Make announcements
- Talk about their products in more detail
- Show off their expertise
- Connect with their customers and
- Boost their shop's search engine rankings

Haravan blogs are like most other blogs: a content management system for articles posted in reverse chronological order. Articles can be posted under one or more user-defined categories and tagged with one or more user-defined tags, with an option to allow readers to post comments to articles. An Atom feed is automatically generated for each blog, allowing for syndication. The search functionality built into every shop also searches the text in blog articles.

Blogs are meant to be used as a type of magazine or newsletter for the shop, with content that changes over time. If your shop needs a static page (such as an "About Us" page), we recommend that you use a Page instead.

**Authenticated access scopes**: `com.read_contents`, `com.write_contents`

### What you can do with Blog [​](https://docs.haravan.com/docs/omni-apis/blogs/\#what-you-can-do-with-blog "Direct link to heading")

The Haravan API lets you do the following with the Blog resource.

- GET `https://apis.haravan.com/web/blogs.json`
  - **[Retrieves a list of blogs](https://docs.haravan.com/docs/omni-apis/blogs/#retrieves-a-list-of-blogs)**
- GET `https://apis.haravan.com/web/blogs/count.json`
  - **[Retrieves a count of blogs](https://docs.haravan.com/docs/omni-apis/blogs/#retrieves-a-count-of-blogs)**
- GET `https://apis.haravan.com/web/blogs/{id}.json`
  - **[Retrieves single the blog](https://docs.haravan.com/docs/omni-apis/blogs/#retrieves-single-the-blog)**
- POST `https://apis.haravan.com/web/blogs.json`
  - **[Create a new blog](https://docs.haravan.com/docs/omni-apis/blogs/#create-a-new-blog)**
- PUT `https://apis.haravan.com/web/blogs.json`
  - **[Modify an existing blog](https://docs.haravan.com/docs/omni-apis/blogs/#modify-an-existing-blog)**
- DELETE `https://apis.haravan.com/web/blogs/{id}.json`
  - **[Delete an existing blog](https://docs.haravan.com/docs/omni-apis/blogs/#delete-an-existing-blog)**

### Blog properties [​](https://docs.haravan.com/docs/omni-apis/blogs/\#blog-properties "Direct link to heading")

| Param | Description |
| --- | --- |
| commentable | `"commentable": "no"`<br> Indicates whether readers can post comments to the blog and if comments are moderated or not. Possible values are:<br>**no (default)**: Readers cannot post comments to blog articles.<br>**moderate**: Readers can post comments to blog articles, but comments must be moderated before they appear.<br>**yes**: Readers can post comments to blog articles without moderation. |
| created\_at | `"created_at": "2021-05-13T07:29:20.1Z"`<br> The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.24591609.2138857477.1661683799-1362597417.1649044980) format) when the blog was created. |
| feedburner | `"feedburner": null`<br> Feedburner is a web feed management provider and can be enabled to provide custom RSS feeds for haravan bloggers. This property will default to blank or "null" unless Feedburner is enabled through the shop admin. |
| feedburner\_location | `"feedburner_location": null`<br> URL to the FeedBurner location for blogs that have enabled FeedBurner through their store admin. |
| handle | `"handle": "apple-blog"`<br> A human-friendly unique string for a blog is automatically generated from its title. This handle is used by the Liquid templating language to refer to the blog. |
| id | `"id": 241253187`<br> A unique numeric identifier for the blog. |
| tags | `"tags" : "tagged"`<br> Tags are additional short descriptors formatted as a string of comma-separated values. For example, if an article has three tags: tag1, tag2, tag3. |
| template\_suffix | `"template_suffix": null`<br> States the name of the template a blog is using if it is using an alternate template. If a blog is using the default blog.liquid template, the value returned is "null". |
| title | `"title": "my blog"`<br> The title of the blog. |
| updated\_at | `"updated_at": "2021-05-13T07:29:20.808Z"`<br> The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601?_ga=2.24591609.2138857477.1661683799-1362597417.1649044980) format) when the blog was last updated. |

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/blogs/\#endpoints "Direct link to heading")

### Retrieves a list of blogs [​](https://docs.haravan.com/docs/omni-apis/blogs/\#retrieves-a-list-of-blogs "Direct link to heading")

GET

https://apis.haravan.com/web/blogs.json

| Param | Description |
| --- | --- |
| limit | Limit of the result. |
| page | Page to show the result. |
| since\_id | Restrict results to after the specified ID |
| handle | Filter by Blog handle. |
| fields | comma-separated list of fields to include in the response. |

Retrieves a list of all blogs by page number. By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/web/blogs.json?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "blogs": [\
        {\
            "commentable": "no",\
            "created_at": "2015-03-28T13:26:28-04:00",\
            "feedburner": null,\
            "feedburner_location": null,\
            "handle": "apple-blog",\
            "id": 241253187,\
            "template_suffix": null,\
            "title": "Mah Blog",\
            "updated_at": "2006-02-01T19:00:00-05:00",\
            "tags": "Announcing, Mystery"\
        }\
    ]
}

```

### Retrieves a count of blogs [​](https://docs.haravan.com/docs/omni-apis/blogs/\#retrieves-a-count-of-blogs "Direct link to heading")

GET

https://apis.haravan.com/com/blogs/count.json

- GET `https://apis.haravan.com/web/blogs/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 570
}

```

### Retrieves single the blog [​](https://docs.haravan.com/docs/omni-apis/blogs/\#retrieves-single-the-blog "Direct link to heading")

GET

https://apis.haravan.com/web/blogs/{id}.json

- GET `https://apis.haravan.com/web/blogs/241253187.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "blogs": [\
        {\
            "commentable": "no",\
            "created_at": "2015-03-28T13:26:28-04:00",\
            "feedburner": null,\
            "feedburner_location": null,\
            "handle": "apple-blog",\
            "id": 241253187,\
            "template_suffix": null,\
            "title": "Mah Blog",\
            "updated_at": "2006-02-01T19:00:00-05:00",\
            "tags": "Announcing, Mystery"\
        }\
    ]
}

```

### Create a new blog [​](https://docs.haravan.com/docs/omni-apis/blogs/\#create-a-new-blog "Direct link to heading")

POST

https://apis.haravan.com/web/blogs.json

- POST `https://apis.haravan.com/web/blogs.json`

```codeBlockLines_e6Vv
{
    "blog": {
        "title": "Apple main blog",
        "tags" : "apple-blog"
    }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "blog": {
    "commentable": "no",
    "created_at": "2015-03-28T13:27:02-04:00",
    "feedburner": null,
    "feedburner_location": null,
    "handle": "apple-main-blog",
    "id": 1008414249,
    "template_suffix": null,
    "title": "Apple main blog",
    "updated_at": "2015-03-28T13:27:02-04:00",
    "tags": "apple-blog"
  }
}

```

### Modify an existing blog [​](https://docs.haravan.com/docs/omni-apis/blogs/\#modify-an-existing-blog "Direct link to heading")

PUT

https://apis.haravan.com/web/blogs/{id}.json

- PUT `https://apis.haravan.com/web/blogs/241253187.json`

```codeBlockLines_e6Vv
{
  "blog": {
    "title": "IPod Updates",
    "handle": "apple-blog",
    "tags": "Announcing, Mystery"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "blog": {
    "commentable": "no",
    "created_at": "2015-03-28T13:26:28-04:00",
    "feedburner": null,
    "feedburner_location": null,
    "handle": "apple-blog",
    "id": 241253187,
    "template_suffix": null,
    "title": "IPod Updates",
    "updated_at": "2015-03-28T13:27:03-04:00",
    "tags": "Announcing, Mystery"
  }
}

```

### Delete an existing blog [​](https://docs.haravan.com/docs/omni-apis/blogs/\#delete-an-existing-blog "Direct link to heading")

DELETE

https://apis.haravan.com/web/blogs/{id}.json

- DELETE `https://apis.haravan.com/web/blogs/241253187.json`

```codeBlockLines_e6Vv
{}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{}

```

[Previous\\
\\
Asset](https://docs.haravan.com/docs/omni-apis/assets/) [Next\\
\\
Comment](https://docs.haravan.com/docs/omni-apis/comments/)

- [What you can do with Blog](https://docs.haravan.com/docs/omni-apis/blogs/#what-you-can-do-with-blog)
- [Blog properties](https://docs.haravan.com/docs/omni-apis/blogs/#blog-properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/blogs/#endpoints)
- [Retrieves a list of blogs](https://docs.haravan.com/docs/omni-apis/blogs/#retrieves-a-list-of-blogs)
- [Retrieves a count of blogs](https://docs.haravan.com/docs/omni-apis/blogs/#retrieves-a-count-of-blogs)
- [Retrieves single the blog](https://docs.haravan.com/docs/omni-apis/blogs/#retrieves-single-the-blog)
- [Create a new blog](https://docs.haravan.com/docs/omni-apis/blogs/#create-a-new-blog)
- [Modify an existing blog](https://docs.haravan.com/docs/omni-apis/blogs/#modify-an-existing-blog)
- [Delete an existing blog](https://docs.haravan.com/docs/omni-apis/blogs/#delete-an-existing-blog)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.