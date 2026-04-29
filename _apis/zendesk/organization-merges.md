---
aid: zendesk:organization-merges
baseURL: https://{subdomain}.zendesk.com
description: Zendesks Organization Merges API lets you consolidate two organizations into one clean record by merging a source organization into a target. During a merge, all users belonging to the source organization are moved to the target, and tickets associated with the source (as requester or via organization) are re-associated to the target, preserving ticket history and continuity.
humanURL: https://developer.zendesk.com/api-reference/ticketing/organizations/organizations/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Organization Merges API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/organizations/organizations/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/organization-merges-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: organization-merges
source_filename: organization-merges-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Organization Merges\n  description: Needs a description.\npaths:\n  /api/v2/organization_merges/{organization_merge_id}:\n    parameters:\n      - $ref: '#/components/parameters/OrganizationMergeId'\n    get:\n      operationId: ShowOrganizationMerge\n      tags:\n        - Organizations\n      summary: Zendesk Get  Api V2 Organization_merges Organization_merge_id\n      description: >\n        Retrieves the details of a specific organization merge operation. This\n        endpoint is useful for obtaining the status and outcome of a merge that\n        was previously initiated. It provides information such as the winning\n        and losing organization IDs, the status of the merge, and the associated\n        URLs.\n\n\n        This endpoint can be used to determine if a merge is still in progress,\n        has completed successfully, or has encountered an error.\n\n\n        #### Allowed For\n\n\n        * Admins\n      responses:\n\
  \        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/OrganizationMergeResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/OrganizationMergeResponseExample'\ncomponents:\n  schemas:\n    OrganizationMergeResponse:\n      type: object\n      properties:\n        organization_merge:\n          type: object\n          properties:\n            id:\n              type: string\n              format: string\n            loser_id:\n              type: integer\n            status:\n              type: string\n              enum:\n                - new\n                - in_progress\n                - error\n                - complete\n            url:\n              type: string\n              format: string\n            winner_id:\n              type: integer\n          required:\n            - id\n            - url\n\
  \            - loser_id\n            - winner_id\n            - status\ntags:\n  - name: Organizations\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/organization-merges-openapi-original.yml
tags:
- Organization Merges
---
