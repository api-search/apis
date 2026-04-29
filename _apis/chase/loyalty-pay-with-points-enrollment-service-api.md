---
aid: chase:loyalty-pay-with-points-enrollment-service-api
baseURL: https://api.chase.com/loyalty/pay-with-points/enrollment
description: API that allows merchants and partners to enroll customer payment cards in the Chase Pay with Points program so points can be redeemed against future purchases.
humanURL: https://developer.chase.com/products/loyalty-pay-with-points-enrollment-service/
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Chase Loyalty Pay with Points Enrollment Service API
properties:
- type: Documentation
  url: https://developer.chase.com/products/loyalty-pay-with-points-enrollment-service/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-loyalty-pay-with-points-enrollment-service-api-openapi.yml
provider_name: Chase
provider_slug: chase
slug: loyalty-pay-with-points-enrollment-service-api
source_filename: chase-loyalty-pay-with-points-enrollment-service-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Chase Loyalty Pay with Points Enrollment Service API\n  description: >-\n    Enrollment service that registers customer payment cards in the Chase\n    Pay with Points program so points can be redeemed against future\n    purchases.\n  version: '1.0'\n  contact:\n    name: Chase Developer Support\n    url: https://developer.chase.com/support\nservers:\n  - url: https://api.chase.com/loyalty/pay-with-points/enrollment\n    description: Pay with Points Enrollment Production\ntags:\n  - name: Enrollments\nsecurity:\n  - oauth2: []\npaths:\n  /enrollments:\n    post:\n      operationId: createEnrollment\n      summary: Enroll a card in Pay with Points\n      tags: [Enrollments]\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              required: [cardToken, merchantId]\n              properties:\n                cardToken:\n                  type: string\n\
  \                merchantId:\n                  type: string\n                customerId:\n                  type: string\n      responses:\n        '201':\n          description: Enrollment created\n  /enrollments/{enrollmentId}:\n    get:\n      operationId: getEnrollment\n      summary: Get an enrollment record\n      tags: [Enrollments]\n      parameters:\n        - name: enrollmentId\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Enrollment\n    delete:\n      operationId: revokeEnrollment\n      summary: Revoke a Pay with Points enrollment\n      tags: [Enrollments]\n      parameters:\n        - name: enrollmentId\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '204':\n          description: Enrollment revoked\ncomponents:\n  securitySchemes:\n    oauth2:\n      type: oauth2\n      flows:\n        clientCredentials:\n\
  \          tokenUrl: https://api.chase.com/oauth2/token\n          scopes:\n            enrollments.write: Manage enrollments\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-loyalty-pay-with-points-enrollment-service-api-openapi.yml
tags:
- Loyalty
- Payments
- Rewards
---
