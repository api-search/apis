---
aid: zendesk:imports
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Imports API lets you programmatically load large volumes of records into Zendesk in a controlled, asynchronous wayideal for migrations, initial seeding, or ongoing syncs. You submit a file or batched payload, define which object type to import (for example, users/organizations/tickets in Support or leads/contacts/deals in Sell), and map fields. The import runs as a background job you can monitor via status endpoints, with progress, per-row validation, and detailed error reporting.
humanURL: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_import/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Imports API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/tickets/ticket_import/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/imports-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: imports
source_filename: imports-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Imports\n  description: Needs a description.\npaths:\n  /api/v2/imports/tickets:\n    post:\n      operationId: TicketImport\n      tags:\n        - Ticket Import\n      summary: Zendesk Post  Api V2 Imports Tickets\n      description: |-\n        #### Allowed For\n\n        * Admins\n      parameters:\n        - $ref: '#/components/parameters/ArchiveImmediately'\n      requestBody:\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/TicketImportRequest'\n            examples:\n              default:\n                $ref: '#/components/examples/TicketImportRequestExample'\n      responses:\n        '201':\n          description: Successfully created\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TicketResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/TicketResponseExample'\n\
  \  /api/v2/imports/tickets/create_many:\n    post:\n      operationId: TicketBulkImport\n      tags:\n        - Ticket Import\n      summary: Zendesk Post  Api V2 Imports Tickets Create_many\n      description: |-\n        Accepts an array of up to 100 ticket objects.\n\n        #### Allowed For\n\n        * Admins\n      parameters:\n        - $ref: '#/components/parameters/ArchiveImmediately'\n      requestBody:\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/TicketBulkImportRequest'\n            examples:\n              default:\n                $ref: '#/components/examples/TicketBulkImportRequestExample'\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/JobStatusResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/JobStatusResponseExample'\n\
  components:\n  schemas:\n    JobStatusResponse:\n      type: object\n      properties:\n        job_status:\n          $ref: '#/components/schemas/JobStatusObject'\ntags:\n  - name: Ticket Import\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/imports-openapi-original.yml
tags:
- Imports
---
