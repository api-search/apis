---
aid: chase:loyalty-pci-merchant-relationship-manager-api
baseURL: https://api.chase.com/loyalty/merchant-relationship-manager
description: API for managing PCI-compliant merchant relationships for the Chase loyalty platform, supporting onboarding, profile updates, and configuration of merchant integrations.
humanURL: https://developer.chase.com/products/loyalty-pci-merchant-relation-manager/
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Chase Loyalty PCI Merchant Relationship Manager API
properties:
- type: Documentation
  url: https://developer.chase.com/products/loyalty-pci-merchant-relation-manager/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-loyalty-pci-merchant-relationship-manager-api-openapi.yml
provider_name: Chase
provider_slug: chase
slug: loyalty-pci-merchant-relationship-manager-api
source_filename: chase-loyalty-pci-merchant-relationship-manager-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Chase Loyalty PCI Merchant Relationship Manager API\n  description: >-\n    PCI-compliant merchant management API for the Chase loyalty platform.\n    Used to onboard merchants, update merchant profiles, and configure\n    integration settings for Pay with Points and Rewards Balance products.\n  version: '1.0'\n  contact:\n    name: Chase Developer Support\n    url: https://developer.chase.com/support\nservers:\n  - url: https://api.chase.com/loyalty/merchant-relationship-manager\n    description: Merchant Relationship Manager Production\ntags:\n  - name: Merchants\nsecurity:\n  - oauth2: []\npaths:\n  /merchants:\n    post:\n      operationId: createMerchant\n      summary: Onboard a new merchant\n      tags: [Merchants]\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              required: [name, mcc]\n              properties:\n                name:\n\
  \                  type: string\n                mcc:\n                  type: string\n                  description: Merchant category code.\n                contact:\n                  type: object\n      responses:\n        '201':\n          description: Merchant created\n    get:\n      operationId: listMerchants\n      summary: List merchants\n      tags: [Merchants]\n      responses:\n        '200':\n          description: Merchant list\n  /merchants/{merchantId}:\n    get:\n      operationId: getMerchant\n      summary: Get merchant details\n      tags: [Merchants]\n      parameters:\n        - name: merchantId\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Merchant details\n    put:\n      operationId: updateMerchant\n      summary: Update merchant details\n      tags: [Merchants]\n      parameters:\n        - name: merchantId\n          in: path\n          required: true\n   \
  \       schema:\n            type: string\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n      responses:\n        '200':\n          description: Merchant updated\ncomponents:\n  securitySchemes:\n    oauth2:\n      type: oauth2\n      flows:\n        clientCredentials:\n          tokenUrl: https://api.chase.com/oauth2/token\n          scopes:\n            merchants.write: Manage merchants\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chase/refs/heads/main/openapi/chase-loyalty-pci-merchant-relationship-manager-api-openapi.yml
tags:
- Loyalty
- Merchants
- PCI
---
