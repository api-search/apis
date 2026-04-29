---
aid: checkpoint:harmony-email-api
baseURL: https://smart-api.avanan.net/v2.0
description: REST API for Harmony Email and Collaboration (formerly Avanan) surfacing email security events, quarantined items, and admin actions.
humanURL: https://sc1.checkpoint.com/documents/Harmony_Email_and_Collaboration_API_Reference/Topics-HEC-Avanan-API-Reference-Guide/Overview/API-Overview.htm
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Check Point Harmony Email API
properties:
- type: Documentation
  url: https://sc1.checkpoint.com/documents/Harmony_Email_and_Collaboration_API_Reference/Topics-HEC-Avanan-API-Reference-Guide/Overview/API-Overview.htm
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-harmony-email-api-openapi.yml
provider_name: Check Point
provider_slug: checkpoint
slug: harmony-email-api
source_filename: checkpoint-harmony-email-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Check Point Harmony Email API\n  description: >-\n    REST API for Check Point Harmony Email and Collaboration (formerly\n    Avanan). Surfaces email security events, quarantined items, and\n    administrative actions.\n  version: '1.0'\n  contact:\n    name: Check Point Harmony Support\n    url: https://www.checkpoint.com/harmony/email-security/\nexternalDocs:\n  description: Harmony Email API Reference\n  url: https://sc1.checkpoint.com/documents/Harmony_Email_and_Collaboration_API_Reference/Topics-HEC-Avanan-API-Reference-Guide/Overview/API-Overview.htm\nservers:\n  - url: https://smart-api.avanan.net/v2.0\n    description: Harmony Email Production\ntags:\n  - name: Events\n  - name: Quarantine\nsecurity:\n  - bearerAuth: []\npaths:\n  /events:\n    get:\n      operationId: listEvents\n      summary: List Harmony Email security events\n      tags: [Events]\n      parameters:\n        - name: startDate\n          in: query\n          schema:\n\
  \            type: string\n            format: date-time\n        - name: endDate\n          in: query\n          schema:\n            type: string\n            format: date-time\n      responses:\n        '200':\n          description: Events list\n  /quarantine:\n    get:\n      operationId: listQuarantine\n      summary: List quarantined items\n      tags: [Quarantine]\n      responses:\n        '200':\n          description: Quarantine items\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-harmony-email-api-openapi.yml
tags:
- Email Security
- Harmony
---
