---
aid: avalara:activation-service-api
baseURL: ''
description: The Avalara Activation Service API allows technology partners to retrieve the status of their registrations within the Avalara Compliance Cloud platform, providing endpoints for listing all registrations and retrieving individual registration details.
humanURL: https://developer.avalara.com/api-reference/activationService/activationService/
image: ''
layout: api
name: Activation Service API
properties:
- type: Documentation
  url: https://developer.avalara.com/api-reference/activationService/activationService/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-activation-service-openapi.yml
provider_name: Avalara
provider_slug: avalara
slug: activation-service-api
source_filename: avalara-activation-service-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Avalara Activation Service API\n  description: >-\n    The Avalara Activation Service API allows technology partners to retrieve\n    the status of their registrations within the Avalara Compliance Cloud\n    platform, providing endpoints for listing all registrations and retrieving\n    individual registration details.\n  version: '1.0'\n  contact:\n    name: Avalara Developer Relations\n    url: https://developer.avalara.com/\n    email: developer.relations@avalara.com\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0\n  termsOfService: https://legal.avalara.com/#siteterms\nexternalDocs:\n  description: Activation Service API Documentation\n  url: https://developer.avalara.com/api-reference/activationService/activationService/\nservers:\n- url: https://api.avalara.com/activation/v1\n  description: Activation Service API Production\ntags:\n- name: Registrations\n  description: Manage partner registrations\n\
  security:\n- bearerAuth: []\npaths:\n  /registrations:\n    get:\n      operationId: listRegistrations\n      summary: Avalara List All Registrations\n      description: Retrieves all registrations for the authenticated partner.\n      tags:\n      - Registrations\n      parameters:\n      - name: status\n        in: query\n        schema:\n          type: string\n          enum:\n          - Pending\n          - Active\n          - Expired\n          - Cancelled\n      - name: $top\n        in: query\n        schema:\n          type: integer\n      - name: $skip\n        in: query\n        schema:\n          type: integer\n      responses:\n        '200':\n          description: List of registrations\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/RegistrationList'\n        '401':\n          $ref: '#/components/responses/Unauthorized'\n  /registrations/{registrationId}:\n    get:\n      operationId: getRegistration\n\
  \      summary: Avalara Get a Registration by ID\n      description: Retrieves details for a specific registration.\n      tags:\n      - Registrations\n      parameters:\n      - name: registrationId\n        in: path\n        required: true\n        schema:\n          type: string\n      responses:\n        '200':\n          description: Registration details\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Registration'\n        '404':\n          $ref: '#/components/responses/NotFound'\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n  responses:\n    Unauthorized:\n      description: Authentication failed\n      content:\n        application/json:\n          schema:\n            $ref: '#/components/schemas/ErrorResponse'\n    NotFound:\n      description: Resource not found\n      content:\n        application/json:\n          schema:\n            $ref: '#/components/schemas/ErrorResponse'\n\
  \  schemas:\n    RegistrationList:\n      type: object\n      properties:\n        '@recordSetCount':\n          type: integer\n        value:\n          type: array\n          items:\n            $ref: '#/components/schemas/Registration'\n    Registration:\n      type: object\n      properties:\n        registrationId:\n          type: string\n        partnerId:\n          type: string\n        companyName:\n          type: string\n        status:\n          type: string\n          enum:\n          - Pending\n          - Active\n          - Expired\n          - Cancelled\n        product:\n          type: string\n          description: Avalara product registered for\n        accountId:\n          type: string\n        activationDate:\n          type: string\n          format: date-time\n        expirationDate:\n          type: string\n          format: date-time\n        createdDate:\n          type: string\n          format: date-time\n    ErrorResponse:\n      type: object\n      properties:\n\
  \        error:\n          type: object\n          properties:\n            code:\n              type: string\n            message:\n              type: string\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-activation-service-openapi.yml
tags:
- Registration
- Taxes
---
