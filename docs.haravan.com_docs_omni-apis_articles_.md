---
url: "https://docs.haravan.com/docs/omni-apis/articles/"
title: "Article | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/articles/#)

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
- Online store

On this page

# Article

An article is a single entry in a blog.

Articles appear in reverse chronological order, with the most recent entry at the top of the blog's page. A blog can contain any number of articles.

**Authenticated access scopes**: `com.read_contents`, `com.write_contents`

### What you can do with Article [​](https://docs.haravan.com/docs/omni-apis/articles/\#what-you-can-do-with-article "Direct link to heading")

The Haravan API lets you do the following with the Article resource.

- GET `https://apis.haravan.com/web/blogs/{blog_id}/articles.json`
  - **[Receive a list of all articles](https://docs.haravan.com/docs/omni-apis/articles/#receive-a-list-of-all-articles)**
- GET `https://apis.haravan.com/web/blogs/{blog_id}/articles/count.json`
  - **[Retrieves a count of all articles](https://docs.haravan.com/docs/omni-apis/articles/#retrieves-a-count-of-all-articles)**
- GET `https://apis.haravan.com/web/blogs/{blog_id}/articles/{article_id}.json`
  - **[Retrieves single the article](https://docs.haravan.com/docs/omni-apis/articles/#retrieves-single-the-article)**
- GET `https://apis.haravan.com/web/articles/tags.json`
  - **[Retrieves a list of all the tags](https://docs.haravan.com/docs/omni-apis/articles/#retrieves-a-list-of-all-the-tags)**
- GET `https://apis.haravan.com/web/articles/authors.json`
  - **[Retrieves a list of all the authors](https://docs.haravan.com/docs/omni-apis/articles/#retrieves-a-list-of-all-the-authors)**
- POST `https://apis.haravan.com/web/blogs/{blog_id}/articles.json`
  - **[Create a new article](https://docs.haravan.com/docs/omni-apis/articles/#create-a-new-article)**
- PUT `https://apis.haravan.com/web/blogs/{blog_id}/articles/{article_id}.json`
  - **[Modify an existing article](https://docs.haravan.com/docs/omni-apis/articles/#modify-an-existing-article)**
- DELETE `https://apis.haravan.com/web/blogs/{blog_id}/articles/{article_id}.json`
  - **[Delete an existing article](https://docs.haravan.com/docs/omni-apis/articles/#delete-an-existing-article)**

### Article properties [​](https://docs.haravan.com/docs/omni-apis/articles/\#article-properties "Direct link to heading")

* * *

`author`: `string`

```codeBlockLines_e6Vv
"author": "John"

```

The name of the author of this article.

`blog_id`: `number`

```codeBlockLines_e6Vv
"blog_id": 241253187

```

A unique numeric identifier for the blog containing the article.

`body_html`: `string`

```codeBlockLines_e6Vv
"body_html": "I have no idea what to write about!"

```

The text of the body of the article, complete with HTML markup.

`created_at`: `Datetime`

```codeBlockLines_e6Vv
"created_at": "2021-05-13T07:29:20.808Z"

```

The date and time [(ISO 8601 format)](https://en.wikipedia.org/wiki/ISO_8601) when the article was created.

`id`: `number`

```codeBlockLines_e6Vv
"id": 989034056

```

A unique numeric identifier for the article.

`handle`: `string`

```codeBlockLines_e6Vv
"handle": "apple-blog"

```

A human-friendly unique string for an article is automatically generated from its title. It is used in the article's URL.

`image`: `string`

```codeBlockLines_e6Vv
"image": null

```

The article image.

`published`: `boolean`

```codeBlockLines_e6Vv
"published": false

```

States whether or not the article is visible. Valid values are "true" for published or "false" for hidden.

`published_at`: `datetime`

```codeBlockLines_e6Vv
"published_at": "2021-05-06T10:27:33.385Z"

```

The date and time [(ISO 8601 format)](https://en.wikipedia.org/wiki/ISO_8601) when the article was published.

`summary_html`: `string`

```codeBlockLines_e6Vv
"summary_html": null

```

The text of the summary of the article, complete with HTML markup.

`tags`: `string`

```codeBlockLines_e6Vv
"tags": "tagsational"

```

Tags are additional short descriptors formatted as a string of comma-separated values. For example, if an article has three tags: tag1, tag2, tag3.

`template_suffix`: `string`

```codeBlockLines_e6Vv
"template_suffix": null

```

States the name of the template an article is using if it is using an alternate template. If an article is using the default article.liquid template, the value returned is "null".

`title`: `string`

```codeBlockLines_e6Vv
"title": "Some crazy article I'm coming up with"

```

The title of the article.

`user_id`: `number`

```codeBlockLines_e6Vv
"user_id": 799407056

```

A unique numeric identifier for the author of the article.

`updated_at`: `datetime`

```codeBlockLines_e6Vv
"updated_at": "2021-05-13T07:29:20.808Z"

```

The date and time [(ISO 8601 format)](https://en.wikipedia.org/wiki/ISO_8601) when the article was last updated.

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/articles/\#endpoints "Direct link to heading")

### Receive a list of all articles [​](https://docs.haravan.com/docs/omni-apis/articles/\#receive-a-list-of-all-articles "Direct link to heading")

GET

https://apis.haravan.com/web/blogs/{blog\_id}/articles.json

**Retrieves a list of all articles from a certain blog.**

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/articles/\#parameters "Direct link to heading")

* * *

`limit`

Limit of the result.

* * *

`page`

Page to show the result.

* * *

`since_id`

Restrict results to after the specified ID

* * *

`handle`

Filter by Blog handle.

* * *

`fields`

comma-separated list of fields to include in the response.

* * *

`created_at_min`

Show articles created after the date (format: 2008-12-31T02:01:27.483Z).

* * *

`created_at_max`

Show articles created before date (format: 2008-12-31T02:01:27.483Z).

* * *

`updated_at_min`

Show articles last updated after date (format: 2008-12-31T02:01:27.483Z).

* * *

`updated_at_max`

Show articles last updated before date (format: 2008-12-31T02:01:27.483Z).

* * *

`published_at_min`

Show articles published after the date (format: 2008-12-31T02:01:27.483Z).

* * *

`published_at_max`

Show articles published before date (format: 2008-12-31T02:01:27.483Z).

* * *

`published_status`

- published - Show only published articles
- unpublished - Show only unpublished articles
- any - Show all articles (default)

* * *

`author`

Filter by the article author.

* * *

**Retrieves a list of all articles from a certain blog by page number. By default, the number of resources on the page is 50.**

- GET `https://apis.haravan.com/web/blogs/24125318/articles.json?page=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "articles": [\
    {\
      "id": 294160202,\
      "title": "Just us bots here",\
      "created_at": "2013-11-06T19:00:00-05:00Z",\
      "body_html": "beep boop",\
      "blog_id": 241253187,\
      "author": "dennis",\
      "user_id": null,\
      "published_at": null,\
      "updated_at": "2022-02-25T12:04:51.000Z",\
      "summary_html": null,\
      "template_suffix": null,\
      "handle": "just-us-bots-here",\
      "tags": ""\
    },\
    {\
      "id": 989034056,\
      "title": "Some crazy article I'm coming up with",\
      "created_at": "2008-12-31T19:00:00-05:00Z",\
      "body_html": "I have no idea what to write about, but it's going to rock!",\
      "blog_id": 241253187,\
      "author": "John",\
      "user_id": null,\
      "published_at": null,\
      "updated_at": "2009-01-31T19:00:00-05:00Z",\
      "summary_html": null,\
      "template_suffix": null,\
      "handle": "some-crazy-article-im-coming-up-with",\
      "tags": "Mystery"\
    },\
    {\
      "id": 1051293780,\
      "title": "Welcome to the world of tomorrow!",\
      "created_at": "2022-02-25T12:04:51.000Z",\
      "body_html": "Good news, everybody!",\
      "blog_id": 241253187,\
      "author": "dennis",\
      "user_id": null,\
      "published_at": null,\
      "updated_at": "2022-02-25T12:04:51.000Z",\
      "summary_html": null,\
      "template_suffix": null,\
      "handle": "welcome-to-the-world-of-tomorrow",\
      "tags": ""\
    }\
  ]
}

```

**Retrieves a list of articles from a certain blog by handle.**

- GET `https://apis.haravan.com/web/blogs/241253187/articles.json?author=dennis`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "articles": [\
    {\
      "id": 294160202,\
      "title": "Just us bots here",\
      "created_at": "2013-11-06T19:00:00-05:00Z",\
      "body_html": "beep boop",\
      "blog_id": 241253187,\
      "author": "dennis",\
      "user_id": null,\
      "published_at": null,\
      "updated_at": "2022-02-25T12:04:51.000Z",\
      "summary_html": null,\
      "template_suffix": null,\
      "handle": "just-us-bots-here",\
      "tags": ""\
    },\
    {\
      "id": 1051293780,\
      "title": "Welcome to the world of tomorrow!",\
      "created_at": "2013-11-06T19:00:00-05:00Z",\
      "body_html": "Good news, everybody!",\
      "blog_id": 241253187,\
      "author": "dennis",\
      "user_id": null,\
      "published_at": null,\
      "updated_at": "2022-02-25T12:04:51.000Z",\
      "summary_html": null,\
      "template_suffix": null,\
      "handle": "welcome-to-the-world-of-tomorrow",\
      "tags": ""\
    }\
  ]
}

```

### Retrieves a count of all articles [​](https://docs.haravan.com/docs/omni-apis/articles/\#retrieves-a-count-of-all-articles "Direct link to heading")

GET

https://apis.haravan.com/web/blogs/{blog\_id}/articles/count.json

**Retrieves a count of the articles from a certain blog.**

- GET `https://apis.haravan.com/web/blogs/1051293780/articles/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "count": 20
}

```

### Retrieves single the article [​](https://docs.haravan.com/docs/omni-apis/articles/\#retrieves-single-the-article "Direct link to heading")

GET

https://apis.haravan.com/web/blogs/{blog\_id}/articles/{article\_id}.json

**Retrieves a single article by its ID and the ID of the parent blog.**

- GET `https://apis.haravan.com/web/blogs/241253187/articles/134645308.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "article": {
        "id": 134645308,
        "title": "get on the train now",
        "created_at": "2022-02-25T12:04:51.000Z",
        "body_html": "
Do you have an IPod yet?
",
        "blog_id": 241253187,
        "author": "Dennis",
        "user_id": 799407056,
        "published_at": "2022-02-25T12:04:51.000Z",
        "updated_at": "2022-02-25T12:04:51.000Z",
        "summary_html": null,
        "template_suffix": null,
        "handle": "get-on-the-train-now",
        "tags": "Announcing",
        "image": {
            "created_at": "2022-02-25T12:04:51.000Z",
            "attachment": null,
            "filename": null,
            "src": "https://www.file.hstatic.net/imac.jpg?v=1500937783"
        }
    }
}

```

### Retrieves a list of all the tags [​](https://docs.haravan.com/docs/omni-apis/articles/\#retrieves-a-list-of-all-the-tags "Direct link to heading")

GET

https://apis.haravan.com/web/articles/tags.json

**Retrieves a list of all the tags of articles.**

- GET `https://apis.haravan.com/web/articles/tags.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "tags": [\
    "Announcing"\
  ]
}

```

### Retrieves a list of all the authors [​](https://docs.haravan.com/docs/omni-apis/articles/\#retrieves-a-list-of-all-the-authors "Direct link to heading")

GET

https://apis.haravan.com/web/articles/authors.json

**Retrieves a list of all the authors of articles.**

- GET `https://apis.haravan.com/web/articles/authors.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "authors": [\
    "dennis",\
    "John",\
    "Rob",\
    "Dennis"\
  ]
}

```

### Create a new article [​](https://docs.haravan.com/docs/omni-apis/articles/\#create-a-new-article "Direct link to heading")

POST

https://apis.haravan.com/web/blogs/{blog\_id}/articles.json

**Create a new article for a blog.**

**Create a new article with an image that will be downloaded by Haravan.**

- POST `https://apis.haravan.com/web/blogs/{blog_id}/articles.json`

```codeBlockLines_e6Vv
{
  "article": {
    "title": "My new Article title",
    "author": "John Smith",
    "tags": "This Post, Has Been Tagged",
    "body_html": "I like articles. Yea, I like posting them through REST.",
    "published_at": "2022-02-25T12:04:51.000Z",
    "image": {
      "src": "https://www.example.com/rails_logo.gif"
    }
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "article": {
    "id": 1051293783,
    "title": "My new Article title",
    "created_at": "2022-02-25T12:04:51.000Z",
    "body_html": "I like articles. Yea, I like posting them through REST.",
    "blog_id": 241253187,
    "author": "John Smith",
    "user_id": null,
    "published_at": "2022-02-25T12:04:51.000Z",
    "updated_at": "2022-02-25T12:04:51.000Z",
    "summary_html": null,
    "template_suffix": null,
    "handle": "my-new-article-title",
    "tags": "Has Been Tagged, This Post",
    "image": {
      "created_at": "2022-02-25T12:04:51.000Z",
      "attachment": null,
      "filename": null,
      "src": "https://www.file.hstatic.net/rails_logo.gif?v=1500938183"
    }
  }
}

```

**Create a new article with a base64 encoded image.**

- POST `https://apis.haravan.com/web/blogs/{blog_id}/articles.json`

```codeBlockLines_e6Vv
{
  "article": {
    "title": "My new Article title",
    "author": "John Smith",
    "tags": "This Post, Has Been Tagged",
    "body_html": "I like articles. Yea, I like posting them through REST.",
    "published_at": "2022-02-25T12:04:51.000Z",
    "image": {
      "attachment": "R0lGODlhAQABAIAAAAAAAAAAACH5BAEAAAAALAAAAAABAAEAAAICRAEAOw==\n"
    }
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "article": {
    "id": 1051293789,
    "title": "My new Article title",
    "created_at": "2022-02-25T12:04:51.000Z",
    "body_html": "I like articles.Yea, I like posting them through REST.",
    "blog_id": 241253187,
    "author": "John Smith",
    "user_id": null,
    "published_at": "2022-02-25T12:04:51.000Z",
    "updated_at": "2022-02-25T12:04:51.000Z",
    "summary_html": null,
    "template_suffix": null,
    "handle": "my-new-article-title",
    "tags": "Has Been Tagged, This Post",
    "image": {
      "created_at": "2022-02-25T12:04:51.000Z",
      "attachment": null,
      "filename": null,
      "src": "https://www.file.hstatic.net/df3e567d6f16d040326c7a0ea29a4f41.gif?v=1500938193"
    }
  }
}

```

### Modify an existing article [​](https://docs.haravan.com/docs/omni-apis/articles/\#modify-an-existing-article "Direct link to heading")

PUT

https://apis.haravan.com/web/blogs/{blog\_id}/articles/{article\_id}.json

**Update an existing article of a blog.**

- PUT `https://apis.haravan.com/web/blogs/241253187/articles/134645308.json`

```codeBlockLines_e6Vv
{
    "article": {
    "id": 134645308,
    "title": "My new Title",
    "author": "Your name",
    "tags": "Tags, Will Be, Updated",
    "body_html": "
Look, I can even update through a web service.

",
    "published_at": "2022-02-25T12:04:51.000Z"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "article": {
    "id": 134645308,
    "title": "My new Title",
    "created_at": "2022-02-25T12:04:51.000Z",
    "body_html": "
Look, I can even update through a web service.

",
    "blog_id": 241253187,
    "author": "Your name",
    "user_id": null,
    "published_at": "2022-02-25T12:04:51.000Z",
    "updated_at": "2022-02-25T12:04:51.000Z",
    "summary_html": null,
    "template_suffix": null,
    "handle": "get-on-the-train-now",
    "tags": "Tags, Updated, Will Be",
    "image": {
      "created_at": "2022-02-25T12:04:51.000Z",
      "attachment": null,
      "filename": null,
      "src": "https://www.file.hstatic.net/imac.jpg?v=1500937783"
    }
  }
}

```

### Delete an existing article [​](https://docs.haravan.com/docs/omni-apis/articles/\#delete-an-existing-article "Direct link to heading")

DELETE

https://apis.haravan.com/web/blogs/{blog\_id}/articles/{article\_id}.json

**Delete an article of a blog.**

- DELETE `https://apis.haravan.com/web/blogs/241253187/articles/134645308.json`

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
Metafield](https://docs.haravan.com/docs/omni-apis/metafield/) [Next\\
\\
Article](https://docs.haravan.com/docs/omni-apis/articles/)

- [What you can do with Article](https://docs.haravan.com/docs/omni-apis/articles/#what-you-can-do-with-article)
- [Article properties](https://docs.haravan.com/docs/omni-apis/articles/#article-properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/articles/#endpoints)
- [Receive a list of all articles](https://docs.haravan.com/docs/omni-apis/articles/#receive-a-list-of-all-articles)
- [Retrieves a count of all articles](https://docs.haravan.com/docs/omni-apis/articles/#retrieves-a-count-of-all-articles)
- [Retrieves single the article](https://docs.haravan.com/docs/omni-apis/articles/#retrieves-single-the-article)
- [Retrieves a list of all the tags](https://docs.haravan.com/docs/omni-apis/articles/#retrieves-a-list-of-all-the-tags)
- [Retrieves a list of all the authors](https://docs.haravan.com/docs/omni-apis/articles/#retrieves-a-list-of-all-the-authors)
- [Create a new article](https://docs.haravan.com/docs/omni-apis/articles/#create-a-new-article)
- [Modify an existing article](https://docs.haravan.com/docs/omni-apis/articles/#modify-an-existing-article)
- [Delete an existing article](https://docs.haravan.com/docs/omni-apis/articles/#delete-an-existing-article)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.