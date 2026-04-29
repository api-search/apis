---
aid: chase:rewards-balance-api
baseURL: https://api.chase.com/loyalty/rewards-balance
description: API that allows merchant and partner systems to retrieve a Chase cardholder's current rewards points balance for use in loyalty experiences and Pay with Points checkouts.
humanURL: https://developer.chase.com/products/rewards-balance-api/
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Chase Rewards Balance API
properties:
- type: Documentation
  url: https://developer.chase.com/products/rewards-balance-api/specification
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-rewards-balance-api-openapi.yml
provider_name: Chase
provider_slug: chase
slug: rewards-balance-api
source_filename: chase-rewards-balance-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Chase Rewards Balance API\n  description: >-\n    Retrieves a Chase cardholder's current Ultimate Rewards points\n    balance for use in loyalty experiences and Pay with Points checkouts.\n  version: '1.0'\n  contact:\n    name: Chase Developer Support\n    url: https://developer.chase.com/support\nexternalDocs:\n  description: Rewards Balance API Specification\n  url: https://developer.chase.com/products/rewards-balance-api/specification\nservers:\n  - url: https://api.chase.com/loyalty/rewards-balance\n    description: Chase Loyalty Production\ntags:\n  - name: Rewards Balance\nsecurity:\n  - oauth2: []\npaths:\n  /balances:\n    post:\n      operationId: getRewardsBalance\n      summary: Retrieve a rewards balance for a tokenized card\n      tags: [Rewards Balance]\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              required: [cardToken]\n\
  \              properties:\n                cardToken:\n                  type: string\n                  description: PCI-compliant card token issued by Chase.\n                merchantId:\n                  type: string\n      responses:\n        '200':\n          description: Rewards balance\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  cardToken:\n                    type: string\n                  pointsBalance:\n                    type: integer\n                  cashValue:\n                    type: number\n                  currency:\n                    type: string\ncomponents:\n  securitySchemes:\n    oauth2:\n      type: oauth2\n      flows:\n        clientCredentials:\n          tokenUrl: https://api.chase.com/oauth2/token\n          scopes:\n            rewards.read: Read rewards balances\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-rewards-balance-api-openapi.yml
tags:
- Loyalty
- Rewards
---
