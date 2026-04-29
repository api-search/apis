---
aid: bigcommerce:bigcommerce-storefront-subscriptions
baseURL: https://api.example.com
description: BigCommerce Storefront Subscriptions is a feature that allows businesses to offer subscription-based products and services through their online store. With this feature, customers can sign up for recurring purchases and payments, providing convenience and predictability for both the business and its customers. Storefront Subscriptions also enables businesses to manage and track subscription orders, automate billing and payments, and easily offer discounts or promotions to subscribers.
humanURL: https://developer.bigcommerce.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Big Commerce Storefront Subscriptions
properties:
- type: Documentation
  url: https://developer.bigcommerce.com/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bigcommerce/refs/heads/main/openapi/storefront-subscriptions-openapi-original.yml
- type: API Reference
  url: https://developer.bigcommerce.com/docs/rest-storefront/subscriptions
provider_name: BigCommerce
provider_slug: bigcommerce
slug: bigcommerce-storefront-subscriptions
source_filename: storefront-subscriptions-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.1\ninfo:\n  title: BigCommerce Storefront Subscriptions\n  description: >-\n    Manage newsletter and marketing email subscriptions on the storefront.\n\n\n    For info about API accounts, see our [Guide to API\n    Accounts](/docs/start/authentication/api-accounts).\n        \n    For info about authenticating BigCommerce APIs, see [Authentication and\n    Example\n    Requests](/docs/start/authentication#same-origin-cors-authentication).\n\n\n    ## Additional Information\n\n\n    * [Collecting Newsletter\n    Subscriptions](https://support.bigcommerce.com/s/article/Collecting-Newsletter-Subscriptions)\n    (support.bigcommerce.com)\n\n    * [Customers Overview](/docs/store-operations/customers)\n\n    * [Working with Storefront\n    APIs](/docs/storefront/cart-checkout/guide/rest-storefront)\n  termsOfService: https://www.bigcommerce.com/terms\n  contact:\n    name: BigCommerce\n    url: https://www.bigcommerce.com\n    email: support@bigcommerce.com\n  version:\
  \ ''\nservers:\n  - url: https://{store_domain}/api/storefront\n    variables:\n      store_domain:\n        default: your_store.example.com\n        description: >-\n          The [URL\n          authority](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_URL#authority)\n          of the storefront.\ntags:\n  - name: Subscription\npaths:\n  /subscriptions:\n    post:\n      tags:\n        - Subscription\n      summary: BigCommerce Create a Subscription\n      operationId: createSubscription\n      description: >-\n        Creates or updates an email subscription.\n\n\n        By default, customers receive abandoned cart emails as soon as they\n        provide their email address in the checkout flow. They can opt out using\n        this endpoint.\n\n\n        However, if **Store Settings > Miscellaneous > Require Consent** is\n        enabled, Abandoned Cart Emails are not sent by default, and the customer\n        should opt-in.\n\n\n        > ####\
  \ Note\n\n        > * Substitute your storefront domain for `yourstore.example.com`. \n\n        > * The Send a Test Request feature is not currently supported for this\n        endpoint.\n      requestBody:\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/SubscriptionRequest'\n        required: false\n      responses:\n        '200':\n          description: ''\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Subscription'\ncomponents:\n  schemas:\n    SubscriptionRequest:\n      type: object\n      properties:\n        email:\n          type: string\n          description: Email of subscriber\n        acceptsMarketingNewsletter:\n          type: boolean\n          description: >-\n            Describes whether subscriber has consented to receive Marketing\n            emails.\n        acceptsAbandonedCartEmails:\n          type: boolean\n          description:\
  \ >-\n            Describes whether subscriber has consented to receive Abandoned Cart\n            emails.\n      x-internal: false\n    Subscription:\n      type: object\n      properties:\n        id:\n          type: integer\n          description: |\n            The unique numeric ID of the subscriber; increments sequentially.\n        email:\n          type: string\n          description: |\n            The email of the subscriber. Must be unique.\n        firstName:\n          maxLength: 255\n          minLength: 0\n          type: string\n          description: |\n            The first name of the subscriber.\n        lastName:\n          maxLength: 255\n          minLength: 0\n          type: string\n          description: |\n            The last name of the subscriber.\n        source:\n          maxLength: 255\n          minLength: 0\n          type: string\n          description: >\n            The source of the subscriber. Values are: `storefront`, `order`, or\n          \
  \  `custom`.\n        orderId:\n          maximum: 2147483647\n          minimum: 1\n          type: integer\n          description: |\n            The ID of the source order, if source was an order.\n          nullable: true\n        consents:\n          type: array\n          items: {}\n          description: |\n            The collection of consents the shopper is subscribing to.\n      description: Subscription properties.\n      x-internal: false\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bigcommerce/refs/heads/main/openapi/storefront-subscriptions-openapi-original.yml
tags:
- Storefronts
- Subscriptions
---
