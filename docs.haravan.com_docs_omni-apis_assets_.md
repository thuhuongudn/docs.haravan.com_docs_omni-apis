---
url: "https://docs.haravan.com/docs/omni-apis/assets/"
title: "Asset | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/assets/#)

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
- Asset

On this page

# Asset

`Version: 1.0`

**Assets** are individual files that make up a shop's theme.

![omni-api-theme-asset](https://docs.haravan.com/assets/images/omni-api-theme-asset-559c75f78017448485e3184be2b6fdc6.png)

Assets can be any additional file; from images and stylesheets to extra snippets of code. Assets can be easily added, changed or removed from a shop's theme.

**Authenticated access scopes**: `web.read_themes`, `web.write_themes`

### What can you do with Asset? [​](https://docs.haravan.com/docs/omni-apis/assets/\#what-can-you-do-with-asset "Direct link to heading")

The haravan API lets you do the following with the Asset resource. More detailed versions of these general actions may be available:

- GET `https://apis.haravan.com/web/themes/{theme_id}/assets.json`
  - **[Receive a list of all Assets](https://docs.haravan.com/docs/omni-apis/assets/#receive-a-list-of-all-assets)**
- GET `https://apis.haravan.com/web/themes/{theme_id}/assets.json?asset[key]=templates/index.liquid`
  - **[Receive a single Asset](https://docs.haravan.com/docs/omni-apis/assets/#receive-a-single-asset)**
- PUT `https://apis.haravan.com/web/themes/{theme_id}/assets.json`
  - **[Creating or Modifying an Asset](https://docs.haravan.com/docs/omni-apis/assets/#creating-or-modifying-an-asset)**
- DELETE `https://apis.haravan.com/web/themes/{theme_id}/assets.json?asset[key]=assets/bg-body.gif`
  - **[Remove a Asset from the database](https://docs.haravan.com/docs/omni-apis/assets/#remove-a-asset-from-the-database)**

### Asset Properties [​](https://docs.haravan.com/docs/omni-apis/assets/\#asset-properties "Direct link to heading")

`attachment`: `string`

```codeBlockLines_e6Vv
"attachment": "R0lGODlhAQABAPABAPwAAACH5Ow=="

```

An asset attached to a store's theme.

`content_type`: `string`

```codeBlockLines_e6Vv
"content_type": "image/gif"

```

MIME representation of the content, consisting of the type and subtype of the asset.

`created_at`: `datetime`

```codeBlockLines_e6Vv
"created_at": "2010-07-12T15:31:50-04:00"

```

The date and time when the asset was created. The API returns this value in [ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601).

`key`: `string`

```codeBlockLines_e6Vv
"key": "assets/bg-body-green.gif"

```

The path to the asset within a shop. For example, the asset bg-body-green.gif is located in the assets folder.

`public_url`: `string`

```codeBlockLines_e6Vv
"public_url": "http://static.haravan.com/assets/bg.gif?1"

```

The public facing URL of the asset.

`size`: `int`

```codeBlockLines_e6Vv
"size": 1542

```

The asset size in bytes.

`source_key`: `string`

```codeBlockLines_e6Vv
"source_key": "layout/theme.liquid"

```

The source key copies an asset.

`src`: `string`

```codeBlockLines_e6Vv
"src": "http://apple.com/new_bg.gif"

```

Specifies the location of an asset.

`theme_id`: `number`

```codeBlockLines_e6Vv
"theme_id": 828155753

```

A unique numeric identifier for the theme.

`updated_at`: `datetime`

```codeBlockLines_e6Vv
"updated_at": "2010-07-12T15:31:50-04:00"

```

The date and time when an asset was last updated. The API returns this value in [ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601).

`value`: `string`

```codeBlockLines_e6Vv
"value": '<img src="backsoon-postit.png">'

```

The asset that you are adding.

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/assets/\#endpoints "Direct link to heading")

### Receive a list of all Assets [​](https://docs.haravan.com/docs/omni-apis/assets/\#receive-a-list-of-all-assets "Direct link to heading")

GET

https://apis.haravan.com/web/themes/{theme\_id}/assets.json

**Listing theme assets only returns metadata about each asset. You need to request assets individually in order to get their contents.**

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/assets/\#parameters "Direct link to heading")

* * *

`fields`

comma-separated list of fields to include in the response

* * *

**Get a list of all theme assets**

- GET `https://apis.haravan.com/web/themes/828155753/assets.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "assets": [\
    {\
      "key": "assets/bg-body-green.gif",\
      "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/bg-body-green.gif?12441496865301016029",\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "image/gif",\
      "size": 1542,\
      "theme_id": 828155753\
    },\
    {\
      "key": "assets/bg-body-orange.gif",\
      "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/bg-body-orange.gif?12441496865301016029",\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "image/gif",\
      "size": 1548,\
      "theme_id": 828155753\
    },\
    {\
      "key": "assets/bg-body-pink.gif",\
      "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/bg-body-pink.gif?12441496865301016029",\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "image/gif",\
      "size": 1562,\
      "theme_id": 828155753\
    },\
    {\
      "key": "assets/bg-body.gif",\
      "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/bg-body.gif?12441496865301016029",\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "image/gif",\
      "size": 1571,\
      "theme_id": 828155753\
    },\
    {\
      "key": "assets/bg-content.gif",\
      "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/bg-content.gif?12441496865301016029",\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "image/gif",\
      "size": 134,\
      "theme_id": 828155753\
    },\
    {\
      "key": "assets/bg-footer.gif",\
      "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/bg-footer.gif?12441496865301016029",\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "image/gif",\
      "size": 1434,\
      "theme_id": 828155753\
    },\
    {\
      "key": "assets/bg-main.gif",\
      "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/bg-main.gif?12441496865301016029",\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "image/gif",\
      "size": 297,\
      "theme_id": 828155753\
    },\
    {\
      "key": "assets/bg-sidebar.gif",\
      "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/bg-sidebar.gif?12441496865301016029",\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "image/gif",\
      "size": 124,\
      "theme_id": 828155753\
    },\
    {\
      "key": "assets/shop.css",\
      "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/shop.css?12441496865301016029",\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "text/css",\
      "size": 14058,\
      "theme_id": 828155753\
    },\
    {\
      "key": "assets/shop.css.liquid",\
      "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/shop.css.liquid?12441496865301016029",\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "text/x-liquid",\
      "size": 14675,\
      "theme_id": 828155753\
    },\
    {\
      "key": "assets/shop.js",\
      "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/shop.js?12441496865301016029",\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "application/javascript",\
      "size": 348,\
      "theme_id": 828155753\
    },\
    {\
      "key": "assets/sidebar-devider.gif",\
      "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/sidebar-devider.gif?12441496865301016029",\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "image/gif",\
      "size": 1016,\
      "theme_id": 828155753\
    },\
    {\
      "key": "assets/sidebar-menu.jpg",\
      "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/sidebar-menu.jpg?12441496865301016029",\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "image/jpeg",\
      "size": 1609,\
      "theme_id": 828155753\
    },\
    {\
      "key": "config/settings.html",\
      "public_url": null,\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "text/html",\
      "size": 4570,\
      "theme_id": 828155753\
    },\
    {\
      "key": "layout/theme.liquid",\
      "public_url": null,\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "text/x-liquid",\
      "size": 3252,\
      "theme_id": 828155753\
    },\
    {\
      "key": "templates/article.liquid",\
      "public_url": null,\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "text/x-liquid",\
      "size": 2486,\
      "theme_id": 828155753\
    },\
    {\
      "key": "templates/blog.liquid",\
      "public_url": null,\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "text/x-liquid",\
      "size": 786,\
      "theme_id": 828155753\
    },\
    {\
      "key": "templates/cart.liquid",\
      "public_url": null,\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "text/x-liquid",\
      "size": 2047,\
      "theme_id": 828155753\
    },\
    {\
      "key": "templates/collection.liquid",\
      "public_url": null,\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "text/x-liquid",\
      "size": 946,\
      "theme_id": 828155753\
    },\
    {\
      "key": "templates/index.liquid",\
      "public_url": null,\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "text/x-liquid",\
      "size": 1068,\
      "theme_id": 828155753\
    },\
    {\
      "key": "templates/page.liquid",\
      "public_url": null,\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "text/x-liquid",\
      "size": 147,\
      "theme_id": 828155753\
    },\
    {\
      "key": "templates/product.liquid",\
      "public_url": null,\
      "created_at": "2010-07-12T15:31:50-04:00",\
      "updated_at": "2010-07-12T15:31:50-04:00",\
      "content_type": "text/x-liquid",\
      "size": 2796,\
      "theme_id": 828155753\
    }\
  ]
}

```

### Receive a single Asset [​](https://docs.haravan.com/docs/omni-apis/assets/\#receive-a-single-asset "Direct link to heading")

GET

https://apis.haravan.com/web/themes/{theme\_id}/assets.json?asset\[key\]=templates/index.liquid

There are different buckets which hold different kinds of assets, each corresponding to one of the folders within a theme's zip file: **layout, templates**, and **assets**. The full key of an asset always starts with the bucket name, and the path separator is a forward slash, like **layout/theme.liquid** or **assets/bg-body.gif**.

#### Parameters [​](https://docs.haravan.com/docs/omni-apis/assets/\#parameters-1 "Direct link to heading")

* * *

`fields`

comma-separated list of fields to include in the response

* * *

**Get a liquid template**

- GET `https://apis.haravan.com/web/themes/828155753/assets.json?asset[key]=templates/index.liquid`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "asset": {
    "key": "templates/index.liquid",
    "public_url": null,
    "value": "<!-- LIST 3 PER ROW -->\n<h2>Featured Products</h2>\n<table id=\"products\" cellspacing=\"0\" cellpadding=\"0\">\n\n</table>\n<!-- /LIST 3 PER ROW  -->\n\n  <div id=\"articles\">\n  \t\n\n    <div class=\"article\">\n    \n      <div class=\"article-body textile\">\n  \t  In <em>Admin > Blogs & Pages</em>, create a page with the handle <strong><code>frontpage</code></strong> and it will show up here.<br />\n  \t  \n      </div>\n  \t\n    </div>\n\n  </div>\n\n",
    "created_at": "2010-07-12T15:31:50-04:00",
    "updated_at": "2010-07-12T15:31:50-04:00",
    "content_type": "text/x-liquid",
    "size": 1068,
    "theme_id": 828155753
  }
}

```

**Get a theme image**

- GET `https://apis.haravan.com/web/themes/828155753/assets.json?asset[key]=assets/bg-body.gif`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "asset": {
    "key": "assets/bg-body.gif",
    "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/bg-body.gif?12339842436141157369",
    "attachment": "R0lGODlhBgCTAPcAAIzH6Xu423y53IO/4pXP8CAgIJPN75HM7X263YvG6Hq3\n2nq325XP8X+835LM7pDL7YTA45TO8I3I6pLN7oG+4IfD5ZPO75DK7I7J64K+\n4YC94IbC5ITA4onF54rF54C834jD5o/K7JDL7JHM7nq424XB45TP8JXQ8YC9\n34jE5onE5pTO74K/4ZbQ8n+73u7u7iQkJDU1NYrF6FpaWsvLy+Xl5VNTU47K\n63y63YnE51dXVzw8PEJCQk5OTkhISITB49TU1CkpKS8vL5HL7X263JXQ8IG+\n4X+83o/J64XB5Hy43Hy63IbB5IfD5obC5YvH6ZPN7n673Xu43IjD5Y/K64fC\n5IPA4pbR8o3J6oG94Hu53Hu323273Xq42orG6IfC5X663ZfQ8pLN73663nu5\n25fQ8ZPO8IzI6ovF6Hy53YvH6I7I6o7J6nm32ny524O/4Y3H6pbR8YzI6X+7\n34XC45fR8oPA44G934fD5H253Y3I63y424K+4Hm42o3I6X273ozG6Y7I64C8\n4IzH6oC734O/45bQ8JLO7pHL7oS/4obD5X253InF5pTP8YK94H6735XO8JDK\n7ZTN8JbP8Hm324jE54/L7IXA44TB5JLM7YO+4YnG54zG6I7J7Hu32oK94YK/\n4n673pbQ8QAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\nAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\nAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\nAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\nAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\nAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\nAAAAAAAAAAAAAAAAAAAAACH5BAAAAAAALAAAAAAGAJMAAAj+AMvUaXGlThiC\nLeKEEZUwTJgrokSVaSERIsOIGDNSjHgiIoOMogyd6HiCAYMiJk8UKTnJZBEC\nK2GaJNCIgE0GERiYILAzAgFINk1EMCE0gk8CRomuWFHUzIoISw2skGrAjAUL\nkqxaMADlqoGtBsJe3QplwiExEwyg5VoWrYMJb+PChevAwQi7I0Yc0HvArgNE\nIzLtPTDkgGHCBx4QfsD4wRARiocwliwC8gXIlSNZuhxCRIgLny+IBh06BBUq\nSEIg6XTj9A0kr0NgeH0Dg+3ZbGyzCWQ7EBssGLBgWSNBjx4sEpKvIZ68uQQ/\nfs7IgSPnzCAA1gFo1w5nu3dA25/+POEE6EkCAGrMJ0igXs16L+7Xy0CDxgsa\nGV4S4Pcgo7+H/x5s0oEHA3aQA4E55NDBggumkKAKOahQiQqMpKDChSmAoEKG\nIICQQoYpTAFCBU2QOEWJTYAgYolTVPBFBYpUIOMXVVRRQRV4bPCFE058gYcT\nG2zAYxVBFrkBE0gmUQITJSTBRBJ00FHCD01WCUEJmFwyJQQ/QOAllxBwwCUH\ndtjxg5hhQmAFB2wWksiaHFgxgJwD1PnGACwMcGedA4DCgiZvsJAnnhmwkEGh\nGVBwqBF8ZGDEoRnwQYERlFLgCAUUZPEJphpkgSkFGtyRRRYaaIBCqafegQIK\nH5z6gQb+HwiyaqwfNNBArR/UaqutRzTgAiG2uiDsHMI+ckQox86B7LGhNOts\nKFFAK+0YoXARyhjU/gFGKGAgwAUYYHCBQBR/iIvAuecSsQQRRCCAQx44LIED\nETicK4C8eaSBgAD03rvIvWmkIcDABGvhhgBaDKyEGwEkrIQWSkjBsBJkkBGA\nFEoEsMceAQRgsRQkSBEACR13TPICWwSwxckoK9DxAguQEDPKMC/gCQkKLNBF\nzgq00UcXXfisgAI470xJz0MrUMDSTM/g9NM6RC21DVRX3cPVWPug9dY8dO31\nDmCHHcPYZAth9tlBpK02DGy3zTTTNMQtNxB0113D3Xi/oPcD3gEBADs=\n",
    "created_at": "2010-07-12T15:31:50-04:00",
    "updated_at": "2010-07-12T15:31:50-04:00",
    "content_type": "image/gif",
    "size": 1571,
    "theme_id": 828155753
  }
}

```

### Creating or Modifying an Asset [​](https://docs.haravan.com/docs/omni-apis/assets/\#creating-or-modifying-an-asset "Direct link to heading")

PUT

https://apis.haravan.com/web/themes/{theme\_id}/assets.json

**PUT takes care of both creating new assets and updating existing ones**

**Change an existing liquid template's value**

- PUT `https://apis.haravan.com/web/themes/828155753/assets.json`

```codeBlockLines_e6Vv
{
  "asset": {
    "key": "templates/index.liquid",
    "value": "<img src='backsoon-postit.png'><p>We are busy updating the store for you and will be back within the hour.</p>"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "asset": {
    "key": "templates/index.liquid",
    "public_url": null,
    "created_at": "2010-07-12T15:31:50-04:00",
    "updated_at": "2015-03-28T13:26:53-04:00",
    "content_type": "text/x-liquid",
    "size": 110,
    "theme_id": 828155753
  }
}

```

**Create a new image by providing a base64-encoded attachment**

- PUT `https://apis.haravan.com/web/themes/828155753/assets.json`

```codeBlockLines_e6Vv
{
  "asset": {
    "key": "assets/empty.gif",
    "attachment": "R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==\n"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "asset": {
    "key": "assets/empty.gif",
    "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/empty.gif?4403551604110394662",
    "created_at": "2015-03-28T13:26:53-04:00",
    "updated_at": "2015-03-28T13:26:53-04:00",
    "content_type": "image/gif",
    "size": 43,
    "theme_id": 828155753
  }
}

```

**Update an image by providing a source URL from which to fetch the value**

- PUT `https://apis.haravan.com/web/themes/828155753/assets.json`

```codeBlockLines_e6Vv
{
  "asset": {
    "key": "assets/bg-body.gif",
    "src": "http://apple.com/new_bg.gif"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "asset": {
    "key": "assets/bg-body.gif",
    "public_url": "https://cdn.haravan.com/s/files/1/0006/9093/3842/t/1/assets/bg-body.gif?3530484542103056718",
    "created_at": "2010-07-12T15:31:50-04:00",
    "updated_at": "2015-03-28T13:26:54-04:00",
    "content_type": "image/gif",
    "size": 43,
    "theme_id": 828155753
  }
}

```

**Copy an asset by providing a source key**

- PUT `https://apis.haravan.com/web/themes/828155753/assets.json`

```codeBlockLines_e6Vv
{
  "asset": {
    "key": "layout/alternate.liquid",
    "source_key": "layout/theme.liquid"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "asset": {
    "key": "layout/alternate.liquid",
    "public_url": null,
    "created_at": "2015-03-28T13:26:54-04:00",
    "updated_at": "2015-03-28T13:26:54-04:00",
    "content_type": "text/x-liquid",
    "size": 3174,
    "theme_id": 828155753
  }
}

```

### Remove a Asset from the database [​](https://docs.haravan.com/docs/omni-apis/assets/\#remove-a-asset-from-the-database "Direct link to heading")

DELETE

https://apis.haravan.com/web/themes/{theme\_id}/assets.json?asset\[key\]=assets/bg-body.gif

**Remove assets from your shop**

**Delete an image from your theme**

- DELETE `https://apis.haravan.com/web/themes/828155753/assets.json?asset[key]=assets/bg-body.gif`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{}

```

**There are some files you cannot delete**

- DELETE `https://apis.haravan.com/web/themes/828155753/assets.json?asset[key]=layout/theme.liquid`

Details

```codeBlockLines_e6Vv
HTTP/1.1 403 Forbidden
{}

```

[Previous\\
\\
Article](https://docs.haravan.com/docs/omni-apis/articles/) [Next\\
\\
Blog](https://docs.haravan.com/docs/omni-apis/blogs/)

- [What can you do with Asset?](https://docs.haravan.com/docs/omni-apis/assets/#what-can-you-do-with-asset)
- [Asset Properties](https://docs.haravan.com/docs/omni-apis/assets/#asset-properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/assets/#endpoints)
- [Receive a list of all Assets](https://docs.haravan.com/docs/omni-apis/assets/#receive-a-list-of-all-assets)
- [Receive a single Asset](https://docs.haravan.com/docs/omni-apis/assets/#receive-a-single-asset)
- [Creating or Modifying an Asset](https://docs.haravan.com/docs/omni-apis/assets/#creating-or-modifying-an-asset)
- [Remove a Asset from the database](https://docs.haravan.com/docs/omni-apis/assets/#remove-a-asset-from-the-database)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.