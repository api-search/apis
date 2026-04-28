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
tags:
- Agriculture
- Construction
- ISO 15143-3
- OAuth2
- Telemetry
- Vehicles
---
