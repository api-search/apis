---
aid: cnh:cnh-fieldops-api
baseURL: https://api.fieldops.cnh.com
description: The CNH FieldOps API replaces the previously available CNH Ag Data and CONNECT Machine Data APIs and provides a unified, OAuth 2.0 secured REST API for both agronomic machinery and construction equipment connected to a FieldOps account. Vehicle telemetry follows the ISO 15143-3 specification with two profiles - CP (CAN Parameter, default) and MH (Machine Health) - and supports time-series data such as locations, operating hours, idle hours, fuel and DEF remaining, peak speed, distance, fault codes, and engine condition. Additional endpoint groups cover Equipment, Operations By Vehicle, Prescriptions (send Rx files), Farm Setup (Grower / Farm / Field / Boundary), Files, and Webhooks.
humanURL: https://develop.cnh.com/api-guides/fieldops-api
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CNH FieldOps API
properties:
- type: GettingStarted
  url: https://develop.cnh.com/get-started
- type: Documentation
  url: https://develop.cnh.com/api-guides
- type: Reference
  url: https://develop.cnh.com/api-guides/fieldops-api
- type: Reference
  url: https://develop.cnh.com/api-guides/fieldops-api/vehicle-telemetry
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cnh/refs/heads/main/openapi/cnh-fieldops-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cnh/refs/heads/main/json-schema/cnh-equipment-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cnh/refs/heads/main/json-schema/cnh-telemetry-schema.json
- type: JSONLDContext
  url: https://raw.githubusercontent.com/api-evangelist/cnh/refs/heads/main/json-ld/cnh-context.jsonld
- type: SpectralRuleset
  url: https://raw.githubusercontent.com/api-evangelist/cnh/refs/heads/main/rules/cnh-rules.yml
- type: NaftikoCapabilities
  url: https://raw.githubusercontent.com/api-evangelist/cnh/refs/heads/main/capabilities/cnh-fieldops-capabilities.yml
provider_name: CNH
provider_slug: cnh
slug: cnh-fieldops-api
source_yaml: "aid: cnh:cnh-fieldops-api\nname: CNH FieldOps API\ntags:\n- Agriculture\n- Construction\n- ISO 15143-3\n- OAuth2\n- Telemetry\n- Vehicles\nimage: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://develop.cnh.com/api-guides/fieldops-api\nbaseURL: https://api.fieldops.cnh.com\nproperties:\n- url: https://develop.cnh.com/get-started\n  type: GettingStarted\n- url: https://develop.cnh.com/api-guides\n  type: Documentation\n- url: https://develop.cnh.com/api-guides/fieldops-api\n  type: Reference\n- url: https://develop.cnh.com/api-guides/fieldops-api/vehicle-telemetry\n  type: Reference\n- url: openapi/cnh-fieldops-openapi.yml\n  type: OpenAPI\n- url: json-schema/cnh-equipment-schema.json\n  type: JSONSchema\n- url: json-schema/cnh-telemetry-schema.json\n  type: JSONSchema\n- url: json-ld/cnh-context.jsonld\n  type: JSONLDContext\n- url: rules/cnh-rules.yml\n  type: SpectralRuleset\n- url: capabilities/cnh-fieldops-capabilities.yml\n \
  \ type: NaftikoCapabilities\ndescription: The CNH FieldOps API replaces the previously available CNH Ag Data and CONNECT Machine Data\n  APIs and provides a unified, OAuth 2.0 secured REST API for both agronomic machinery and construction\n  equipment connected to a FieldOps account. Vehicle telemetry follows the ISO 15143-3 specification with\n  two profiles - CP (CAN Parameter, default) and MH (Machine Health) - and supports time-series data such\n  as locations, operating hours, idle hours, fuel and DEF remaining, peak speed, distance, fault codes,\n  and engine condition. Additional endpoint groups cover Equipment, Operations By Vehicle, Prescriptions\n  (send Rx files), Farm Setup (Grower / Farm / Field / Boundary), Files, and Webhooks.\nx-features:\n- name: ISO 15143-3 Telemetry\n  description: Standards-based vehicle telemetry across CNH brands and equipment classes.\n- name: CP and MH Profiles\n  description: CAN Parameter (default) and Machine Health telemetry profiles.\n- name:\
  \ Fault Codes\n  description: Fault, caution, and engine-condition codes per vehicle.\n- name: Aggregated Metrics\n  description: Daily metrics including operating hours, idle hours, fuel ratio, distance, and peak speed.\n- name: Prescription Rx Delivery\n  description: Push prescription files directly to a vehicle or FieldOps field.\n- name: Farm Hierarchy\n  description: Grower / Farm / Field / Boundary management.\n- name: Operations by Vehicle\n  description: Recorded field operations per vehicle.\n- name: Webhooks\n  description: Subscribe to FieldOps event notifications.\n- name: OAuth 2.0\n  description: Refresh and access token authentication via develop.cnh.com.\nx-useCases:\n- name: Fleet Telematics\n  description: Power third-party fleet-management systems with CNH equipment telemetry.\n- name: Predictive Maintenance\n  description: Use Machine Health telemetry and fault codes to anticipate maintenance.\n- name: Precision Agriculture\n  description: Push prescription Rx files\
  \ into the workflow for variable-rate application.\n- name: Farm Management Systems\n  description: Hydrate FMS dashboards with grower / farm / field hierarchies and operations.\n- name: Construction Equipment Tracking\n  description: Track Case CE and New Holland Construction equipment via standardized ISO telematics.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cnh/refs/heads/main/apis.yml
tags:
- Agriculture
- Construction
- ISO 15143-3
- OAuth2
- Telemetry
- Vehicles
---
