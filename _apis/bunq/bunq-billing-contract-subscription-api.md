---
aid: bunq:bunq-billing-contract-subscription-api
baseURL: ''
description: The Bunq Billing Contract Subscription API is a tool that allows businesses to create and manage subscription billing contracts with their customers. This API provides businesses with the ability to automate recurring billing processes, set up payment schedules, and track customer invoices. By using this API, businesses can streamline their subscription billing procedures, reduce manual administrative tasks, and improve overall efficiency in managing customer contracts.
humanURL: https://doc.bunq.com/#/billing-contract-subscription/List_all_BillingContractSubscription_for_User
image: ''
layout: api
name: Bunq Billing Contract Subscription API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-billing-contract-subscription-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-billing-contract-subscription-api
source_filename: bunq-user-userid-billing-contract-subscription-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq user/{userID}/billing-contract-subscription'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths:\n  /user/{userID}/billing-contract-subscription:\n    get:\n      tags:\n        - User\n      summary: ''\n      operationId: List_all_BillingContractSubscription_for_User\n      description: Get all subscription billing contract for the authenticated user.\n      parameters:\n        - in: path\n         \
  \ name: userID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: Show the subscription billing contract for the authenticated user.\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/BillingContractSubscriptionListing'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n\
  \            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: User\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-billing-contract-subscription-openapi-original.yml
tags:
- Billing
- Contracts
- Subscriptions
- Users
---
