---
url: "https://docs.haravan.com/docs/omni-apis/comments/"
title: "Comment | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/comments/#)

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
- Comment

On this page

# Comment

A comment is a reader's response to an article in a blog. They appear on the article page in chronological order, typically after the article body.

![omni_api_comment_img01](https://docs.haravan.com/assets/images/omni_api_comment_img01-a21335d5a040908059550158ea2ba938.png)

Just as a blog can have any number of articles, an article can have any number of comments. Blog comments are a target for spammers, so haravan's blogs make use of a spam detection system to identify comments that are likely to be spam. Shop owners can mark comments as spam and not spam, which not only hides or unhides them from the readers' view, but also trains the haravan spam detection system.

**Authenticated access scopes**: `com.read_contents`, `com.write_contents`

### What you can do with Comment? [​](https://docs.haravan.com/docs/omni-apis/comments/\#what-you-can-do-with-comment "Direct link to heading")

The haravan API lets you do the following with the Comment resource. More detailed versions of these general actions may be available:

- GET `https://apis.haravan.com/web/comments.json?article_id=134645308&blog_id=241253187`
  - **[Receive a list of all Comments](https://docs.haravan.com/docs/omni-apis/comments/#receive-a-list-of-all-comments)**
- GET `https://apis.haravan.com/web/comments/count.json?article_id=134645308&blog_id=241253187`
  - **[Receive a count of all Comments](https://docs.haravan.com/docs/omni-apis/comments/#receive-a-count-of-all-comments)**
- GET `https://apis.haravan.com/web/comments/{comment_id}.json`
  - **[Receive a single Comment](https://docs.haravan.com/docs/omni-apis/comments/#receive-a-single-comment)**
- POST `https://apis.haravan.com/web/comments.json`
  - **[Create a new Comment](https://docs.haravan.com/docs/omni-apis/comments/#create-a-new-comment)**
- PUT `https://apis.haravan.com/web/comments/{comment_id}.json`
  - **[Modify an existing Comment](https://docs.haravan.com/docs/omni-apis/comments/#modify-an-existing-comment)**
- POST `https://apis.haravan.com/web/comments/{comment_id}/spam.json`
  - **[Mark a Comment as spam](https://docs.haravan.com/docs/omni-apis/comments/#mark-a-comment-as-spam)**
- POST `https://apis.haravan.com/web/comments/{comment_id}/not_spam.json`
  - **[Mark a Comment as not spam](https://docs.haravan.com/docs/omni-apis/comments/#mark-a-comment-as-not-spam)**
- POST `https://apis.haravan.com/web/comments/{comment_id}/approve.json`
  - **[Approve a Comment](https://docs.haravan.com/docs/omni-apis/comments/#approve-a-comment)**
- POST `https://apis.haravan.com/web/comments/{comment_id}/remove.json`
  - **[Remove a Comment](https://docs.haravan.com/docs/omni-apis/comments/#remove-a-comment)**
- POST `https://apis.haravan.com/web/comments/{comment_id}/restore.json`
  - **[Restore a Comment](https://docs.haravan.com/docs/omni-apis/comments/#restore-a-comment)**

### Comment Properties [​](https://docs.haravan.com/docs/omni-apis/comments/\#comment-properties "Direct link to heading")

* * *

`article_id`: `number`

```codeBlockLines_e6Vv
{ "article_id" : 134645308 }

```

A unique numeric identifier for the article to which the comment belongs.

`author`: `string`

```codeBlockLines_e6Vv
{ "author" : "Soleone" }

```

The name of the author of the comment.

`blog_id`: `number`

```codeBlockLines_e6Vv
{ "blog_id" : 241253187  }

```

A unique numeric identifier for the blog containing the article that the comment belongs to.

`body`: `string`

```codeBlockLines_e6Vv
{ "body" : "I really _like_ this." }

```

The basic textile markup of a comment.

`body_html`: `string`

```codeBlockLines_e6Vv
{ "body_html" : "I really _like_ this."}

```

The text of the comment, complete with HTML markup.

`created_at`: `string`

```codeBlockLines_e6Vv
{ "created_at" : "2012-08-24T14:01:46-04:00" }

```

The date and time when the comment was created. The API returns this value in [ISO 8601 format](http://en.wikipedia.org/wiki/ISO_8601).

`email`: `string`

```codeBlockLines_e6Vv
{ "email" : "sole@one.de" }

```

The email address of the author of the comment.

`id`: `number`

```codeBlockLines_e6Vv
{ "id" : 653537639 }

```

A unique numeric identifier for the comment.

`ip`: `string`

```codeBlockLines_e6Vv
{ "ip" : "127.0.0.1" }

```

The IP address from which the comment was posted.

`published_at`: `string`

```codeBlockLines_e6Vv
{ "published_at" : "2012-08-24T14:02:00-04:00" }

```

The date and time when the comment was published. In the case of comments, this is the date and time when the comment was created, meaning that it has the same value as created\_at. The API returns this value in [ISO 8601 format](http://en.wikipedia.org/wiki/ISO_8601).

`status`: `string`

```codeBlockLines_e6Vv
{ "status" : "removed" }

```

The status of the comment. The possible values are:

- **unapproved (default)**: The comment is awaiting moderation by the shop owner and is not visible to the readers of the blog.
- **published**: The comment has been approved (if the blog requires comments to be moderated) and is visible to readers of the blog.
- **spam**: The comment has been marked as spam by the shop owner and is not visible to readers of the blog.
- **removed**: The comment has been removed from the article.

`updated_at`: `string`

```codeBlockLines_e6Vv
{ "updated_at" : "null" }

```

The date and time when the comment was last modified. When the comment is first created, this is the date and time when the comment was created, meaning that it has the same value as created\_at. If the blog requires comments to be approved, this value is updated to the date and time the comment was approved upon approval. The API returns this value in [ISO 8601 format](http://en.wikipedia.org/wiki/ISO_8601).

`user_agent`: `string`

```codeBlockLines_e6Vv
{ "user_agent" : "Mozilla/5.0" }

```

The user agent string provided by the software (usually a browser) used to create the comment.

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/comments/\#endpoints "Direct link to heading")

### Receive a list of all Comments [​](https://docs.haravan.com/docs/omni-apis/comments/\#receive-a-list-of-all-comments "Direct link to heading")

GET

https://apis.haravan.com/web/comments.json

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/comments/\#parameters "Direct link to heading")

* * *

`limit` `≤250` `default: 250`

Amount of results

* * *

`page` (default: 1)

Page to show

* * *

`since_id`

Restrict results to after the specified ID

* * *

`created_at_min`

Show comments created after date (format: 2008-12-31 03:00)

* * *

`created_at_max`

Show comments created before date (format: 2008-12-31 03:00)

* * *

`updated_at_min`

Show comments last updated after date (format: 2008-12-31 03:00)

* * *

`updated_at_max`

Show comments last updated before date (format: 2008-12-31 03:00)

* * *

`published_at_min`

Show comments published after date (format: 2008-12-31 03:00)

* * *

`published_at_max`

Show comments published before date (format: 2008-12-31 03:00)

* * *

`fields`

comma-separated list of fields to include in the response

* * *

`published_status`

- **published** \- Show only published comments
- **unpublished** \- Show only unpublished comments
- **any** \- Show all comments (default)

* * *

`status`

- **published** \- Show only published comments
- **unapproved** \- Show only unapproved comments

* * *


**Get all the comments for a certain article of a blog**

- GET `https://apis.haravan.com/web/comments.json?article_id=134645308&blog_id=241253187`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "comments": [\
    {\
      "article_id": 134645308,\
      "author": "Soleone",\
      "blog_id": 241253187,\
      "body": "Hi author, I really _like_ what you're doing there.",\
      "body_html": "<p>Hi author, I really <em>like<\/em> what you're doing there.<\/p>",\
      "created_at": "2015-03-28T13:26:28-04:00",\
      "email": "sole@one.de",\
      "id": 653537639,\
      "ip": "127.0.0.1",\
      "published_at": null,\
      "status": "unapproved",\
      "updated_at": "2015-03-28T13:26:28-04:00",\
      "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"\
    },\
    {\
      "article_id": 134645308,\
      "author": "Soleone",\
      "blog_id": 241253187,\
      "body": "Hi author, I really _like_ what you're doing there.",\
      "body_html": "<p>Hi author, I really <em>like<\/em> what you're doing there.<\/p>",\
      "created_at": "2015-03-28T13:26:28-04:00",\
      "email": "sole@one.de",\
      "id": 118373535,\
      "ip": "127.0.0.1",\
      "published_at": null,\
      "status": "published",\
      "updated_at": "2015-03-28T13:26:28-04:00",\
      "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"\
    }\
  ]
}

```

**Get all the comments for all the articles of a certain blog**

- GET `https://apis.haravan.com/web/comments.json?blog_id=241253187`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "comments": [\
    {\
      "article_id": 134645308,\
      "author": "Soleone",\
      "blog_id": 241253187,\
      "body": "Hi author, I really _like_ what you're doing there.",\
      "body_html": "<p>Hi author, I really <em>like<\/em> what you're doing there.<\/p>",\
      "created_at": "2015-03-28T13:26:28-04:00",\
      "email": "sole@one.de",\
      "id": 653537639,\
      "ip": "127.0.0.1",\
      "published_at": null,\
      "status": "unapproved",\
      "updated_at": "2015-03-28T13:26:28-04:00",\
      "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"\
    },\
    {\
      "article_id": 134645308,\
      "author": "Soleone",\
      "blog_id": 241253187,\
      "body": "Hi author, I really _like_ what you're doing there.",\
      "body_html": "<p>Hi author, I really <em>like<\/em> what you're doing there.<\/p>",\
      "created_at": "2015-03-28T13:26:28-04:00",\
      "email": "sole@one.de",\
      "id": 118373535,\
      "ip": "127.0.0.1",\
      "published_at": null,\
      "status": "published",\
      "updated_at": "2015-03-28T13:26:28-04:00",\
      "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"\
    }\
  ]
}

```

**Get all the comments for this shop**

- GET `https://apis.haravan.com/web/comments.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "comments": [\
    {\
      "article_id": 134645308,\
      "author": "Soleone",\
      "blog_id": 241253187,\
      "body": "Hi author, I really _like_ what you're doing there.",\
      "body_html": "<p>Hi author, I really <em>like<\/em> what you're doing there.<\/p>",\
      "created_at": "2015-03-28T13:26:28-04:00",\
      "email": "sole@one.de",\
      "id": 653537639,\
      "ip": "127.0.0.1",\
      "published_at": null,\
      "status": "unapproved",\
      "updated_at": "2015-03-28T13:26:28-04:00",\
      "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"\
    },\
    {\
      "article_id": 134645308,\
      "author": "Soleone",\
      "blog_id": 241253187,\
      "body": "Hi author, I really _like_ what you're doing there.",\
      "body_html": "<p>Hi author, I really <em>like<\/em> what you're doing there.<\/p>",\
      "created_at": "2015-03-28T13:26:28-04:00",\
      "email": "sole@one.de",\
      "id": 118373535,\
      "ip": "127.0.0.1",\
      "published_at": null,\
      "status": "published",\
      "updated_at": "2015-03-28T13:26:28-04:00",\
      "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"\
    }\
  ]
}

```

**Get all comments after the specified ID**

- GET `https://apis.haravan.com/web/comments.json?since_id=118373535`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "comments": [\
    {\
      "article_id": 134645308,\
      "author": "Soleone",\
      "blog_id": 241253187,\
      "body": "Hi author, I really _like_ what you're doing there.",\
      "body_html": "<p>Hi author, I really <em>like<\/em> what you're doing there.<\/p>",\
      "created_at": "2015-03-28T13:26:28-04:00",\
      "email": "sole@one.de",\
      "id": 653537639,\
      "ip": "127.0.0.1",\
      "published_at": null,\
      "status": "unapproved",\
      "updated_at": "2015-03-28T13:26:28-04:00",\
      "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"\
    }\
  ]
}

```

### Receive a count of all Comments [​](https://docs.haravan.com/docs/omni-apis/comments/\#receive-a-count-of-all-comments "Direct link to heading")

GET

https://apis.haravan.com/web/comments/count.json

Get a count of all comments for an article

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/comments/\#parameters-1 "Direct link to heading")

* * *

`created_at_min`

Show comments created after date (format: 2008-12-31 03:00)

* * *

`created_at_max`

Show comments created before date (format: 2008-12-31 03:00)

* * *

`updated_at_min`

Show comments last updated after date (format: 2008-12-31 03:00)

* * *

`updated_at_max`

Show comments last updated before date (format: 2008-12-31 03:00)

* * *

`published_at_min`

Show comments published after date (format: 2008-12-31 03:00)

* * *

`published_at_max`

Show comments published before date (format: 2008-12-31 03:00)

* * *

`fields`

comma-separated list of fields to include in the response

* * *

`published_status`

- **published** \- Show only published comments
- **unpublished** \- Show only unpublished comments
- **any** \- Show all comments (default)

* * *

`status`

- **pending** \- All pending comments
- **published** \- Show only published comments
- **unapproved** \- Show only unapproved comments

* * *

**Count all comments for a certain article of a blog**

- GET `https://apis.haravan.com/web/comments/count.json?article_id=134645308&blog_id=241253187`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "count": 2
}

```

**Get a count of all the comments for all the articles of a certain blog**

- GET `https://apis.haravan.com/web/comments/count.json?blog_id=241253187`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "count": 2
}

```

**Get a count of all the comments for this shop**

- GET `https://apis.haravan.com/web/comments/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "count": 2
}

```

### Receive a single Comment [​](https://docs.haravan.com/docs/omni-apis/comments/\#receive-a-single-comment "Direct link to heading")

GET

https://apis.haravan.com/web/comments/{comment\_id}.json

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/comments/\#parameters-2 "Direct link to heading")

* * *

`fields`

comma-separated list of fields to include in the response

* * *

**Get a single comment**

- GET `https://apis.haravan.com/web/comments/118373535.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "comment": {
    "article_id": 134645308,
    "author": "Soleone",
    "blog_id": 241253187,
    "body": "Hi author, I really _like_ what you're doing there.",
    "body_html": "<p>Hi author, I really <em>like<\/em> what you're doing there.<\/p>",
    "created_at": "2015-03-28T13:26:28-04:00",
    "email": "sole@one.de",
    "id": 118373535,
    "ip": "127.0.0.1",
    "published_at": null,
    "status": "published",
    "updated_at": "2015-03-28T13:26:28-04:00",
    "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"
  }
}

```

### Create a new Comment [​](https://docs.haravan.com/docs/omni-apis/comments/\#create-a-new-comment "Direct link to heading")

POST

https://apis.haravan.com/web/comments.json

**Create a new comment with basic textile markup for a certain article of a blog**

- POST `https://apis.haravan.com/web/comments.json`

```codeBlockLines_e6Vv
{
  "comment": {
    "body": "I like comments\nAnd I like posting them *RESTfully*.",
    "author": "Your name",
    "email": "your@email.com",
    "ip": "107.20.160.121",
    "blog_id": 241253187,
    "article_id": 134645308
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "comment": {
    "article_id": 134645308,
    "author": "Your name",
    "blog_id": 241253187,
    "body": "I like comments\nAnd I like posting them *RESTfully*.",
    "body_html": "<p>I like comments<br \/>\nAnd I like posting them <strong>RESTfully<\/strong>.<\/p>",
    "created_at": "2015-03-28T13:27:26-04:00",
    "email": "your@email.com",
    "id": 757536352,
    "ip": "107.20.160.121",
    "published_at": "2015-03-28T13:27:26-04:00",
    "status": "pending",
    "updated_at": "2015-03-28T13:27:26-04:00",
    "user_agent": null
  }
}

```

**Trying to create a comment without a body, author, and email will return an error**

- POST `https://apis.haravan.com/web/comments.json`

```codeBlockLines_e6Vv
{
  "comment": {
    "article_id": 134645308
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 422 Unprocessable Entity
{
  "errors": {
    "author": [\
      "can't be blank"\
    ],
    "body": [\
      "can't be blank"\
    ],
    "email": [\
      "is invalid"\
    ]
  }
}

```

### Modify an existing Comment [​](https://docs.haravan.com/docs/omni-apis/comments/\#modify-an-existing-comment "Direct link to heading")

PUT

https://apis.haravan.com/web/comments/{comment\_id}.json

Update a comment of an article within a blog

```codeBlockLines_e6Vv
**Update an existing comment body**

```

- PUT `https://apis.haravan.com/web/comments/118373535.json`

```codeBlockLines_e6Vv
{
  "comment": {
    "id": 118373535,
    "body": "You can even update through a web service.",
    "author": "Your new name",
    "email": "your@updated-email.com",
    "published_at": "2015-03-28T17:27:28+00:00"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "comment": {
    "article_id": 134645308,
    "author": "Your new name",
    "blog_id": 241253187,
    "body": "You can even update through a web service.",
    "body_html": "<p>You can even update through a web service.<\/p>",
    "created_at": "2015-03-28T13:26:28-04:00",
    "email": "your@updated-email.com",
    "id": 118373535,
    "ip": "127.0.0.1",
    "published_at": "2015-03-28T13:27:28-04:00",
    "status": "published",
    "updated_at": "2015-03-28T13:27:29-04:00",
    "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"
  }
}

```

### Mark a Comment as spam [​](https://docs.haravan.com/docs/omni-apis/comments/\#mark-a-comment-as-spam "Direct link to heading")

POST

https://apis.haravan.com/web/comments/{comment\_id}/spam.json

Mark a comment as spam

**Mark a comment as spam, helping to train our spam detection as well as remove the comment sometime soon**

- POST `https://apis.haravan.com/web/comments/653537639/spam.json`

```codeBlockLines_e6Vv
{ }

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "article_id": 134645308,
  "author": "Soleone",
  "blog_id": 241253187,
  "body": "Hi author, I really _like_ what you're doing there.",
  "body_html": "<p>Hi author, I really <em>like<\/em> what you're doing there.<\/p>",
  "created_at": "2015-03-28T13:26:28-04:00",
  "email": "sole@one.de",
  "id": 653537639,
  "ip": "127.0.0.1",
  "published_at": "2015-03-28T13:27:28-04:00",
  "status": "spam",
  "updated_at": "2015-03-28T13:27:28-04:00",
  "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"
}

```

### Mark a Comment as not spam [​](https://docs.haravan.com/docs/omni-apis/comments/\#mark-a-comment-as-not-spam "Direct link to heading")

POST

https://apis.haravan.com/web/comments/{comment\_id}/not\_spam.json

Mark a comment as not spam

**Mark a comment as not spam, restoring a comment marked as spam back to published**

- POST `https://apis.haravan.com/web/comments/653537639/not_spam.json`

```codeBlockLines_e6Vv
{ }

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "article_id": 134645308,
  "author": "Soleone",
  "blog_id": 241253187,
  "body": "Hi author, I really _like_ what you're doing there.",
  "body_html": "<p>Hi author, I really <em>like<\/em> what you're doing there.<\/p>",
  "created_at": "2015-03-28T13:26:28-04:00",
  "email": "sole@one.de",
  "id": 653537639,
  "ip": "127.0.0.1",
  "published_at": "2015-03-28T13:27:28-04:00",
  "status": "published",
  "updated_at": "2015-03-28T13:27:28-04:00",
  "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"
}

```

### Approve a Comment [​](https://docs.haravan.com/docs/omni-apis/comments/\#approve-a-comment "Direct link to heading")

POST

https://apis.haravan.com/web/comments/{comment\_id}/approve.json

Approve a comment

**Approve a comment that is currently pending unapproved so that it will be published on the site**

- POST `https://apis.haravan.com/web/comments/653537639/approve.json`

```codeBlockLines_e6Vv
{ }

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "article_id": 134645308,
  "author": "Soleone",
  "blog_id": 241253187,
  "body": "Hi author, I really _like_ what you're doing there.",
  "body_html": "<p>Hi author, I really <em>like<\/em> what you're doing there.<\/p>",
  "created_at": "2015-03-28T13:26:28-04:00",
  "email": "sole@one.de",
  "id": 653537639,
  "ip": "127.0.0.1",
  "published_at": "2015-03-28T13:27:26-04:00",
  "status": "published",
  "updated_at": "2015-03-28T13:27:26-04:00",
  "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"
}

```

### Remove a Comment [​](https://docs.haravan.com/docs/omni-apis/comments/\#remove-a-comment "Direct link to heading")

POST

https://apis.haravan.com/web/comments/{comment\_id}/remove.json

Remove a comment

**Remove a comment**

- POST `https://apis.haravan.com/web/comments/653537639/remove.json`

```codeBlockLines_e6Vv
{ }

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "article_id": 134645308,
  "author": "Soleone",
  "blog_id": 241253187,
  "body": "Hi author, I really _like_ what you're doing there.",
  "body_html": "<p>Hi author, I really <em>like<\/em> what you're doing there.<\/p>",
  "created_at": "2015-03-28T13:26:28-04:00",
  "email": "sole@one.de",
  "id": 653537639,
  "ip": "127.0.0.1",
  "published_at": "2015-03-28T13:27:28-04:00",
  "status": "removed",
  "updated_at": "2015-03-28T13:27:28-04:00",
  "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"
}

```

### Restore a Comment [​](https://docs.haravan.com/docs/omni-apis/comments/\#restore-a-comment "Direct link to heading")

POST

https://apis.haravan.com/web/comments/{comment\_id}/restore.json

**Restore a Comment**

- POST `https://apis.haravan.com/web/comments/653537639/restore.json`

```codeBlockLines_e6Vv
{ }

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "article_id": 134645308,
  "author": "Soleone",
  "blog_id": 241253187,
  "body": "Hi author, I really _like_ what you're doing there.",
  "body_html": "<p>Hi author, I really <em>like<\/em> what you're doing there.<\/p>",
  "created_at": "2015-03-28T13:26:28-04:00",
  "email": "sole@one.de",
  "id": 653537639,
  "ip": "127.0.0.1",
  "published_at": "2015-03-28T13:27:28-04:00",
  "status": "published",
  "updated_at": "2015-03-28T13:27:28-04:00",
  "user_agent": "Mozilla\/5.0 (Macintosh; U; Intel Mac OS X 10_5_4; en-us) AppleWebKit\/525.18 (KHTML, like Gecko) Version\/3.1.2 Safari\/525.20.1"
}

```

[Previous\\
\\
Blog](https://docs.haravan.com/docs/omni-apis/blogs/) [Next\\
\\
Page](https://docs.haravan.com/docs/omni-apis/pages/)

- [What you can do with Comment?](https://docs.haravan.com/docs/omni-apis/comments/#what-you-can-do-with-comment)
- [Comment Properties](https://docs.haravan.com/docs/omni-apis/comments/#comment-properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/comments/#endpoints)
- [Receive a list of all Comments](https://docs.haravan.com/docs/omni-apis/comments/#receive-a-list-of-all-comments)
- [Receive a count of all Comments](https://docs.haravan.com/docs/omni-apis/comments/#receive-a-count-of-all-comments)
- [Receive a single Comment](https://docs.haravan.com/docs/omni-apis/comments/#receive-a-single-comment)
- [Create a new Comment](https://docs.haravan.com/docs/omni-apis/comments/#create-a-new-comment)
- [Modify an existing Comment](https://docs.haravan.com/docs/omni-apis/comments/#modify-an-existing-comment)
- [Mark a Comment as spam](https://docs.haravan.com/docs/omni-apis/comments/#mark-a-comment-as-spam)
- [Mark a Comment as not spam](https://docs.haravan.com/docs/omni-apis/comments/#mark-a-comment-as-not-spam)
- [Approve a Comment](https://docs.haravan.com/docs/omni-apis/comments/#approve-a-comment)
- [Remove a Comment](https://docs.haravan.com/docs/omni-apis/comments/#remove-a-comment)
- [Restore a Comment](https://docs.haravan.com/docs/omni-apis/comments/#restore-a-comment)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.