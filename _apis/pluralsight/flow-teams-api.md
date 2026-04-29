---
aid: pluralsight:flow-teams-api
baseURL: https://<workspace>.appfireflow.com/v3/customer/core
description: REST API for managing Flow engineering teams and team membership data.
humanURL: https://help.pluralsight.com/hc/en-us/sections/24176771997588-Customer-API-references
image: https://www.pluralsight.com/content/dam/pluralsight2/general/headers/logo.png
layout: api
name: Pluralsight Flow Teams API
properties:
- type: Documentation
  url: https://help.pluralsight.com/hc/en-us/sections/24176771997588-Customer-API-references
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/flow-teams.yml
provider_name: Pluralsight
provider_slug: pluralsight
slug: flow-teams-api
source_filename: flow-teams.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Pluralsight Flow Teams API\n  description: REST API for managing Flow engineering teams and team membership data.\n  version: 1.0.0\n  contact:\n    name: Pluralsight API Support\n    email: support@pluralsight.com\n    url: https://help.pluralsight.com\n  license:\n    name: Proprietary\n    url: https://www.pluralsight.com/terms\nservers:\n- url: https://{workspace}.appfireflow.com/v3/customer/core\n  description: Production\n  variables:\n    workspace:\n      description: Your Flow workspace identifier\n      default: your-workspace\nexternalDocs:\n  description: Customer API References\n  url: https://help.pluralsight.com/hc/en-us/sections/24176771997588-Customer-API-references\ntags:\n- name: Teams\n  description: Flow team management operations\npaths:\n  /teams:\n    get:\n      summary: Pluralsight List Teams\n      description: Retrieve a list of Flow engineering teams and team membership data.\n      operationId: listTeams\n      tags:\n\
  \      - Teams\n      security:\n      - bearerAuth: []\n      responses:\n        '200':\n          description: Successful response with team data\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    type: array\n                    items:\n                      type: object\n                    description: Team records\n        '401':\n          description: Unauthorized - Invalid or missing authentication token\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: JWT\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/flow-teams.yml
tags:
- Engineering Data
- Management
- Teams
---
