---
aid: pluralsight:reports-rest-api
baseURL: https://app.pluralsight.com/plans/api/reports/v1
description: Legacy REST API for downloading user, course completion, and course usage reports as CSV files. Deprecated as of February 2025, removal scheduled for November 2025.
humanURL: https://help.pluralsight.com/hc/en-us/articles/24420566008084-Migrating-from-REST-to-GraphQL-APIs
image: https://www.pluralsight.com/content/dam/pluralsight2/general/headers/logo.png
layout: api
name: Pluralsight Reports REST API
properties:
- type: Documentation
  url: https://help.pluralsight.com/hc/en-us/articles/24420566008084-Migrating-from-REST-to-GraphQL-APIs
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/reports-rest.yml
provider_name: Pluralsight
provider_slug: pluralsight
slug: reports-rest-api
source_filename: reports-rest.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Pluralsight Reports REST API\n  description: Legacy REST API for downloading user, course completion, and course usage reports as CSV files. Deprecated as of February 2025, removal scheduled for November 2025.\n  version: 1.0.0\n  contact:\n    name: Pluralsight API Support\n    email: support@pluralsight.com\n    url: https://help.pluralsight.com\n  license:\n    name: Proprietary\n    url: https://www.pluralsight.com/terms\nservers:\n- url: https://app.pluralsight.com/plans/api/reports/v1\n  description: Production\nexternalDocs:\n  description: Migration Guide - REST to GraphQL\n  url: https://help.pluralsight.com/hc/en-us/articles/24420566008084-Migrating-from-REST-to-GraphQL-APIs\ntags:\n- name: Reports\n  description: Report download operations (deprecated)\npaths:\n  /users:\n    get:\n      summary: Pluralsight Download User Report\n      description: Download a user report as CSV. Deprecated - migrate to GraphQL User Management API.\n\
  \      operationId: downloadUserReport\n      deprecated: true\n      tags:\n      - Reports\n      security:\n      - bearerAuth: []\n      responses:\n        '200':\n          description: CSV file download\n          content:\n            text/csv:\n              schema:\n                type: string\n        '401':\n          description: Unauthorized - Invalid or missing authentication token\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /course-completion:\n    get:\n      summary: Pluralsight Download Course Completion Report\n      description: Download a course completion report as CSV. Deprecated - migrate to GraphQL Course Progress API.\n      operationId: downloadCourseCompletionReport\n      deprecated: true\n      tags:\n      - Reports\n      security:\n      - bearerAuth: []\n      responses:\n        '200':\n          description: CSV file download\n      \
  \    content:\n            text/csv:\n              schema:\n                type: string\n        '401':\n          description: Unauthorized - Invalid or missing authentication token\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /course-usage:\n    get:\n      summary: Pluralsight Download Course Usage Report\n      description: Download a course usage report as CSV. Deprecated - migrate to GraphQL Course Daily Usage API.\n      operationId: downloadCourseUsageReport\n      deprecated: true\n      tags:\n      - Reports\n      security:\n      - bearerAuth: []\n      responses:\n        '200':\n          description: CSV file download\n          content:\n            text/csv:\n              schema:\n                type: string\n        '401':\n          description: Unauthorized - Invalid or missing authentication token\n        '429':\n          description: Too Many Requests\
  \ - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: JWT\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/reports-rest.yml
tags:
- Csv
- Deprecated
- Legacy
- Reports
---
