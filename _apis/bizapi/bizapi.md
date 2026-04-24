---
aid: bizapi:bizapi
baseURL: ''
description: Real-time REST API from the NAICS Association that returns firmographic data on over 220 million US and international business locations. Provides DUNS numbers, SIC codes, NAICS codes, company details, contact information, sales volume, employee counts, and corporate hierarchy. Supports both live production and test (sandbox) endpoints. Rate limited to 3 requests per rolling second. Authentication via HTTP Basic with credentials provided at account activation.
humanURL: https://www.naics.com/business-intelligence-api/
image: ''
layout: api
name: BizAPI Business Intelligence API
properties:
- type: Documentation
  url: https://www.naics.com/business-intelligence-api/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bizapi/refs/heads/main/openapi/bizapi-business-intelligence-api-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/bizapi/refs/heads/main/json-schema/bizapi-company-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/bizapi/refs/heads/main/json-structure/bizapi-company-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/bizapi/refs/heads/main/json-ld/bizapi-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/bizapi/refs/heads/main/examples/bizapi-company-example.json
provider_name: BizAPI
provider_slug: bizapi
slug: bizapi
tags:
- Business Intelligence
- Company Data
- Firmographic Data
- NAICS
- SIC
---
