---
aid: zendesk:satisfaction-reasons
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Satisfaction Reasons API lets you programmatically manage the predefined list of reasons customers can choose when they leave a bad satisfaction rating on a ticket. With it, admins can list, create, update, reorder, activate/deactivate, and delete reasons that appear in the followup survey, ensuring the choices align with current operations or policies.
humanURL: https://developer.zendesk.com/api-reference/ticketing/ticket-management/satisfaction_reasons/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Satisfaction Reasons API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/ticket-management/satisfaction_reasons/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/satisfaction-reasons-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: satisfaction-reasons
source_filename: satisfaction-reasons-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Satisfaction Reasons\n  description: Needs a description.\npaths:\n  /api/v2/satisfaction_reasons:\n    get:\n      operationId: ListSatisfactionRatingReasons\n      tags:\n        - Satisfaction Reasons\n      summary: Zendesk Get  Api V2 Satisfaction_reasons\n      description: |\n        List all reasons for an account\n\n        #### Allowed For\n\n        * Admins\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/SatisfactionReasonsResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/SatisfactionReasonsResponseExample'\n  /api/v2/satisfaction_reasons/{satisfaction_reason_id}:\n    get:\n      operationId: ShowSatisfactionRatings\n      tags:\n        - Satisfaction Reasons\n      summary: Zendesk Get  Api V2 Satisfaction_reasons Satisfaction_reason_id\n\
  \      description: |\n        #### Allowed For\n\n        * Admins\n      parameters:\n        - name: satisfaction_reason_id\n          in: path\n          description: The id of the satisfaction rating reason\n          required: true\n          schema:\n            type: integer\n          example: 35121\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/SatisfactionReasonResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/SatisfactionReasonResponseExample'\ncomponents:\n  schemas:\n    SatisfactionReasonsResponse:\n      type: object\n      properties:\n        reasons:\n          type: array\n          items:\n            $ref: '#/components/schemas/SatisfactionReasonObject'\n    SatisfactionReasonResponse:\n      type: object\n      properties:\n        reason:\n          type: array\n\
  \          items:\n            $ref: '#/components/schemas/SatisfactionReasonObject'\ntags:\n  - name: Satisfaction Reasons\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/satisfaction-reasons-openapi-original.yml
tags:
- Satisfaction Reasons
---
