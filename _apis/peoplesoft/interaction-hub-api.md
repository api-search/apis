---
aid: peoplesoft:interaction-hub-api
baseURL: https://{hostname}:{port}/psft/api/hub/v1
description: Content management, branding, and portal administration APIs for the PeopleSoft Interaction Hub (formerly Enterprise Portal) with Integration Broker services.
humanURL: https://docs.oracle.com/cd/F75142_01/ps91pbr15/eng/ps/psad/PeopleSoftInteractionHubOverview.html
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Interaction Hub API
properties:
- type: Documentation
  url: https://docs.oracle.com/cd/F75142_01/ps91pbr15/eng/ps/psad/PeopleSoftInteractionHubOverview.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/interaction-hub.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: interaction-hub-api
source_filename: interaction-hub.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Interaction Hub API\n  description: Content management, branding, and portal administration APIs for the PeopleSoft Interaction Hub (formerly Enterprise Portal) with Integration Broker services.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/api/hub/v1\n  description: PeopleSoft Instance\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: PeopleSoft Interaction Hub Documentation\n  url: https://docs.oracle.com/cd/F75142_01/ps91pbr15/eng/ps/psad/PeopleSoftInteractionHubOverview.html\ntags:\n- name: Content\n  description: Content management operations\n- name: Branding\n  description:\
  \ Branding and theme operations\npaths:\n  /content:\n    get:\n      summary: PeopleSoft List Content\n      description: Retrieve portal content items.\n      operationId: listContent\n      tags:\n      - Content\n      security:\n      - basicAuth: []\n      parameters:\n      - name: category\n        in: query\n        description: Content category filter\n        schema:\n          type: string\n        example: example_value\n      responses:\n        '200':\n          description: Successful response with content items\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  items:\n                    type: array\n                    items:\n                      type: object\n                      properties:\n                        contentId:\n                          type: string\n                        title:\n                          type: string\n                        category:\n\
  \                          type: string\n                        publishDate:\n                          type: string\n                          format: date\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n    post:\n      summary: PeopleSoft Create Content\n      description: Create a new portal content item.\n      operationId: createContent\n      tags:\n      - Content\n      security:\n      - basicAuth: []\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                title:\n                  type: string\n                body:\n                  type: string\n                category:\n                  type: string\n      responses:\n        '201':\n          description: Content created\n        '400':\n          description: Bad request\n        '401':\n          description:\
  \ Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /branding/themes:\n    get:\n      summary: PeopleSoft List Themes\n      description: Retrieve available branding themes.\n      operationId: listThemes\n      tags:\n      - Branding\n      security:\n      - basicAuth: []\n      responses:\n        '200':\n          description: Successful response with themes\n          content:\n            application/json:\n              schema:\n                type: object\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/interaction-hub.yml
tags:
- Branding
- Content Management
- Interaction Hub
- Portal
---
