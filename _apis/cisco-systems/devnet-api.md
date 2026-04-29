---
aid: cisco-systems:devnet-api
baseURL: https://developer.cisco.com/api
description: Cisco DevNet is the unified developer portal for Cisco Systems products, exposing APIs, SDKs, sandboxes, and learning resources for networking, security, collaboration, and cloud infrastructure. The DevNet catalog is the entry point for discovering and authenticating against the broader Cisco API surface.
humanURL: https://developer.cisco.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Cisco DevNet API Catalog
properties:
- type: Documentation
  url: https://developer.cisco.com/
- type: API Reference
  url: https://developer.cisco.com/docs/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cisco-systems/refs/heads/main/openapi/cisco-systems-cisco-api-openapi.yml
provider_name: Cisco Systems
provider_slug: cisco-systems
slug: devnet-api
source_filename: cisco-systems-cisco-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Cisco DevNet API\n  description: >-\n    Cisco DevNet provides APIs for networking, security, collaboration, and cloud infrastructure. Developers can programmatically configure and manage Cisco networking equipment, Webex services, and security tools.\n  version: '1.0'\n  contact:\n    name: Cisco Systems Developer Support\n    url: https://developer.cisco.com/\nexternalDocs:\n  description: Documentation\n  url: https://developer.cisco.com/\nservers:\n  - url: https://developer.cisco.com/api\n    description: Production\ntags:\n  - name: Networking\n    description: Networking operations\nsecurity:\n  - bearerAuth: []\npaths:\n  /status:\n    get:\n      operationId: getStatus\n      summary: Get API status\n      description: >-\n        Returns the current status of the API.\n      tags:\n        - Networking\n      responses:\n        '200':\n          description: Success\n          content:\n            application/json:\n             \
  \ schema:\n                type: object\n                properties:\n                  status:\n                    type: string\n                  version:\n                    type: string\n        '401':\n          description: Unauthorized\n        '429':\n          description: Too many requests\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cisco-systems/refs/heads/main/openapi/cisco-systems-cisco-api-openapi.yml
tags:
- Collaboration
- DevNet
- Infrastructure
- Networking
- Security
---
