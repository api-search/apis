---
aid: apiida:api-control-plane
baseURL: https://api.apiida.com
description: REST API for the APIIDA API Control Plane, enabling programmatic management of APIs across multiple API gateways. Supports validation of proxy specifications, API version management, and deployment to gateways from a central federated control plane.
humanURL: https://apiida.com/product/apiida-api-control-plane/
image: ''
layout: api
name: APIIDA API Control Plane
properties:
- type: Documentation
  url: https://apiida.com/product/apiida-api-control-plane/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apiida/refs/heads/main/openapi/apiida-api-control-plane-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apiida/refs/heads/main/json-schema/apiida-api.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apiida/refs/heads/main/json-schema/apiida-deployment.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/apiida/refs/heads/main/json-ld/apiida-context.jsonld
provider_name: APIIDA
provider_slug: apiida
slug: api-control-plane
source_filename: apiida-api-control-plane-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: APIIDA API Control Plane\n  description: >-\n    REST API for the APIIDA API Control Plane, enabling programmatic management\n    of APIs across multiple API gateways. Supports validation of proxy\n    specifications, API version management, and deployment to gateways.\n  version: '1.0'\n  contact:\n    name: APIIDA Support\n    url: https://www.apiida.com\nexternalDocs:\n  description: APIIDA Documentation\n  url: https://apiida.atlassian.net\nservers:\n- url: https://{tenant}.backend.apiida.io\n  description: APIIDA Backend\n  variables:\n    tenant:\n      description: Your APIIDA tenant identifier\n      default: example\ntags:\n- name: Deployments\n  description: Gateway deployment operations\n- name: Versions\n  description: API version management\nsecurity:\n- bearerAuth: []\npaths:\n  /apis/analyzeOpenProxySpec:\n    post:\n      operationId: analyzeOpenProxySpec\n      summary: APIIDA Validate Open Proxy Specification\n      description:\
  \ >-\n        Validate an Open Proxy Specification file to check for errors\n        and compatibility before creating API versions.\n      tags: []\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                spec:\n                  type: string\n                  description: The Open Proxy Specification content to validate\n      responses:\n        '200':\n          description: Validation results\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  valid:\n                    type: boolean\n                    description: Whether the specification is valid\n                  errors:\n                    type: array\n                    items:\n                      type: string\n                    description: List of validation errors if any\n        '401':\n\
  \          description: Unauthorized\n  /apis/{apiId}/versions:\n    post:\n      operationId: createApiVersion\n      summary: APIIDA Create API Version\n      description: >-\n        Create a new version for an existing API in the control plane.\n      tags:\n      - Versions\n      parameters:\n      - $ref: '#/components/parameters/apiId'\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                version:\n                  type: string\n                  description: Version identifier\n                description:\n                  type: string\n                  description: Version description\n      responses:\n        '201':\n          description: API version created successfully\n        '401':\n          description: Unauthorized\n        '404':\n          description: API not found\n  /apis/{apiId}/versions/{version}/openProxySpec:\n    put:\n   \
  \   operationId: uploadOpenProxySpec\n      summary: APIIDA Upload Specification to API Version\n      description: >-\n        Upload an Open Proxy Specification to a specific API version.\n      tags:\n      - Versions\n      parameters:\n      - $ref: '#/components/parameters/apiId'\n      - $ref: '#/components/parameters/version'\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                spec:\n                  type: string\n                  description: The Open Proxy Specification content\n      responses:\n        '200':\n          description: Specification uploaded successfully\n        '401':\n          description: Unauthorized\n        '404':\n          description: API or version not found\n  /apis/{apiId}/versions/{version}/importIntoGateways:\n    post:\n      operationId: deployToGateways\n      summary: APIIDA Deploy API to Gateways\n      description:\
  \ >-\n        Deploy a specific API version to one or more connected API gateways.\n      tags:\n      - Deployments\n      parameters:\n      - $ref: '#/components/parameters/apiId'\n      - $ref: '#/components/parameters/version'\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                gatewayIds:\n                  type: array\n                  items:\n                    type: string\n                  description: List of gateway identifiers to deploy to\n      responses:\n        '200':\n          description: Deployment initiated successfully\n        '401':\n          description: Unauthorized\n        '404':\n          description: API or version not found\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      description: Bearer token authentication\n  parameters:\n    apiId:\n      name: apiId\n      in: path\n\
  \      required: true\n      schema:\n        type: string\n      description: The API identifier\n    version:\n      name: version\n      in: path\n      required: true\n      schema:\n        type: string\n      description: The API version identifier\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apiida/refs/heads/main/openapi/apiida-api-control-plane-openapi.yml
tags:
- API Lifecycle
- API Management
- Federated Control Plane
- Governance
---
