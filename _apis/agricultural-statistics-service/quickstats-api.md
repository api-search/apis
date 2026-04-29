---
aid: agricultural-statistics-service:quickstats-api
baseURL: https://quickstats.nass.usda.gov/api
description: The QuickStats API provides direct programmatic access to the statistical information contained in the NASS Quick Stats database, covering official published aggregate estimates related to U.S. agricultural production. The API supports filtering by commodity, location, and time with comparison operators. Responses are available in JSON, XML, or CSV format. An API key is required; maximum 50,000 records per request.
humanURL: https://quickstats.nass.usda.gov/api
image: ''
layout: api
name: USDA NASS QuickStats API
properties:
- type: Documentation
  url: https://quickstats.nass.usda.gov/api
- type: APIReference
  url: https://quickstats.nass.usda.gov/api/#param_define
- type: Authentication
  url: https://quickstats.nass.usda.gov/api
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/agricultural-statistics-service/refs/heads/main/openapi/agricultural-statistics-service-quickstats-api.yaml
- title: Statistics Record Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/agricultural-statistics-service/refs/heads/main/json-schema/quickstats-api-statistics-record-schema.json
- title: Statistics Response Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/agricultural-statistics-service/refs/heads/main/json-schema/quickstats-api-statistics-response-schema.json
- title: Count Response Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/agricultural-statistics-service/refs/heads/main/json-schema/quickstats-api-count-response-schema.json
- title: Statistics Record Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/agricultural-statistics-service/refs/heads/main/json-structure/quickstats-api-statistics-record-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/agricultural-statistics-service/refs/heads/main/json-ld/agricultural-statistics-service-quickstats-api-context.jsonld
provider_name: Agricultural Statistics Service
provider_slug: agricultural-statistics-service
slug: quickstats-api
source_yaml: "aid: agricultural-statistics-service:quickstats-api\nname: USDA NASS QuickStats API\ndescription: The QuickStats API provides direct programmatic access to the statistical information contained\n  in the NASS Quick Stats database, covering official published aggregate estimates related to U.S. agricultural\n  production. The API supports filtering by commodity, location, and time with comparison operators. Responses\n  are available in JSON, XML, or CSV format. An API key is required; maximum 50,000 records per request.\nhumanURL: https://quickstats.nass.usda.gov/api\nbaseURL: https://quickstats.nass.usda.gov/api\ntags:\n- Agricultural Statistics\n- Crop Data\n- Livestock Data\n- Census Of Agriculture\n- Open Data\nproperties:\n- type: Documentation\n  url: https://quickstats.nass.usda.gov/api\n- type: APIReference\n  url: https://quickstats.nass.usda.gov/api/#param_define\n- type: Authentication\n  url: https://quickstats.nass.usda.gov/api\n- type: OpenAPI\n  url: openapi/agricultural-statistics-service-quickstats-api.yaml\n\
  - type: JSONSchema\n  url: json-schema/quickstats-api-statistics-record-schema.json\n  title: Statistics Record Schema\n- type: JSONSchema\n  url: json-schema/quickstats-api-statistics-response-schema.json\n  title: Statistics Response Schema\n- type: JSONSchema\n  url: json-schema/quickstats-api-count-response-schema.json\n  title: Count Response Schema\n- type: JSONStructure\n  url: json-structure/quickstats-api-statistics-record-structure.json\n  title: Statistics Record Structure\n- type: JSON-LD\n  url: json-ld/agricultural-statistics-service-quickstats-api-context.jsonld\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/agricultural-statistics-service/refs/heads/main/apis.yml
tags:
- Agricultural Statistics
- Crop Data
- Livestock Data
- Census Of Agriculture
- Open Data
---
