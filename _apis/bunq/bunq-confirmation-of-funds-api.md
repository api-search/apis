---
aid: bunq:bunq-confirmation-of-funds-api
baseURL: ''
description: Bunq Confirmation Of Funds API is a service that allows businesses to verify the availability of funds in a customer's account before processing a payment. This helps to reduce the risk of insufficient funds and associated fees, as well as providing peace of mind for both the business and the customer. By using this API, businesses can ensure that transactions will go through smoothly and efficiently, enhancing the overall customer experience.
humanURL: https://doc.bunq.com/#/confirmation-of-funds/CREATE_ConfirmationOfFunds_for_User
image: ''
layout: api
name: Bunq Confirmation of Funds API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-confirmation-of-funds-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-confirmation-of-funds-api
source_filename: bunq-user-userid-confirmation-of-funds-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq user/{userID}/confirmation-of-funds'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas:\n    ConfirmationOfFundsCreate:\n      type: object\n      properties:\n        Id:\n          type: object\n          description: The id of the created item\n          readOnly: true\n          writeOnly: false\n          $ref: '#/components/schemas/BunqId'\npaths:\n  /user/{userID}/confirmation-of-funds:\n    post:\n      tags:\n\
  \        - User\n      summary: ''\n      operationId: CREATE_ConfirmationOfFunds_for_User\n      description: Used to confirm availability of funds on an account.\n      parameters:\n        - in: path\n          name: userID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      requestBody:\n        description: ''\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/ConfirmationOfFunds'\n      responses:\n        '200':\n        \
  \  description: Used to confirm availability of funds on an account.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ConfirmationOfFundsCreate'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: User\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-confirmation-of-funds-openapi-original.yml
tags:
- Confirmation
- Funds
- Users
---
