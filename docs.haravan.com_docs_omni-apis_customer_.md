---
url: "https://docs.haravan.com/docs/omni-apis/customer/"
title: "Customer | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/customer/#)

[![Haravan Platform](https://docs.haravan.com/img/logo-haravan.svg)](https://docs.haravan.com/)[Get Started](https://docs.haravan.com/docs/get-started/overview/) [Tutorials](https://docs.haravan.com/docs/tutorials/authentication/apps-overview/) [Haravan APIs](https://docs.haravan.com/docs/omni-apis/) [Themes](https://docs.haravan.com/docs/themes/) [Partners](https://docs.haravan.com/docs/partners/)

[Sign In](https://partners.haravan.com/) [Sign Up](https://partners.haravan.com/signup)

Search...

- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)

  - [AccessScope](https://docs.haravan.com/docs/omni-apis/access-scopes/)
  - [API Rate Limits](https://docs.haravan.com/docs/omni-apis/api-call-limit/)
  - [Customers](https://docs.haravan.com/docs/omni-apis/customer/)

    - [Customer](https://docs.haravan.com/docs/omni-apis/customer/)
    - [Customer Address](https://docs.haravan.com/docs/omni-apis/customer-address/)
  - [Discounts](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/)

  - [Events](https://docs.haravan.com/docs/omni-apis/event/)
  - [Inventory](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/)

  - [Metafield](https://docs.haravan.com/docs/omni-apis/metafield/)
  - [Online store](https://docs.haravan.com/docs/omni-apis/articles/)

  - [Orders](https://docs.haravan.com/docs/omni-apis/orders/)

  - [Products](https://docs.haravan.com/docs/omni-apis/collects/)

  - [Shipping](https://docs.haravan.com/docs/omni-apis/shipping-rates/)

  - [Store properties](https://docs.haravan.com/docs/omni-apis/country/)

  - [Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [Home page](https://docs.haravan.com/)
- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)
- Customers

On this page

# Customer

`Version: 1.0`

The Customer resource stores information about a shop's customers, such as their contact details, their order history, and whether they've agreed to receive email marketing.

![customer-1](<Base64-Image-Removed>)

The Customer resource also holds information on the status of a customer's account. Customers with accounts save time at checkout when they're logged in because they don't need to enter their contact information. You can use the Customer API to check whether a customer has an active account, and then invite them to create one if they don't.

In a shop's checkout settings, there are three options for customer accounts:

- **Accounts are disabled**: Customers can't create accounts and can check out only as guests.
- **Accounts are optional**: Customers have the choice of either signing into their account or checking out as a guest. Customers can create accounts for themselves, and the shop owner can create an account for a customer and then invite them by email to use it.
- **Accounts are required**: Customers can't check out unless they're logged in, and the shop owner must create their accounts.

**Authenticated access scopes**: `com.read_customers`, `com.write_customers`

### What you can do with Customer [​](https://docs.haravan.com/docs/omni-apis/customer/\#what-you-can-do-with-customer "Direct link to heading")

The Haravan API lets you do the following with the Customer resource.

- GET `https://apis.haravan.com/com/customers.json`
  - **[Retrieves a list of customers.](https://docs.haravan.com/docs/omni-apis/customer/#retrieves-a-list-of-customers)**
- GET `https://apis.haravan.com/com/customers/search.json`
  - **[Searches for customers that match a supplied query.](https://docs.haravan.com/docs/omni-apis/customer/#searches-for-customers-that-match-a-supplied-query)**
- GET `https://apis.haravan.com/com/customers/count.json`
  - **[Retrieves a count of customers.](https://docs.haravan.com/docs/omni-apis/customer/#retrieves-a-count-of-customers)**
- GET `https://apis.haravan.com/com/customers/{customer_id}.json`
  - **[Retrieves detail of a customer.](https://docs.haravan.com/docs/omni-apis/customer/#retrieves-detail-of-a-customer)**
- POST `https://apis.haravan.com/com/customers.json`
  - **[Create a customer.](https://docs.haravan.com/docs/omni-apis/customer/#create-a-customer)**
- PUT `https://apis.haravan.com/com/customers/{customer_id}.json`
  - **[Update a customer.](https://docs.haravan.com/docs/omni-apis/customer/#update-a-customer)**
- DELETE `https://apis.haravan.com/com/customers/{customer_id}.json`
  - **[Delete a customer.](https://docs.haravan.com/docs/omni-apis/customer/#delete-a-customer)**
- POST `https://apis.haravan.com/com/customers/{customer_id}/tags.json`
  - **[Add customer tags.](https://docs.haravan.com/docs/omni-apis/customer/#add-customer-tags)**
- DELETE `https://apis.haravan.com/com/customers/{customer_id}/tags.json`
  - **[Delete customer tags.](https://docs.haravan.com/docs/omni-apis/customer/#delete-customer-tags)**
- GET `https://apis.haravan.com/com/customers/groups.json`
  - **[Retrieves a list of all customer groups.](https://docs.haravan.com/docs/omni-apis/customer/#retrieves-a-list-of-all-customer-groups)**

### Customer properties [​](https://docs.haravan.com/docs/omni-apis/customer/\#customer-properties "Direct link to heading")

* * *

`accepts_marketing` : `boolean`

```codeBlockLines_e6Vv
"accepts_marketing":  false

```

Whether the customer has consented to receive marketing material via email.

`addresses` : `json`

A list of the ten most recently updated addresses for the customer.

Each address has the following properties:

Details

- **address1**: The customer's mailing address.
- **address2**: An additional field for the customer's mailing address.
- **city**: The customer's city, town, or village.
- **company**: The customer's company.
- **country**: The customer's country.
- **country\_code**: The two-letter country code corresponding to the customer's country.
- **country\_name**: The customer's normalized country name.
- **customer\_id**: A unique identifier for the customer.
- **default**: Whether this address is the default address for the customer.
- **first\_name**: The customer's first name.
- **id**: A unique identifier for the address.
- **last\_name**: The customer's last name.
- **name**: The customer's first and last names.
- **phone**: The customer's phone number at this address.
- **province**: The customer's region name. Typically a province, a state, or a prefecture.
- **province\_code**: The two-letter province code for the customer's region.
- **zip**: The customer's postal code, also known as zip, postcode, Eircode, etc.

`created_at` : `string`

```codeBlockLines_e6Vv
"created_at": 2021-05-13T07:29:20.1Z

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format) when the customer was created.

`default_address` : `json`

The default address for the customer.

The default address has the following properties:

Details

- **address1**: The customer's mailing address.
- **address2**: An additional field for the customer's mailing address.
- **city**: The customer's city, town, or village.
- **company**: The customer's company.
- **country**: The customer's country.
- **country\_code**: The two-letter country code corresponding to the customer's country.
- **country\_name**: The customer's normalized country name.
- **customer\_id**: A unique identifier for the customer.
- **default**: Whether this address is the default address for the customer.
- **first\_name**: The customer's first name.
- **id**: A unique identifier for the address.
- **last\_name**: The customer's last name.
- **name**: The customer's first and last names.
- **phone**: The customer's phone number at this address.
- **province**: The customer's region name. Typically a province, a state, or a prefecture.
- **province\_code**: The two-letter province code for the customer's region.
- **zip**: The customer's postal code, also known as zip, postcode, Eircode, etc.

`email` : `string`

```codeBlockLines_e6Vv
"email": "bob.norman@hostmail.com"

```

The unique email address of the customer. Attempting to assign the same email address to multiple customers returns an error.

`first_name` : `string`

```codeBlockLines_e6Vv
"first_name": "John"

```

The customer's first name.

`id` : `number`

```codeBlockLines_e6Vv
"id": 1042784950

```

A unique identifier for the customer.

`last_name` : `string`

```codeBlockLines_e6Vv
"last_name": "Norman"

```

The customer's last name.

`last_order_id` : `number`

```codeBlockLines_e6Vv
"last_order_id":  234132602919

```

The ID of the customer's last order.

`last_order_name` : `string`

```codeBlockLines_e6Vv
"last_order_name": "#2111"

```

The name of the customer's last order. This is directly related to the name field on the Order resource.

`published` : `boolean`

```codeBlockLines_e6Vv
"published": true

```

States whether the custom collection is visible. Valid values are "true" for visible and "false" for hidden.

`multipass_identifier` : `boolean`

```codeBlockLines_e6Vv
"multipass_identifier": false

```

A unique identifier for the customer that's used with ' 'Multipass login.

`note` : `string`

```codeBlockLines_e6Vv
"note": "VIP"

```

A note about the customer.

`orders_count` : `number`

```codeBlockLines_e6Vv
"orders_count": 4

```

The number of orders associated with this customer.

`phone` : `string`

```codeBlockLines_e6Vv
"phone": "0333333333"

```

The unique phone number for this customer. Attempting to assign the same phone number to multiple customers returns an error. The property can be set using different formats, but each format must represent a number that can be dialed from anywhere in the world.

`state` : `string`

```codeBlockLines_e6Vv
"state": "disabled"

```

The state of the customer's account with a shop. The state can be changed in the Haravan admin or by the customer, but not through the API. Default value: disabled.

Valid values:

- **disabled**: The customer doesn't have an active account. Customer accounts can be disabled from the Haravan admin at any time.
- **invited**: The customer has received an emailed invite to create an account.
- **enabled**: The customer has created an account.
- **declined**: The customer declined the email invite to create an account.

`orders_count` : `number`

```codeBlockLines_e6Vv
"orders_count": 4

```

The number of orders associated with this customer.

`phone` : `string`

```codeBlockLines_e6Vv
"phone": "0333333333"

```

The unique phone number for this customer. Attempting to assign the same phone number to multiple customers returns an error. The property can be set using different formats, but each format must represent a number that can be dialed from anywhere in the world.

`tags` : `string`

```codeBlockLines_e6Vv
"tags": "loyal"

```

Tags that the shop owner has attached to the customer, formatted as a string of comma-separated values.

`total_spent` : `number`

```codeBlockLines_e6Vv
"total_spent": 0.0000

```

The total amount of money that the customer has spent across their order history.

`updated_at` : `string`

```codeBlockLines_e6Vv
"updated_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format) when the customer was updated.

`verified_email` : `boolean`

```codeBlockLines_e6Vv
"verified_email": true

```

Whether the customer has verified their email address.

`birthday` : `string`

```codeBlockLines_e6Vv
"birthday": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format) when the customer was born. Default value: null when empty info.

`gender` : `number`

```codeBlockLines_e6Vv
"gender": null

```

Gender of the customer.

Default value: null.

Valid values:

- **null**: Empty info.
- **1**: The customer is male.
- **0**: The customer is female.

`last_order_date` : `string`

```codeBlockLines_e6Vv
"last_order_date": "2021-05-13T07:29:20.1Z"

```

The last time the customer made a purchase ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format). Default value: null.

### Retrieves a list of customers. [​](https://docs.haravan.com/docs/omni-apis/customer/\#retrieves-a-list-of-customers "Direct link to heading")

GET

https://apis.haravan.com/com/customers.json

* * *

`ids`

Restrict results to customers specified by a comma-separated list of IDs.

* * *

`since_id`

Restrict results to after the specified ID.

* * *

`created_at_min`

Show customers created after a specified date. (format: 2014-04-25T16:15:47-04:00).

* * *

`created_at_max`

Show customers created before a specified date. (format: 2014-04-25T16:15:47-04:00).

* * *

`updated_at_min`

Show customers last updated after a specified date. (format: 2014-04-25T16:15:47-04:00).

* * *

`updated_at_max`

Show customers last updated before a specified date. (format: 2014-04-25T16:15:47-04:00).

* * *

`limit`

Limit of the result.

* * *

`page`

Page to show the result.

* * *

`fields`

Comma-separated list of fields to include in the response.

* * *

Retrieve all custom collections by page number. By default, the number of resources on the page is 50.

- GET `https://apis.haravan.com/com/customers.json?page=1&limit=1`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "customers": [\
        {\
            "accepts_marketing": false,\
            "addresses": [\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1058135354,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": "70000",\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                }\
            ],\
            "created_at": "2020-10-22T03:37:03.796Z",\
            "default_address": {\
                "address1": "182 Lê Đại Hành",\
                "address2": null,\
                "city": null,\
                "company": null,\
                "country": "Vietnam",\
                "first_name": "Haravan Demo",\
                "id": 1058135354,\
                "last_name": null,\
                "phone": null,\
                "province": "Hồ Chí Minh",\
                "zip": "70000",\
                "name": " Haravan Demo",\
                "province_code": "HC",\
                "country_code": "vn",\
                "default": true,\
                "district": "Quận 11",\
                "district_code": "HC476",\
                "ward": "Phường 15",\
                "ward_code": "27208"\
            },\
            "email": "hello@haravan.com",\
            "phone": null,\
            "first_name": "Haravan Demo",\
            "id": 1037889951,\
            "multipass_identifier": null,\
            "last_name": null,\
            "last_order_id": 1146065300,\
            "last_order_name": "#100027",\
            "note": null,\
            "orders_count": 28,\
            "state": "Disabled",\
            "tags": null,\
            "total_spent": 261380000.0000,\
            "total_paid": 0.0,\
            "updated_at": "2020-10-22T03:37:09Z",\
            "verified_email": false,\
            "group_name": null,\
            "birthday": null,\
            "gender": null,\
            "last_order_date": "2020-10-23T07:37:04Z"\
        }\
    ]
}

```

Retrieve all customer changes after a certain date.

- GET `https://apis.haravan.com/com/customers.json?updated_at_max=2020-10-23`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "customers": [\
        {\
            "accepts_marketing": false,\
            "addresses": [\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1058135354,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": "70000",\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                }\
            ],\
            "created_at": "2020-10-22T03:37:03.796Z",\
            "default_address": {\
                "address1": "182 Lê Đại Hành",\
                "address2": null,\
                "city": null,\
                "company": null,\
                "country": "Vietnam",\
                "first_name": "Haravan Demo",\
                "id": 1058135354,\
                "last_name": null,\
                "phone": null,\
                "province": "Hồ Chí Minh",\
                "zip": "70000",\
                "name": " Haravan Demo",\
                "province_code": "HC",\
                "country_code": "vn",\
                "default": true,\
                "district": "Quận 11",\
                "district_code": "HC476",\
                "ward": "Phường 15",\
                "ward_code": "27208"\
            },\
            "email": "hello@haravan.com",\
            "phone": null,\
            "first_name": "Haravan Demo",\
            "id": 1037889951,\
            "multipass_identifier": null,\
            "last_name": null,\
            "last_order_id": 1146065300,\
            "last_order_name": "#100027",\
            "note": null,\
            "orders_count": 28,\
            "state": "Disabled",\
            "tags": null,\
            "total_spent": 261380000.0000,\
            "total_paid": 0.0,\
            "updated_at": "2020-10-22T03:37:09Z",\
            "verified_email": false,\
            "group_name": null,\
            "birthday": null,\
            "gender": null,\
            "last_order_date": "2020-10-23T07:37:04Z"\
        }\
    ]
}

```

### Searches for customers that match a supplied query. [​](https://docs.haravan.com/docs/omni-apis/customer/\#searches-for-customers-that-match-a-supplied-query "Direct link to heading")

GET

https://apis.haravan.com/com/customers/search.json

* * *

`order`

Set the field and direction by which to order results. (default: last\_order\_date DESC).

* * *

`query`

Text to search for in the shop's customer data.

* * *

`created_at_min`

Show customers created after a specified date. (format: 2014-04-25T16:15:47-04:00).

* * *

`limit`

Limit of the result.

* * *

`page`

Page to show the result.

* * *

`fields`

Comma-separated list of fields to include in the response.

* * *

Retrieve all customers with the name "Haravan".

- GET `https://apis.haravan.com/com/customers/search.json?query=haravan`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "customers": [\
        {\
            "accepts_marketing": false,\
            "addresses": [\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1058135354,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": "70000",\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                }\
            ],\
            "created_at": "2020-10-22T03:37:03.796Z",\
            "default_address": {\
                "address1": "182 Lê Đại Hành",\
                "address2": null,\
                "city": null,\
                "company": null,\
                "country": "Vietnam",\
                "first_name": "Haravan Demo",\
                "id": 1058135354,\
                "last_name": null,\
                "phone": null,\
                "province": "Hồ Chí Minh",\
                "zip": "70000",\
                "name": " Haravan Demo",\
                "province_code": "HC",\
                "country_code": "vn",\
                "default": true,\
                "district": "Quận 11",\
                "district_code": "HC476",\
                "ward": "Phường 15",\
                "ward_code": "27208"\
            },\
            "email": "hello@haravan.com",\
            "phone": null,\
            "first_name": "Haravan Demo",\
            "id": 1037889951,\
            "multipass_identifier": null,\
            "last_name": null,\
            "last_order_id": 1146065300,\
            "last_order_name": "#100027",\
            "note": null,\
            "orders_count": 28,\
            "state": "Disabled",\
            "tags": null,\
            "total_spent": 261380000.0000,\
            "total_paid": 0.0,\
            "updated_at": "2020-10-22T03:37:09Z",\
            "verified_email": false,\
            "group_name": null,\
            "birthday": null,\
            "gender": null,\
            "last_order_date": "2020-10-23T07:37:04Z"\
        }\
    ]
}

```

### Retrieves a count of customers. [​](https://docs.haravan.com/docs/omni-apis/customer/\#retrieves-a-count-of-customers "Direct link to heading")

GET

https://apis.haravan.com/com/customers/count.json

Count all customers for your shop.

- GET `https://apis.haravan.com/com/customers/count.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

```

### Retrieves detail of a customer. [​](https://docs.haravan.com/docs/omni-apis/customer/\#retrieves-detail-of-a-customer "Direct link to heading")

GET

https://apis.haravan.com/com/customers/{customer\_id}.json

Retrieves detail a customer with id.

- GET `https://apis.haravan.com/com/customers/1037889951.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK

{
    "customer":
        {
            "accepts_marketing": false,
            "addresses": [\
                {\
                    "address1": "182 Lê Đại Hành",\
                    "address2": null,\
                    "city": null,\
                    "company": null,\
                    "country": "Vietnam",\
                    "first_name": "Haravan Demo",\
                    "id": 1058135354,\
                    "last_name": null,\
                    "phone": null,\
                    "province": "Hồ Chí Minh",\
                    "zip": "70000",\
                    "name": " Haravan Demo",\
                    "province_code": "HC",\
                    "country_code": "vn",\
                    "default": true,\
                    "district": "Quận 11",\
                    "district_code": "HC476",\
                    "ward": "Phường 15",\
                    "ward_code": "27208"\
                }\
            ],
            "created_at": "2020-10-22T03:37:03.796Z",
            "default_address": {
                "address1": "182 Lê Đại Hành",
                "address2": null,
                "city": null,
                "company": null,
                "country": "Vietnam",
                "first_name": "Haravan Demo",
                "id": 1058135354,
                "last_name": null,
                "phone": null,
                "province": "Hồ Chí Minh",
                "zip": "70000",
                "name": " Haravan Demo",
                "province_code": "HC",
                "country_code": "vn",
                "default": true,
                "district": "Quận 11",
                "district_code": "HC476",
                "ward": "Phường 15",
                "ward_code": "27208"
            },
            "email": "hello@haravan.com",
            "phone": null,
            "first_name": "Haravan Demo",
            "id": 1037889951,
            "multipass_identifier": null,
            "last_name": null,
            "last_order_id": 1146065300,
            "last_order_name": "#100027",
            "note": null,
            "orders_count": 28,
            "state": "Disabled",
            "tags": null,
            "total_spent": 261380000.0000,
            "total_paid": 0.0,
            "updated_at": "2020-10-22T03:37:09Z",
            "verified_email": false,
            "group_name": null,
            "birthday": null,
            "gender": null,
            "last_order_date": "2020-10-23T07:37:04Z"
        }
}

```

### Create a customer. [​](https://docs.haravan.com/docs/omni-apis/customer/\#create-a-customer "Direct link to heading")

POST

https://apis.haravan.com/com/customers.json

Create a customer.

- POST `https://apis.haravan.com/com/customers.json`

```codeBlockLines_e6Vv
{
    "customer": {
        "first_name": "Steve",
        "last_name": "Lastnameson",
        "email": "steve.lastnameson@example.com",
        "phone": "05142546011",
        "verified_email": true
    }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created

{
    "customer": {
        "accepts_marketing": false,
        "addresses": [],
        "created_at": "2021-08-18T05:58:03.3618601Z",
        "default_address": null,
        "email": "steve.lastnameson@example.com",
        "phone": "05142546011",
        "first_name": "Steve",
        "id": 1050763804,
        "multipass_identifier": null,
        "last_name": "Lastnameson",
        "last_order_id": null,
        "last_order_name": null,
        "note": null,
        "orders_count": 0,
        "state": "Enabled",
        "tags": null,
        "total_spent": 0.0,
        "total_paid": 0.0,
        "updated_at": "2021-08-18T05:58:03.3618709Z",
        "verified_email": false,
        "group_name": null,
        "birthday": null,
        "gender": null,
        "last_order_date": null
    }
}

```

Create a customer with send\_email\_invite.

- POST `https://apis.haravan.com/com/customers.json`

```codeBlockLines_e6Vv
{
    "customer": {
        "first_name": "Steve",
        "last_name": "Lastnameson",
        "email": "steve.lastnameson@example.com",
        "phone": "05142546011",
        "verified_email": true,
        "send_email_invite": true
    }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
    "customer": {
        "accepts_marketing": false,
        "addresses": [],
        "created_at": "2021-08-18T05:58:03.3618601Z",
        "default_address": null,
        "email": "steve.lastnameson@example.com",
        "phone": "05142546011",
        "first_name": "Steve",
        "id": 1050763804,
        "multipass_identifier": null,
        "last_name": "Lastnameson",
        "last_order_id": null,
        "last_order_name": null,
        "note": null,
        "orders_count": 0,
        "state": "Enabled",
        "tags": null,
        "total_spent": 0.0,
        "total_paid": 0.0,
        "updated_at": "2021-08-18T05:58:03.3618709Z",
        "verified_email": false,
        "group_name": null,
        "birthday": null,
        "gender": null,
        "last_order_date": null
    }
}

```

Create a customer with password and password\_confirmation and skip sending the welcome email.

- POST `https://apis.haravan.com/com/customers.json`

```codeBlockLines_e6Vv
{
    "customer": {
        "first_name": "Steve",
        "last_name": "Lastnameson",
        "email": "steve.lastnameson@example.com",
        "phone": "05142546011",
        "verified_email": true,
        "password": "newpass",
        "password_confirmation": "newpass",
        "send_email_welcome": false
    }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
    "customer": {
        "accepts_marketing": false,
        "addresses": [],
        "created_at": "2021-08-18T05:58:03.3618601Z",
        "default_address": null,
        "email": "steve.lastnameson@example.com",
        "phone": "05142546011",
        "first_name": "Steve",
        "id": 1050763804,
        "multipass_identifier": null,
        "last_name": "Lastnameson",
        "last_order_id": null,
        "last_order_name": null,
        "note": null,
        "orders_count": 0,
        "state": "Enabled",
        "tags": null,
        "total_spent": 0.0,
        "total_paid": 0.0,
        "updated_at": "2021-08-18T05:58:03.3618709Z",
        "verified_email": false,
        "group_name": null,
        "birthday": null,
        "gender": null,
        "last_order_date": null
    }
}

```

Create a customer with the address.

- POST `https://apis.haravan.com/com/customers.json`

```codeBlockLines_e6Vv
{
    "customer": {
        "first_name": "New",
        "last_name": "Haravan",
        "email": "new.haravan@example.com",
        "phone": "04142546011",
        "verified_email": true,
        "password": "newpass",
        "password_confirmation": "newpass",
        "send_email_welcome": false,
        "addresses":[\
            {\
                    "country": "Vietnam",\
                    "first_name": "New",\
                    "last_name": "Haravan",\
                    "zip": "70000",\
                    "address1":"182 Lê Đại Hành",\
                    "country_code": "vn",\
                    "province_code": "HC",\
                    "district_code": "HC476",\
                    "ward_code": "27208"\
                }\
        ]
    }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
    "customer": {
        "accepts_marketing": false,
        "addresses": [\
            {\
                "address1": "182 Lê Đại Hành",\
                "address2": null,\
                "city": null,\
                "company": null,\
                "country": "Vietnam",\
                "first_name": "New",\
                "id": 1084464836,\
                "last_name": "Haravan",\
                "phone": null,\
                "province": "Hồ Chí Minh",\
                "zip": "70000",\
                "name": "Haravan New",\
                "province_code": "HC",\
                "country_code": "vn",\
                "default": true,\
                "district": "Quận 11",\
                "district_code": "HC476",\
                "ward": "Phường 15",\
                "ward_code": "27208"\
            }\
        ],
        "created_at": "2021-08-18T06:18:27.4880706Z",
        "default_address": {
            "address1": "182 Lê Đại Hành",
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": "New",
            "id": 1084464836,
            "last_name": "Haravan",
            "phone": null,
            "province": "Hồ Chí Minh",
            "zip": "70000",
            "name": "Haravan New",
            "province_code": "HC",
            "country_code": "vn",
            "default": true,
            "district": "Quận 11",
            "district_code": "HC476",
            "ward": "Phường 15",
            "ward_code": "27208"
        },
        "email": "new.haravan@example.com",
        "phone": "04142546011",
        "first_name": "New",
        "id": 1050764416,
        "multipass_identifier": null,
        "last_name": "Haravan",
        "last_order_id": null,
        "last_order_name": null,
        "note": null,
        "orders_count": 0,
        "state": "Enabled",
        "tags": null,
        "total_spent": 0.0,
        "total_paid": 0.0,
        "updated_at": "2021-08-18T06:18:27.4880823Z",
        "verified_email": false,
        "group_name": null,
        "birthday": null,
        "gender": null,
        "last_order_date": null
    }
}

```

### Update a customer. [​](https://docs.haravan.com/docs/omni-apis/customer/\#update-a-customer "Direct link to heading")

PUT

https://apis.haravan.com/com/customers/{customer\_id}.json

Update details for a customer.

- PUT `https://apis.haravan.com/com/customers/1050764416.json`

```codeBlockLines_e6Vv
{
    "customer": {
       "tags": "VIP",
        "email": "change.haravan@example.com",
        "note": "Customer is a great guy"
    }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 Ok
{
    "customer": {
        "accepts_marketing": false,
        "addresses": [\
            {\
                "address1": "182 Lê Đại Hành",\
                "address2": null,\
                "city": null,\
                "company": null,\
                "country": "Vietnam",\
                "first_name": "New",\
                "id": 1084464836,\
                "last_name": "Haravan",\
                "phone": null,\
                "province": "Hồ Chí Minh",\
                "zip": "70000",\
                "name": "Haravan New",\
                "province_code": "HC",\
                "country_code": "vn",\
                "default": true,\
                "district": "Quận 11",\
                "district_code": "HC476",\
                "ward": "Phường 15",\
                "ward_code": "27208"\
            }\
        ],
        "created_at": "2021-08-18T06:18:27.488Z",
        "default_address": {
            "address1": "182 Lê Đại Hành",
            "address2": null,
            "city": null,
            "company": null,
            "country": "Vietnam",
            "first_name": "New",
            "id": 1084464836,
            "last_name": "Haravan",
            "phone": null,
            "province": "Hồ Chí Minh",
            "zip": "70000",
            "name": "Haravan New",
            "province_code": "HC",
            "country_code": "vn",
            "default": true,
            "district": "Quận 11",
            "district_code": "HC476",
            "ward": "Phường 15",
            "ward_code": "27208"
        },
        "email": "change.haravan@example.com",
        "phone": "04142546011",
        "first_name": "New",
        "id": 1050764416,
        "multipass_identifier": null,
        "last_name": "Haravan",
        "last_order_id": null,
        "last_order_name": null,
        "note": "Customer is a great guy",
        "orders_count": 0,
        "state": "Enabled",
        "tags": "VIP",
        "total_spent": 0.0000,
        "total_paid": 0.0,
        "updated_at": "2021-08-18T06:23:19.553646Z",
        "verified_email": false,
        "group_name": null,
        "birthday": null,
        "gender": null,
        "last_order_date": null
    }
}

```

### Delete a customer. [​](https://docs.haravan.com/docs/omni-apis/customer/\#delete-a-customer "Direct link to heading")

DELETE

https://apis.haravan.com/com/customers/{customer\_id}.json

Delete a customer.

- Delete `https://apis.haravan.com/com/customers/1050764416.json`

```codeBlockLines_e6Vv
{}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
[]

```

### Add customer tags. [​](https://docs.haravan.com/docs/omni-apis/customer/\#add-customer-tags "Direct link to heading")

POST

https://apis.haravan.com/com/customers/{customer\_id}/tags.json

Add customer tags.

- POST `https://apis.haravan.com/com/customers/1050764416/tags.json`

```codeBlockLines_e6Vv
{
    "tags": "a1,a2"
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "tags": "VIP,a1,a2"
}

```

### Delete customer tags. [​](https://docs.haravan.com/docs/omni-apis/customer/\#delete-customer-tags "Direct link to heading")

DELETE

https://apis.haravan.com/com/customers/{customer\_id}/tags.json

Delete customer tags.

- DELETE `https://apis.haravan.com/com/customers/1050764416/tags.json`

```codeBlockLines_e6Vv
{
    "tags": "a1,a2"
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "tags": "VIP"
}

```

### Retrieves a list of all customer groups. [​](https://docs.haravan.com/docs/omni-apis/customer/\#retrieves-a-list-of-all-customer-groups "Direct link to heading")

GET

https://apis.haravan.com/com/customers/groups.json

Retrieves a list of all customer groups.

- GET `https://apis.haravan.com/com/customers/groups.json`

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
    "customer_groups": [\
        {\
            "id": 39550382,\
            "name": "Tất cả khách hàng",\
            "created_at": "2020-09-18T04:10:29.954Z",\
            "updated_at": "2020-09-18T04:10:29.954Z"\
        },\
        {\
            "id": 39550398,\
            "name": "Nhận email quảng cáo",\
            "created_at": "2020-09-18T04:10:30.217Z",\
            "updated_at": "2020-09-18T04:10:30.217Z"\
        },\
        {\
            "id": 39550400,\
            "name": "Khách hàng thân thiết",\
            "created_at": "2020-09-18T04:10:30.259Z",\
            "updated_at": "2020-09-18T04:10:30.259Z"\
        },\
        {\
            "id": 39550402,\
            "name": "Khách hàng tiềm năng",\
            "created_at": "2020-09-18T04:10:30.298Z",\
            "updated_at": "2020-09-18T04:10:30.298Z"\
        },\
        {\
            "id": 39550404,\
            "name": "Trong nước",\
            "created_at": "2020-09-18T04:10:30.341Z",\
            "updated_at": "2020-09-18T04:10:30.341Z"\
        },\
        {\
            "id": 47243142,\
            "name": "test",\
            "created_at": "2021-08-18T04:22:18.793Z",\
            "updated_at": "2021-08-18T04:22:18.793Z"\
        }\
    ]
}

```

[Previous\\
\\
API Rate Limits](https://docs.haravan.com/docs/omni-apis/api-call-limit/) [Next\\
\\
Customer](https://docs.haravan.com/docs/omni-apis/customer/)

- [What you can do with Customer](https://docs.haravan.com/docs/omni-apis/customer/#what-you-can-do-with-customer)
- [Customer properties](https://docs.haravan.com/docs/omni-apis/customer/#customer-properties)
- [Retrieves a list of customers.](https://docs.haravan.com/docs/omni-apis/customer/#retrieves-a-list-of-customers)
- [Searches for customers that match a supplied query.](https://docs.haravan.com/docs/omni-apis/customer/#searches-for-customers-that-match-a-supplied-query)
- [Retrieves a count of customers.](https://docs.haravan.com/docs/omni-apis/customer/#retrieves-a-count-of-customers)
- [Retrieves detail of a customer.](https://docs.haravan.com/docs/omni-apis/customer/#retrieves-detail-of-a-customer)
- [Create a customer.](https://docs.haravan.com/docs/omni-apis/customer/#create-a-customer)
- [Update a customer.](https://docs.haravan.com/docs/omni-apis/customer/#update-a-customer)
- [Delete a customer.](https://docs.haravan.com/docs/omni-apis/customer/#delete-a-customer)
- [Add customer tags.](https://docs.haravan.com/docs/omni-apis/customer/#add-customer-tags)
- [Delete customer tags.](https://docs.haravan.com/docs/omni-apis/customer/#delete-customer-tags)
- [Retrieves a list of all customer groups.](https://docs.haravan.com/docs/omni-apis/customer/#retrieves-a-list-of-all-customer-groups)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.