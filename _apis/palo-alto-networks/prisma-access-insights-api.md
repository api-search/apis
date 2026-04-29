---
aid: palo-alto-networks:prisma-access-insights-api
baseURL: https://api.sase.paloaltonetworks.com
description: A REST API for querying the health and performance of Prisma Access network deployments across multiple API versions (v1.0, v2.0, v3.0). Supports data resource queries for tunnel status, bandwidth utilization, connected user analytics, site health, accelerated application performance, and PAB events. Available for both cloud-managed (TSG-based) and Panorama-managed Prisma Access customers. Uses OAuth 2.0 bearer token authentication consistent with the SASE platform.
humanURL: https://pan.dev/access/api/insights/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Prisma Access Insights API
properties:
- type: Documentation
  url: https://pan.dev/access/api/insights/
- type: APIReference
  url: https://pan.dev/access/api/insights/1.0/
- type: APIReference
  url: https://pan.dev/access/api/insights/2.0/
- type: APIReference
  url: https://pan.dev/access/api/insights/3.0/
- type: GettingStarted
  url: https://pan.dev/sase/docs/getstarted/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/openapi/palo-alto-prisma-access-insights-api-openapi-original.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-insights-api-custom-query-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-insights-api-data-resource-query-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-insights-api-data-resource-response-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-insights-api-export-job-response-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-insights-api-export-job-status-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-insights-api-query-filter-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-insights-api-time-range-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-insights-api-custom-query-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-insights-api-data-resource-query-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-insights-api-data-resource-response-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-insights-api-export-job-response-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-insights-api-export-job-status-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-insights-api-query-filter-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-insights-api-time-range-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-ld/palo-alto-prisma-access-insights-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-insights-api-custom-query-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-insights-api-data-resource-query-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-insights-api-data-resource-response-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-insights-api-export-job-response-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-insights-api-export-job-status-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-insights-api-query-filter-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-insights-api-time-range-example.json
provider_name: Palo Alto Networks
provider_slug: palo-alto-networks
slug: prisma-access-insights-api
source_yaml: "aid: palo-alto-networks:prisma-access-insights-api\nname: Prisma Access Insights API\ntags:\n- Analytics\n- Monitoring\n- Network Health\n- Prisma Access\n- SASE\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api.sase.paloaltonetworks.com\nhumanURL: https://pan.dev/access/api/insights/\nproperties:\n- url: https://pan.dev/access/api/insights/\n  type: Documentation\n- url: https://pan.dev/access/api/insights/1.0/\n  type: APIReference\n- url: https://pan.dev/access/api/insights/2.0/\n  type: APIReference\n- url: https://pan.dev/access/api/insights/3.0/\n  type: APIReference\n- url: https://pan.dev/sase/docs/getstarted/\n  type: GettingStarted\n- url: openapi/palo-alto-prisma-access-insights-api-openapi-original.yml\n  type: OpenAPI\n- url: json-schema/prisma-access-insights-api-custom-query-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-access-insights-api-data-resource-query-schema.json\n  type: JSONSchema\n\
  - url: json-schema/prisma-access-insights-api-data-resource-response-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-access-insights-api-export-job-response-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-access-insights-api-export-job-status-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-access-insights-api-query-filter-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-access-insights-api-time-range-schema.json\n  type: JSONSchema\n- url: json-structure/prisma-access-insights-api-custom-query-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-access-insights-api-data-resource-query-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-access-insights-api-data-resource-response-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-access-insights-api-export-job-response-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-access-insights-api-export-job-status-structure.json\n  type: JSONStructure\n\
  - url: json-structure/prisma-access-insights-api-query-filter-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-access-insights-api-time-range-structure.json\n  type: JSONStructure\n- url: json-ld/palo-alto-prisma-access-insights-api-context.jsonld\n  type: JSON-LD\n- url: examples/prisma-access-insights-api-custom-query-example.json\n  type: Example\n- url: examples/prisma-access-insights-api-data-resource-query-example.json\n  type: Example\n- url: examples/prisma-access-insights-api-data-resource-response-example.json\n  type: Example\n- url: examples/prisma-access-insights-api-export-job-response-example.json\n  type: Example\n- url: examples/prisma-access-insights-api-export-job-status-example.json\n  type: Example\n- url: examples/prisma-access-insights-api-query-filter-example.json\n  type: Example\n- url: examples/prisma-access-insights-api-time-range-example.json\n  type: Example\ndescription: A REST API for querying the health and performance of Prisma Access\
  \ network deployments across\n  multiple API versions (v1.0, v2.0, v3.0). Supports data resource queries for tunnel status, bandwidth\n  utilization, connected user analytics, site health, accelerated application performance, and PAB events.\n  Available for both cloud-managed (TSG-based) and Panorama-managed Prisma Access customers. Uses OAuth\n  2.0 bearer token authentication consistent with the SASE platform.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/apis.yml
tags:
- Analytics
- Monitoring
- Network Health
- Prisma Access
- SASE
---
