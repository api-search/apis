---
aid: asana:asana-batch-api
baseURL: ''
description: Asana Batch API is a tool that allows users to perform multiple operations in Asana in a single request. This API enables users to efficiently manage and organize tasks, projects, and workflows by allowing them to make multiple updates or queries at once. By batching requests, users can streamline their workflow, reduce the number of API calls needed, and improve overall performance.
humanURL: https://developers.asana.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Asana Batch  API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/asana/refs/heads/main/openapi/asana-batch-api-openapi.yml
- type: Documentation
  url: https://developers.asana.com/reference/batch-api
provider_name: Asana
provider_slug: asana
slug: asana-batch-api
source_filename: asana-batch-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Asana Batch API\n  description: >-\n    The Asana Batch API enables developers to perform multiple actions by making\n    only a single HTTP request. The maximum number of actions allowed in a\n    single batch request is 10. Actions are dispatched in parallel.\n  version: '1.0'\n  termsOfService: https://asana.com/terms\n  contact:\n    name: Asana Support\n    url: https://asana.com/support\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0\nservers:\n  - url: https://app.asana.com/api/1.0\n    description: Main endpoint.\nsecurity:\n  - personalAccessToken: []\n  - oauth2: []\ntags:\n  - name: Batch API\n    description: Perform multiple operations in a single HTTP request.\npaths:\n  /batch:\n    post:\n      summary: Asana Submit parallel requests\n      description: >-\n        Make multiple API requests in a single call. The maximum number of\n        actions allowed in a single batch request is 10.\n\
  \      operationId: createBatchRequest\n      tags:\n        - Batch API\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                data:\n                  type: object\n                  properties:\n                    actions:\n                      type: array\n                      items:\n                        $ref: '#/components/schemas/BatchRequestAction'\n              required:\n                - data\n      responses:\n        '200':\n          description: Successfully completed the batch request.\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    type: array\n                    items:\n                      $ref: '#/components/schemas/BatchResponse'\n        '400':\n          description: Bad request.\n        '401':\n \
  \         description: Unauthorized.\n        '403':\n          description: Forbidden.\n        '429':\n          description: Too many requests.\n        '500':\n          description: Internal server error.\ncomponents:\n  securitySchemes:\n    personalAccessToken:\n      type: http\n      scheme: bearer\n    oauth2:\n      type: oauth2\n      flows:\n        authorizationCode:\n          authorizationUrl: https://app.asana.com/-/oauth_authorize\n          tokenUrl: https://app.asana.com/-/oauth_token\n          scopes:\n            default: Provides access to all endpoints documented in the API reference.\n  schemas:\n    BatchRequestAction:\n      type: object\n      properties:\n        relative_path:\n          type: string\n          description: The path of the desired endpoint relative to the API's base URL.\n          example: /tasks/123\n        method:\n          type: string\n          description: The HTTP method for the action.\n          enum:\n            - get\n    \
  \        - post\n            - put\n            - delete\n            - patch\n          example: get\n        data:\n          type: object\n          description: For POST/PUT requests, an object containing the data for the action.\n        options:\n          type: object\n          description: Pagination and other options for the action.\n          properties:\n            limit:\n              type: integer\n            offset:\n              type: string\n            fields:\n              type: array\n              items:\n                type: string\n      required:\n        - relative_path\n        - method\n    BatchResponse:\n      type: object\n      properties:\n        status_code:\n          type: integer\n          description: The HTTP status code for the individual action.\n          example: 200\n        headers:\n          type: object\n          description: HTTP headers for the individual action.\n        body:\n          type: object\n          description: The\
  \ body of the response for the individual action.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/asana/refs/heads/main/openapi/asana-batch-api-openapi.yml
tags: []
---
