---
aid: palo-alto-networks:cortex-xpanse-api
baseURL: https://api-{fqdn}/public_api/v1/
description: A REST API for Cortex Xpanse, the attack surface management platform that discovers, evaluates, and mitigates risks on internet-facing assets. The API provides programmatic access to asset inventories, attack surface rules, risk identification, and remediation workflows. Supports querying discovered services, certificates, domains, and cloud resources exposed to the internet. Authentication uses RBAC API key pairs consistent with other Cortex platform APIs.
humanURL: https://docs-cortex.paloaltonetworks.com/r/Cortex-Xpanse-REST-API
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Cortex Xpanse API
properties:
- type: Documentation
  url: https://docs-cortex.paloaltonetworks.com/r/Cortex-Xpanse-REST-API
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/openapi/palo-alto-cortex-xpanse-api-openapi-original.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cortex-xpanse-api-asm-incident-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cortex-xpanse-api-asset-internet-exposure-detail-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cortex-xpanse-api-asset-internet-exposure-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cortex-xpanse-api-attack-surface-rule-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cortex-xpanse-api-audit-log-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cortex-xpanse-api-exposed-service-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cortex-xpanse-api-filter-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cortex-xpanse-api-owned-ip-range-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/cortex-xpanse-api-sort-order-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cortex-xpanse-api-asm-incident-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cortex-xpanse-api-asset-internet-exposure-detail-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cortex-xpanse-api-asset-internet-exposure-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cortex-xpanse-api-attack-surface-rule-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cortex-xpanse-api-audit-log-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cortex-xpanse-api-exposed-service-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cortex-xpanse-api-filter-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cortex-xpanse-api-owned-ip-range-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/cortex-xpanse-api-sort-order-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-ld/palo-alto-cortex-xpanse-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cortex-xpanse-api-asm-incident-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cortex-xpanse-api-asset-internet-exposure-detail-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cortex-xpanse-api-asset-internet-exposure-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cortex-xpanse-api-attack-surface-rule-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cortex-xpanse-api-audit-log-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cortex-xpanse-api-exposed-service-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cortex-xpanse-api-filter-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cortex-xpanse-api-owned-ip-range-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/cortex-xpanse-api-sort-order-example.json
provider_name: Palo Alto Networks
provider_slug: palo-alto-networks
slug: cortex-xpanse-api
source_yaml: "aid: palo-alto-networks:cortex-xpanse-api\nname: Cortex Xpanse API\ntags:\n- Asset Discovery\n- Attack Surface Management\n- Exposure Management\n- Internet-Facing Assets\n- Risk Assessment\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api-{fqdn}/public_api/v1/\nhumanURL: https://docs-cortex.paloaltonetworks.com/r/Cortex-Xpanse-REST-API\nproperties:\n- url: https://docs-cortex.paloaltonetworks.com/r/Cortex-Xpanse-REST-API\n  type: Documentation\n- url: openapi/palo-alto-cortex-xpanse-api-openapi-original.yml\n  type: OpenAPI\n- url: json-schema/cortex-xpanse-api-asm-incident-schema.json\n  type: JSONSchema\n- url: json-schema/cortex-xpanse-api-asset-internet-exposure-detail-schema.json\n  type: JSONSchema\n- url: json-schema/cortex-xpanse-api-asset-internet-exposure-schema.json\n  type: JSONSchema\n- url: json-schema/cortex-xpanse-api-attack-surface-rule-schema.json\n  type: JSONSchema\n- url: json-schema/cortex-xpanse-api-audit-log-schema.json\n\
  \  type: JSONSchema\n- url: json-schema/cortex-xpanse-api-exposed-service-schema.json\n  type: JSONSchema\n- url: json-schema/cortex-xpanse-api-filter-schema.json\n  type: JSONSchema\n- url: json-schema/cortex-xpanse-api-owned-ip-range-schema.json\n  type: JSONSchema\n- url: json-schema/cortex-xpanse-api-sort-order-schema.json\n  type: JSONSchema\n- url: json-structure/cortex-xpanse-api-asm-incident-structure.json\n  type: JSONStructure\n- url: json-structure/cortex-xpanse-api-asset-internet-exposure-detail-structure.json\n  type: JSONStructure\n- url: json-structure/cortex-xpanse-api-asset-internet-exposure-structure.json\n  type: JSONStructure\n- url: json-structure/cortex-xpanse-api-attack-surface-rule-structure.json\n  type: JSONStructure\n- url: json-structure/cortex-xpanse-api-audit-log-structure.json\n  type: JSONStructure\n- url: json-structure/cortex-xpanse-api-exposed-service-structure.json\n  type: JSONStructure\n- url: json-structure/cortex-xpanse-api-filter-structure.json\n\
  \  type: JSONStructure\n- url: json-structure/cortex-xpanse-api-owned-ip-range-structure.json\n  type: JSONStructure\n- url: json-structure/cortex-xpanse-api-sort-order-structure.json\n  type: JSONStructure\n- url: json-ld/palo-alto-cortex-xpanse-api-context.jsonld\n  type: JSON-LD\n- url: examples/cortex-xpanse-api-asm-incident-example.json\n  type: Example\n- url: examples/cortex-xpanse-api-asset-internet-exposure-detail-example.json\n  type: Example\n- url: examples/cortex-xpanse-api-asset-internet-exposure-example.json\n  type: Example\n- url: examples/cortex-xpanse-api-attack-surface-rule-example.json\n  type: Example\n- url: examples/cortex-xpanse-api-audit-log-example.json\n  type: Example\n- url: examples/cortex-xpanse-api-exposed-service-example.json\n  type: Example\n- url: examples/cortex-xpanse-api-filter-example.json\n  type: Example\n- url: examples/cortex-xpanse-api-owned-ip-range-example.json\n  type: Example\n- url: examples/cortex-xpanse-api-sort-order-example.json\n\
  \  type: Example\ndescription: A REST API for Cortex Xpanse, the attack surface management platform that discovers, evaluates,\n  and mitigates risks on internet-facing assets. The API provides programmatic access to asset inventories,\n  attack surface rules, risk identification, and remediation workflows. Supports querying discovered services,\n  certificates, domains, and cloud resources exposed to the internet. Authentication uses RBAC API key\n  pairs consistent with other Cortex platform APIs.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/apis.yml
tags:
- Asset Discovery
- Attack Surface Management
- Exposure Management
- Internet-Facing Assets
- Risk Assessment
---
