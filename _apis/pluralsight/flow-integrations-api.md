---
aid: pluralsight:flow-integrations-api
baseURL: https://<workspace>.appfireflow.com/v3/customer/core
description: REST API for managing Flow integrations and checking connection status with external tools and services.
humanURL: https://help.pluralsight.com/hc/en-us/articles/24285986280212-Integrations-API
image: https://www.pluralsight.com/content/dam/pluralsight2/general/headers/logo.png
layout: api
name: Pluralsight Flow Integrations API
properties:
- type: Documentation
  url: https://help.pluralsight.com/hc/en-us/articles/24285986280212-Integrations-API
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/flow-integrations.yml
provider_name: Pluralsight
provider_slug: pluralsight
slug: flow-integrations-api
source_filename: flow-integrations.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Pluralsight Flow Integrations API\n  description: REST API for managing Flow integrations and checking connection status with external tools and services.\n  version: 1.0.0\n  contact:\n    name: Pluralsight API Support\n    email: support@pluralsight.com\n    url: https://help.pluralsight.com\n  license:\n    name: Proprietary\n    url: https://www.pluralsight.com/terms\nservers:\n- url: https://{workspace}.appfireflow.com/v3/customer/core\n  description: Production\n  variables:\n    workspace:\n      description: Your Flow workspace identifier\n      default: your-workspace\nexternalDocs:\n  description: Integrations API Documentation\n  url: https://help.pluralsight.com/hc/en-us/articles/24285986280212-Integrations-API\ntags:\n- name: Integrations\n  description: Flow integration management operations\npaths:\n  /integrations:\n    get:\n      summary: Pluralsight List Integrations\n      description: Retrieve a list of Flow integrations\
  \ and check connection status with external tools and services.\n      operationId: listIntegrations\n      tags:\n      - Integrations\n      security:\n      - bearerAuth: []\n      responses:\n        '200':\n          description: Successful response with integration data\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    type: array\n                    items:\n                      type: object\n                    description: Integration records\n        '401':\n          description: Unauthorized - Invalid or missing authentication token\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: JWT\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/flow-integrations.yml
tags:
- Connections
- Engineering Data
- Integrations
---
