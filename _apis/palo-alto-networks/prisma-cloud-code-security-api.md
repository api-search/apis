---
aid: palo-alto-networks:prisma-cloud-code-security-api
baseURL: https://api.prismacloud.io
description: A REST API for Prisma Cloud Application Security (formerly Bridgecrew) providing infrastructure-as-code scanning, software composition analysis, and supply chain security. The API supports checking Terraform, CloudFormation, Kubernetes manifests, and Dockerfiles against security policies, managing code repositories, retrieving scan results, and configuring fix suggestions. Integrates with CI/CD pipelines for shift-left security enforcement during the development lifecycle.
humanURL: https://pan.dev/prisma-cloud/api/code/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Prisma Cloud Code Security API
properties:
- type: Documentation
  url: https://pan.dev/prisma-cloud/api/code/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/openapi/palo-alto-prisma-cloud-code-security-api-openapi-original.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-cloud-code-security-api-code-error-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-cloud-code-security-api-fix-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-cloud-code-security-api-repository-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-cloud-code-security-api-scan-integration-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-cloud-code-security-api-scan-status-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-schema/prisma-cloud-code-security-api-suppression-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-cloud-code-security-api-code-error-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-cloud-code-security-api-fix-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-cloud-code-security-api-repository-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-cloud-code-security-api-scan-integration-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-cloud-code-security-api-scan-status-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-structure/prisma-cloud-code-security-api-suppression-structure.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/json-ld/palo-alto-prisma-cloud-code-security-api-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-cloud-code-security-api-code-error-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-cloud-code-security-api-fix-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-cloud-code-security-api-repository-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-cloud-code-security-api-scan-integration-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-cloud-code-security-api-scan-status-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/examples/prisma-cloud-code-security-api-suppression-example.json
provider_name: Palo Alto Networks
provider_slug: palo-alto-networks
slug: prisma-cloud-code-security-api
source_yaml: "aid: palo-alto-networks:prisma-cloud-code-security-api\nname: Prisma Cloud Code Security API\ntags:\n- Code Security\n- DevSecOps\n- IaC Scanning\n- Shift Left\n- Supply Chain\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api.prismacloud.io\nhumanURL: https://pan.dev/prisma-cloud/api/code/\nproperties:\n- url: https://pan.dev/prisma-cloud/api/code/\n  type: Documentation\n- url: openapi/palo-alto-prisma-cloud-code-security-api-openapi-original.yml\n  type: OpenAPI\n- url: json-schema/prisma-cloud-code-security-api-code-error-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-cloud-code-security-api-fix-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-cloud-code-security-api-repository-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-cloud-code-security-api-scan-integration-schema.json\n  type: JSONSchema\n- url: json-schema/prisma-cloud-code-security-api-scan-status-schema.json\n  type: JSONSchema\n\
  - url: json-schema/prisma-cloud-code-security-api-suppression-schema.json\n  type: JSONSchema\n- url: json-structure/prisma-cloud-code-security-api-code-error-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-cloud-code-security-api-fix-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-cloud-code-security-api-repository-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-cloud-code-security-api-scan-integration-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-cloud-code-security-api-scan-status-structure.json\n  type: JSONStructure\n- url: json-structure/prisma-cloud-code-security-api-suppression-structure.json\n  type: JSONStructure\n- url: json-ld/palo-alto-prisma-cloud-code-security-api-context.jsonld\n  type: JSON-LD\n- url: examples/prisma-cloud-code-security-api-code-error-example.json\n  type: Example\n- url: examples/prisma-cloud-code-security-api-fix-example.json\n  type: Example\n- url: examples/prisma-cloud-code-security-api-repository-example.json\n\
  \  type: Example\n- url: examples/prisma-cloud-code-security-api-scan-integration-example.json\n  type: Example\n- url: examples/prisma-cloud-code-security-api-scan-status-example.json\n  type: Example\n- url: examples/prisma-cloud-code-security-api-suppression-example.json\n  type: Example\ndescription: A REST API for Prisma Cloud Application Security (formerly Bridgecrew) providing infrastructure-as-code\n  scanning, software composition analysis, and supply chain security. The API supports checking Terraform,\n  CloudFormation, Kubernetes manifests, and Dockerfiles against security policies, managing code repositories,\n  retrieving scan results, and configuring fix suggestions. Integrates with CI/CD pipelines for shift-left\n  security enforcement during the development lifecycle.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/palo-alto-networks/refs/heads/main/apis.yml
tags:
- Code Security
- DevSecOps
- IaC Scanning
- Shift Left
- Supply Chain
---
