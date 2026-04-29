---
aid: cloudflare:cloudflare-durable-objects-api
baseURL: https://api.cloudflare.com
description: Cloudflare Durable Objects combine compute with persistent storage in a single Worker. The API provides transactional and strongly consistent storage with support for SQL, key-value, alarms, and WebSocket hibernation for building stateful serverless applications.
humanURL: https://developers.cloudflare.com/durable-objects/
image: ''
layout: api
name: Cloudflare Durable Objects API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cloudflare/refs/heads/main/openapi/cloudflare-durable-objects-openapi.yml
- type: Documentation
  url: https://developers.cloudflare.com/durable-objects/
- type: GettingStarted
  url: https://developers.cloudflare.com/durable-objects/get-started/
- type: APIReference
  url: https://developers.cloudflare.com/durable-objects/api/
provider_name: Cloudflare
provider_slug: cloudflare
slug: cloudflare-durable-objects-api
source_filename: cloudflare-durable-objects-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Cloudflare Durable Objects API\n  description: >-\n    Cloudflare Durable Objects combine compute with persistent storage in a\n    single Worker. The management API provides endpoints for listing and\n    managing Durable Object namespaces and individual objects within those\n    namespaces, enabling developers to build stateful serverless applications.\n  version: '4.0'\n  contact:\n    name: Cloudflare Support\n    url: https://support.cloudflare.com/\n  termsOfService: https://www.cloudflare.com/terms/\nexternalDocs:\n  description: Cloudflare Durable Objects Documentation\n  url: https://developers.cloudflare.com/durable-objects/\nservers:\n- url: https://api.cloudflare.com/client/v4\n  description: Cloudflare API v4 Production Server\ntags:\n- name: Namespaces\n  description: >-\n    Manage Durable Object namespaces that group related object instances.\n- name: Objects\n  description: >-\n    List and manage individual Durable Object instances\
  \ within a namespace.\nsecurity:\n- bearerAuth: []\npaths:\n  /accounts/{account_id}/workers/durable_objects/namespaces:\n    get:\n      operationId: listDurableObjectNamespaces\n      summary: Cloudflare List Durable Object Namespaces\n      description: >-\n        Returns all Durable Object namespaces for the account.\n      tags:\n      - Namespaces\n      parameters:\n      - $ref: '#/components/parameters/AccountId'\n      responses:\n        '200':\n          description: List of Durable Object namespaces.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/NamespaceListResponse'\n              examples:\n                Listdurableobjectnamespaces200Example:\n                  summary: Default listDurableObjectNamespaces 200 response\n                  x-microcks-default: true\n                  value:\n                    result:\n                    - id: abc123\n                      name: Example Title\n  \
  \                    script: example_value\n                      class: example_value\n                    success: true\n                    errors:\n                    - {}\n                    messages:\n                    - {}\n        '401':\n          description: Unauthorized.\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /accounts/{account_id}/workers/durable_objects/namespaces/{namespace_id}/objects:\n    get:\n      operationId: listDurableObjects\n      summary: Cloudflare List Durable Objects\n      description: >-\n        Returns a list of Durable Objects within a namespace with cursor-based\n        pagination.\n      tags:\n      - Objects\n      parameters:\n      - $ref: '#/components/parameters/AccountId'\n      - $ref: '#/components/parameters/NamespaceId'\n      - name: cursor\n        in: query\n        description: Cursor for pagination.\n        schema:\n          type: string\n        example: example_value\n      - name: limit\n\
  \        in: query\n        description: Maximum number of objects to return.\n        schema:\n          type: integer\n        example: 10\n      responses:\n        '200':\n          description: List of Durable Objects.\n        '401':\n          description: Unauthorized.\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      description: >-\n        API token with Workers permissions.\n  parameters:\n    AccountId:\n      name: account_id\n      in: path\n      required: true\n      description: The unique identifier of the Cloudflare account.\n      schema:\n        type: string\n    NamespaceId:\n      name: namespace_id\n      in: path\n      required: true\n      description: The unique identifier of the Durable Object namespace.\n      schema:\n        type: string\n  schemas:\n    DurableObjectNamespace:\n      type: object\n      properties:\n        id:\n\
  \          type: string\n          description: The unique identifier of the namespace.\n          example: abc123\n        name:\n          type: string\n          description: The name of the namespace.\n          example: Example Title\n        script:\n          type: string\n          description: The Worker script associated with the namespace.\n          example: example_value\n        class:\n          type: string\n          description: The Durable Object class name.\n          example: example_value\n    NamespaceListResponse:\n      type: object\n      properties:\n        result:\n          type: array\n          items:\n            $ref: '#/components/schemas/DurableObjectNamespace'\n          example: []\n        success:\n          type: boolean\n          example: true\n        errors:\n          type: array\n          items:\n            type: object\n          example: []\n        messages:\n          type: array\n          items:\n            type: object\n        \
  \  example: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudflare/refs/heads/main/openapi/cloudflare-durable-objects-openapi.yml
tags:
- Serverless
- Stateful
- Storage
---
