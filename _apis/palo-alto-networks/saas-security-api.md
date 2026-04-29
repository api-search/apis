---
aid: palo-alto-networks:saas-security-api
baseURL: https://api.example.com
description: A REST API for scanning and protecting assets stored in sanctioned SaaS applications. The API provides at-rest detection, inspection, and remediation capabilities for data stored across cloud applications including file scanning, policy violation detection, and automated remediation workflows. Supports integration with enterprise SaaS applications for continuous data security monitoring.
humanURL: https://docs.paloaltonetworks.com/saas-security/saas-security-admin/saas-security-api
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: SaaS Security API
properties:
- type: Documentation
  url: https://docs.paloaltonetworks.com/saas-security/saas-security-admin/saas-security-api
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/openapi/palo-alto-saas-security-api-openapi-original.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/saas-security-api-application-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/saas-security-api-asset-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/saas-security-api-incident-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/saas-security-api-log-forwarding-settings-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/saas-security-api-user-activity-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/saas-security-api-user-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/saas-security-api-application-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/saas-security-api-asset-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/saas-security-api-incident-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/saas-security-api-log-forwarding-settings-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/saas-security-api-user-activity-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/saas-security-api-user-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-ld/palo-alto-saas-security-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/saas-security-api-application-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/saas-security-api-asset-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/saas-security-api-incident-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/saas-security-api-log-forwarding-settings-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/saas-security-api-user-activity-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/saas-security-api-user-example.json
provider_name: Palo Alto Networks
provider_slug: palo-alto-networks
slug: saas-security-api
source_yaml: "aid: palo-alto-networks:saas-security-api\nname: SaaS Security API\ntags:\n- CASB\n- Cloud Applications\n- Compliance\n- Data Protection\n- SaaS Security\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api.example.com\nhumanURL: https://docs.paloaltonetworks.com/saas-security/saas-security-admin/saas-security-api\nproperties:\n- url: https://docs.paloaltonetworks.com/saas-security/saas-security-admin/saas-security-api\n  type: Documentation\n- url: openapi/palo-alto-saas-security-api-openapi-original.yml\n  type: OpenAPI\n- url: json-schema/saas-security-api-application-schema.json\n  type: JSONSchema\n- url: json-schema/saas-security-api-asset-schema.json\n  type: JSONSchema\n- url: json-schema/saas-security-api-incident-schema.json\n  type: JSONSchema\n- url: json-schema/saas-security-api-log-forwarding-settings-schema.json\n  type: JSONSchema\n- url: json-schema/saas-security-api-user-activity-schema.json\n  type: JSONSchema\n\
  - url: json-schema/saas-security-api-user-schema.json\n  type: JSONSchema\n- url: json-structure/saas-security-api-application-structure.json\n  type: JSONStructure\n- url: json-structure/saas-security-api-asset-structure.json\n  type: JSONStructure\n- url: json-structure/saas-security-api-incident-structure.json\n  type: JSONStructure\n- url: json-structure/saas-security-api-log-forwarding-settings-structure.json\n  type: JSONStructure\n- url: json-structure/saas-security-api-user-activity-structure.json\n  type: JSONStructure\n- url: json-structure/saas-security-api-user-structure.json\n  type: JSONStructure\n- url: json-ld/palo-alto-saas-security-api-context.jsonld\n  type: JSON-LD\n- url: examples/saas-security-api-application-example.json\n  type: Example\n- url: examples/saas-security-api-asset-example.json\n  type: Example\n- url: examples/saas-security-api-incident-example.json\n  type: Example\n- url: examples/saas-security-api-log-forwarding-settings-example.json\n  type: Example\n\
  - url: examples/saas-security-api-user-activity-example.json\n  type: Example\n- url: examples/saas-security-api-user-example.json\n  type: Example\ndescription: A REST API for scanning and protecting assets stored in sanctioned SaaS applications. The\n  API provides at-rest detection, inspection, and remediation capabilities for data stored across cloud\n  applications including file scanning, policy violation detection, and automated remediation workflows.\n  Supports integration with enterprise SaaS applications for continuous data security monitoring.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/apis.yml
tags:
- CASB
- Cloud Applications
- Compliance
- Data Protection
- SaaS Security
---
