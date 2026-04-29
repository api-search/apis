---
aid: checkpoint:gaia-api
baseURL: https://gateway.example.com/gaia_api
description: REST API for the Check Point Gaia operating system. Manages gateway interfaces, routing, system info, and configuration.
humanURL: https://sc1.checkpoint.com/documents/latest/GaiaAPIs/
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Check Point Gaia API
properties:
- type: Documentation
  url: https://sc1.checkpoint.com/documents/latest/GaiaAPIs/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-gaia-api-openapi.yml
provider_name: Check Point
provider_slug: checkpoint
slug: gaia-api
source_filename: checkpoint-gaia-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Check Point Gaia API\n  description: >-\n    REST API for the Check Point Gaia operating system. Allows\n    administrators to manage gateway interfaces, routing, and system\n    configuration through automation.\n  version: '1.8'\n  contact:\n    name: Check Point Support\n    url: https://www.checkpoint.com/support-services/\nexternalDocs:\n  description: Gaia API Reference\n  url: https://sc1.checkpoint.com/documents/latest/GaiaAPIs/\nservers:\n  - url: https://{gateway}/gaia_api\n    description: Gaia REST API\n    variables:\n      gateway:\n        default: gateway.example.com\ntags:\n  - name: Login\n  - name: System\n  - name: Interfaces\n  - name: Routes\nsecurity:\n  - sidToken: []\npaths:\n  /login:\n    post:\n      operationId: gaiaLogin\n      summary: Login to Gaia\n      tags: [Login]\n      security: []\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n          \
  \    type: object\n              required: [user, password]\n              properties:\n                user:\n                  type: string\n                password:\n                  type: string\n      responses:\n        '200':\n          description: Session\n  /show-system-info:\n    post:\n      operationId: showSystemInfo\n      summary: Show system information\n      tags: [System]\n      responses:\n        '200':\n          description: System info\n  /show-interfaces:\n    post:\n      operationId: showInterfaces\n      summary: Show network interfaces\n      tags: [Interfaces]\n      responses:\n        '200':\n          description: Interfaces\n  /show-static-routes:\n    post:\n      operationId: showStaticRoutes\n      summary: Show static routes\n      tags: [Routes]\n      responses:\n        '200':\n          description: Static routes\ncomponents:\n  securitySchemes:\n    sidToken:\n      type: apiKey\n      in: header\n      name: X-chkp-sid\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-gaia-api-openapi.yml
tags:
- Gaia
- Operating System
---
