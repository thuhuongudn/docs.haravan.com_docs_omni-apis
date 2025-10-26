---
url: "https://docs.haravan.com/docs/omni-apis/customer-address/"
title: "Customer Address | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/customer-address/#)

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
- [Customers](https://docs.haravan.com/docs/omni-apis/customer/)
- Customer Address

On this page

# Customer Address

`Version: 1.0`

A **customer address** resource instance represents one of the many addresses a customer may have

For more information about Customers, see the Customer API Documentation

**Authenticated access scopes**: `com.read_customers`, `com.write_customers`

### What can you do with CustomerAddress? [​](https://docs.haravan.com/docs/omni-apis/customer-address/\#what-can-you-do-with-customeraddress "Direct link to heading")

The haravan API lets you do the following with the CustomerAddress resource. More detailed versions of these general actions may be available:

- GET `https://apis.haravan.com/com/customers/{customer_id}/addresses.json`
  - **[Receive a list of all CustomerAddresses.](https://docs.haravan.com/docs/omni-apis/customer-address/#receive-a-list-of-all-customeraddresses)**
- GET `https://apis.haravan.com/com/customers/{customer_id}/addresses/{address_id}.json`
  - **[Receive a single CustomerAddress.](https://docs.haravan.com/docs/omni-apis/customer-address/#receive-a-single-customeraddress)**
- POST `https://apis.haravan.com/com/customers/{customer_id}/addresses.json`
  - **[Create a new CustomerAddress.](https://docs.haravan.com/docs/omni-apis/customer-address/#create-a-new-customeraddress)**
- PUT `https://apis.haravan.com/com/customers/{customer_id}/addresses/{address_id}.json`
  - **[Modify an existing CustomerAddress.](https://docs.haravan.com/docs/omni-apis/customer-address/#modify-an-existing-customeraddress)**
- DELETE `https://apis.haravan.com/com/customers/{customer_id}/addresses/{address_id}.json`
  - **[Remove a CustomerAddress from the database.](https://docs.haravan.com/docs/omni-apis/customer-address/#remove-a-customeraddress-from-the-database)**
- PUT `https://apis.haravan.com/com/customers/{customer_id}/addresses/set.json`
  - **[Perform bulk operations against a number of addresses.](https://docs.haravan.com/docs/omni-apis/customer-address/#perform-bulk-operations-against-a-number-of-addresses)**
- PUT `https://apis.haravan.com/com/customers/{customer_id}/addresses/{address_id}/default.json`
  - **[Sets default address for a customer.](https://docs.haravan.com/docs/omni-apis/customer-address/#sets-default-address-for-a-customer)**

### CustomerAddress Properties [​](https://docs.haravan.com/docs/omni-apis/customer-address/\#customeraddress-properties "Direct link to heading")

* * *

`address1` : `string`

```codeBlockLines_e6Vv
"address1": "1 Rue des Carrieres"

```

`address2` : `string`

```codeBlockLines_e6Vv
"address2": "Suite 1234"

```

`city` : `string`

```codeBlockLines_e6Vv
"city": "Montreal"

```

`company` : `string`

```codeBlockLines_e6Vv
"company": "Fancy Co."

```

Company name associated with address (optional)

`first_name` : `string`

```codeBlockLines_e6Vv
"first_name": "Samuel"

```

`last_name` : `string`

```codeBlockLines_e6Vv
"last_name": "de Champlain"

```

`phone` : `string`

```codeBlockLines_e6Vv
"phone": "819-555-5555"

```

`province` : `string`

```codeBlockLines_e6Vv
"province": "province"

```

`country` : `string`

```codeBlockLines_e6Vv
"country": "Canada"

```

`zip` : `string`

```codeBlockLines_e6Vv
"zip": "G1R 4P5"

```

`name` : `string`

```codeBlockLines_e6Vv
"name": "Samuel de Champlain"

```

`province_code` : `string`

```codeBlockLines_e6Vv
"province_code": "QC"

```

`country_code` : `string`

```codeBlockLines_e6Vv
"country_code": "CA"

```

Country Code in ISO 3166-1 (alpha-2) format. [See Current ISO Codes](http://en.wikipedia.org/wiki/ISO_3166-1#Current_codes)

`country_name` : `string`

```codeBlockLines_e6Vv
"country_name": "Canada"

```

### Receive a list of all CustomerAddresses. [​](https://docs.haravan.com/docs/omni-apis/customer-address/\#receive-a-list-of-all-customeraddresses "Direct link to heading")

GET

https://apis.haravan.com/com/customers/{customer\_id}/addresses.json

Retrieve all addresses for a customer

* * *

`page`

Page to show(default: 1)

* * *

`limit`

Amount of results(default: 50) (maximum: 250)

* * *

Get all of a customers addresses

- GET `https://apis.haravan.com/com/customers/207119551/addresses.json`

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "addresses": [\
    {\
      "address1": "Chestnut Street 92",\
      "address2": "",\
      "city": "Louisville",\
      "company": null,\
      "country": "United States",\
      "first_name": null,\
      "id": 207119551,\
      "last_name": null,\
      "phone": "555-625-1199",\
      "province": "Kentucky",\
      "zip": "40202",\
      "name": "",\
      "province_code": "KY",\
      "country_code": "US",\
      "country_name": "United States",\
      "default": true\
    }\
  ]
}

```

Get a limited number of addresses for a customer

- GET `https://apis.haravan.com/com/customers/207119551/addresses.json?limit=1&page=1`

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "addresses": [\
    {\
      "address1": "Chestnut Street 92",\
      "address2": "",\
      "city": "Louisville",\
      "company": null,\
      "country": "United States",\
      "first_name": null,\
      "id": 207119551,\
      "last_name": null,\
      "phone": "555-625-1199",\
      "province": "Kentucky",\
      "zip": "40202",\
      "name": "",\
      "province_code": "KY",\
      "country_code": "US",\
      "country_name": "United States",\
      "default": true\
    }\
  ]
}

```

### Receive a single CustomerAddress. [​](https://docs.haravan.com/docs/omni-apis/customer-address/\#receive-a-single-customeraddress "Direct link to heading")

GET

https://apis.haravan.com/com/customers/{customer\_id}/addresses/{address\_id}.json

Retrieve details for one of a customers addresses

- GET `https://apis.haravan.com/com/customers/207119551/addresses/207119551.json`

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "customer_address": {
    "address1": "Chestnut Street 92",
    "address2": "",
    "city": "Louisville",
    "company": null,
    "country": "United States",
    "first_name": null,
    "id": 207119551,
    "last_name": null,
    "phone": "555-625-1199",
    "province": "Kentucky",
    "zip": "40202",
    "name": "",
    "province_code": "KY",
    "country_code": "US",
    "country_name": "United States",
    "default": true
  }
}

```

### Create a new CustomerAddress. [​](https://docs.haravan.com/docs/omni-apis/customer-address/\#create-a-new-customeraddress "Direct link to heading")

POST

https://apis.haravan.com/com/customers/{customer\_id}/addresses.json

Creating a new address for a customer

- POST `https://apis.haravan.com/com/customers/207119551/addresses.json`

```codeBlockLines_e6Vv
{
  "address": {
    "address1": "182 Lê Đại Hành",
    "address2": null,
    "city": null,
    "company": null,
    "country": "Vietnam",
    "first_name": "New",
    "id": 10226732601,
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
  }
}

```

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 201 Created
{
  "address": {
    "address1": "182 Lê Đại Hành",
    "address2": null,
    "city": null,
    "company": null,
    "country": "Vietnam",
    "first_name": "New",
    "id": 10226732601,
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
  }
}

```

### Modify an existing CustomerAddress. [​](https://docs.haravan.com/docs/omni-apis/customer-address/\#modify-an-existing-customeraddress "Direct link to heading")

PUT

https://apis.haravan.com/com/customers/{customer\_id}/addresses/{address\_id}.json

Updating a customers postal code

- PUT `https://apis.haravan.com/com/customers/207119551/addresses/207119551.json`

```codeBlockLines_e6Vv
{
  "address": {
    "id": 207119551,
    "zip": "H0H 0H0"
  }
}

```

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "customer_address": {
    "address1": "Chestnut Street 92",
    "address2": "",
    "city": "Louisville",
    "company": null,
    "country": "United States",
    "first_name": null,
    "id": 207119551,
    "last_name": null,
    "phone": "555-625-1199",
    "province": "Kentucky",
    "zip": "H0H 0H0",
    "name": "",
    "province_code": "KY",
    "country_code": "US",
    "country_name": "United States",
    "default": true
  }
}

```

### Remove a CustomerAddress from the database. [​](https://docs.haravan.com/docs/omni-apis/customer-address/\#remove-a-customeraddress-from-the-database "Direct link to heading")

DELETE

https://apis.haravan.com/com/customers/{customer\_id}/addresses/{address\_id}.json

Removes an address from the customers address list

Removing a customers address

- DELETE `https://apis.haravan.com/com/customers/207119551/addresses/1053317288.json`

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{}

```

Trying to remove a customers default address results in a failure

- DELETE `https://apis.haravan.com/com/customers/207119551/addresses/1053317288.json`

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 422 Unprocessable Entity
{
  "errors": {
    "base": [\
      "Cannot delete the customers default address"\
    ]
  }
}

```

### Perform bulk operations against a number of addresses. [​](https://docs.haravan.com/docs/omni-apis/customer-address/\#perform-bulk-operations-against-a-number-of-addresses "Direct link to heading")

PUT

https://apis.haravan.com/com/customers/{customer\_id}/addresses/set.json

Destroying multiple customer addresses

- PUT `https://apis.haravan.com/com/customers/207119551/addresses/set.json?address_ids[]=1053317289&operation=destroy`

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{}

```

### Sets default address for a customer. [​](https://docs.haravan.com/docs/omni-apis/customer-address/\#sets-default-address-for-a-customer "Direct link to heading")

PUT

https://apis.haravan.com/com/customers/{customer\_id}/addresses/{address\_id}/default.json

Assigning a new default address to a customer

- PUT `https://apis.haravan.com/com/customers/207119551/addresses/1053317287/default.json`

Response:

Details

```codeBlockLines_e6Vv
HTTP/1.1 200 OK
{
  "customer_address": {
    "address1": "Chestnut Street 92",
    "address2": "",
    "city": "Louisville",
    "company": null,
    "country": "United States",
    "first_name": "Bob",
    "id": 1053317287,
    "last_name": "Norman",
    "phone": "555-625-1199",
    "province": "Kentucky",
    "zip": "40202",
    "name": "Bob Norman",
    "province_code": "KY",
    "country_code": "US",
    "country_name": "United States",
    "default": true
  }
}

```

[Previous\\
\\
Customer](https://docs.haravan.com/docs/omni-apis/customer/) [Next\\
\\
DiscountCode](https://docs.haravan.com/docs/omni-apis/discount/discount-codes/)

- [What can you do with CustomerAddress?](https://docs.haravan.com/docs/omni-apis/customer-address/#what-can-you-do-with-customeraddress)
- [CustomerAddress Properties](https://docs.haravan.com/docs/omni-apis/customer-address/#customeraddress-properties)
- [Receive a list of all CustomerAddresses.](https://docs.haravan.com/docs/omni-apis/customer-address/#receive-a-list-of-all-customeraddresses)
- [Receive a single CustomerAddress.](https://docs.haravan.com/docs/omni-apis/customer-address/#receive-a-single-customeraddress)
- [Create a new CustomerAddress.](https://docs.haravan.com/docs/omni-apis/customer-address/#create-a-new-customeraddress)
- [Modify an existing CustomerAddress.](https://docs.haravan.com/docs/omni-apis/customer-address/#modify-an-existing-customeraddress)
- [Remove a CustomerAddress from the database.](https://docs.haravan.com/docs/omni-apis/customer-address/#remove-a-customeraddress-from-the-database)
- [Perform bulk operations against a number of addresses.](https://docs.haravan.com/docs/omni-apis/customer-address/#perform-bulk-operations-against-a-number-of-addresses)
- [Sets default address for a customer.](https://docs.haravan.com/docs/omni-apis/customer-address/#sets-default-address-for-a-customer)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.