---
aid: zendesk:ticket-metrics
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Ticket Metrics API lets you programmatically access the operational and SLA metrics that Zendesk calculates for each support ticket. It provides perticket summaries such as first reply time, full resolution time, requester and agent wait times, onhold time, number of replies and reopens, and key timestamps (for example, assigned and solved), often available in both calendar and business minutes.
humanURL: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_metrics/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Ticket Metrics API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_metrics/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/ticket-metrics-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: ticket-metrics
source_filename: ticket-metrics-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Ticket Metrics\n  description: Needs a description.\npaths:\n  /api/v2/ticket_metrics:\n    get:\n      operationId: ListTicketMetrics\n      tags:\n        - Ticket Metrics\n      summary: Zendesk Get  Api V2 Ticket_metrics\n      description: >\n        Returns a list of tickets with their metrics.\n\n\n        Tickets are ordered chronologically by created date, from newest to\n        oldest.\n\n        The last ticket listed may not be the absolute oldest ticket in your\n        account\n\n        due to ticket archiving.\n\n\n        Archived tickets are not included in the response. See\n\n        [About archived\n        tickets](https://support.zendesk.com/hc/en-us/articles/203657756) in\n\n        Zendesk help.\n\n\n        #### Pagination\n\n\n        - Cursor pagination (recommended)\n\n        - Offset pagination\n\n\n        See [Pagination](/api-reference/introduction/pagination/).\n\n\n        Returns a maximum of 100\
  \ records per page.\n\n\n\n        #### Allowed For\n\n\n        * Agents\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TicketMetricsResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/TicketMetricsResponseExample'\n  /api/v2/ticket_metrics/{ticket_metric_id}:\n    get:\n      operationId: ShowTicketMetrics\n      tags:\n        - Ticket Metrics\n      summary: Zendesk Get  Api V2 Ticket_metrics Ticket_metric_id\n      description: |\n        Returns a specific metric, or the metrics of a specific ticket.\n\n        #### Pagination\n\n        - Cursor pagination (recommended)\n        - Offset pagination\n\n        See [Pagination](/api-reference/introduction/pagination/).\n\n        Returns a maximum of 100 records per page.\n\n        #### Allowed For\n\n        * Agents\n      parameters:\n\
  \        - name: ticket_metric_id\n          in: path\n          description: The id of the ticket metric to retrieve\n          required: true\n          schema:\n            type: string\n          example: '10001'\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TicketMetricsByTicketMetricIdResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/TicketMetricResponseExample'\ncomponents:\n  schemas:\n    TicketMetricsResponse:\n      type: object\n      properties:\n        ticket_metrics:\n          type: array\n          items:\n            $ref: '#/components/schemas/TicketMetricObject'\n    TicketMetricsByTicketMetricIdResponse:\n      type: object\n      properties:\n        ticket_metric:\n          type: array\n          items:\n            $ref: '#/components/schemas/TicketMetricObject'\n\
  tags:\n  - name: Ticket Metrics\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/ticket-metrics-openapi-original.yml
tags:
- Metrics
- Tickets
---
