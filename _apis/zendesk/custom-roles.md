---
aid: zendesk:custom-roles
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Custom Roles API lets you programmatically manage the agent permission sets used in Zendesk Support (typically on Enterprise plans). Through it, you can list and fetch existing roles, create new ones, update their names, descriptions, and granular permissions, and delete roles you no longer need.
humanURL: https://developer.zendesk.com/api-reference/ticketing/account-configuration/custom_roles/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Custom Roles API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/account-configuration/custom_roles/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/custom-roles-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: custom-roles
source_filename: custom-roles-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Custom Roles\n  description: Needs a description.\npaths:\n  /api/v2/custom_roles:\n    get:\n      operationId: ListCustomRoles\n      tags:\n        - Custom Roles\n      summary: Zendesk Get  Api V2 Custom_roles\n      description: |\n        #### Availability\n\n        * Accounts on the Enterprise plan or above\n\n        #### Allowed For\n\n        * Agents\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/CustomRolesResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/CustomRolesResponseExample'\n    post:\n      operationId: CreateCustomRole\n      tags:\n        - Custom Roles\n      summary: Zendesk Post  Api V2 Custom_roles\n      description: |\n        #### Availability\n\n        * Accounts on the Enterprise plan or above\n\n\
  \        #### Allowed for\n\n        * Administrators\n        * Agents with the `manage_roles` permission\n      responses:\n        '200':\n          description: Created response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/CustomRoleResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/CustomRoleResponseExample'\n  /api/v2/custom_roles/{custom_role_id}:\n    parameters:\n      - $ref: '#/components/parameters/CustomRoleId'\n    get:\n      operationId: ShowCustomRoleById\n      tags:\n        - Custom Roles\n      summary: Zendesk Get  Api V2 Custom_roles Custom_role_id\n      description: |\n        #### Availability\n\n        * Accounts on the Enterprise plan or above\n\n        #### Allowed for\n\n        * Administrators\n        * Agents with the `manage_roles` permission\n      responses:\n        '200':\n          description: Success response\n \
  \         content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/CustomRoleResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/CustomRoleResponseExample'\n    put:\n      operationId: UpdateCustomRoleById\n      tags:\n        - Custom Roles\n      summary: Zendesk Put  Api V2 Custom_roles Custom_role_id\n      description: |\n        #### Availability\n\n        * Accounts on the Enterprise plan or above\n\n        #### Allowed for\n\n        * Administrators\n        Agents with the `manage_roles` permission\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/CustomRoleResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/CustomRoleResponseExample'\n    delete:\n      operationId: DeleteCustomRoleById\n\
  \      tags:\n        - Custom Roles\n      summary: Zendesk Delete  Api V2 Custom_roles Custom_role_id\n      description: |\n        #### Availability\n\n        * Accounts on the Enterprise plan or above\n\n        #### Allowed for\n\n        * Administrators\n        * Agents with the `manage_roles` permission\n      responses:\n        '204':\n          description: No Contetnt response\ncomponents:\n  schemas:\n    CustomRolesResponse:\n      type: object\n      properties:\n        custom_roles:\n          type: array\n          items:\n            $ref: '#/components/schemas/CustomRoleObject'\n    CustomRoleResponse:\n      type: object\n      properties:\n        custom_role:\n          $ref: '#/components/schemas/CustomRoleObject'\ntags:\n  - name: Custom Roles\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/custom-roles-openapi-original.yml
tags:
- Custom Roles
---
