---
aid: checkpoint:identity-awareness-api
baseURL: https://gateway.example.com/_IA_MU_Agent
description: REST API for posting and revoking user-to-IP identity associations on Check Point gateways, enabling identity-aware policy enforcement.
humanURL: https://sc1.checkpoint.com/documents/latest/IdentityAPIs/
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Check Point Identity Awareness API
properties:
- type: Documentation
  url: https://sc1.checkpoint.com/documents/latest/IdentityAPIs/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-identity-awareness-api-openapi.yml
provider_name: Check Point
provider_slug: checkpoint
slug: identity-awareness-api
source_filename: checkpoint-identity-awareness-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Check Point Identity Awareness API\n  description: >-\n    REST API for posting and querying user-to-IP identity associations on\n    Check Point gateways for use in identity-aware policy enforcement.\n  version: '1.0'\n  contact:\n    name: Check Point Support\n    url: https://www.checkpoint.com/support-services/\nexternalDocs:\n  description: Identity Awareness API Reference\n  url: https://sc1.checkpoint.com/documents/latest/IdentityAPIs/\nservers:\n  - url: https://{gateway}/_IA_MU_Agent\n    description: Identity Awareness Web API\n    variables:\n      gateway:\n        default: gateway.example.com\ntags:\n  - name: Identity\nsecurity:\n  - sharedSecret: []\npaths:\n  /idasdk/add-identity:\n    post:\n      operationId: addIdentity\n      summary: Associate a user identity with an IP\n      tags: [Identity]\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type:\
  \ object\n              required: [shared-secret, requests]\n              properties:\n                shared-secret:\n                  type: string\n                requests:\n                  type: array\n                  items:\n                    type: object\n                    properties:\n                      ip-address:\n                        type: string\n                      user:\n                        type: string\n                      machine:\n                        type: string\n                      session-timeout:\n                        type: integer\n      responses:\n        '200':\n          description: Identity registered\n  /idasdk/delete-identity:\n    post:\n      operationId: deleteIdentity\n      summary: Remove a user identity association\n      tags: [Identity]\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              required: [shared-secret, requests]\n\
  \              properties:\n                shared-secret:\n                  type: string\n                requests:\n                  type: array\n                  items:\n                    type: object\n                    properties:\n                      ip-address:\n                        type: string\n                      revoke-method:\n                        type: string\n      responses:\n        '200':\n          description: Identity removed\ncomponents:\n  securitySchemes:\n    sharedSecret:\n      type: apiKey\n      in: header\n      name: X-chkp-shared-secret\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-identity-awareness-api-openapi.yml
tags:
- Identity
- Network Security
---
