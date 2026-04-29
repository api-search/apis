---
aid: figma:figma-api
baseURL: https://api.figma.com
description: Figma allows designers to create and prototype their digital experiences - together in real-time and in one place - helping them turn their ideas and visions into products, faster. Figma's mission is to make design accessible to everyone. The Figma API is one of the ways we aim to do that.
humanURL: https://www.figma.com/developers
image: https://www.figma.com/favicon.ico
layout: api
name: Figma API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-api-openapi.yml
- title: Figma REST API
  type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-rest-api-openapi.yml
- type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/asyncapi/figma-webhooks-asyncapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-file-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-component-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-user-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-error-response-payload-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-schema/figma-get-me-response-body-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-structure/figma-get-me-response-body-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-structure/figma-error-response-payload-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-structure/figma-user-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/json-ld/figma-context.jsonld
- type: Documentation
  url: https://developers.figma.com/docs/rest-api/
provider_name: Figma
provider_slug: figma
slug: figma-api
source_filename: figma-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Figma API\n  version: 0.21.0\n  description: >-\n    This is the OpenAPI specification for the [Figma REST\n    API](https://www.figma.com/developers/api).\n\n    Note: we are releasing the OpenAPI specification as a beta given the large\n    surface area and complexity of the REST API. If you notice any inaccuracies\n    with the specification, please [file an\n    issue](https://github.com/figma/rest-api-spec/issues).\n  termsOfService: https://www.figma.com/developer-terms/\n  contact:\n    email: support@figma.com\nservers:\n- url: https://api.figma.com\n  description: Figma Production API Server\ntags:\n- name: Users\n  description: Operations related to user information and authentication\npaths:\n  /v1/me:\n    get:\n      tags:\n      - Users\n      summary: Figma Get Current User\n      security:\n      - PersonalAccessToken: []\n      - OAuth2:\n        - files:read\n      description: Returns the user information for the currently\
  \ authenticated user.\n      operationId: getMe\n      x-microcks-operation:\n        dispatcher: FALLBACK\n        dispatcherRules: |\n          {\n            \"dispatcher\": \"FALLBACK\",\n            \"fallback\": \"GetMeSuccessExample\"\n          }\n      responses:\n        '200':\n          $ref: '#/components/responses/GetMeResponse'\n        '403':\n          $ref: '#/components/responses/ForbiddenErrorResponse'\n        '429':\n          $ref: '#/components/responses/TooManyRequestsErrorResponse'\n        '500':\n          $ref: '#/components/responses/InternalServerErrorResponse'\ncomponents:\n  securitySchemes:\n    PersonalAccessToken:\n      type: http\n      scheme: bearer\n      bearerFormat: Figma Personal Access Token\n      description: Personal Access Token for authentication\n    OAuth2:\n      type: oauth2\n      flows:\n        authorizationCode:\n          authorizationUrl: https://www.figma.com/oauth\n          tokenUrl: https://api.figma.com/v1/oauth/token\n\
  \          scopes:\n            files:read: Read files\n  responses:\n    GetMeResponse:\n      description: Response from the GET /v1/me endpoint.\n      content:\n        application/json:\n          schema:\n            $ref: '#/components/schemas/GetMeResponseBody'\n          examples:\n            GetMeSuccessExample:\n              $ref: '#/components/examples/GetMeSuccessExample'\n    ForbiddenErrorResponse:\n      description: >-\n        The request was valid, but the server is refusing action. The user might\n        not have the necessary permissions for a resource.\n      content:\n        application/json:\n          schema:\n            $ref: '#/components/schemas/ErrorResponsePayload'\n          examples:\n            ForbiddenExample:\n              $ref: '#/components/examples/ForbiddenExample'\n    TooManyRequestsErrorResponse:\n      description: >-\n        API requests may be throttled or rate limited. Please wait a while\n        before attempting the request again.\n\
  \      content:\n        application/json:\n          schema:\n            $ref: '#/components/schemas/ErrorResponsePayload'\n          examples:\n            TooManyRequestsExample:\n              $ref: '#/components/examples/TooManyRequestsExample'\n    InternalServerErrorResponse:\n      description: An internal server error occurred.\n      content:\n        application/json:\n          schema:\n            $ref: '#/components/schemas/ErrorResponsePayload'\n          examples:\n            InternalServerErrorExample:\n              $ref: '#/components/examples/InternalServerErrorExample'\n  schemas:\n    GetMeResponseBody:\n      allOf:\n      - $ref: '#/components/schemas/User'\n      - type: object\n        properties:\n          email:\n            type: string\n            description: >-\n              Email associated with the user's account. This property is\n              only present on the /v1/me endpoint.\n        required:\n        - email\n    User:\n      type: object\n\
  \      description: A description of a user.\n      properties:\n        id:\n          type: string\n          description: Unique stable id of the user.\n          example: abc123\n        handle:\n          type: string\n          description: Name of the user.\n          example: example_value\n        imgUrl:\n          type: string\n          description: URL link to the user's profile image.\n          example: https://www.example.com\n      required:\n      - id\n      - handle\n      - imgUrl\n    ErrorResponsePayload:\n      type: object\n      description: A response indicating an error occurred.\n      properties:\n        status:\n          type: number\n          description: Status code\n          example: 42.5\n        err:\n          type: string\n          description: A string describing the error\n          example: example_value\n      required:\n      - status\n      - err\n  examples:\n    GetMeSuccessExample:\n      summary: Successful user profile response\n  \
  \    value:\n        id: \"1234567890\"\n        handle: \"John Doe\"\n        imgUrl: \"https://s3-alpha.figma.com/profile/1234567890\"\n        email: \"john.doe@example.com\"\n    ForbiddenExample:\n      summary: Forbidden error\n      value:\n        status: 403\n        err: \"You do not have permission to access this resource\"\n    TooManyRequestsExample:\n      summary: Rate limit error\n      value:\n        status: 429\n        err: \"Rate limit exceeded. Please wait before making another request\"\n    InternalServerErrorExample:\n      summary: Internal server error\n      value:\n        status: 500\n        err: \"An internal server error occurred\"\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-api-openapi.yml
tags:
- Design
- Users
---
