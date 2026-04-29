---
aid: palo-alto-networks:sase-iam-api
baseURL: https://api.sase.paloaltonetworks.com
description: A REST API for managing identity and access on the SASE platform including creating service accounts, managing access policies, and configuring role-based access control for SASE API consumers. The API supports provisioning service account credentials used for OAuth 2.0 authentication across all SASE platform APIs. Part of the common SASE management services layer.
humanURL: https://pan.dev/sase/api/iam/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: SASE IAM API
properties:
- type: Documentation
  url: https://pan.dev/sase/api/iam/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/openapi/palo-alto-sase-iam-api-openapi-original.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/sase-iam-api-access-policy-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/sase-iam-api-access-policy-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/sase-iam-api-role-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/sase-iam-api-service-account-credentials-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/sase-iam-api-service-account-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/sase-iam-api-service-account-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/sase-iam-api-service-account-update-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/sase-iam-api-access-policy-request-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/sase-iam-api-access-policy-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/sase-iam-api-role-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/sase-iam-api-service-account-credentials-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/sase-iam-api-service-account-request-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/sase-iam-api-service-account-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/sase-iam-api-service-account-update-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-ld/palo-alto-sase-iam-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/sase-iam-api-access-policy-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/sase-iam-api-access-policy-request-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/sase-iam-api-role-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/sase-iam-api-service-account-credentials-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/sase-iam-api-service-account-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/sase-iam-api-service-account-request-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/sase-iam-api-service-account-update-example.json
provider_name: Palo Alto Networks
provider_slug: palo-alto-networks
slug: sase-iam-api
source_yaml: "aid: palo-alto-networks:sase-iam-api\nname: SASE IAM API\ntags:\n- Access Control\n- Identity Management\n- RBAC\n- SASE\n- Service Accounts\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api.sase.paloaltonetworks.com\nhumanURL: https://pan.dev/sase/api/iam/\nproperties:\n- url: https://pan.dev/sase/api/iam/\n  type: Documentation\n- url: openapi/palo-alto-sase-iam-api-openapi-original.yml\n  type: OpenAPI\n- url: json-schema/sase-iam-api-access-policy-request-schema.json\n  type: JSONSchema\n- url: json-schema/sase-iam-api-access-policy-schema.json\n  type: JSONSchema\n- url: json-schema/sase-iam-api-role-schema.json\n  type: JSONSchema\n- url: json-schema/sase-iam-api-service-account-credentials-schema.json\n  type: JSONSchema\n- url: json-schema/sase-iam-api-service-account-request-schema.json\n  type: JSONSchema\n- url: json-schema/sase-iam-api-service-account-schema.json\n  type: JSONSchema\n- url: json-schema/sase-iam-api-service-account-update-schema.json\n\
  \  type: JSONSchema\n- url: json-structure/sase-iam-api-access-policy-request-structure.json\n  type: JSONStructure\n- url: json-structure/sase-iam-api-access-policy-structure.json\n  type: JSONStructure\n- url: json-structure/sase-iam-api-role-structure.json\n  type: JSONStructure\n- url: json-structure/sase-iam-api-service-account-credentials-structure.json\n  type: JSONStructure\n- url: json-structure/sase-iam-api-service-account-request-structure.json\n  type: JSONStructure\n- url: json-structure/sase-iam-api-service-account-structure.json\n  type: JSONStructure\n- url: json-structure/sase-iam-api-service-account-update-structure.json\n  type: JSONStructure\n- url: json-ld/palo-alto-sase-iam-api-context.jsonld\n  type: JSON-LD\n- url: examples/sase-iam-api-access-policy-example.json\n  type: Example\n- url: examples/sase-iam-api-access-policy-request-example.json\n  type: Example\n- url: examples/sase-iam-api-role-example.json\n  type: Example\n- url: examples/sase-iam-api-service-account-credentials-example.json\n\
  \  type: Example\n- url: examples/sase-iam-api-service-account-example.json\n  type: Example\n- url: examples/sase-iam-api-service-account-request-example.json\n  type: Example\n- url: examples/sase-iam-api-service-account-update-example.json\n  type: Example\ndescription: A REST API for managing identity and access on the SASE platform including creating service\n  accounts, managing access policies, and configuring role-based access control for SASE API consumers.\n  The API supports provisioning service account credentials used for OAuth 2.0 authentication across all\n  SASE platform APIs. Part of the common SASE management services layer.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/apis.yml
tags:
- Access Control
- Identity Management
- RBAC
- SASE
- Service Accounts
---
