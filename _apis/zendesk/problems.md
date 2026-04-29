---
aid: zendesk:problems
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Problems API helps you manage problem tickets and their relationship to incident tickets, so you can track and resolve widespread issues affecting multiple customers. It provides endpoints to list and query problem tickets and to retrieve the incidents linked to a specific problem (for example, to understand scope and impact).
humanURL: https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Problems API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/problems-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: problems
source_filename: problems-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Problems\n  description: Needs a description.\npaths:\n  /api/v2/problems:\n    get:\n      operationId: ListTicketProblems\n      tags:\n        - Tickets\n      summary: Zendesk Get  Api V2 Problems\n      description: |-\n        The response is always ordered by `updated_at` in descending order\n\n        #### Allowed For\n\n        * Agents\n\n        #### Pagination\n\n        * Cursor pagination (recommended)\n        * Offset pagination\n\n        See [Pagination](/api-reference/introduction/pagination/).\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ListTicketProblemsResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/ListTicketProblemsResponseExample'\n  /api/v2/problems/autocomplete:\n    post:\n      operationId: AutocompleteProblems\n\
  \      tags:\n        - Tickets\n      summary: Zendesk Post  Api V2 Problems Autocomplete\n      description: >-\n        Returns tickets whose type is \"problem\" and whose subject contains the\n        string specified in the `text` parameter.\n\n\n        You can specify the `text` parameter in the request body rather than the\n        query string. Example:\n\n\n        `{\"text\": \"fire\"}`\n\n\n        #### Allowed For\n\n\n        * Agents\n      parameters:\n        - name: text\n          in: query\n          description: The text to search for\n          schema:\n            type: string\n      requestBody:\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                text:\n                  type: string\n                  description: The text to search for\n            example:\n              text: fire\n      responses:\n        '200':\n          description: Successful response\n          content:\n\
  \            application/json:\n              schema:\n                $ref: '#/components/schemas/ListTicketProblemsResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/ListTicketProblemsResponseExample'\ncomponents:\n  schemas:\n    ListTicketProblemsResponse:\n      type: object\n      additionalProperties: true\ntags:\n  - name: Tickets\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/problems-openapi-original.yml
tags:
- Problems
---
