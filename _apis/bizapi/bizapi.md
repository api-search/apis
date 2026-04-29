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
source_yaml: "aid: bizapi:bizapi\nname: BizAPI Business Intelligence API\ndescription: Real-time REST API from the NAICS Association that returns firmographic data on over 220\n  million US and international business locations. Provides DUNS numbers, SIC codes, NAICS codes, company\n  details, contact information, sales volume, employee counts, and corporate hierarchy. Supports both\n  live production and test (sandbox) endpoints. Rate limited to 3 requests per rolling second. Authentication\n  via HTTP Basic with credentials provided at account activation.\nhumanURL: https://www.naics.com/business-intelligence-api/\ntags:\n- Business Intelligence\n- Company Data\n- Firmographic Data\n- NAICS\n- SIC\nproperties:\n- type: Documentation\n  url: https://www.naics.com/business-intelligence-api/\n- type: OpenAPI\n  url: openapi/bizapi-business-intelligence-api-openapi.yml\n- type: JSONSchema\n  url: json-schema/bizapi-company-schema.json\n- type: JSONStructure\n  url: json-structure/bizapi-company-structure.json\n\
  - type: JSONLD\n  url: json-ld/bizapi-context.jsonld\n- type: Example\n  url: examples/bizapi-company-example.json\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bizapi/refs/heads/main/apis.yml
tags:
- Business Intelligence
- Company Data
- Firmographic Data
- NAICS
- SIC
---
