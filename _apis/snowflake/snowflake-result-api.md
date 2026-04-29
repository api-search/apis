---
aid: snowflake:snowflake-result-api
baseURL: ''
description: The Snowflake Result API is a REST API that you can use to check request status and fetch request response.
humanURL: ''
image: ''
layout: api
name: Snowflake Result API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/snowflake/refs/heads/main/openapi/result.yaml
- type: Documentation
  url: https://docs.snowflake.com/en/developer-guide/snowflake-rest-api/reference/result
provider_name: Snowflake
provider_slug: snowflake
slug: snowflake-result-api
source_filename: result.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\nservers:\n- description: Snowflake Result API\n  url: https://org-account.snowflakecomputing.com\ninfo:\n  version: 0.0.1\n  title: Snowflake Result API\n  description: The Snowflake Result API is a REST API that you can use to check request status and fetch request response.\n  contact:\n    name: Snowflake, Inc.\n    url: https://snowflake.com\n    email: support@snowflake.com\npaths:\n  /api/v2/results/{result_handler}:\n    get:\n      summary: Check Result Status or Fetch Request\n      tags:\n      - result\n      description: Get result status or the result when it is ready.\n      operationId: fetchResult\n      parameters:\n      - name: result_handler\n        in: path\n        required: true\n        schema:\n          type: string\n        description: The opaque result id.\n        example: example_value\n      - name: page\n        in: query\n        required: false\n        schema:\n          type: integer\n          format: int64\n          minimum:\
  \ 0\n          default: 0\n        description: Number of the page of results to return. The number can range from 0 to the total number of pages minus 1.\n        example: 10\n      responses:\n        '200':\n          description: successful\n          headers:\n            X-Snowflake-Request-ID:\n              $ref: common.yaml#/components/headers/X-Snowflake-Request-ID\n            Link:\n              $ref: common.yaml#/components/headers/Link\n          content:\n            application/json:\n              examples:\n                Fetchresult200Example:\n                  summary: Default fetchResult 200 response\n                  x-microcks-default: true\n                  value: {}\n        '202':\n          $ref: common.yaml#/components/responses/202SuccessAcceptedResponse\n        '400':\n          $ref: common.yaml#/components/responses/400BadRequest\n        '401':\n          $ref: common.yaml#/components/responses/401Unauthorized\n        '403':\n          $ref: common.yaml#/components/responses/403Forbidden\n\
  \        '404':\n          $ref: common.yaml#/components/responses/404NotFound\n        '405':\n          $ref: common.yaml#/components/responses/405MethodNotAllowed\n        '408':\n          $ref: common.yaml#/components/responses/408RequestTimeout\n        '409':\n          $ref: common.yaml#/components/responses/409Conflict\n        '500':\n          $ref: common.yaml#/components/responses/500InternalServerError\n        '503':\n          $ref: common.yaml#/components/responses/503ServiceUnavailable\n        '504':\n          $ref: common.yaml#/components/responses/504GatewayTimeout\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    KeyPair:\n      $ref: common.yaml#/components/securitySchemes/KeyPair\n    ExternalOAuth:\n      $ref: common.yaml#/components/securitySchemes/ExternalOAuth\n    SnowflakeOAuth:\n      $ref: common.yaml#/components/securitySchemes/SnowflakeOAuth\nsecurity:\n- KeyPair: []\n- ExternalOAuth: []\n\
  - SnowflakeOAuth: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/snowflake/refs/heads/main/openapi/result.yaml
tags:
- Query Results
- SQL
---
