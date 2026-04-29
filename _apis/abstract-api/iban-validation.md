---
aid: abstract-api:iban-validation
baseURL: https://ibanvalidation.abstractapi.com/v1/
description: Determine the validity and details of International Bank Account Numbers (IBANs), including bank name, account type, and country code.
humanURL: https://www.abstractapi.com/api/iban-validation
image: ''
layout: api
name: IBAN Validation API
properties:
- type: Documentation
  url: https://docs.abstractapi.com/api/iban-validation.md
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-iban-validation.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/json-schema/iban-validation-iban-validation-response-schema.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/examples/iban-validation-iban-validation-response-example.json
provider_name: Abstract API
provider_slug: abstract-api
slug: iban-validation
source_filename: abstract-api-iban-validation.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Abstract API - IBAN Validation API\n  description: Determine the validity and details of International Bank Account Numbers (IBANs), including bank name, account type, and country code.\n  version: 1.0.0\n  contact:\n    url: https://www.abstractapi.com/\n  x-generated-from: documentation\nservers:\n  - url: https://ibanvalidation.abstractapi.com/v1\n    description: IBAN Validation API v1\nsecurity:\n  - apiKey: []\ntags:\n  - name: IBAN Validation\n    description: IBAN number validation operations\npaths:\n  /:\n    get:\n      operationId: validateIBAN\n      summary: Abstract API Validate IBAN\n      description: Validate an IBAN number and retrieve bank details, account type, and country information.\n      tags:\n        - IBAN Validation\n      parameters:\n        - name: api_key\n          in: query\n          required: true\n          description: Your unique API key for the IBAN Validation API.\n          schema:\n            type:\
  \ string\n          example: abc123def456\n        - name: iban\n          in: query\n          required: true\n          description: The IBAN to validate.\n          schema:\n            type: string\n          example: GB82WEST12345698765432\n      responses:\n        '200':\n          description: IBAN validation result\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/IBANValidationResponse'\n              examples:\n                validateIBAN200Example:\n                  summary: Default validateIBAN 200 response\n                  x-microcks-default: true\n                  value:\n                    iban: GB82WEST12345698765432\n                    is_valid: true\n                    country:\n                      code: GB\n                      name: United Kingdom\n                    bank:\n                      bank_name: Westpac Banking Corporation\n                      bank_code: WEST\n           \
  \           bic: WESTGB22\n                    account_number: 98765432\n                    check_digits: '82'\n                    sepa_member: true\n        '400':\n          description: Bad request\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '401':\n          description: Unauthorized\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: query\n      name: api_key\n  schemas:\n    IBANValidationResponse:\n      type: object\n      description: IBAN validation and enrichment response\n      properties:\n        iban:\n          type: string\n          description: The IBAN submitted for validation\n          example: GB82WEST12345698765432\n        is_valid:\n\
  \          type: boolean\n          description: Whether the IBAN is valid\n          example: true\n        country:\n          type: object\n          properties:\n            code:\n              type: string\n              description: ISO 3166-1 alpha-2 country code\n              example: GB\n            name:\n              type: string\n              description: Country name\n              example: United Kingdom\n        bank:\n          type: object\n          properties:\n            bank_name:\n              type: string\n              description: Name of the bank\n              example: Westpac Banking Corporation\n            bank_code:\n              type: string\n              description: Bank identifier code within the IBAN\n              example: WEST\n            bic:\n              type: string\n              description: Bank Identifier Code (BIC/SWIFT)\n              example: WESTGB22\n        account_number:\n          type: string\n          description: Account\
  \ number extracted from the IBAN\n          example: '98765432'\n        check_digits:\n          type: string\n          description: Check digits from the IBAN\n          example: '82'\n        sepa_member:\n          type: boolean\n          description: Whether the country is a SEPA member\n          example: true\n    ErrorResponse:\n      type: object\n      properties:\n        message:\n          type: string\n          example: The provided API key is invalid\n        error:\n          type: string\n          example: invalid_api_key\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-iban-validation.yaml
tags:
- IBAN Validation
- Finance
- Banking
---
