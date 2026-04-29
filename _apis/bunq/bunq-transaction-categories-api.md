---
aid: bunq:bunq-transaction-categories-api
baseURL: https://public-api.sandbox.bunq.com/
description: The Bunq Transaction Categories API is a tool that allows users to easily categorize their transactions based on various criteria. This API assists in sorting transactions into specific categories such as groceries, dining, entertainment, and more, making it easier for users to track and manage their spending habits. By integrating this API into their platforms, users can get a better understanding of where their money is being spent and make more informed financial decisions.
humanURL: https://doc.bunq.com/#/additional-transaction-information-category
image: ''
layout: api
name: Bunq Transaction Categories API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-additional-transaction-information-category-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-transaction-categories-api
source_filename: bunq-user-userid-additional-transaction-information-category-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq user/{userID}/additional-transaction-information-category'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas:\n    AdditionalTransactionInformationCategoryUserDefinedCreate:\n      type: object\n      properties:\n        Id:\n          type: object\n          description: The id of the created item\n          readOnly: true\n          writeOnly: false\n          $ref: '#/components/schemas/BunqId'\npaths:\n  /user/{userID}/additional-transaction-information-category:\n\
  \    get:\n      tags:\n        - User\n      summary: ''\n      operationId: List_all_AdditionalTransactionInformationCategory_for_User\n      description: Get the available categories.\n      parameters:\n        - in: path\n          name: userID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: Get the available categories.\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n     \
  \             $ref: >-\n                    #/components/schemas/AdditionalTransactionInformationCategoryListing\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\n  /user/{userID}/additional-transaction-information-category-user-defined:\n    post:\n      tags:\n        - User\n      summary: ''\n      operationId: CREATE_AdditionalTransactionInformationCategoryUserDefined_for_User\n      description: Manage user-defined categories.\n      parameters:\n        - in: path\n          name: userID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n\
  \        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      requestBody:\n        description: ''\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: >-\n                #/components/schemas/AdditionalTransactionInformationCategoryUserDefined\n      responses:\n        '200':\n          description: Manage user-defined categories.\n          content:\n            application/json:\n              schema:\n                $ref: >-\n                  #/components/schemas/AdditionalTransactionInformationCategoryUserDefinedCreate\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n\
  \            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: User\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-additional-transaction-information-category-openapi-original.yml
tags:
- Additional
- Categories
- Defined
- Information
- Transactions
- Users
---
