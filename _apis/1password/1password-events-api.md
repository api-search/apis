---
aid: 1password:1password-events-api
baseURL: https://events.1password.com
description: The 1Password Events API provides programmatic access to event data generated within a 1Password account. It enables security teams and administrators to retrieve sign-in attempts, item usage records, and audit events for monitoring, compliance, and security analysis. The API uses cursor-based pagination with POST requests to efficiently stream large volumes of event data.
humanURL: https://developer.1password.com/docs/events-api/reference/
image: ''
layout: api
name: 1Password Events API
properties:
- type: Documentation
  url: https://developer.1password.com/docs/events-api/reference/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/1password/refs/heads/main/openapi/1password-events-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/1password/refs/heads/main/json-schema/1password-events-sign-in-attempt-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/1password/refs/heads/main/json-schema/1password-events-item-usage-schema.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/1password/refs/heads/main/json-ld/1password-events-context.jsonld
provider_name: 1Password
provider_slug: 1password
slug: 1password-events-api
source_yaml: "aid: 1password:1password-events-api\nname: 1Password Events API\ntags:\n- Audit\n- Events\n- Monitoring\n- Security\nhumanURL: https://developer.1password.com/docs/events-api/reference/\nbaseURL: https://events.1password.com\nproperties:\n- url: https://developer.1password.com/docs/events-api/reference/\n  type: Documentation\n- url: openapi/1password-events-openapi.yml\n  type: OpenAPI\n- url: json-schema/1password-events-sign-in-attempt-schema.json\n  type: JSONSchema\n- url: json-schema/1password-events-item-usage-schema.json\n  type: JSONSchema\n- url: json-ld/1password-events-context.jsonld\n  type: JSON-LD\ndescription: The 1Password Events API provides programmatic access to event data generated within a 1Password\n  account. It enables security teams and administrators to retrieve sign-in attempts, item usage records,\n  and audit events for monitoring, compliance, and security analysis. The API uses cursor-based pagination\n  with POST requests to efficiently stream\
  \ large volumes of event data.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/1password/refs/heads/main/apis.yml
tags:
- Audit
- Events
- Monitoring
- Security
---
