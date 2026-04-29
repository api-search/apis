---
aid: cbre:cbre-api
baseURL: https://api.cbre.com
description: CBRE provides APIs for commercial real estate data including property listings, market analytics, facilities management, lease administration, valuation, and investment management. The platform enables partners and clients to access CBRE's real estate intelligence and integrate with internal systems.
humanURL: https://developer.cbre.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CBRE Developer API
properties:
- type: Documentation
  url: https://developer.cbre.com/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cbre/refs/heads/main/openapi/cbre-cbre-api-openapi.yml
- type: Portal
  url: https://developer.cbre.com/
provider_name: CBRE
provider_slug: cbre
slug: cbre-api
source_filename: cbre-cbre-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: CBRE API\n  description: >-\n    CBRE provides APIs for commercial real estate data including property listings, market analytics, and facility management. The platform enables partners to access CBRE's real estate intelligence.\n  version: '1.0'\n  contact:\n    name: CBRE Developer Support\n    url: https://developer.cbre.com/\nexternalDocs:\n  description: Documentation\n  url: https://developer.cbre.com/\nservers:\n  - url: https://api.cbre.com\n    description: Production\ntags:\n  - name: Real Estate\n    description: Real Estate operations\nsecurity:\n  - bearerAuth: []\npaths:\n  /status:\n    get:\n      operationId: getStatus\n      summary: Get API status\n      description: >-\n        Returns the current status of the API.\n      tags:\n        - Real Estate\n      responses:\n        '200':\n          description: Success\n          content:\n            application/json:\n              schema:\n                type: object\n  \
  \              properties:\n                  status:\n                    type: string\n                  version:\n                    type: string\n        '401':\n          description: Unauthorized\n        '429':\n          description: Too many requests\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cbre/refs/heads/main/openapi/cbre-cbre-api-openapi.yml
tags:
- Analytics
- Commercial Property
- Facilities
- Investment
- Real Estate
- Valuation
---
