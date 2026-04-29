---
aid: bunq:bunq-user-transferwise-user-api
baseURL: ''
description: The Bunq User Transferwise User API allows Bunq users to seamlessly transfer money using Transferwise's platform. This API facilitates convenient, fast, and secure international money transfers for Bunq account holders, with the added benefit of Transferwise's competitive exchange rates and low fees. Users can easily initiate transfers, track their status, and manage their transactions directly within the Bunq app, making cross-border payments simpler and more efficient.
humanURL: ''
image: ''
layout: api
name: Bunq User Transferwise User API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-transferwise-user-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-user-transferwise-user-api
source_filename: bunq-user-userid-transferwise-user-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq user/{userID}/transferwise-user'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas:\n    TransferwiseUserCreate:\n      type: object\n      properties:\n        Id:\n          type: object\n          description: The id of the created item\n          readOnly: true\n          writeOnly: false\n          $ref: '#/components/schemas/BunqId'\npaths:\n  /user/{userID}/transferwise-user:\n    post:\n      tags:\n    \
  \    - User\n      summary: ''\n      operationId: CREATE_TransferwiseUser_for_User\n      description: Used to manage Transferwise users.\n      parameters:\n        - in: path\n          name: userID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      requestBody:\n        description: ''\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/TransferwiseUser'\n      responses:\n        '200':\n          description: Used to manage\
  \ Transferwise users.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TransferwiseUserCreate'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\n    get:\n      tags:\n        - User\n      summary: ''\n      operationId: List_all_TransferwiseUser_for_User\n      description: Used to manage Transferwise users.\n      parameters:\n        - in: path\n          name: userID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n\
  \        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: Used to manage Transferwise users.\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/TransferwiseUserListing'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\n\
  tags:\n  - name: User\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-transferwise-user-openapi-original.yml
tags:
- Transferwise
- Users
---
