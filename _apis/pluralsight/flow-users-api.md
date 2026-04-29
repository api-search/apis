---
aid: pluralsight:flow-users-api
baseURL: https://<workspace>.appfireflow.com/v3/customer/core
description: REST API for managing Flow users including listing, updating, merging, hiding, and bulk operations on user accounts.
humanURL: https://help.pluralsight.com/hc/en-us/sections/24176771997588-Customer-API-references
image: https://www.pluralsight.com/content/dam/pluralsight2/general/headers/logo.png
layout: api
name: Pluralsight Flow Users API
properties:
- type: Documentation
  url: https://help.pluralsight.com/hc/en-us/sections/24176771997588-Customer-API-references
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/flow-users.yml
provider_name: Pluralsight
provider_slug: pluralsight
slug: flow-users-api
source_filename: flow-users.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Pluralsight Flow Users API\n  description: REST API for managing Flow users including listing, updating, merging, hiding, and bulk operations on user accounts.\n  version: 1.0.0\n  contact:\n    name: Pluralsight API Support\n    email: support@pluralsight.com\n    url: https://help.pluralsight.com\n  license:\n    name: Proprietary\n    url: https://www.pluralsight.com/terms\nservers:\n- url: https://{workspace}.appfireflow.com/v3/customer/core\n  description: Production\n  variables:\n    workspace:\n      description: Your Flow workspace identifier\n      default: your-workspace\nexternalDocs:\n  description: Customer API References\n  url: https://help.pluralsight.com/hc/en-us/sections/24176771997588-Customer-API-references\ntags:\n- name: Users\n  description: Flow user management operations\npaths:\n  /users:\n    get:\n      summary: Pluralsight List Users\n      description: Retrieve a list of Flow users in the workspace.\n      operationId:\
  \ listUsers\n      tags:\n      - Users\n      security:\n      - bearerAuth: []\n      responses:\n        '200':\n          description: Successful response with user data\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    type: array\n                    items:\n                      type: object\n                    description: User records\n        '401':\n          description: Unauthorized - Invalid or missing authentication token\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n    put:\n      summary: Pluralsight Update Users\n      description: Update, merge, hide, or perform bulk operations on Flow user accounts.\n      operationId: updateUsers\n      tags:\n      - Users\n      security:\n      - bearerAuth: []\n      requestBody:\n       \
  \ required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              description: User update payload\n      responses:\n        '200':\n          description: Successful update response\n          content:\n            application/json:\n              schema:\n                type: object\n        '401':\n          description: Unauthorized - Invalid or missing authentication token\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: JWT\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/flow-users.yml
tags:
- Engineering Data
- Management
- Users
---
