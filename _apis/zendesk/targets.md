---
aid: zendesk:targets
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Targets API lets you programmatically manage targets, which are external destinations that Zendesk Support triggers and automations can notify when conditions are met. Using the API, you can create, list, update, activate/deactivate, and delete targets, configure details such as URLs, HTTP methods, authentication, and content types, and review delivery failures to troubleshoot outbound notifications.
humanURL: https://developer.zendesk.com/api-reference/ticketing/targets/targets/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Targets API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/targets/targets/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/targets-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: targets
source_filename: targets-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Targets\n  description: Needs a description.\npaths:\n  /api/v2/targets:\n    get:\n      operationId: ListTargets\n      tags:\n        - Targets\n      summary: Zendesk Get  Api V2 Targets\n      description: |\n        #### Allowed For\n\n        * Agents\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TargetsResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/TargetsResponseExample'\n    post:\n      operationId: CreateTarget\n      tags:\n        - Targets\n      summary: Zendesk Post  Api V2 Targets\n      description: |\n        #### Allowed For\n\n        * Admins\n      responses:\n        '201':\n          description: Created response\n          content:\n            application/json:\n              schema:\n               \
  \ $ref: '#/components/schemas/TargetResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/TargetCreateResponseExample'\n  /api/v2/targets/{target_id}:\n    parameters:\n      - $ref: '#/components/parameters/TargetId'\n    get:\n      operationId: ShowTarget\n      tags:\n        - Targets\n      summary: Zendesk Get  Api V2 Targets Target_id\n      description: |\n        #### Allowed For\n\n        * Agents\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TargetResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/TargetResponseExample'\n    put:\n      operationId: UpdateTarget\n      tags:\n        - Targets\n      summary: Zendesk Put  Api V2 Targets Target_id\n      description: |\n        #### Allowed For\n        * Admins\n   \
  \   responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TargetResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/TargetUpdateResponseExample'\n    delete:\n      operationId: DeleteTarget\n      tags:\n        - Targets\n      summary: Zendesk Delete  Api V2 Targets Target_id\n      description: |\n        #### Allowed For\n        * Admins\n      responses:\n        '204':\n          description: No Content response\ncomponents:\n  schemas:\n    TargetsResponse:\n      type: object\n      properties:\n        targets:\n          type: array\n          items:\n            $ref: '#/components/schemas/TargetObject'\n    TargetResponse:\n      type: object\n      properties:\n        target:\n          $ref: '#/components/schemas/TargetObject'\ntags:\n  - name: Targets\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/targets-openapi-original.yml
tags:
- Targets
---
