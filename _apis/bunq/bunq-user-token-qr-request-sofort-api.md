---
aid: bunq:bunq-user-token-qr-request-sofort-api
baseURL: ''
description: The Bunq User Token Qr Request Sofort API is a tool that allows users to generate QR codes for requesting payment tokens in real-time. This API enables users to quickly and easily create secure payment requests using a unique token system. By simply scanning the QR code with their mobile device, customers can instantly authorize transactions and complete payments without the need for manual input or data entry.
humanURL: ''
image: ''
layout: api
name: Bunq User Token Qr Request Sofort API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-token-qr-request-sofort-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-user-token-qr-request-sofort-api
source_filename: bunq-user-userid-token-qr-request-sofort-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq user/{userID}/token-qr-request-sofort'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas:\n    TokenQrRequestSofortCreate:\n      type: object\n      properties:\n        Id:\n          type: object\n          description: The id of the created item\n          readOnly: true\n          writeOnly: false\n          $ref: '#/components/schemas/BunqId'\npaths:\n  /user/{userID}/token-qr-request-sofort:\n    post:\n \
  \     tags:\n        - User\n      summary: ''\n      operationId: CREATE_TokenQrRequestSofort_for_User\n      description: Create a request from an SOFORT transaction.\n      parameters:\n        - in: path\n          name: userID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      requestBody:\n        description: ''\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/TokenQrRequestSofort'\n      responses:\n        '200':\n  \
  \        description: >-\n            Using this call you can create a SOFORT Request assigned to your\n            User by providing the Token of the request.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TokenQrRequestSofortCreate'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: User\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-token-qr-request-sofort-openapi-original.yml
tags:
- Tokens
- Users
---
