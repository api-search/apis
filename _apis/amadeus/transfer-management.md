---
aid: amadeus:transfer-management
baseURL: https://api.amadeus.com
description: The Amadeus Transfer Management API allows you to cancel transfers linked with existing orders. It provides post-booking management capabilities for ground transportation reservations, including cancellation confirmation.
humanURL: https://developers.amadeus.com/self-service/category/cars-and-transfers/api-doc/transfer-management
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Amadeus Transfer Management API
properties:
- type: Documentation
  url: https://developers.amadeus.com/self-service/category/cars-and-transfers/api-doc/transfer-management
- type: APIReference
  url: https://developers.amadeus.com/self-service/category/cars-and-transfers/api-doc/transfer-management/api-reference
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/openapi/transfer-management-openapi.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/transfer-management-error-400-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/transfer-management-error-401-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/transfer-management-error-404-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/transfer-management-error-500-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-schema/transfer-management-issue-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/transfer-management-error-400-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/transfer-management-error-401-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-structure/transfer-management-error-404-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/json-ld/amadeus-transfer-management-context.jsonld
provider_name: Amadeus
provider_slug: amadeus
slug: transfer-management
source_filename: transfer-management-openapi.yaml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  version: 1.11.0\n  title: Amadeus Transfer Management\n  description: >-\n    Before using this API, we recommend you read our **[Authorization\n    Guide](https://developers.amadeus.com/self-service/apis-docs/guides/authorization-262)**\n    for more information on how to generate an access token. \n\n\n    Please also be aware that our test environment is based on a subset of the\n    production for this API it may change dynamically. For your tests, use big\n    cities like LON (London) or NYC (New-York).\nhost: test.api.amadeus.com\nbasePath: /v1\nschemes:\n- https\nconsumes:\n- application/vnd.amadeus+json\n- application/json\nproduces:\n- application/vnd.amadeus+json\n- application/json\npaths:\n  /ordering/transfer-orders/{orderId}/transfers/cancellation:\n    post:\n      tags:\n      - Ordering\n      operationId: cancelTransfer\n      summary: Amadeus Cancel a Transfer in an Existing OrderId.\n      parameters:\n      - name: orderId\n   \
  \     in: path\n        type: string\n        required: true\n        description: transfer order identifier\n      - name: confirmNbr\n        in: query\n        type: string\n        required: true\n        description: >-\n          transfer identifier - confirmation number from transfer supplier\n          that identifies the ride\n      responses:\n        '200':\n          $ref: '#/responses/transfer_cancel'\n        '400':\n          $ref: '#/responses/400'\n        '401':\n          $ref: '#/responses/401'\n        '404':\n          $ref: '#/responses/404'\n        default:\n          $ref: '#/responses/500'\n      description: ''\ndefinitions:\n  TransferCancellation:\n    type: object\n    description: information returned in cancelation response\n    properties:\n      confirmNbr:\n        type: string\n        description: >-\n          transfer identifier - confirmation number from service provider that\n          identifies the ride\n      reservationStatus:\n        type:\
  \ string\n        enum:\n        - CANCELLED\n        - CONFIRMED\n        description: status of reservation\n  Error_400:\n    properties:\n      errors:\n        type: array\n        items:\n          $ref: '#/definitions/Issue'\n    required:\n    - errors\n    example:\n      errors:\n      - status: 400\n        code: 4926\n        title: INVALID DATA RECEIVED\n        detail: Transfer type is not valid\n        source:\n          parameter: transferType\n  Error_401:\n    properties:\n      errors:\n        type: array\n        items:\n          $ref: '#/definitions/Issue'\n    required:\n    - errors\n    example:\n      errors:\n      - status: 401\n        code: 20\n        title: RESTRICTED\n        detail: Query unauthorized\n  Error_404:\n    properties:\n      errors:\n        type: array\n        items:\n          $ref: '#/definitions/Issue'\n    required:\n    - errors\n    example:\n      errors:\n      - status: 404\n        code: 1797\n        title: NOT FOUND\n    \
  \    detail: no response found for this query parameter\n        source:\n          parameter: orderId\n  Error_500:\n    properties:\n      errors:\n        type: array\n        items:\n          $ref: '#/definitions/Issue'\n    required:\n    - errors\n    example:\n      errors:\n      - status: 500\n        code: 141\n        title: SYSTEM ERROR HAS OCCURRED\n  Issue:\n    properties:\n      status:\n        description: the HTTP status code applicable to this error\n        type: integer\n      code:\n        description: an application-specific error code\n        type: integer\n        format: int64\n      title:\n        description: a short summary of the error\n        type: string\n      detail:\n        description: explanation of the error\n        type: string\n      source:\n        type: object\n        title: Issue_Source\n        description: an object containing references to the source of the error\n        maxProperties: 1\n        properties:\n          pointer:\n\
  \            description: >-\n              a JSON Pointer [RFC6901] to the associated entity in the request\n              document\n            type: string\n          parameter:\n            description: a string indicating which URI query parameter caused the issue\n            type: string\n          example:\n            description: a string indicating an example of the right value\n            type: string\nresponses:\n  '400':\n    description: \"code    | title                                 \\n- | -                 \\n32171   | MANDATORY DATA MISSING \\t     \\n\"\n    schema:\n      $ref: '#/definitions/Error_400'\n  '401':\n    description: Unauthorized\n    schema:\n      $ref: '#/definitions/Error_401'\n  '404':\n    description: Not Found\n    schema:\n      $ref: '#/definitions/Error_404'\n  '500':\n    description: Unexpected Error\n    schema:\n      $ref: '#/definitions/Error_500'\n  transfer_cancel:\n    description: Successful Operation\n    schema:\n      title:\
  \ Success_Cancellation\n      required:\n      - data\n      properties:\n        data:\n          $ref: '#/definitions/TransferCancellation'\n      example:\n        data:\n          confirmNbr: '2904892'\n          reservationStatus: CANCELLED\nx-generatedAt: '2021-04-19T12:58:58.637Z'\ntags:\n- name: Ordering\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amadeus/refs/heads/main/openapi/transfer-management-openapi.yaml
tags:
- Ground Transportation
- Management
- Transfers
---
