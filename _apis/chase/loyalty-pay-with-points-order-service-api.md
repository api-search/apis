---
aid: chase:loyalty-pay-with-points-order-service-api
baseURL: https://api.chase.com/loyalty/pay-with-points/orders
description: API that lets merchants accept Chase Ultimate Rewards points as payment at checkout. Supports order creation, redemption, capture, refund, and reversal flows for the Pay with Points program.
humanURL: https://developer.chase.com/products/loyalty-pay-with-points-order-service/
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Chase Loyalty Pay with Points Order Service API
properties:
- type: Documentation
  url: https://developer.chase.com/products/loyalty-pay-with-points-order-service/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-loyalty-pay-with-points-order-service-api-openapi.yml
provider_name: Chase
provider_slug: chase
slug: loyalty-pay-with-points-order-service-api
source_filename: chase-loyalty-pay-with-points-order-service-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Chase Loyalty Pay with Points Order Service API\n  description: >-\n    Order service that lets merchants redeem Chase Ultimate Rewards points\n    against purchases. Supports order creation, capture, refund, and\n    reversal flows.\n  version: '1.0'\n  contact:\n    name: Chase Developer Support\n    url: https://developer.chase.com/support\nservers:\n  - url: https://api.chase.com/loyalty/pay-with-points/orders\n    description: Pay with Points Production\ntags:\n  - name: Orders\n  - name: Refunds\nsecurity:\n  - oauth2: []\npaths:\n  /orders:\n    post:\n      operationId: createOrder\n      summary: Create a Pay with Points order\n      tags: [Orders]\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              required: [cardToken, merchantId, amount]\n              properties:\n                cardToken:\n                  type: string\n    \
  \            merchantId:\n                  type: string\n                amount:\n                  type: number\n                pointsToRedeem:\n                  type: integer\n                currency:\n                  type: string\n      responses:\n        '201':\n          description: Order created\n  /orders/{orderId}:\n    get:\n      operationId: getOrder\n      summary: Get a Pay with Points order\n      tags: [Orders]\n      parameters:\n        - name: orderId\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Order details\n  /orders/{orderId}/capture:\n    post:\n      operationId: captureOrder\n      summary: Capture a Pay with Points order\n      tags: [Orders]\n      parameters:\n        - name: orderId\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Order captured\n \
  \ /orders/{orderId}/refunds:\n    post:\n      operationId: refundOrder\n      summary: Refund a Pay with Points order\n      tags: [Refunds]\n      parameters:\n        - name: orderId\n          in: path\n          required: true\n          schema:\n            type: string\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                amount:\n                  type: number\n                reason:\n                  type: string\n      responses:\n        '201':\n          description: Refund issued\n  /orders/{orderId}/reverse:\n    post:\n      operationId: reverseOrder\n      summary: Reverse a Pay with Points order\n      tags: [Orders]\n      parameters:\n        - name: orderId\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Order reversed\ncomponents:\n  securitySchemes:\n\
  \    oauth2:\n      type: oauth2\n      flows:\n        clientCredentials:\n          tokenUrl: https://api.chase.com/oauth2/token\n          scopes:\n            orders.write: Create and modify orders\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-loyalty-pay-with-points-order-service-api-openapi.yml
tags:
- Loyalty
- Payments
- Rewards
---
