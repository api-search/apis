---
aid: completedns:dns-history-api
baseURL: https://api.completedns.com/v2
description: The CompleteDNS API v2 returns the historical nameserver record for a domain, including counts of changes and drops, years of history, and a chronologically ordered list of events. Authentication uses an API key passed as a query parameter.
humanURL: https://completedns.com/api/documentation/v2
image: ''
layout: api
name: CompleteDNS API v2
properties:
- type: Documentation
  url: https://completedns.com/api/documentation/v2
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/completedns/refs/heads/main/openapi/completedns-v2-openapi.yml
- type: Spectral Rules
  url: https://raw.githubusercontent.com/api-evangelist/completedns/refs/heads/main/rules/completedns-rules.yml
- type: Naftiko Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/completedns/refs/heads/main/capabilities/completedns-dns-history-lookup.yml
provider_name: CompleteDNS
provider_slug: completedns
slug: dns-history-api
source_filename: completedns-v2-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: CompleteDNS API v2\n  description: >-\n    The CompleteDNS API v2 returns the historical nameserver record for a\n    domain. The service tracks nameserver changes and domain drops for over\n    twenty years and returns the chronological list of events for a queried\n    domain. Authentication is via an API key passed as a query string\n    parameter.\n  version: v2\n  contact:\n    name: CompleteDNS\n    url: https://completedns.com/contact\n  termsOfService: https://completedns.com/terms\nexternalDocs:\n  description: CompleteDNS API v2 Documentation\n  url: https://completedns.com/api/documentation/v2\nservers:\n  - url: https://api.completedns.com/v2\n    description: CompleteDNS v2 production API\ntags:\n  - name: DNS History\n    description: Nameserver and drop history for a domain\nsecurity:\n  - apiKey: []\npaths:\n  /dns-history/{domain}:\n    get:\n      operationId: getDnsHistory\n      summary: Get DNS history for a domain\n    \
  \  description: >-\n        Returns the full history of nameserver changes and drop events for\n        the requested domain, including the count of changes, count of\n        drops, years tracked, and a chronologically ordered list of events.\n      tags:\n        - DNS History\n      parameters:\n        - name: domain\n          in: path\n          required: true\n          description: The fully qualified domain to look up.\n          schema:\n            type: string\n            example: youtube.com\n        - name: key\n          in: query\n          required: true\n          description: API key issued in the CompleteDNS account API section.\n          schema:\n            type: string\n      responses:\n        '200':\n          description: DNS history record for the domain.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/DnsHistoryResponse'\n        '400':\n          description: Invalid domain or unsupported\
  \ TLD.\n        '401':\n          description: Missing or invalid API key.\n        '403':\n          description: IP restriction or quota exhausted.\n        '404':\n          description: Domain not tracked.\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: query\n      name: key\n  schemas:\n    DnsHistoryResponse:\n      type: object\n      properties:\n        domain:\n          type: string\n          description: The queried domain name.\n        drops:\n          type: integer\n          description: Total nameserver removal events recorded.\n        changes:\n          type: integer\n          description: Total nameserver change events recorded.\n        years:\n          type: number\n          description: Years of history tracked for the domain.\n        was_parked:\n          type: boolean\n          description: Whether the domain was parked at any point in the history.\n        events:\n          type: array\n          items:\n            $ref:\
  \ '#/components/schemas/DnsEvent'\n    DnsEvent:\n      type: object\n      properties:\n        date:\n          type: string\n          description: Exact date or date range when the event occurred.\n        type:\n          type: string\n          enum:\n            - start_tracking\n            - dropped\n            - created\n            - change\n        nameservers:\n          type: array\n          items:\n            type: string\n          description: Active nameservers at the time of the event.\n        changes:\n          type: array\n          items:\n            $ref: '#/components/schemas/NameserverChange'\n    NameserverChange:\n      type: object\n      properties:\n        action:\n          type: string\n          enum:\n            - added\n            - removed\n        nameserver:\n          type: string\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/completedns/refs/heads/main/openapi/completedns-v2-openapi.yml
tags:
- DNS History
- Domains
- Lookup
- Nameservers
---
