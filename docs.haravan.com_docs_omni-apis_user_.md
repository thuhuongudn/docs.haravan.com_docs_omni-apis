---
url: "https://docs.haravan.com/docs/omni-apis/user/"
title: "User | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/user/#)

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
- User

On this page

# User

`Version: 1.0`

The User resource is currently only available to Haravan Plus Customers.

**Authenticated access scopes**: `com.read_shop`

### What you can do with User [​](https://docs.haravan.com/docs/omni-apis/user/\#what-you-can-do-with-user "Direct link to heading")

The Haravan API lets you do the following with the User resource.

- GET `https://apis.haravan.com/com/users.json`
  - **[Retrieves a list of all users](https://docs.haravan.com/docs/omni-apis/user/#retrieves-a-list-of-all-users)**
- GET `https://apis.haravan.com/com/users/{user_id}.json`
  - **[Retrieves single the user](https://docs.haravan.com/docs/omni-apis/user/#retrieves-single-the-user)**
- GET `https://apis.haravan.com/com/users/groups.json`
  - **[Retrieves a list of all the group user](https://docs.haravan.com/docs/omni-apis/user/#retrieves-a-list-of-all-the-group-user)**

### Properties [​](https://docs.haravan.com/docs/omni-apis/user/\#properties "Direct link to heading")

* * *

`account_owner` : `bool`

```codeBlockLines_e6Vv
"account_owner": false

```

Identifies if the user is the owner of the Haravan account.

`bio` : `string`

```codeBlockLines_e6Vv
"bio": "A person on a mission"

```

User-specified description of oneself.

`email` : `string`

```codeBlockLines_e6Vv
"email": "joe@example.com"

```

The email address associated with this account.

`first_name` : `string`

```codeBlockLines_e6Vv
"first_name": "Joe"

```

The first name of the account user.

`id` : `number`

```codeBlockLines_e6Vv
"id":1234567890

```

The account id.

`im` : `string`

```codeBlockLines_e6Vv
"im" : "joe-chat@example.com"

```

The IM account address.

`last_name` : `string`

```codeBlockLines_e6Vv
"last_name": "Smith"

```

The last name of the account user.

`permissions` : `array`

```codeBlockLines_e6Vv
"permissions":["limited", "orders", "products"]

```

The permissions that the account has. Users will either have "full" or "limited" permissions. Limited permissions are scoped to a user in that they can only view certain parts of the Haravan Admin.
The types of permissions a limited user can have are as follows:

- **dashboard**: Can see Shop performance and statistics
- **orders**: Can view and modify orders
- **customers**: Can view and modify customers
- **marketing**: Can view and modify marketing related products such as discount codes
- **products**: Can view and modify products
- **gift\_cards**: Can view and modify gift cards
- **pages**: Can view and modify shop pages
- **links**: Can view and modify links and link lists
- **themes**: Can view and modify shop themes
- **applications**: Can authorize the installation of third-party applications
- **preferences**: Can view the preferences and configuration of a shop
- **reports**: Can view and create reports

### Endpoints [​](https://docs.haravan.com/docs/omni-apis/user/\#endpoints "Direct link to heading")

### Retrieves a list of all users [​](https://docs.haravan.com/docs/omni-apis/user/\#retrieves-a-list-of-all-users "Direct link to heading")

GET

https://apis.haravan.com/com/users.json

Retrieves a list of all users.

- GET `https://apis.haravan.com/com/users.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "users": [\
        {\
            "account_owner": false,\
            "bio": null,\
            "email": "tony.teo@yopmail.com",\
            "first_name": "Tèos",\
            "id": 200000665752,\
            "im": null,\
            "last_name": "Tony",\
            "phone": null,\
            "receive_announcements": 1,\
            "url": null,\
            "user_type": "invited",\
            "permissions": [\
                "Limit"\
            ]\
        }\
    ]
}

```

### Retrieves single the user [​](https://docs.haravan.com/docs/omni-apis/user/\#retrieves-single-the-user "Direct link to heading")

GET

https://apis.haravan.com/com/users/{user\_id}.json

Retrieves single the user.

- GET `https://apis.haravan.com/com/users/200000665752.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "user": {
        "account_owner": false,
        "bio": null,
        "email": "tony.teo@yopmail.com",
        "first_name": "Tèos",
        "id": 200000665752,
        "im": null,
        "last_name": "Tony",
        "phone": null,
        "receive_announcements": 1,
        "url": null,
        "user_type": "invited",
        "permissions": [\
            "Limit"\
        ]
    }
}

```

### Retrieves a list of all the group user [​](https://docs.haravan.com/docs/omni-apis/user/\#retrieves-a-list-of-all-the-group-user "Direct link to heading")

GET

https://apis.haravan.com/com/users/groups.json

Retrieves a list of all the group user.

- GET `https://apis.haravan.com/com/users/groups.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "user_groups": [\
        {\
            "id": 259160,\
            "name": "Danh sách nhân viên Địa điểm mặc định",\
            "type": "system",\
            "created_at": "2020-10-06T07:31:03.111Z",\
            "updated_at": "2020-10-06T07:31:03.111Z"\
        },\
        {\
            "id": 243586,\
            "name": "Địa điểm mặc định",\
            "type": "system",\
            "created_at": "2020-09-18T04:10:29.739Z",\
            "updated_at": "2020-09-18T04:10:29.739Z"\
        }\
    ]
}

```

[Previous\\
\\
Shop](https://docs.haravan.com/docs/omni-apis/shop/) [Next\\
\\
Ward](https://docs.haravan.com/docs/omni-apis/ward/)

- [What you can do with User](https://docs.haravan.com/docs/omni-apis/user/#what-you-can-do-with-user)
- [Properties](https://docs.haravan.com/docs/omni-apis/user/#properties)
- [Endpoints](https://docs.haravan.com/docs/omni-apis/user/#endpoints)
- [Retrieves a list of all users](https://docs.haravan.com/docs/omni-apis/user/#retrieves-a-list-of-all-users)
- [Retrieves single the user](https://docs.haravan.com/docs/omni-apis/user/#retrieves-single-the-user)
- [Retrieves a list of all the group user](https://docs.haravan.com/docs/omni-apis/user/#retrieves-a-list-of-all-the-group-user)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.