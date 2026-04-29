---
aid: completedns:ns-history-api
baseURL: https://api.completedns.com/v1
description: The CompleteDNS API v1 (legacy) returns the historical nameserver record for a domain. Includes drop and change counts, TLD support indicator, and chronologically ordered events with added/removed nameservers. CompleteDNS recommends migrating to v2.
humanURL: https://completedns.com/api/documentation/v1
image: ''
layout: api
name: CompleteDNS API v1
properties:
- type: Documentation
  url: https://completedns.com/api/documentation/v1
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/completedns/refs/heads/main/openapi/completedns-v1-openapi.yml
- type: Spectral Rules
  url: https://raw.githubusercontent.com/api-evangelist/completedns/refs/heads/main/rules/completedns-rules.yml
- type: Naftiko Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/completedns/refs/heads/main/capabilities/completedns-dns-history-lookup.yml
provider_name: CompleteDNS
provider_slug: completedns
slug: ns-history-api
source_filename: completedns-v1-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: CompleteDNS API v1\n  description: >-\n    The CompleteDNS API v1 returns the historical nameserver record for a\n    domain (legacy version). The service tracks nameserver changes and\n    domain drops and returns chronologically ordered events for a queried\n    domain. Authentication is via an API key passed as a query string\n    parameter. CompleteDNS recommends using the v2 API for new\n    integrations.\n  version: v1\n  contact:\n    name: CompleteDNS\n    url: https://completedns.com/contact\n  termsOfService: https://completedns.com/terms\nexternalDocs:\n  description: CompleteDNS API v1 Documentation\n  url: https://completedns.com/api/documentation/v1\nservers:\n  - url: https://api.completedns.com/v1\n    description: CompleteDNS v1 production API\ntags:\n  - name: NS History\n    description: Nameserver history (legacy) for a domain\nsecurity:\n  - apiKey: []\npaths:\n  /ns-history/{domain}:\n    get:\n      operationId: getNsHistory\n\
  \      summary: Get nameserver history for a domain\n      description: >-\n        Returns the full history of nameserver changes and drop events for\n        the requested domain. Response includes drop count, change count,\n        years tracked, TLD support flag, and a chronologically ordered list\n        of events.\n      tags:\n        - NS History\n      parameters:\n        - name: domain\n          in: path\n          required: true\n          description: The fully qualified domain to look up.\n          schema:\n            type: string\n            example: youtube.com\n        - name: key\n          in: query\n          required: true\n          description: API key issued in the CompleteDNS account API section.\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Nameserver history record for the domain.\n          headers:\n            requestsLeft:\n              description: Number of API requests remaining in the current\
  \ quota.\n              schema:\n                type: integer\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/NsHistoryResponse'\n        '400':\n          description: Invalid domain.\n        '401':\n          description: Missing or invalid API key.\n        '403':\n          description: IP restriction or quota exhausted.\n        '404':\n          description: Domain not tracked.\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: query\n      name: key\n  schemas:\n    NsHistoryResponse:\n      type: object\n      properties:\n        drops:\n          type: integer\n          description: Total nameserver removal events recorded.\n        changes:\n          type: integer\n          description: Total nameserver change events recorded.\n        years:\n          type: number\n          description: Years of history tracked for the domain.\n        supported:\n          type: boolean\n\
  \          description: Whether the queried TLD is supported.\n        data:\n          type: array\n          items:\n            $ref: '#/components/schemas/NsEvent'\n    NsEvent:\n      type: object\n      properties:\n        type:\n          type: string\n          enum:\n            - started_tracking\n            - ns_change\n            - new_domain\n            - deleted_domain\n        date:\n          type: string\n        nameservers:\n          type: array\n          items:\n            type: object\n            properties:\n              added_ns:\n                type: string\n              deleted_ns:\n                type: string\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/completedns/refs/heads/main/openapi/completedns-v1-openapi.yml
tags:
- DNS History
- Legacy
- Lookup
- Nameservers
---
