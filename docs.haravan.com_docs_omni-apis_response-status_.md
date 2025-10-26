---
url: "https://docs.haravan.com/docs/omni-apis/response-status/"
title: "API response status and error codes | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/response-status/#)

[![Haravan Platform](https://docs.haravan.com/img/logo-haravan.svg)](https://docs.haravan.com/)[Get Started](https://docs.haravan.com/docs/get-started/overview/) [Tutorials](https://docs.haravan.com/docs/tutorials/authentication/apps-overview/) [Haravan APIs](https://docs.haravan.com/docs/omni-apis/) [Themes](https://docs.haravan.com/docs/themes/) [Partners](https://docs.haravan.com/docs/partners/)

[Sign In](https://partners.haravan.com/) [Sign Up](https://partners.haravan.com/signup)

Search...

# API response status and error codes

When receives a request to an API endpoint, a number of different HTTP status codes can be returned in the response depending on the original request.

| HTTP status | Description |
| --- | --- |
| 200 OK | The request was successfully processed by Haravan. |
| 400 Bad Request | The request wasn't understood by the server, generally due to bad syntax or because the `Content-Type` header wasn't correctly set to `application/json`. <br>This status is also returned when the request provides an invalid code parameter during the OAuth token exchange process. |
| 401 Unauthorized | The necessary `authentication credentials` are not present in the request or are incorrect. |
| 403 Forbidden | The server is refusing to respond to the request. This status is generally returned if you haven't `requested the appropriate scope` for this action. |
| 404 Not Found | The requested resource was not found but could be available again in the future. |
| 502 Bad Gateway | The server, while acting as a gateway or proxy, received an invalid response from the upstream server. A 502 error isn't typically something you can fix. It usually requires a fix on the web server or the proxies that you're trying to get access through. |
| 500 Internal ServerError | An internal error occurred in Haravan |

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.