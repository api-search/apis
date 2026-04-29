---
aid: pluralsight:flow-tickets-api
baseURL: https://<workspace>.appfireflow.com/v3/customer/core
description: REST API for accessing ticket data including comments, events, and project associations from connected project management tools.
humanURL: https://help.pluralsight.com/hc/en-us/sections/24176771997588-Customer-API-references
image: https://www.pluralsight.com/content/dam/pluralsight2/general/headers/logo.png
layout: api
name: Pluralsight Flow Tickets API
properties:
- type: Documentation
  url: https://help.pluralsight.com/hc/en-us/sections/24176771997588-Customer-API-references
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/flow-tickets.yml
provider_name: Pluralsight
provider_slug: pluralsight
slug: flow-tickets-api
source_filename: flow-tickets.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Pluralsight Flow Tickets API\n  description: REST API for accessing ticket data including comments, events, and project associations from connected project management tools.\n  version: 1.0.0\n  contact:\n    name: Pluralsight API Support\n    email: support@pluralsight.com\n    url: https://help.pluralsight.com\n  license:\n    name: Proprietary\n    url: https://www.pluralsight.com/terms\nservers:\n- url: https://{workspace}.appfireflow.com/v3/customer/core\n  description: Production\n  variables:\n    workspace:\n      description: Your Flow workspace identifier\n      default: your-workspace\nexternalDocs:\n  description: Customer API References\n  url: https://help.pluralsight.com/hc/en-us/sections/24176771997588-Customer-API-references\ntags:\n- name: Tickets\n  description: Ticket data operations\npaths:\n  /tickets:\n    get:\n      summary: Pluralsight Get Tickets\n      description: Retrieve ticket data including comments, events, and\
  \ project associations from connected project management tools.\n      operationId: getTickets\n      tags:\n      - Tickets\n      security:\n      - bearerAuth: []\n      parameters:\n      - name: start_date\n        in: query\n        description: Start date for the query period\n        schema:\n          type: string\n          format: date\n        example: '2026-04-17T12:00:00Z'\n      - name: end_date\n        in: query\n        description: End date for the query period\n        schema:\n          type: string\n          format: date\n        example: '2026-04-17T12:00:00Z'\n      responses:\n        '200':\n          description: Successful response with ticket data\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    type: array\n                    items:\n                      type: object\n                    description: Ticket records\n        '401':\n\
  \          description: Unauthorized - Invalid or missing authentication token\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: JWT\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/flow-tickets.yml
tags:
- Engineering Data
- Project Management
- Tickets
---
