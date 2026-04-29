---
aid: charter-communications:spectrum-enterprise-api
baseURL: https://enterprise.spectrum.com/api
description: The Spectrum Enterprise Open API exposes REST endpoints that let enterprise clients integrate their systems with Spectrum Enterprise portal features including service ticket management and carrier serviceability lookups. The API uses OAuth 2.0 authentication.
humanURL: https://enterprise.spectrum.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Charter Communications Spectrum Enterprise API
properties:
- type: Documentation
  url: https://enterprise.spectrum.com/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/charter-communications/refs/heads/main/openapi/charter-communications-spectrum-enterprise-api-openapi.yml
- type: Spectral
  url: https://raw.githubusercontent.com/api-evangelist/charter-communications/refs/heads/main/spectral/charter-communications-spectral.yml
provider_name: Charter Communications
provider_slug: charter-communications
slug: spectrum-enterprise-api
source_filename: charter-communications-spectrum-enterprise-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Charter Communications Spectrum Enterprise API\n  description: >-\n    The Spectrum Enterprise Open API provides enterprise clients the ability to\n    integrate their systems with Spectrum Enterprise portal features including\n    service ticketing and carrier serviceability.\n  version: 1.0.0\n  contact:\n    name: Spectrum Enterprise\n    url: https://enterprise.spectrum.com/\nservers:\n  - url: https://enterprise.spectrum.com/api\n    description: Production\npaths:\n  /tickets:\n    get:\n      operationId: getTickets\n      summary: Get Service Tickets\n      description: Retrieve a list of service tickets.\n      tags:\n        - Tickets\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TicketList'\n    post:\n      operationId: createTicket\n      summary: Create Service Ticket\n      description:\
  \ Create a new service ticket.\n      tags:\n        - Tickets\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/TicketRequest'\n      responses:\n        '201':\n          description: Ticket created\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Ticket'\n  /tickets/{ticketId}:\n    get:\n      operationId: getTicketById\n      summary: Get Ticket by ID\n      description: Retrieve a specific service ticket.\n      tags:\n        - Tickets\n      parameters:\n        - name: ticketId\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Ticket'\n  /serviceability:\n    get:\n     \
  \ operationId: checkServiceability\n      summary: Check Serviceability\n      description: Check carrier serviceability for a location.\n      tags:\n        - Serviceability\n      parameters:\n        - name: address\n          in: query\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ServiceabilityResult'\ntags:\n  - name: Serviceability\n    description: Carrier serviceability operations\n  - name: Tickets\n    description: Service ticket operations\ncomponents:\n  schemas:\n    Ticket:\n      type: object\n      properties:\n        id:\n          type: string\n        subject:\n          type: string\n        status:\n          type: string\n        priority:\n          type: string\n        createdAt:\n          type: string\n          format: date-time\n    TicketList:\n\
  \      type: object\n      properties:\n        tickets:\n          type: array\n          items:\n            $ref: '#/components/schemas/Ticket'\n    TicketRequest:\n      type: object\n      properties:\n        subject:\n          type: string\n        description:\n          type: string\n        priority:\n          type: string\n    ServiceabilityResult:\n      type: object\n      properties:\n        address:\n          type: string\n        serviceable:\n          type: boolean\n        availableServices:\n          type: array\n          items:\n            type: string\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/charter-communications/refs/heads/main/openapi/charter-communications-spectrum-enterprise-api-openapi.yml
tags:
- Enterprise
- Networking
- Telecommunications
- Ticketing
---
