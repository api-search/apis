---
aid: chase:account-aggregation-user-consent-api
baseURL: https://api.chase.com/aggregation/consent
description: Consent management API used to obtain, store, and revoke customer consent for sharing account information with authorized third-party data recipients. Implements the FDX consent model.
humanURL: https://developer.chase.com/products/aggregation-consent/
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Chase Account Aggregation User Consent API
properties:
- type: Documentation
  url: https://developer.chase.com/products/aggregation-consent/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-account-aggregation-user-consent-api-openapi.yml
provider_name: Chase
provider_slug: chase
slug: account-aggregation-user-consent-api
source_filename: chase-account-aggregation-user-consent-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Chase Account Aggregation User Consent API\n  description: >-\n    Consent management API for the Chase FDX aggregation platform.\n    Supports requesting, retrieving, updating, and revoking user consent\n    for sharing account data with authorized data recipients.\n  version: '1.0'\n  contact:\n    name: Chase Developer Support\n    url: https://developer.chase.com/support\nexternalDocs:\n  description: Account Aggregation User Consent\n  url: https://developer.chase.com/products/aggregation-consent/\nservers:\n  - url: https://api.chase.com/aggregation/consent\n    description: Chase Consent Production\ntags:\n  - name: Consents\nsecurity:\n  - oauth2: []\npaths:\n  /consents:\n    post:\n      operationId: createConsent\n      summary: Create a consent request\n      tags: [Consents]\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n\
  \                permissions:\n                  type: array\n                  items:\n                    type: string\n                expirationTime:\n                  type: string\n                  format: date-time\n      responses:\n        '201':\n          description: Consent created\n    get:\n      operationId: listConsents\n      summary: List consents\n      tags: [Consents]\n      responses:\n        '200':\n          description: Consents list\n  /consents/{consentId}:\n    get:\n      operationId: getConsent\n      summary: Get a consent record\n      tags: [Consents]\n      parameters:\n        - name: consentId\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Consent record\n    delete:\n      operationId: revokeConsent\n      summary: Revoke a consent\n      tags: [Consents]\n      parameters:\n        - name: consentId\n          in: path\n          required: true\n\
  \          schema:\n            type: string\n      responses:\n        '204':\n          description: Consent revoked\ncomponents:\n  securitySchemes:\n    oauth2:\n      type: oauth2\n      flows:\n        authorizationCode:\n          authorizationUrl: https://api.chase.com/oauth2/authorize\n          tokenUrl: https://api.chase.com/oauth2/token\n          scopes:\n            consents.write: Manage consents\n            consents.read: Read consents\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-account-aggregation-user-consent-api-openapi.yml
tags:
- Consent
- FDX
- Open Banking
---
