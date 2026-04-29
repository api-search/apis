---
aid: at-t-developer-hub:att-number-verification-api
baseURL: https://api.att.com
description: CAMARA-standard API enabling seamless device authentication via the mobile network. Verifies that a device is currently using a specific phone number without requiring the user to enter an OTP, leveraging the AT&T network signal for frictionless identity verification in mobile applications.
humanURL: https://devex-web.att.com/developer-hub/
image: ''
layout: api
name: AT&T Number Verification API
properties:
- type: Documentation
  url: https://devex-web.att.com/developer-hub/
- type: GettingStarted
  url: https://devex-web.att.com/developer-hub/docs/network-api-accelerator-program
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/at-t-developer-hub/refs/heads/main/openapi/at-t-developer-hub-number-verification-api.yaml
provider_name: AT&T Developer Hub
provider_slug: at-t-developer-hub
slug: att-number-verification-api
source_filename: at-t-developer-hub-number-verification-api.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: AT&T Number Verification API\n  description: >-\n    CAMARA-standard API enabling seamless device authentication via the mobile\n    network. Verifies that a device is currently using a specific phone number\n    without requiring the user to enter an OTP, leveraging the AT&T network\n    signal for frictionless identity verification. Part of the AT&T Network API\n    Accelerator Program.\n  version: '1.0'\n  contact:\n    url: https://devex-web.att.com/developer-hub/docs/network-api-accelerator-program\n  termsOfService: https://www.att.com/gen/general?pid=11561\n  x-generated-from: documentation\n  x-last-validated: '2026-04-19'\nservers:\n  - url: https://api.att.com/camara/number-verification/v1\n    description: AT&T CAMARA Number Verification API endpoint\npaths:\n  /verify:\n    post:\n      operationId: verifyPhoneNumber\n      summary: AT&T Verify Phone Number\n      description: >-\n        Verify that the device making the request\
  \ is associated with the provided\n        phone number. The verification is performed silently using the mobile\n        network connection without requiring the user to enter a code, providing\n        frictionless authentication for mobile applications.\n      tags:\n        - Number Verification\n      security:\n        - oauth2: []\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/NumberVerificationRequest'\n            examples:\n              VerifyPhoneNumberRequestExample:\n                summary: Default verifyPhoneNumber request\n                x-microcks-default: true\n                value:\n                  phoneNumber: '+12125551234'\n      responses:\n        '200':\n          description: Number verification result\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/NumberVerificationResponse'\n\
  \              examples:\n                VerifyPhoneNumber200Example:\n                  summary: Default verifyPhoneNumber 200 response\n                  x-microcks-default: true\n                  value:\n                    devicePhoneNumberVerified: true\n        '400':\n          description: Bad request - invalid phone number format\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorInfo'\n        '401':\n          description: Unauthorized - invalid or missing token\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorInfo'\n        '403':\n          description: Forbidden - insufficient scope\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorInfo'\n        '404':\n          description: Phone number not found\n          content:\n            application/json:\n\
  \              schema:\n                $ref: '#/components/schemas/ErrorInfo'\n        '429':\n          description: Too many requests\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorInfo'\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    oauth2:\n      type: oauth2\n      description: AT&T OAuth 2.0 for CAMARA network APIs\n      flows:\n        clientCredentials:\n          tokenUrl: https://api.att.com/oauth/v4/token\n          scopes: {}\n  schemas:\n    NumberVerificationRequest:\n      type: object\n      required:\n        - phoneNumber\n      properties:\n        phoneNumber:\n          type: string\n          description: Phone number in E.164 format to verify against the requesting device\n          example: '+12125551234'\n    NumberVerificationResponse:\n      type: object\n      properties:\n        devicePhoneNumberVerified:\n    \
  \      type: boolean\n          description: >-\n            True if the device's network connection matches the provided phone\n            number, false otherwise.\n          example: true\n    ErrorInfo:\n      type: object\n      properties:\n        status:\n          type: integer\n          description: HTTP status code\n          example: 400\n        code:\n          type: string\n          description: CAMARA error code\n          example: INVALID_ARGUMENT\n        message:\n          type: string\n          description: Human-readable error message\n          example: Invalid phone number format. Must be E.164.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/at-t-developer-hub/refs/heads/main/openapi/at-t-developer-hub-number-verification-api.yaml
tags:
- Number Verification
- Authentication
- Identity
- CAMARA
- Mobile
---
