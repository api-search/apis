---
aid: pluralsight:licensing-rest-api
baseURL: https://app.pluralsight.com/plans/api/license/v1
description: Legacy REST API for managing user invitations, users, and teams within a plan. Deprecated as of February 2025, removal scheduled for November 2025.
humanURL: https://help.pluralsight.com/hc/en-us/articles/24420566008084-Migrating-from-REST-to-GraphQL-APIs
image: https://www.pluralsight.com/content/dam/pluralsight2/general/headers/logo.png
layout: api
name: Pluralsight Licensing REST API
properties:
- type: Documentation
  url: https://help.pluralsight.com/hc/en-us/articles/24420566008084-Migrating-from-REST-to-GraphQL-APIs
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/licensing-rest.yml
provider_name: Pluralsight
provider_slug: pluralsight
slug: licensing-rest-api
source_filename: licensing-rest.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Pluralsight Licensing REST API\n  description: Legacy REST API for managing user invitations, users, and teams within a plan. Deprecated as of February 2025, removal scheduled for November 2025.\n  version: 1.0.0\n  contact:\n    name: Pluralsight API Support\n    email: support@pluralsight.com\n    url: https://help.pluralsight.com\n  license:\n    name: Proprietary\n    url: https://www.pluralsight.com/terms\nservers:\n- url: https://app.pluralsight.com/plans/api/license/v1\n  description: Production\nexternalDocs:\n  description: Migration Guide - REST to GraphQL\n  url: https://help.pluralsight.com/hc/en-us/articles/24420566008084-Migrating-from-REST-to-GraphQL-APIs\ntags:\n- name: Licensing\n  description: License management operations (deprecated)\npaths:\n  /invitations:\n    get:\n      summary: Pluralsight List Invitations\n      description: Retrieve a list of pending user invitations. Deprecated - migrate to GraphQL User Management\
  \ API.\n      operationId: listInvitations\n      deprecated: true\n      tags:\n      - Licensing\n      security:\n      - bearerAuth: []\n      responses:\n        '200':\n          description: Successful response with invitation data\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    type: array\n                    items:\n                      type: object\n                    description: Invitation records\n        '401':\n          description: Unauthorized - Invalid or missing authentication token\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n    post:\n      summary: Pluralsight Create Invitation\n      description: Send a new user invitation. Deprecated - migrate to GraphQL User Management API.\n      operationId: createInvitation\n    \
  \  deprecated: true\n      tags:\n      - Licensing\n      security:\n      - bearerAuth: []\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              description: Invitation details\n      responses:\n        '201':\n          description: Invitation created successfully\n          content:\n            application/json:\n              schema:\n                type: object\n        '401':\n          description: Unauthorized - Invalid or missing authentication token\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /users:\n    get:\n      summary: Pluralsight List Users\n      description: Retrieve a list of users in the plan. Deprecated - migrate to GraphQL User Management API.\n      operationId: listUsers\n      deprecated: true\n      tags:\n      - Licensing\n      security:\n\
  \      - bearerAuth: []\n      responses:\n        '200':\n          description: Successful response with user data\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    type: array\n                    items:\n                      type: object\n                    description: User records\n        '401':\n          description: Unauthorized - Invalid or missing authentication token\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /teams:\n    get:\n      summary: Pluralsight List Teams\n      description: Retrieve a list of teams in the plan. Deprecated - migrate to GraphQL Teams API.\n      operationId: listTeams\n      deprecated: true\n      tags:\n      - Licensing\n      security:\n      - bearerAuth: []\n      responses:\n        '200':\n     \
  \     description: Successful response with team data\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    type: array\n                    items:\n                      type: object\n                    description: Team records\n        '401':\n          description: Unauthorized - Invalid or missing authentication token\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: JWT\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/licensing-rest.yml
tags:
- Deprecated
- Invitations
- Legacy
- Licensing
- Users
---
