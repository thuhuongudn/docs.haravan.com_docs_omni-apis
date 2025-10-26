---
url: "https://docs.haravan.com/docs/omni-apis/access-scopes/"
title: "AccessScope | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/access-scopes/#)

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

  - [Subscription](https://docs.haravan.com/docs/omni-apis/subscription/)

- [Home page](https://docs.haravan.com/)
- [Omni APIs](https://docs.haravan.com/docs/omni-apis/)
- AccessScope

On this page

# AccessScope

`Version: 1.0`

### TABLE OF CONTENTS [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#table-of-contents "Direct link to heading")

- **[1\. SCOPE HARAWEB](https://docs.haravan.com/docs/omni-apis/access-scopes/#1-scope-haraweb)**
  - **[1.1 Scope](https://docs.haravan.com/docs/omni-apis/access-scopes/#11-scope)**
  - **[1.2 API List for haraweb scope](https://docs.haravan.com/docs/omni-apis/access-scopes/#12-api-list-for-haraweb-scope)**
- **[2\. SCOPE COMMERCE](https://docs.haravan.com/docs/omni-apis/access-scopes/#2-scope-commerce)**
  - **[2.1 Scope](https://docs.haravan.com/docs/omni-apis/access-scopes/#21-Scope)**
  - **[2.2 API List for commerce scope](https://docs.haravan.com/docs/omni-apis/access-scopes/#22-api-list-for-commerce-scope)**
- **[3\. SCOPE WEBHOOK](https://docs.haravan.com/docs/omni-apis/access-scopes/#3-scope-webhook)**
- **[4\. SCOPE LOGIN](https://docs.haravan.com/docs/omni-apis/access-scopes/#4-scope-login)**
- **[5\. SCOPE INSTALL](https://docs.haravan.com/docs/omni-apis/access-scopes/#5-scope-install)**
- **[6\. HOW TO USE SCOPE WHEN INSTALLING THE APP](https://docs.haravan.com/docs/omni-apis/access-scopes/#6-how-to-use-scope-when-installing-the-app)**
  - **[6.1 Option 1: Use scope login to install the app](https://docs.haravan.com/docs/omni-apis/access-scopes/#61-option-1:-use-scope-login-to-install-the-app)**
    - **[6.1.1 How it works](https://docs.haravan.com/docs/omni-apis/access-scopes/#611-how-it-works)**
    - **[6.1.2 Features](https://docs.haravan.com/docs/omni-apis/access-scopes/#612-features)**
  - **[6.2 Option 2: Use scope login and scope install to install the app(Recommended)](https://docs.haravan.com/docs/omni-apis/access-scopes/#62-option-2:-use-scope-login-and-scope-install-to-install-the-app(recommended))**
    - **[6.2.1 How it works](https://docs.haravan.com/docs/omni-apis/access-scopes/#621-how-it-works)**
    - **[6.2.2 Features](https://docs.haravan.com/docs/omni-apis/access-scopes/#622-features)**
- **[7\. GET SHOP INFORMATION AFTER INSTALLING THE APP](https://docs.haravan.com/docs/omni-apis/access-scopes/#7-get-shop-information-after-installing-the-app)**
- **[8\. HOW TO USE SCOPE LOGIN WHEN USING THE APP](https://docs.haravan.com/docs/omni-apis/access-scopes/#8-how-to-use-scope-login-when-using-the-app)**

## 1\. SCOPE HARAWEB [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#1-scope-haraweb "Direct link to heading")

### 1.1 Scope [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#11-scope "Direct link to heading")

- These are scopes in “Haraweb” of [https://partners.haravan.com/apps](https://partners.haravan.com/apps)

- Once selected here, you must pass the corresponding scopes when you install the application.

- For the API use at the sales page.

- The way to declare haraweb scope: **web. {scope\_name}**.


Ex: web.read\_script\_tags.

![access-scope-1](https://docs.haravan.com/assets/images/access-scope-1-921e3cc662c931e096e588a3a300777d.png)

| Name | Scope | API |
| --- | --- | --- |
| Contents | web.read\_contents<br>web.write\_contents | [Blog](https://docs.haravan.com/docs/omni-apis/blogs/)<br>[Comment](https://docs.haravan.com/docs/omni-apis/comments/)<br>[Page](https://docs.haravan.com/docs/omni-apis/pages/)<br>[Redirect](https://docs.haravan.com/docs/omni-apis/redirects/)<br>[Article](https://docs.haravan.com/docs/omni-apis/articles/) |
| Themes | web.read\_themes<br>web.write\_themes | [Theme](https://docs.haravan.com/docs/omni-apis/themes/) |
| ScriptTags | web.read\_script\_tags<br>web.write\_script\_tags | [ScriptTag](https://docs.haravan.com/docs/omni-apis/script_tags/) |

### 1.2 API List for haraweb scope [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#12-api-list-for-haraweb-scope "Direct link to heading")

- Corresponding to the scope will be access to the corresponding API.

- The write scope will include read permissions and use the methods: GET, POST, PUT, DELETE.

- The Read scope only uses the GET method.

- API prefix: [https://apis.haravan.com/web](https://apis.haravan.com/web)

- Call the API with the syntax: [https://apis.haravan.com/web/{api}](https://apis.haravan.com/web/%7Bapi%7D).


EX: Call API get scriptTags: [https://apis.haravan.com/web/script\_tags.json](https://apis.haravan.com/web/script_tags.json) (GET).

## 2\. SCOPE COMMERCE [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#2-scope-commerce "Direct link to heading")

### 2.1 Scope [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#21-scope "Direct link to heading")

- These are scopes in “Commerce” of [https://partners.haravan.com/apps](https://partners.haravan.com/apps)

- Once selected here, you must pass the corresponding scopes when you install the application.

- For the API use at the admin page.

- The way to declare commerce scope: **com.{scope\_name}**.


Ex: com.write\_products

![access-scope-2](https://docs.haravan.com/assets/images/access-scope-2-7a8e774226381095614ec2753bd1c773.png)

### 2.2 API List for commerce scope [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#22-api-list-for-commerce-scope "Direct link to heading")

- Corresponding to the scope will be access to the corresponding API.

- The write scope will include read permissions and use the methods: GET, POST, PUT, DELETE.

- The Read scope only uses the GET method

- API prefix: [https://apis.haravan.com/com](https://apis.haravan.com/com)

- Call the API with the syntax: [https://apis.haravan.com/com/{api}](https://apis.haravan.com/com/%7Bapi%7D).


EX: Call API products: [https://apis.haravan.com/com/products.json](https://apis.haravan.com/com/products.json) (GET).

| Name | Scope | API |
| --- | --- | --- |
| Inventories | com.read\_inventories<br>com.write\_inventories | [Inventory adjustment](https://docs.haravan.com/docs/omni-apis/inventory-adjustment/)<br>[Inventory transfer](https://docs.haravan.com/docs/omni-apis/inventory-transfer/)<br>[Purchase order](https://docs.haravan.com/docs/omni-apis/inventory-purchase-orders/)<br>[Purchase receive](https://docs.haravan.com/docs/omni-apis/inventory-purchase-receives/)<br>[Inventory location](https://docs.haravan.com/docs/omni-apis/inventory-locations/) |
| Shippings | com.read\_shippings <br>com.write\_shippings | [Shipping Rates](https://docs.haravan.com/docs/omni-apis/shipping-rates/) |
| Customers | com.read\_customers<br> com.write\_customers | [Customer](https://docs.haravan.com/docs/omni-apis/customer/)<br>[Customer address](https://docs.haravan.com/docs/omni-apis/customer-address/) |
| Products | com.read\_products<br>com.write\_products | [Product](https://docs.haravan.com/docs/omni-apis/products/)<br>[Smart\_collection](https://docs.haravan.com/docs/omni-apis/smart-collections/)<br>[Collect](https://docs.haravan.com/docs/omni-apis/collects/)<br>[Custom\_collections](https://docs.haravan.com/docs/omni-apis/custom-collections/)<br>[Product variant](https://docs.haravan.com/docs/omni-apis/product-variants/)<br>[Product Image](https://docs.haravan.com/docs/omni-apis/product-images/) |
| Write Orders | com.read\_orders<br>com.write\_orders | [Order](https://docs.haravan.com/docs/omni-apis/orders/)<br>[Transaction](https://docs.haravan.com/docs/omni-apis/transactions/) |

## 3\. SCOPE WEBHOOK [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#3-scope-webhook "Direct link to heading")

- This is a scope to using webhooks for the application. Only shop owner (role contains ‘admin’) can use it.

- When using webhooks, this scope is required.

- You need to register webhook on [https://partners.haravan.com/apps](https://partners.haravan.com/apps) before using this scope.


| Scope | Description |
| --- | --- |
| wh\_api | Scope use webhook |

## 4\. SCOPE LOGIN [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#4-scope-login "Direct link to heading")

- These are the required scopes to log in and get user information

- Also you can add more scope from **haraweb** and **commerce**


|  | Scope | Description |
| --- | --- | --- |
| 1 | openid |  |
| 2 | profile |  |
| 3 | email | Get an email of the login user |
| 4 | org | Get org information (org\_id , org\_name) |
| 5 | userinfo | Get information of login user |

## 5\. SCOPE INSTALL [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#5-scope-install "Direct link to heading")

- These are the scopes used to install the application.

- These are the scopes include:

  - Required scopes.



    |  | Scope | Description |
    | --- | --- | --- |
    | 1 | openid |  |
    | 2 | profile |  |
    | 3 | email | Get an email of the login user |
    | 4 | org | Get org information (org\_id , org\_name) |
    | 5 | userinfo | Get information of login user |
    | 6 | grant\_service | This is the scope that only the shop owner (role contains ‘admin’) can use.<br>function:<br>\+ Get long-lived access\_token<br>\+ Install the application on the Seller application list |

  - Scope use **webhook** (optional)

  - Scopes are selected at **haraweb** and **commerce**

## 6\. HOW TO USE SCOPE WHEN INSTALLING THE APP [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#6-how-to-use-scope-when-installing-the-app "Direct link to heading")

- When installing, you need to focus on the scope login and scope install.

- As you can see, the scope login and install are mostly the same and both are used to pass to the authorized URL to get the code and id\_token. So, depending on how to use the scope, you can install the app in two options.

- **Note:**

  - **Here only describes how the scope works**

  - **Refer to the link below for more information:**

    - [Create App and Connect API](https://docs.haravan.com/docs/get-started/create-app/)

### 6.1 Option 1: Use scope login to install the app [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#61-option-1-use-scope-login-to-install-the-app "Direct link to heading")

#### 6.1.1 How it works [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#611-how-it-works "Direct link to heading")

- As mentioned, login and install are both call URL authorize but the different scope is passed (scope login or install).

- So, we can pass the selected scope at **haraweb** and **commerce** with the scope login right from the first call to the authorized URL.

- You still have the code corresponding to the scope passed, using the OAuth 2 library to render access\_token.


#### 6.1.2 Features [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#612-features "Direct link to heading")

- call the authorization URL once.

- This access\_token is called access\_token user, and it’s short-lived access\_token

- The application can only be used by users who install it.

- Does not appear on the seller app list.

- Unable to use webhook.


### 6.2 Option 2: Use scope login and scope install to install the app (Recommended) [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#62-option-2-use-scope-login-and-scope-install-to-install-the-app-recommended "Direct link to heading")

#### 6.2.1 How it works [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#621-how-it-works "Direct link to heading")

- First, call the authorization URL with **scope login** to get id\_token.

- Use **JWT** to decode this id\_token to get an object including user information, role users, shop information.

- You need to verify the role of the logged-in user:

  - If the user is the shop owner (role contains ‘admin’) then call URL authorize with **scope install** (because **webhook** scope and **grant\_service** scope are only used by the shop owner)

  - If the user isn’t the shop owner (role doesn’t contain ‘admin’) then show the error message.
- You have the code corresponding to the scope passed, using the OAuth 2 library to render access\_token.


#### 6.2.2 Features [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#622-features "Direct link to heading")

- Can verify user and shop information twice, increase security, and ability to manage users.

- Access\_token is a long-lived access\_token.

- Install the application on the Seller application list.


## 7\. GET SHOP INFORMATION AFTER INSTALLING THE APP. [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#7-get-shop-information-after-installing-the-app "Direct link to heading")

- The application only use scopes in haraweb, use this API:
[https://apis.haravan.com/web/shop.json](https://apis.haravan.com/web/shop.json)

- The application only use scopes in commerce, use this API:
[https://apis.haravan.com/com/shop.json](https://apis.haravan.com/com/shop.json)

- **Note: If you use both the scope in haraweb and commerce, you can use one of the APIs above.**


## 8\. HOW TO USE SCOPE LOGIN WHEN USING THE APP [​](https://docs.haravan.com/docs/omni-apis/access-scopes/\#8-how-to-use-scope-login-when-using-the-app "Direct link to heading")

- When the application was installed, we need to verify that the logged-in user has access to the application

- There are 2 types of user authorization:

  - User authorization on the seller

  - User authorization on Application (configured on the application)
- Before the user starts the application, call the authorization URL with **scope login** to get the id\_token

- Use **JWT** to decode this id\_token to get an object including user information, role users, shop information.

- You need to verify the role of the logged-in user:

  - If the user is the shop owner (role contains ‘admin’) then start the application.

  - If the user isn’t the shop owner (role doesn’t contain ‘admin’), We have 3 cases:

    - **Case 1**: authorization on the seller of the user’s account does not accept to use the scope of the application, show messages “you are not authorized to use the application”.

    - **Case 2**: That user has permission to use the application's scopes but the user is not authorized to use the app (if the application has its own authorization system), show messages “you are not authorized to use the application”.

    - **Case 3**: That user does not have permission to use the application's scopes, but the user is allowed to use the application (if the application has its own authorization system), starts the application.

[Previous\\
\\
About Haravan APIs](https://docs.haravan.com/docs/omni-apis/) [Next\\
\\
API Rate Limits](https://docs.haravan.com/docs/omni-apis/api-call-limit/)

- [TABLE OF CONTENTS](https://docs.haravan.com/docs/omni-apis/access-scopes/#table-of-contents)
- [1\. SCOPE HARAWEB](https://docs.haravan.com/docs/omni-apis/access-scopes/#1-scope-haraweb)
  - [1.1 Scope](https://docs.haravan.com/docs/omni-apis/access-scopes/#11-scope)
  - [1.2 API List for haraweb scope](https://docs.haravan.com/docs/omni-apis/access-scopes/#12-api-list-for-haraweb-scope)
- [2\. SCOPE COMMERCE](https://docs.haravan.com/docs/omni-apis/access-scopes/#2-scope-commerce)
  - [2.1 Scope](https://docs.haravan.com/docs/omni-apis/access-scopes/#21-scope)
  - [2.2 API List for commerce scope](https://docs.haravan.com/docs/omni-apis/access-scopes/#22-api-list-for-commerce-scope)
- [3\. SCOPE WEBHOOK](https://docs.haravan.com/docs/omni-apis/access-scopes/#3-scope-webhook)
- [4\. SCOPE LOGIN](https://docs.haravan.com/docs/omni-apis/access-scopes/#4-scope-login)
- [5\. SCOPE INSTALL](https://docs.haravan.com/docs/omni-apis/access-scopes/#5-scope-install)
- [6\. HOW TO USE SCOPE WHEN INSTALLING THE APP](https://docs.haravan.com/docs/omni-apis/access-scopes/#6-how-to-use-scope-when-installing-the-app)
  - [6.1 Option 1: Use scope login to install the app](https://docs.haravan.com/docs/omni-apis/access-scopes/#61-option-1-use-scope-login-to-install-the-app)
  - [6.2 Option 2: Use scope login and scope install to install the app (Recommended)](https://docs.haravan.com/docs/omni-apis/access-scopes/#62-option-2-use-scope-login-and-scope-install-to-install-the-app-recommended)
- [7\. GET SHOP INFORMATION AFTER INSTALLING THE APP.](https://docs.haravan.com/docs/omni-apis/access-scopes/#7-get-shop-information-after-installing-the-app)
- [8\. HOW TO USE SCOPE LOGIN WHEN USING THE APP](https://docs.haravan.com/docs/omni-apis/access-scopes/#8-how-to-use-scope-login-when-using-the-app)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.