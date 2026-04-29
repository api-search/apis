---
aid: zendesk:ticket-audits
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Ticket Audits API exposes the complete, immutable change history of a Support ticket, letting you retrieve every audit generated whenever a ticket is created or updated. Each audit contains timestamped events that record who made a change and how it happened (agent, end user, trigger, automation, or API), along with metadata such as author, channel, and system details.
humanURL: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_audits/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Ticket Audits API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_audits/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/ticket-audits-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: ticket-audits
source_filename: ticket-audits-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Ticket Audits\n  description: Needs a description.\npaths:\n  /api/v2/ticket_audits:\n    get:\n      operationId: ListTicketAudits\n      tags:\n        - Ticket Audits\n      summary: Zendesk Get  Api V2 Ticket_audits\n      description: >\n        Returns ticket audits. Archived tickets are not included in the\n        response. Use the [List Audits for a Ticket](#list-audits-for-a-ticket)\n        endpoint to\n\n        retrieve audit records for an archived ticket. To learn more about\n        archived tickets, see [About archived\n        tickets](https://support.zendesk.com/hc/en-us/articles/203657756).\n\n\n        This endpoint should not be used for capturing change data. When\n        continually chasing the tail of a cursor, some records will be skipped.\n        For this use case, use the [Incremental Ticket Event Export\n        API](/api-reference/ticketing/ticket-management/incremental_exports/#incremental-ticket-event-export).\n\
  \n\n        #### Allowed For\n\n\n        * Admins\n      parameters:\n        - name: page[before]\n          in: query\n          description: >\n            A [pagination\n            cursor](/documentation/api-basics/pagination/paginating-through-lists-using-cursor-pagination)\n            that tells the endpoint which page to start on. It should be a\n            `meta.before_cursor` value from a previous request. Note:\n            `page[before]` and `page[after]` can't be used together in the same\n            request.\n          schema:\n            type: string\n        - name: page[after]\n          in: query\n          description: >\n            A [pagination\n            cursor](/documentation/api-basics/pagination/paginating-through-lists-using-cursor-pagination)\n            that tells the endpoint which page to start on. It should be a\n            `meta.after_cursor` value from a previous request. Note:\n            `page[before]` and `page[after]` can't be used together\
  \ in the same\n            request.\n          schema:\n            type: string\n        - name: page[size]\n          in: query\n          description: >-\n            Specifies how many records to be returned in the response. You can\n            specify up to 100 records per page.\n          schema:\n            type: integer\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TicketAuditsResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/TicketAuditsResponseExample'\ncomponents:\n  schemas:\n    TicketAuditsResponse:\n      type: object\n      properties:\n        after_cursor:\n          type: string\n          readOnly: true\n        after_url:\n          type: string\n          readOnly: true\n        audits:\n          type: array\n          items:\n            $ref: '#/components/schemas/TicketAuditObject'\n\
  \        before_cursor:\n          type: string\n          readOnly: true\n        before_url:\n          type: string\n          readOnly: true\ntags:\n  - name: Ticket Audits\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/ticket-audits-openapi-original.yml
tags:
- Audits
- Ticket Audits
---
