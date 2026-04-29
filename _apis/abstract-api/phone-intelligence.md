---
aid: abstract-api:phone-intelligence
baseURL: https://phoneintelligence.abstractapi.com/v1/
description: Identify carrier, line type, validity, location, and get deep insights including line status, VoIP detection, and risk scoring for any phone number globally.
humanURL: https://www.abstractapi.com/api/phone-validation-api
image: ''
layout: api
name: Phone Intelligence API
properties:
- type: Documentation
  url: https://docs.abstractapi.com/api/phone-intelligence.md
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-phone-intelligence.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/json-schema/phone-intelligence-phone-country-schema.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/examples/phone-intelligence-phone-country-example.json
provider_name: Abstract API
provider_slug: abstract-api
slug: phone-intelligence
source_filename: abstract-api-phone-intelligence.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Abstract API - Phone Intelligence API\n  description: Identify carrier, line type, validity, location, and get deep insights including line status, VoIP detection, and risk scoring for any phone number globally.\n  version: 1.0.0\n  contact:\n    url: https://www.abstractapi.com/\n  x-generated-from: documentation\nservers:\n  - url: https://phoneintelligence.abstractapi.com/v1\n    description: Phone Intelligence API v1\nsecurity:\n  - apiKey: []\ntags:\n  - name: Phone Intelligence\n    description: Phone number validation and intelligence\npaths:\n  /:\n    get:\n      operationId: getPhoneIntelligence\n      summary: Abstract API Get Phone Intelligence\n      description: Validate a phone number and retrieve carrier, location, line type, VoIP status, and risk information.\n      tags:\n        - Phone Intelligence\n      parameters:\n        - name: api_key\n          in: query\n          description: Your unique API key for the Phone Intelligence\
  \ API.\n          required: true\n          schema:\n            type: string\n          example: abc123def456\n        - name: phone\n          in: query\n          description: The phone number to validate and analyze.\n          required: true\n          schema:\n            type: string\n          example: '+14155552671'\n        - name: country\n          in: query\n          description: ISO 3166-1 alpha-2 country code to specify the phone number origin.\n          required: false\n          schema:\n            type: string\n          example: US\n      responses:\n        '200':\n          description: Successful phone intelligence response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/PhoneIntelligenceResponse'\n              examples:\n                getPhoneIntelligence200Example:\n                  summary: Default getPhoneIntelligence 200 response\n                  x-microcks-default: true\n       \
  \           value:\n                    phone: '+14155552671'\n                    valid: true\n                    country:\n                      code: US\n                      name: United States\n                      prefix: '1'\n                    location: California\n                    type: mobile\n                    carrier: Verizon\n                    is_voip: false\n                    risk_score: 12\n        '400':\n          description: Bad request\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '401':\n          description: Unauthorized - invalid API key\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '429':\n          description: Rate limit exceeded\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n\
  \      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: query\n      name: api_key\n  schemas:\n    PhoneIntelligenceResponse:\n      type: object\n      description: Phone number intelligence response\n      properties:\n        phone:\n          type: string\n          description: The phone number in E.164 format\n          example: '+14155552671'\n        valid:\n          type: boolean\n          description: Whether the phone number is valid\n          example: true\n        country:\n          $ref: '#/components/schemas/PhoneCountry'\n        location:\n          type: string\n          description: Geographic location of the phone number\n          example: California\n        type:\n          type: string\n          description: Line type\n          example: mobile\n          enum:\n            - mobile\n            - landline\n            - voip\n            - toll_free\n      \
  \      - premium_rate\n            - shared_cost\n            - unknown\n        carrier:\n          type: string\n          description: Carrier or service provider\n          example: Verizon\n        is_voip:\n          type: boolean\n          description: Whether the number is a VoIP number\n          example: false\n        risk_score:\n          type: integer\n          description: Risk score from 0 (low risk) to 100 (high risk)\n          example: 12\n    PhoneCountry:\n      type: object\n      properties:\n        code:\n          type: string\n          description: ISO 3166-1 alpha-2 country code\n          example: US\n        name:\n          type: string\n          description: Country name\n          example: United States\n        prefix:\n          type: string\n          description: International dialing prefix\n          example: '1'\n    ErrorResponse:\n      type: object\n      properties:\n        message:\n          type: string\n          example: The provided\
  \ API key is invalid\n        error:\n          type: string\n          example: invalid_api_key\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-phone-intelligence.yaml
tags:
- Phone Validation
- Phone Intelligence
- Fraud Detection
---
