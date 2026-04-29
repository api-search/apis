---
aid: cisco-webex:webex-roles-api
baseURL: https://webexapis.com/v1
description: Retrieve roles available within a Webex organization. Roles define the level of access and permissions granted to users, such as full administrator or read-only administrator.
humanURL: https://developer.webex.com/docs/api/v1/roles
image: https://www.webex.com/content/dam/wbx/us/images/webex-logo.svg
layout: api
name: Webex Roles API
properties:
- type: Documentation
  url: https://developer.webex.com/docs/api/v1/roles
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-roles-openapi.yml
provider_name: Cisco Webex
provider_slug: cisco-webex
slug: webex-roles-api
source_filename: cisco-webex-roles-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Cisco Webex Roles API\n  description: >-\n    Retrieve roles available within a Webex organization. Roles define the\n    level of access and permissions granted to users, such as full\n    administrator or read-only administrator.\n  version: 1.0.0\n  contact:\n    name: Cisco Webex Developer Support\n    url: https://developer.webex.com/support\n  license:\n    name: Cisco Webex API Terms of Service\n    url: https://developer.webex.com/terms-of-service\nservers:\n  - url: https://webexapis.com/v1\n    description: Webex Production API\nsecurity:\n  - bearerAuth: []\ntags:\n  - name: Roles\n    description: Operations for retrieving organizational roles\npaths:\n  /roles:\n    get:\n      operationId: listRoles\n      summary: Cisco Webex List Roles\n      description: >-\n        Lists all roles available in the organization. Must be called by\n        an admin user. Returns role names and unique identifiers.\n      tags:\n        - Roles\n\
  \      responses:\n        '200':\n          description: Successful response with list of roles.\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  items:\n                    type: array\n                    items:\n                      $ref: '#/components/schemas/Role'\n        '401':\n          description: Unauthorized - invalid or missing access token.\n  /roles/{roleId}:\n    get:\n      operationId: getRoleDetails\n      summary: Cisco Webex Get Role Details\n      description: >-\n        Shows details for a role by ID. Returns the role name and unique\n        identifier. Must be called by an admin user.\n      tags:\n        - Roles\n      parameters:\n        - name: roleId\n          in: path\n          required: true\n          description: Unique identifier for the role.\n          schema:\n            type: string\n      responses:\n        '200':\n          description:\
  \ Successful response with role details.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Role'\n        '404':\n          description: Role not found.\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      description: >-\n        Webex API access token. Obtain via OAuth 2.0 authorization flow.\n        Requires spark-admin:roles_read scope.\n  schemas:\n    Role:\n      type: object\n      properties:\n        id:\n          type: string\n          description: Unique identifier for the role.\n        name:\n          type: string\n          description: The name of the role.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco-webex/refs/heads/main/openapi/cisco-webex-roles-openapi.yml
tags:
- Access Control
- Administration
- Permissions
- Roles
- Security
---
