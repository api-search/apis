---
aid: zendesk:target-failures
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Target Failures API helps you monitor and troubleshoot failed delivery attempts to legacy targets (such as HTTP, URL, or email targets) that triggers and automations use to send outbound notifications. It lets you list and inspect recent failures for a target, including details like when they occurred, how many times delivery was attempted, the error or HTTP status returned by the destination, and other diagnostic information.
humanURL: https://developer.zendesk.com/api-reference/ticketing/targets/targets/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Target Failures API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/targets/targets/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/target-failures-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: target-failures
source_filename: target-failures-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Target Failures\n  description: Needs a description.\npaths:\n  /api/v2/target_failures:\n    get:\n      operationId: ListTargetFailures\n      tags:\n        - Target Failures\n      summary: Zendesk Get  Api V2 Target_failures\n      description: |\n        Returns the 25 most recent target failures, per target.\n\n        #### Stability\n\n        * Development\n\n        #### Allowed For\n\n        * Admins\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TargetFailuresResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/TargetFailuresResponseExample'\n  /api/v2/target_failures/{target_failure_id}:\n    parameters:\n      - $ref: '#/components/parameters/TargetFailureId'\n    get:\n      operationId: ShowTargetFailure\n      tags:\n\
  \        - Target Failures\n      summary: Zendesk Get  Api V2 Target_failures Target_failure_id\n      description: |\n        #### Stability\n\n        * Development\n\n        #### Allowed For\n\n        * Admins\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TargetFailureResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/TargetFailureResponseExample'\ncomponents:\n  schemas:\n    TargetFailuresResponse:\n      type: object\n      properties:\n        target_failures:\n          type: array\n          items:\n            $ref: '#/components/schemas/TargetFailureObject'\n    TargetFailureResponse:\n      type: object\n      properties:\n        target_failure:\n          $ref: '#/components/schemas/TargetFailureObject'\ntags:\n  - name: Target Failures\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/target-failures-openapi-original.yml
tags:
- Target Failures
---
