---
aid: bunq:bunq-payment-service-provider-credential-api
baseURL: ''
description: The Bunq Payment Service Provider Credential API allows businesses to securely link their payment service provider accounts with their Bunq accounts, enabling seamless and efficient payment processing. This API provides businesses with a secure method of accessing and managing their payment service provider credentials, allowing for easy integration with their existing payment infrastructure.
humanURL: ''
image: ''
layout: api
name: Bunq Payment Service Provider Credential API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-payment-service-provider-credential--openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-payment-service-provider-credential-api
source_filename: bunq-payment-service-provider-credential--openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq payment-service-provider-credential/'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas:\n    PaymentServiceProviderCredentialRead:\n      type: object\n      properties:\n        id:\n          type: integer\n          description: The id of the credential.\n          readOnly: true\n          writeOnly: false\n        created:\n          type: string\n          description: The timestamp of the credential object's\
  \ creation.\n          readOnly: true\n          writeOnly: false\n        updated:\n          type: string\n          description: The timestamp of the credential object's last update.\n          readOnly: true\n          writeOnly: false\n        status:\n          type: string\n          description: The status of the credential.\n          readOnly: true\n          writeOnly: false\n        expiry_time:\n          type: string\n          description: 'When the status is PENDING_FIRST_USE: when the credential expires.'\n          readOnly: true\n          writeOnly: false\n        token_value:\n          type: string\n          description: 'When the status is PENDING_FIRST_USE: the value of the token.'\n          readOnly: true\n          writeOnly: false\n        permitted_device:\n          type: object\n          description: >-\n            When the status is ACTIVE: the details of the device that may use\n            the credential.\n          readOnly: true\n          writeOnly:\
  \ false\n          $ref: '#/components/schemas/PermittedDevice'\npaths:\n  /payment-service-provider-credential/{itemId}:\n    get:\n      tags:\n        - Payment Service Provider Credential\n      summary: ''\n      operationId: READ_PaymentServiceProviderCredential\n      description: Register a Payment Service Provider and provide credentials\n      parameters:\n        - in: path\n          name: itemId\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: Register\
  \ a Payment Service Provider and provide credentials\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/PaymentServiceProviderCredentialRead'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: Payment Service Provider Credential\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-payment-service-provider-credential--openapi-original.yml
tags:
- Credentials
- Er
- Items
- Payments
- Prov
- Providers
---
