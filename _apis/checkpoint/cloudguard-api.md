---
aid: checkpoint:cloudguard-api
baseURL: https://api.dome9.com/v2
description: REST API for CloudGuard Native cloud security posture management, cloud account onboarding, compliance findings, and rulesets across AWS, Azure, and GCP.
humanURL: https://docs.cgn.portal.checkpoint.com/reference/introduction
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Check Point CloudGuard API
properties:
- type: Documentation
  url: https://docs.cgn.portal.checkpoint.com/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-cloudguard-api-openapi.yml
provider_name: Check Point
provider_slug: checkpoint
slug: cloudguard-api
source_filename: checkpoint-cloudguard-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Check Point CloudGuard API\n  description: >-\n    REST API for Check Point CloudGuard Native cloud security posture\n    management. Manages cloud accounts, assets, security policies, and\n    risk findings across AWS, Azure, and GCP environments.\n  version: '1.0'\n  contact:\n    name: Check Point CloudGuard Support\n    url: https://docs.cgn.portal.checkpoint.com/\nservers:\n  - url: https://api.dome9.com/v2\n    description: CloudGuard Production\ntags:\n  - name: Cloud Accounts\n  - name: Findings\n  - name: Rulesets\n  - name: Compliance\nsecurity:\n  - basicAuth: []\npaths:\n  /CloudAccounts:\n    get:\n      operationId: listCloudAccounts\n      summary: List onboarded cloud accounts\n      tags: [Cloud Accounts]\n      responses:\n        '200':\n          description: Cloud accounts list\n    post:\n      operationId: createCloudAccount\n      summary: Onboard a cloud account\n      tags: [Cloud Accounts]\n      requestBody:\n    \
  \    required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                name:\n                  type: string\n                vendor:\n                  type: string\n                  enum: [aws, azure, google]\n                credentials:\n                  type: object\n      responses:\n        '201':\n          description: Cloud account onboarded\n  /Compliance/Finding:\n    get:\n      operationId: listFindings\n      summary: List compliance findings\n      tags: [Findings]\n      responses:\n        '200':\n          description: Findings\n  /Ruleset/view:\n    get:\n      operationId: listRulesets\n      summary: List rulesets used for posture management\n      tags: [Rulesets]\n      responses:\n        '200':\n          description: Rulesets list\n  /AssessmentHistoryV2:\n    get:\n      operationId: listAssessments\n      summary: List historical compliance assessments\n      tags: [Compliance]\n\
  \      responses:\n        '200':\n          description: Assessments\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/checkpoint/refs/heads/main/openapi/checkpoint-cloudguard-api-openapi.yml
tags:
- Cloud Security
- Compliance
- Posture Management
---
