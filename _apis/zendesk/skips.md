---
aid: zendesk:skips
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Skips API provides programmatic access to events where an agent doesnt accept or actively skips a routed work item (such as a ticket or conversation) in omnichannel routing. It records who skipped, what was skipped, when it happened, and (when available) the reason, so you can analyze agent behavior, finetune routing rules and capacity, and troubleshoot assignment flows.
humanURL: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_skips/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Skips API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_skips/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/skips-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: skips
source_filename: skips-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Skips\n  description: Needs a description.\npaths:\n  /api/v2/skips:\n    post:\n      operationId: RecordNewSkip\n      tags:\n        - Ticket Skips\n      summary: Zendesk Post  Api V2 Skips\n      description: |\n        Record a new ticket skip for the current user.\n\n        #### Allowed For\n\n        * Agents\n      responses:\n        '201':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TicketSkipCreation'\n              examples:\n                default:\n                  $ref: '#/components/examples/TicketSkipCreationExample'\n  /api/v2/users/{user_id}/skips:\n    parameters:\n      - $ref: '#/components/parameters/SkipTicketUserId'\n      - $ref: '#/components/parameters/TicketSortOrder'\n      - $ref: '#/components/parameters/TicketId'\n    get:\n      operationId: ListTicketSkips\n      tags:\n        - Ticket\
  \ Skips\n      summary: Zendesk Get  Api V2 Users User_id Skips\n      description: >\n        Archived tickets are not included in the response. See\n\n        [About archived\n        tickets](https://support.zendesk.com/hc/en-us/articles/203657756) in\n\n        the Support Help Center.\n\n\n        #### Pagination\n\n\n        - Cursor pagination (recommended)\n\n        - Offset pagination\n\n\n        See [Pagination](/api-reference/introduction/pagination/).\n\n\n        Returns a maximum of 100 records per page.\n\n\n        #### Allowed For\n\n        * Agents with \"View only\" or higher reports permissions in Support.\n          These permissions are distinct from Explore permissions.\n        * Agents retrieving their own skips\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TicketSkipsResponse'\n              examples:\n        \
  \        default:\n                  $ref: '#/components/examples/TicketSkipResponseExample'\ncomponents:\n  schemas:\n    TicketSkipsResponse:\n      type: object\n      properties:\n        skips:\n          type: array\n          items:\n            $ref: '#/components/schemas/TicketSkipObject'\ntags:\n  - name: Ticket Skips\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/skips-openapi-original.yml
tags:
- Skips
---
