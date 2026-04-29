---
aid: palo-alto-networks:prisma-cloud-dspm-api
baseURL: https://api.prismacloud.io
description: A REST API for Data Security Posture Management within Prisma Cloud providing visibility and control over sensitive data stored across multi-cloud environments. The API supports data discovery, classification, and risk assessment for cloud data stores including databases, object storage, and file systems. Authentication uses JWT tokens consistent with the broader Prisma Cloud API framework.
humanURL: https://pan.dev/prisma-cloud/api/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Prisma Cloud DSPM API
properties:
- type: Documentation
  url: https://pan.dev/prisma-cloud/api/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/openapi/palo-alto-prisma-cloud-dspm-api-openapi-original.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-cloud-dspm-api-classification-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-cloud-dspm-api-data-asset-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-cloud-dspm-api-data-risk-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-cloud-dspm-api-data-security-alert-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-cloud-dspm-api-data-store-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-cloud-dspm-api-dspm-policy-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-cloud-dspm-api-classification-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-cloud-dspm-api-data-asset-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-cloud-dspm-api-data-risk-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-cloud-dspm-api-data-security-alert-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-cloud-dspm-api-data-store-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-cloud-dspm-api-dspm-policy-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-ld/palo-alto-prisma-cloud-dspm-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-cloud-dspm-api-classification-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-cloud-dspm-api-data-asset-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-cloud-dspm-api-data-risk-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-cloud-dspm-api-data-security-alert-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-cloud-dspm-api-data-store-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-cloud-dspm-api-dspm-policy-example.json
provider_name: Palo Alto Networks
provider_slug: palo-alto-networks
slug: prisma-cloud-dspm-api
source_yaml: "aid: palo-alto-networks:prisma-cloud-dspm-api\nname: Prisma Cloud DSPM API\ntags:\n- Classification\n- Cloud Data\n- Data Posture\n- Data Security\n- Multi-Cloud\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api.prismacloud.io\nhumanURL: https://pan.dev/prisma-cloud/api/\nproperties:\n- url: https://pan.dev/prisma-cloud/api/\n  type: Documentation\n- url: openapi/palo-alto-prisma-cloud-dspm-api-openapi-original.yml\n  type: OpenAPI\n- url: json-schema/prisma-cloud-dspm-api-classification-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-cloud-dspm-api-data-asset-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-cloud-dspm-api-data-risk-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-cloud-dspm-api-data-security-alert-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-cloud-dspm-api-data-store-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-cloud-dspm-api-dspm-policy-schema.json\n\
  \  type: JSONSchema\n- url: json-structure/prisma-cloud-dspm-api-classification-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-cloud-dspm-api-data-asset-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-cloud-dspm-api-data-risk-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-cloud-dspm-api-data-security-alert-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-cloud-dspm-api-data-store-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-cloud-dspm-api-dspm-policy-structure.json\n  type: JSONStructure\n- url: json-ld/palo-alto-prisma-cloud-dspm-api-context.jsonld\n  type: JSON-LD\n- url: examples/prisma-cloud-dspm-api-classification-example.json\n  type: Example\n- url: examples/prisma-cloud-dspm-api-data-asset-example.json\n  type: Example\n- url: examples/prisma-cloud-dspm-api-data-risk-example.json\n  type: Example\n- url: examples/prisma-cloud-dspm-api-data-security-alert-example.json\n  type:\
  \ Example\n- url: examples/prisma-cloud-dspm-api-data-store-example.json\n  type: Example\n- url: examples/prisma-cloud-dspm-api-dspm-policy-example.json\n  type: Example\ndescription: A REST API for Data Security Posture Management within Prisma Cloud providing visibility\n  and control over sensitive data stored across multi-cloud environments. The API supports data discovery,\n  classification, and risk assessment for cloud data stores including databases, object storage, and file\n  systems. Authentication uses JWT tokens consistent with the broader Prisma Cloud API framework.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/apis.yml
tags:
- Classification
- Cloud Data
- Data Posture
- Data Security
- Multi-Cloud
---
