---
aid: palo-alto-networks:prisma-sd-wan-api
baseURL: https://api.sase.paloaltonetworks.com
description: REST APIs for managing Prisma SD-WAN (formerly CloudGenix) branch networking infrastructure. The API supports configuration of sites, WAN interfaces, routing policies, application definitions, path quality monitoring, and network analytics. Provides both a unified API using SASE OAuth 2.0 authentication and a legacy API with session token authentication.
humanURL: https://pan.dev/sdwan/docs/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Prisma SD-WAN API
properties:
- type: Documentation
  url: https://pan.dev/sdwan/docs/
- type: APIReference
  url: https://pan.dev/sdwan/api/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/openapi/palo-alto-prisma-sd-wan-api-openapi-original.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-sd-wan-api-alarm-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-sd-wan-api-application-usage-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-sd-wan-api-lan-network-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-sd-wan-api-path-rule-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-sd-wan-api-qo-s-rule-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-sd-wan-api-site-metric-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-sd-wan-api-site-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-sd-wan-api-wan-interface-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-sd-wan-api-alarm-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-sd-wan-api-application-usage-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-sd-wan-api-lan-network-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-sd-wan-api-path-rule-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-sd-wan-api-qo-s-rule-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-sd-wan-api-site-metric-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-sd-wan-api-site-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-sd-wan-api-wan-interface-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-ld/palo-alto-prisma-sd-wan-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-sd-wan-api-alarm-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-sd-wan-api-application-usage-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-sd-wan-api-lan-network-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-sd-wan-api-path-rule-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-sd-wan-api-qo-s-rule-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-sd-wan-api-site-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-sd-wan-api-site-metric-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-sd-wan-api-wan-interface-example.json
provider_name: Palo Alto Networks
provider_slug: palo-alto-networks
slug: prisma-sd-wan-api
source_yaml: "aid: palo-alto-networks:prisma-sd-wan-api\nname: Prisma SD-WAN API\ntags:\n- Branch Networking\n- CloudGenix\n- Routing\n- SD-WAN\n- WAN Optimization\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api.sase.paloaltonetworks.com\nhumanURL: https://pan.dev/sdwan/docs/\nproperties:\n- url: https://pan.dev/sdwan/docs/\n  type: Documentation\n- url: https://pan.dev/sdwan/api/\n  type: APIReference\n- url: openapi/palo-alto-prisma-sd-wan-api-openapi-original.yml\n  type: OpenAPI\n- url: json-schema/prisma-sd-wan-api-alarm-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-sd-wan-api-application-usage-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-sd-wan-api-lan-network-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-sd-wan-api-path-rule-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-sd-wan-api-qo-s-rule-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-sd-wan-api-site-metric-schema.json\n\
  \  type: JSONSchema\n- url: json-schema/prisma-sd-wan-api-site-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-sd-wan-api-wan-interface-schema.json\n  type: JSONSchema\n- url: json-structure/prisma-sd-wan-api-alarm-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-sd-wan-api-application-usage-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-sd-wan-api-lan-network-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-sd-wan-api-path-rule-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-sd-wan-api-qo-s-rule-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-sd-wan-api-site-metric-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-sd-wan-api-site-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-sd-wan-api-wan-interface-structure.json\n  type: JSONStructure\n- url: json-ld/palo-alto-prisma-sd-wan-api-context.jsonld\n  type: JSON-LD\n- url: examples/prisma-sd-wan-api-alarm-example.json\n\
  \  type: Example\n- url: examples/prisma-sd-wan-api-application-usage-example.json\n  type: Example\n- url: examples/prisma-sd-wan-api-lan-network-example.json\n  type: Example\n- url: examples/prisma-sd-wan-api-path-rule-example.json\n  type: Example\n- url: examples/prisma-sd-wan-api-qo-s-rule-example.json\n  type: Example\n- url: examples/prisma-sd-wan-api-site-example.json\n  type: Example\n- url: examples/prisma-sd-wan-api-site-metric-example.json\n  type: Example\n- url: examples/prisma-sd-wan-api-wan-interface-example.json\n  type: Example\ndescription: REST APIs for managing Prisma SD-WAN (formerly CloudGenix) branch networking infrastructure.\n  The API supports configuration of sites, WAN interfaces, routing policies, application definitions,\n  path quality monitoring, and network analytics. Provides both a unified API using SASE OAuth 2.0 authentication\n  and a legacy API with session token authentication.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/apis.yml
tags:
- Branch Networking
- CloudGenix
- Routing
- SD-WAN
- WAN Optimization
---
