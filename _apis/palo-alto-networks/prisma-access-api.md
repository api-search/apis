---
aid: palo-alto-networks:prisma-access-api
baseURL: https://api.sase.paloaltonetworks.com
description: REST APIs for configuring and monitoring Prisma Access, Palo Alto Networks' cloud-delivered SASE platform. The Configuration API manages security policies, remote networks, service connections, and mobile user configurations for cloud-managed tenants. The Insights API (versions 1.0 through 3.0) provides health monitoring, tunnel status, bandwidth utilization, and user connectivity data.
humanURL: https://pan.dev/access/api/prisma-access-config/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Prisma Access API
properties:
- type: Documentation
  url: https://pan.dev/access/api/prisma-access-config/
- type: APIReference
  url: https://pan.dev/access/api/insights/
- type: GettingStarted
  url: https://pan.dev/sase/docs/
- type: ChangeLog
  url: https://pan.dev/sase/docs/release-notes/changelog/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/openapi/palo-alto-prisma-access-api-openapi-original.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-api-ike-gateway-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-api-ip-sec-tunnel-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-api-job-status-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-api-mobile-agent-infrastructure-settings-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-api-remote-network-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-api-security-rule-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-access-api-service-connection-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-api-ike-gateway-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-api-ip-sec-tunnel-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-api-job-status-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-api-mobile-agent-infrastructure-settings-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-api-remote-network-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-api-security-rule-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-access-api-service-connection-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-ld/palo-alto-prisma-access-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-api-ike-gateway-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-api-ip-sec-tunnel-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-api-job-status-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-api-mobile-agent-infrastructure-settings-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-api-remote-network-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-api-security-rule-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-access-api-service-connection-example.json
provider_name: Palo Alto Networks
provider_slug: palo-alto-networks
slug: prisma-access-api
source_yaml: "aid: palo-alto-networks:prisma-access-api\nname: Prisma Access API\ntags:\n- Cloud Security\n- Configuration\n- Remote Access\n- SASE\n- Zero Trust\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api.sase.paloaltonetworks.com\nhumanURL: https://pan.dev/access/api/prisma-access-config/\nproperties:\n- url: https://pan.dev/access/api/prisma-access-config/\n  type: Documentation\n- url: https://pan.dev/access/api/insights/\n  type: APIReference\n- url: https://pan.dev/sase/docs/\n  type: GettingStarted\n- url: https://pan.dev/sase/docs/release-notes/changelog/\n  type: ChangeLog\n- url: openapi/palo-alto-prisma-access-api-openapi-original.yml\n  type: OpenAPI\n- url: json-schema/prisma-access-api-ike-gateway-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-access-api-ip-sec-tunnel-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-access-api-job-status-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-access-api-mobile-agent-infrastructure-settings-schema.json\n\
  \  type: JSONSchema\n- url: json-schema/prisma-access-api-remote-network-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-access-api-security-rule-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-access-api-service-connection-schema.json\n  type: JSONSchema\n- url: json-structure/prisma-access-api-ike-gateway-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-access-api-ip-sec-tunnel-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-access-api-job-status-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-access-api-mobile-agent-infrastructure-settings-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-access-api-remote-network-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-access-api-security-rule-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-access-api-service-connection-structure.json\n  type: JSONStructure\n- url: json-ld/palo-alto-prisma-access-api-context.jsonld\n\
  \  type: JSON-LD\n- url: examples/prisma-access-api-ike-gateway-example.json\n  type: Example\n- url: examples/prisma-access-api-ip-sec-tunnel-example.json\n  type: Example\n- url: examples/prisma-access-api-job-status-example.json\n  type: Example\n- url: examples/prisma-access-api-mobile-agent-infrastructure-settings-example.json\n  type: Example\n- url: examples/prisma-access-api-remote-network-example.json\n  type: Example\n- url: examples/prisma-access-api-security-rule-example.json\n  type: Example\n- url: examples/prisma-access-api-service-connection-example.json\n  type: Example\ndescription: REST APIs for configuring and monitoring Prisma Access, Palo Alto Networks' cloud-delivered\n  SASE platform. The Configuration API manages security policies, remote networks, service connections,\n  and mobile user configurations for cloud-managed tenants. The Insights API (versions 1.0 through 3.0)\n  provides health monitoring, tunnel status, bandwidth utilization, and user connectivity\
  \ data.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/apis.yml
tags:
- Cloud Security
- Configuration
- Remote Access
- SASE
- Zero Trust
---
