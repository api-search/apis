---
aid: bunq:bunq-user-company-user-company-name-api
baseURL: ''
description: The Bunq User Company User Company Name API is a powerful tool that allows businesses to seamlessly integrate Bunq's banking services into their own applications and systems. With this API, companies can access a wide range of features, including real-time payment processing, account management, and transaction tracking.
humanURL: ''
image: ''
layout: api
name: Bunq User Company User Company Name API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-company-user-companyid-name-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-user-company-user-company-name-api
source_filename: bunq-user-company-user-companyid-name-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq user-company/{user-companyID}/name'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths:\n  /user-company/{user-companyID}/name:\n    get:\n      tags:\n        - User Company\n      summary: ''\n      operationId: List_all_Name_for_UserCompany\n      description: Return all the known (trade) names for a specific user company.\n      parameters:\n        - in: path\n          name: user-companyID\n     \
  \     description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: >-\n            Endpoint for getting all the known (trade) names for a user company.\n            This is needed for updating the user name, as we only accept legal\n            or trade names.\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/UserCompanyNameListing'\n          headers:\n     \
  \       X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: User Company\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-company-user-companyid-name-openapi-original.yml
tags:
- Companies
- Names
- Users
---
