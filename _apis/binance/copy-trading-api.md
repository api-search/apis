---
aid: binance:copy-trading-api
baseURL: https://api.binance.com
description: The Binance Copy Trading API allows developers to interact with the copy trading platform where users can automatically replicate the trades of experienced lead traders. The API provides endpoints for managing copy trading positions, querying lead trader portfolios and performance metrics, and configuring copy trading parameters such as investment amount and risk limits. It supports both futures copy trading for automated portfolio mirroring.
humanURL: https://developers.binance.com/docs/copy_trading/general-info
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Binance Copy Trading API
properties:
- type: Documentation
  url: https://developers.binance.com/docs/copy_trading/general-info
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/binance/refs/heads/main/openapi/binance-copy-trading-openapi.yml
provider_name: Binance
provider_slug: binance
slug: copy-trading-api
source_filename: binance-copy-trading-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Binance Copy Trading API\n  description: >-\n    The Binance Copy Trading API allows developers to interact with the\n    copy trading platform where users can automatically replicate the\n    trades of experienced lead traders. The API provides endpoints for\n    managing copy trading positions, querying lead trader portfolios and\n    performance metrics, and configuring copy trading parameters.\n  version: '1'\n  contact:\n    name: Binance Support\n    url: https://www.binance.com/en/support\n  termsOfService: https://www.binance.com/en/terms\nexternalDocs:\n  description: Binance Copy Trading Documentation\n  url: https://developers.binance.com/docs/copy_trading/general-info\nservers:\n  - url: https://api.binance.com\n    description: Production Server\ntags:\n  - name: Copy Trading\n    description: >-\n      Copy trading position and portfolio management endpoints.\nsecurity:\n  - apiKey: []\npaths:\n  /sapi/v1/copy-trading/futures/userStatus:\n\
  \    get:\n      operationId: getUserStatus\n      summary: Get copy trading user status\n      description: >-\n        Get the copy trading status of the current user.\n      tags:\n        - Copy Trading\n      parameters:\n        - name: recvWindow\n          in: query\n          schema:\n            type: integer\n        - name: timestamp\n          in: query\n          required: true\n          schema:\n            type: integer\n            format: int64\n        - name: signature\n          in: query\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Success\n          content:\n            application/json:\n              schema:\n                type: object\n      security:\n        - apiKey: []\n          hmacSignature: []\n  /sapi/v1/copy-trading/futures/leadSymbol:\n    get:\n      operationId: getLeadSymbols\n      summary: Get lead trading symbol whitelist\n      description: >-\n        Get\
  \ the list of symbols available for lead trading.\n      tags:\n        - Copy Trading\n      parameters:\n        - name: recvWindow\n          in: query\n          schema:\n            type: integer\n        - name: timestamp\n          in: query\n          required: true\n          schema:\n            type: integer\n            format: int64\n        - name: signature\n          in: query\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Success\n          content:\n            application/json:\n              schema:\n                type: object\n      security:\n        - apiKey: []\n          hmacSignature: []\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: header\n      name: X-MBX-APIKEY\n    hmacSignature:\n      type: apiKey\n      in: query\n      name: signature\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/binance/refs/heads/main/openapi/binance-copy-trading-openapi.yml
tags:
- Copy Trading
- Cryptocurrency
- Social Trading
- Trading
---
