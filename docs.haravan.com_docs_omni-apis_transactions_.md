---
url: "https://docs.haravan.com/docs/omni-apis/transactions/"
title: "Transaction | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/transactions/#)

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

    - [Order](https://docs.haravan.com/docs/omni-apis/orders/)
    - [Refund](https://docs.haravan.com/docs/omni-apis/refunds/)
    - [Transaction](https://docs.haravan.com/docs/omni-apis/transactions/)
  - [Products](https://docs.haravan.com/docs/omni-apis/collects/)

  - [Shipping](https://docs.haravan.com/docs/omni-apis/shipping-rates/)

  - [Store properties](https://docs.haravan.com/docs/omni-apis/country/)

  - [Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [Home page](https://docs.haravan.com/)
- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)
- [Orders](https://docs.haravan.com/docs/omni-apis/orders/)
- Transaction

On this page

# Transaction

`Version: 1.0`

Transactions are created for every order that results in an exchange of money.

There are five types of transactions:

- **Pending**: Order wait for pay.
- **Authorization**: represents an amount reserved against the cardholder's funding source. Money does not change hands until authorization is captured.
- **Sale**: an authorization and capture performed together in a single step.
- **Capture**: transfer of the money that was reserved during the authorization stage
- **Void**: cancellation of a pending authorization or capture.
- **Refund**: a partial or full return of captured funds to the cardholder. A refund can only happen after capture is processed.

**Authenticated access scopes**: `com.read_orders`, `com.write_orders`

### What you can do with Transaction [​](https://docs.haravan.com/docs/omni-apis/transactions/\#what-you-can-do-with-transaction "Direct link to heading")

The Haravan API lets you do the following with the Transaction resource.

- GET `https://apis.haravan.com/com/orders/{order_id}/transactions.json`
  - **[Retrieves a list transactions of order.](https://docs.haravan.com/docs/omni-apis/transactions/#retrieves-a-list-transactions-of-order)**
- GET `https://apis.haravan.com/com/orders/{order_id}/transactions/{transaction_id}.json`
  - **[Retrieves single transaction of the order.](https://docs.haravan.com/docs/omni-apis/transactions/#retrieves-single-transaction-of-the-order)**
- POST `https://apis.haravan.com/com/orders/{order_id}/transations.json`
  - **[Create a new transaction for an existing order.](https://docs.haravan.com/docs/omni-apis/transactions/#create-a-new-transaction-for-an-existing-order)**

### Transaction properties [​](https://docs.haravan.com/docs/omni-apis/transactions/\#transaction-properties "Direct link to heading")

* * *

`amount` : `number`

```codeBlockLines_e6Vv
"amount": 180000.0000

```

The amount of money that the transaction was for.

`authorization` : `string`

```codeBlockLines_e6Vv
"authorization": null

```

The authorization code associated with the transaction.

`created_at` : `string`

```codeBlockLines_e6Vv
"created_at": "2021-05-13T07:29:20.1Z"

```

The date and time ( [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format) when the transaction was created.

`device_id` : `number`

```codeBlockLines_e6Vv
"device_id": null

```

The unique identifier for the device.

`gateway` : `string`

```codeBlockLines_e6Vv
"gateway": "Thanh toán khi giao hàng (COD)"

```

The name of the gateway the transaction was issued through. A list of gateways can be found on haravan's Payment Gateway page.

`id` : `number`

```codeBlockLines_e6Vv
"id": 1095862541

```

A unique numeric identifier for the transaction.

`kind` : `string`

```codeBlockLines_e6Vv
"kind": "Capture"

```

The kind of transaction:

- **Pending**: Order wait for pay.
- **Authorization**: Money that the customer has agreed to pay. Authorization period lasts for up to 7 to 30 days (depending on your payment service) while a store awaits for a customer's capture.
- **Capture**: Transfer of money that was reserved during the authorization of a shop.
- **Sale**: The combination of authorization and capture, performed in one single step.
- **Void**: The cancellation of a pending authorization or capture.
- **Refund**: The partial or full return of the captured money to the customer.

`order_id` : `number`

```codeBlockLines_e6Vv
"order_id": 1235924702

```

A unique numeric identifier for the order.

`receipt` : `string`

```codeBlockLines_e6Vv
"receipt": null

```

Transaction receipt.

`status` : `string`

```codeBlockLines_e6Vv
"status": "success"

```

The status of the transaction. Valid values are: pending, failure, success or error.

`test` : `boolean`

```codeBlockLines_e6Vv
"test": false

```

The option to use the transaction for testing purposes. Valid values are "true" or "false".

`user_id` : `number`

```codeBlockLines_e6Vv
"user_id": null

```

The unique identifier for the user.

`location_id` : `number`

```codeBlockLines_e6Vv
"location_id": null

```

The unique identifier of product return location.

`currency` : `string`

```codeBlockLines_e6Vv
"currency": "VND"

```

The three letter code (ISO 4217) for the currency used for the payment.

`is_cod_gateway` : boolean

```codeBlockLines_e6Vv
"is_cod_gateway": false

```

It is true when gateway payment is COD

### Retrieves a list transactions of order. [​](https://docs.haravan.com/docs/omni-apis/transactions/\#retrieves-a-list-transactions-of-order "Direct link to heading")

GET

https://apis.haravan.com/com/orders/{order\_id}/transactions.json

Retrieves a list all transaction of order. You can filter resources by params.

* * *

`fields`

comma-separated list of fields to include in the response.

* * *

Retrieve all transation.

- GET `https://apis.haravan.com/com/orders/1235924702/transactions.json`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK
{
    "transactions": [\
        {\
            "amount": 180000.0000,\
            "authorization": null,\
            "created_at": "2021-10-21T09:53:52.876Z",\
            "device_id": null,\
            "gateway": "Thanh toán khi giao hàng (COD)",\
            "id": 1095862541,\
            "kind": "Pending",\
            "order_id": 1235924702,\
            "receipt": null,\
            "status": "success",\
            "test": false,\
            "user_id": 0,\
            "location_id": 991324,\
            "payment_details": null,\
            "parent_id": null,\
            "currency": "VND",\
            "haravan_transaction_id": null,\
            "external_transaction_id": null,\
            "send_email": false,\
            "is_cod_gateway": false\
        }\
    ]
}

```

### Retrieves single transaction of the order. [​](https://docs.haravan.com/docs/omni-apis/transactions/\#retrieves-single-transaction-of-the-order "Direct link to heading")

GET

https://apis.haravan.com/com/orders/{order\_id}/transactions/{transation\_id}.json

Retrieves single transaction of order by ID.

- GET `https://apis.haravan.com/com/orders/1235924702/transactions/1095862541.json`

Details

```codeBlockLines_e6Vv

HTTP/1.1 200 OK
{
    "transaction": {
        "amount": 180000.0000,
        "authorization": null,
        "created_at": "2021-10-21T09:53:52.876Z",
        "device_id": null,
        "gateway": "Thanh toán khi giao hàng (COD)",
        "id": 1095862541,
        "kind": "Pending",
        "order_id": 1235924702,
        "receipt": null,
        "status": "success",
        "test": false,
        "user_id": 0,
        "location_id": 991324,
        "payment_details": null,
        "parent_id": null,
        "currency": "VND",
        "haravan_transaction_id": null,
        "external_transaction_id": null,
        "send_email": false,
        "is_cod_gateway": false
    }
}

```

### Create a new transaction for an existing order. [​](https://docs.haravan.com/docs/omni-apis/transactions/\#create-a-new-transaction-for-an-existing-order "Direct link to heading")

POST

https://apis.haravan.com/com/orders/{order\_id}/transactions.json

Create a transation for an existing Order.

* * *

`amount`

The amount of money that the transaction was for.

* * *

`kind`

The kind of transaction:

- **Pending**: Order wait for pay.
- **Authorization**: Money that the customer has agreed to pay. Authorization period lasts for up to 7 to 30 days (depending on your payment service) while a store awaits for a customer's capture.
- **Capture**: Transfer of money that was reserved during the authorization of a shop.
- **Sale**: The combination of authorization and capture, performed in one single step.
- **Void**: The cancellation of a pending authorization or capture.
- **Refund**: The partial or full return of the captured money to the customer.

* * *

Create a new transaction for an order.

- POST `https://apis.haravan.com/com/orders/1235924702/transactions.json`

```codeBlockLines_e6Vv
{
    "transaction": {
        "amount": 100000,
        "kind": "Capture"
    }
}

```

Details

```codeBlockLines_e6Vv

HTTP/1.1 201 Created

{
    "transaction": {
        "amount": 100000.0,
        "authorization": null,
        "created_at": "2021-11-05T08:30:43.2513479Z",
        "device_id": null,
        "gateway": "Thanh toán khi giao hàng (COD)",
        "id": 1097603368,
        "kind": "Capture",
        "order_id": 1235924702,
        "receipt": null,
        "status": "success",
        "test": false,
        "user_id": 200000792911,
        "location_id": 991324,
        "payment_details": null,
        "parent_id": 1095862541,
        "currency": "VND",
        "haravan_transaction_id": null,
        "external_transaction_id": "",
        "send_email": false,
        "is_cod_gateway": false
    }
}

```

[Previous\\
\\
Refund](https://docs.haravan.com/docs/omni-apis/refunds/) [Next\\
\\
Collect](https://docs.haravan.com/docs/omni-apis/collects/)

- [What you can do with Transaction](https://docs.haravan.com/docs/omni-apis/transactions/#what-you-can-do-with-transaction)
- [Transaction properties](https://docs.haravan.com/docs/omni-apis/transactions/#transaction-properties)
- [Retrieves a list transactions of order.](https://docs.haravan.com/docs/omni-apis/transactions/#retrieves-a-list-transactions-of-order)
- [Retrieves single transaction of the order.](https://docs.haravan.com/docs/omni-apis/transactions/#retrieves-single-transaction-of-the-order)
- [Create a new transaction for an existing order.](https://docs.haravan.com/docs/omni-apis/transactions/#create-a-new-transaction-for-an-existing-order)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.