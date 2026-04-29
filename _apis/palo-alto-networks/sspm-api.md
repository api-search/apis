---
aid: palo-alto-networks:sspm-api
baseURL: https://api.sase.paloaltonetworks.com
description: A REST API for managing SaaS Security Posture Management providing continuous monitoring of misconfigured SaaS application settings. The API supports managing onboarded SaaS applications, retrieving configuration assessment details, accessing the application catalog, and managing JIRA integrations for remediation tracking. Part of the broader SASE platform with OAuth 2.0 authentication.
humanURL: https://pan.dev/sase/api/sspm/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: SaaS Security Posture Management API
properties:
- type: Documentation
  url: https://pan.dev/sase/api/sspm/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/openapi/palo-alto-sspm-api-openapi-original.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/sspm-api-catalog-app-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/sspm-api-jira-integration-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/sspm-api-jira-integration-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/sspm-api-onboard-app-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/sspm-api-onboarded-app-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/sspm-api-posture-check-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/sspm-api-catalog-app-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/sspm-api-jira-integration-request-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/sspm-api-jira-integration-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/sspm-api-onboard-app-request-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/sspm-api-onboarded-app-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/sspm-api-posture-check-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-ld/palo-alto-sspm-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/sspm-api-catalog-app-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/sspm-api-jira-integration-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/sspm-api-jira-integration-request-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/sspm-api-onboard-app-request-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/sspm-api-onboarded-app-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/sspm-api-posture-check-example.json
provider_name: Palo Alto Networks
provider_slug: palo-alto-networks
slug: sspm-api
source_yaml: "aid: palo-alto-networks:sspm-api\nname: SaaS Security Posture Management API\ntags:\n- Compliance\n- Misconfiguration\n- SaaS Applications\n- SaaS Posture\n- SSPM\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api.sase.paloaltonetworks.com\nhumanURL: https://pan.dev/sase/api/sspm/\nproperties:\n- url: https://pan.dev/sase/api/sspm/\n  type: Documentation\n- url: openapi/palo-alto-sspm-api-openapi-original.yml\n  type: OpenAPI\n- url: json-schema/sspm-api-catalog-app-schema.json\n  type: JSONSchema\n- url: json-schema/sspm-api-jira-integration-request-schema.json\n  type: JSONSchema\n- url: json-schema/sspm-api-jira-integration-schema.json\n  type: JSONSchema\n- url: json-schema/sspm-api-onboard-app-request-schema.json\n  type: JSONSchema\n- url: json-schema/sspm-api-onboarded-app-schema.json\n  type: JSONSchema\n- url: json-schema/sspm-api-posture-check-schema.json\n  type: JSONSchema\n- url: json-structure/sspm-api-catalog-app-structure.json\n\
  \  type: JSONStructure\n- url: json-structure/sspm-api-jira-integration-request-structure.json\n  type: JSONStructure\n- url: json-structure/sspm-api-jira-integration-structure.json\n  type: JSONStructure\n- url: json-structure/sspm-api-onboard-app-request-structure.json\n  type: JSONStructure\n- url: json-structure/sspm-api-onboarded-app-structure.json\n  type: JSONStructure\n- url: json-structure/sspm-api-posture-check-structure.json\n  type: JSONStructure\n- url: json-ld/palo-alto-sspm-api-context.jsonld\n  type: JSON-LD\n- url: examples/sspm-api-catalog-app-example.json\n  type: Example\n- url: examples/sspm-api-jira-integration-example.json\n  type: Example\n- url: examples/sspm-api-jira-integration-request-example.json\n  type: Example\n- url: examples/sspm-api-onboard-app-request-example.json\n  type: Example\n- url: examples/sspm-api-onboarded-app-example.json\n  type: Example\n- url: examples/sspm-api-posture-check-example.json\n  type: Example\ndescription: A REST API for managing\
  \ SaaS Security Posture Management providing continuous monitoring\n  of misconfigured SaaS application settings. The API supports managing onboarded SaaS applications, retrieving\n  configuration assessment details, accessing the application catalog, and managing JIRA integrations\n  for remediation tracking. Part of the broader SASE platform with OAuth 2.0 authentication.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/apis.yml
tags:
- Compliance
- Misconfiguration
- SaaS Applications
- SaaS Posture
- SSPM
---
