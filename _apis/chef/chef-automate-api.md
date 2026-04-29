---
aid: chef:chef-automate-api
baseURL: https://automate.example.com/api/v0
description: REST API for Chef Automate providing visibility into infrastructure convergence, compliance scans, and application deployment. Includes compliance profiles, scan jobs, reports, IAM, and configuration management endpoints.
humanURL: https://docs.chef.io/automate/api/
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Chef Automate API
properties:
- type: Documentation
  url: https://docs.chef.io/automate/api/
- type: Reference
  url: https://docs.chef.io/automate/api_swagger/
- type: Authentication
  url: https://docs.chef.io/automate/api_tokens/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chef/refs/heads/main/openapi/chef-automate-api-openapi.yml
provider_name: Chef
provider_slug: chef
slug: chef-automate-api
source_filename: chef-automate-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Chef Automate API\n  description: >-\n    REST API for Chef Automate providing visibility into infrastructure\n    convergence, compliance scans, and application deployment. Includes\n    endpoints for nodes, profiles, scans, and reports.\n  version: '1.0'\n  contact:\n    name: Chef Software\n    url: https://www.chef.io/support\nexternalDocs:\n  description: Chef Automate API\n  url: https://docs.chef.io/automate/api/\nservers:\n  - url: https://{automate}/api/v0\n    description: Chef Automate\n    variables:\n      automate:\n        default: automate.example.com\ntags:\n  - name: Nodes\n  - name: Profiles\n  - name: Scans\n  - name: Reports\n  - name: IAM\nsecurity:\n  - apiToken: []\npaths:\n  /compliance/profiles:\n    get:\n      operationId: listComplianceProfiles\n      summary: List compliance profiles\n      tags: [Profiles]\n      responses:\n        '200':\n          description: Profiles list\n  /compliance/scanner/jobs:\n    post:\n\
  \      operationId: createScanJob\n      summary: Create a compliance scan job\n      tags: [Scans]\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                name:\n                  type: string\n                profiles:\n                  type: array\n                  items:\n                    type: string\n                nodes:\n                  type: array\n                  items:\n                    type: string\n      responses:\n        '201':\n          description: Scan job created\n  /compliance/reporting/reports:\n    post:\n      operationId: searchReports\n      summary: Search compliance reports\n      tags: [Reports]\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                filters:\n                  type: array\n\
  \                  items:\n                    type: object\n                page:\n                  type: integer\n                per_page:\n                  type: integer\n      responses:\n        '200':\n          description: Reports\n  /cfgmgmt/nodes:\n    get:\n      operationId: listManagedNodes\n      summary: List configuration management nodes\n      tags: [Nodes]\n      responses:\n        '200':\n          description: Nodes list\n  /apis/iam/v2/users:\n    get:\n      operationId: listIamUsers\n      summary: List IAM users\n      tags: [IAM]\n      responses:\n        '200':\n          description: IAM users\ncomponents:\n  securitySchemes:\n    apiToken:\n      type: apiKey\n      in: header\n      name: api-token\n      description: API token issued through the Chef Automate UI or admin API.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chef/refs/heads/main/openapi/chef-automate-api-openapi.yml
tags:
- Automation
- Compliance
- Observability
---
