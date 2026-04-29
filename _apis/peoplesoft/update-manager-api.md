---
aid: peoplesoft:update-manager-api
baseURL: https://{hostname}:{port}/psft/api/pum/v1
description: REST services for automated update image management, change package generation, and PeopleSoft Automated Updates (PAU).
humanURL: https://docs.oracle.com/cd/E52319_01/infoportal/pum.html
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Update Manager API
properties:
- type: Documentation
  url: https://docs.oracle.com/cd/E52319_01/infoportal/pum.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/update-manager.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: update-manager-api
source_filename: update-manager.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Update Manager API\n  description: REST services for automated update image management, change package generation, and PeopleSoft Automated Updates (PAU).\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/api/pum/v1\n  description: PeopleSoft Instance\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: PeopleSoft Update Manager Documentation\n  url: https://docs.oracle.com/cd/E52319_01/infoportal/pum.html\ntags:\n- name: Updates\n  description: Update and patch management operations\npaths:\n  /updates:\n    get:\n      summary: PeopleSoft List Available Updates\n      description:\
  \ Retrieve a list of available updates and change packages.\n      operationId: listUpdates\n      tags:\n      - Updates\n      security:\n      - basicAuth: []\n      responses:\n        '200':\n          description: Successful response with available updates\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  updates:\n                    type: array\n                    items:\n                      type: object\n                      properties:\n                        updateId:\n                          type: string\n                        description:\n                          type: string\n                        version:\n                          type: string\n                        status:\n                          type: string\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /updates/{updateId}/apply:\n\
  \    post:\n      summary: PeopleSoft Apply Update\n      description: Initiate application of a specific update or change package.\n      operationId: applyUpdate\n      tags:\n      - Updates\n      security:\n      - basicAuth: []\n      parameters:\n      - name: updateId\n        in: path\n        required: true\n        description: The update identifier\n        schema:\n          type: string\n        example: PS123456\n      responses:\n        '202':\n          description: Update application initiated\n        '401':\n          description: Unauthorized\n        '404':\n          description: Update not found\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/update-manager.yml
tags:
- Lifecycle Management
- Patching
- Updates
---
