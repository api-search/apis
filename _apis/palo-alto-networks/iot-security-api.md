---
aid: palo-alto-networks:iot-security-api
baseURL: https://{customer}.iot.paloaltonetworks.com/pub/v4.0/
description: A REST API for managing IoT and OT device security including device discovery, profiling, vulnerability assessment, and security policy recommendations. The API provides endpoints for retrieving discovered device inventories, security alerts, vulnerability details, and recommended network segmentation policies. Authentication uses X-Key-Id and X-Access-Key headers with keys generated from the IoT Security portal. Rate limited to 60 requests per minute.
humanURL: https://pan.dev/iot/api/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: IoT Security API
properties:
- type: Documentation
  url: https://pan.dev/iot/api/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/openapi/palo-alto-iot-security-api-openapi-original.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/iot-security-api-alert-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/iot-security-api-asset-report-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/iot-security-api-device-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/iot-security-api-device-tag-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/iot-security-api-policy-recommendation-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/iot-security-api-vulnerability-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/iot-security-api-alert-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/iot-security-api-asset-report-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/iot-security-api-device-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/iot-security-api-device-tag-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/iot-security-api-policy-recommendation-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/iot-security-api-vulnerability-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-ld/palo-alto-iot-security-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/iot-security-api-alert-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/iot-security-api-asset-report-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/iot-security-api-device-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/iot-security-api-device-tag-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/iot-security-api-policy-recommendation-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/iot-security-api-vulnerability-example.json
provider_name: Palo Alto Networks
provider_slug: palo-alto-networks
slug: iot-security-api
source_yaml: "aid: palo-alto-networks:iot-security-api\nname: IoT Security API\ntags:\n- Asset Discovery\n- Device Security\n- IoT\n- Network Segmentation\n- OT Security\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://{customer}.iot.paloaltonetworks.com/pub/v4.0/\nhumanURL: https://pan.dev/iot/api/\nproperties:\n- url: https://pan.dev/iot/api/\n  type: Documentation\n- url: openapi/palo-alto-iot-security-api-openapi-original.yml\n  type: OpenAPI\n- url: json-schema/iot-security-api-alert-schema.json\n  type: JSONSchema\n- url: json-schema/iot-security-api-asset-report-schema.json\n  type: JSONSchema\n- url: json-schema/iot-security-api-device-schema.json\n  type: JSONSchema\n- url: json-schema/iot-security-api-device-tag-schema.json\n  type: JSONSchema\n- url: json-schema/iot-security-api-policy-recommendation-schema.json\n  type: JSONSchema\n- url: json-schema/iot-security-api-vulnerability-schema.json\n  type: JSONSchema\n- url: json-structure/iot-security-api-alert-structure.json\n\
  \  type: JSONStructure\n- url: json-structure/iot-security-api-asset-report-structure.json\n  type: JSONStructure\n- url: json-structure/iot-security-api-device-structure.json\n  type: JSONStructure\n- url: json-structure/iot-security-api-device-tag-structure.json\n  type: JSONStructure\n- url: json-structure/iot-security-api-policy-recommendation-structure.json\n  type: JSONStructure\n- url: json-structure/iot-security-api-vulnerability-structure.json\n  type: JSONStructure\n- url: json-ld/palo-alto-iot-security-api-context.jsonld\n  type: JSON-LD\n- url: examples/iot-security-api-alert-example.json\n  type: Example\n- url: examples/iot-security-api-asset-report-example.json\n  type: Example\n- url: examples/iot-security-api-device-example.json\n  type: Example\n- url: examples/iot-security-api-device-tag-example.json\n  type: Example\n- url: examples/iot-security-api-policy-recommendation-example.json\n  type: Example\n- url: examples/iot-security-api-vulnerability-example.json\n  type:\
  \ Example\ndescription: A REST API for managing IoT and OT device security including device discovery, profiling,\n  vulnerability assessment, and security policy recommendations. The API provides endpoints for retrieving\n  discovered device inventories, security alerts, vulnerability details, and recommended network segmentation\n  policies. Authentication uses X-Key-Id and X-Access-Key headers with keys generated from the IoT Security\n  portal. Rate limited to 60 requests per minute.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/apis.yml
tags:
- Asset Discovery
- Device Security
- IoT
- Network Segmentation
- OT Security
---
