---
url: "https://docs.haravan.com/docs/omni-apis/api-call-limit/"
title: "API Rate Limits | Haravan Platform"
---

[Skip to main content](https://docs.haravan.com/docs/omni-apis/api-call-limit/#)

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
- API Rate Limits

On this page

# API Rate Limits

`Version: 1.0`

The Haravan REST Omni API applies rate limits to the API requests that it receives. Every request is subject to throttling under the general limits. In addition, there are resource-based rate limits and throttles.

Limits are calculated using the leaky bucket algorithm. All requests that are made after rate limits have been exceeded are throttled and an HTTP 429 Too Many Requests error is returned. Requests succeed again after enough requests have emptied out of the bucket. You can see the current state of the throttle for a shop by using the rate limits header.

## General API rate limits [​](https://docs.haravan.com/docs/omni-apis/api-call-limit/\#general-api-rate-limits "Direct link to heading")

The rate limits are designed to allow your app to make unlimited requests at a steady rate over time while also having the capacity to make infrequent bursts. The rate limits use a leaky bucket algorithm. The bucket size and leak rate properties determine the API's burst behavior and request rate.

The default settings are as follows:

- **Bucket size**: 80
- **Leak rate**: 4/second

If the bucket size is exceeded, then an HTTP 429 Too Many Requests error is returned. The bucket empties at a leak rate of four requests per second. To avoid being throttled, you can build your app to average four requests per second. The throttle is a pass or fail operation. If there is available capacity in your bucket, then the request is executed without queueing or processing delays. Otherwise, the request is throttled.

## Recommendations [​](https://docs.haravan.com/docs/omni-apis/api-call-limit/\#recommendations "Direct link to heading")

Design your app with API rate limits in mind to best handle request limits and avoid 429 errors. To avoid rate limiting:

- Stagger API requests in a queue and do other processing tasks while waiting for the next queued job to run.

- Use the rate limits header to balance your request volume.


### Handling exceeded rate limits [​](https://docs.haravan.com/docs/omni-apis/api-call-limit/\#handling-exceeded-rate-limits "Direct link to heading")


If your app is throttled, then it won't be able to make any more requests until enough time has passed and your bucket has capacity again. You can calculate this wait time manually using the bucket size and leak rate properties, or by using the Retry-After response header. Your app can also use a more general exponential backoff algorithm to complete the call at a later time.


### Sync stock to Haravan [​](https://docs.haravan.com/docs/omni-apis/api-call-limit/\#sync-stock-to-haravan "Direct link to heading")


When use API inventory adjustment, the line\_items best supports for <=200 items per request API. More items will less request, help advoid rate limit error.


## Rate limits header [​](https://docs.haravan.com/docs/omni-apis/api-call-limit/\#rate-limits-header "Direct link to heading")

You can check how many requests you've already made using the Haravan X-Haravan-Api-Call-Limit header that was sent in response to your API request. This header lists how many requests you've made for a particular shop. For example:

```codeBlockLines_e6Vv
---
X-Haravan-Api-Call-Limit: 32/80
---

```

In this example, 32 is the current request count and 80 is the bucket size. The request count decreases according to the leak rate over time. For example, if the header displays 39/80 requests, then after a wait period of ten seconds, the header displays 19/80 requests.

## Retry-After header [​](https://docs.haravan.com/docs/omni-apis/api-call-limit/\#retry-after-header "Direct link to heading")

When a request goes over a rate limit, a 429 Too Many Requests error and a Retry-After header are returned. The Retry-After header contains the number of seconds to wait until you can make a request again. Any request made before the wait time has elapsed is throttled.

```codeBlockLines_e6Vv
---
X-Haravan-Api-Call-Limit: 80/80
Retry-After: 2.0
---

```

[Previous\\
\\
AccessScope](https://docs.haravan.com/docs/omni-apis/access-scopes/) [Next\\
\\
Customer](https://docs.haravan.com/docs/omni-apis/customer/)

- [General API rate limits](https://docs.haravan.com/docs/omni-apis/api-call-limit/#general-api-rate-limits)
- [Recommendations](https://docs.haravan.com/docs/omni-apis/api-call-limit/#recommendations)
- [Rate limits header](https://docs.haravan.com/docs/omni-apis/api-call-limit/#rate-limits-header)
- [Retry-After header](https://docs.haravan.com/docs/omni-apis/api-call-limit/#retry-after-header)

Haravan

- [Home](https://www.haravan.com/)

Community

- [Facebook](https://www.facebook.com/haravan.official)
- [Youtube](https://www.youtube.com/c/Haravan)

More

- [GitHub](https://github.com/Haravan)

Copyright © 2025 Haravan.