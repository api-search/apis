---
aid: pluralsight:flow-collaboration-metrics-api
baseURL: https://api.appfireflow.com/collaboration/pullrequest/metrics
description: REST API for accessing pull request and collaboration metrics for engineering teams with date range filtering.
humanURL: https://help.pluralsight.com/hc/en-us/articles/24286030333332-Collaboration-metrics-API
image: https://www.pluralsight.com/content/dam/pluralsight2/general/headers/logo.png
layout: api
name: Pluralsight Flow Collaboration Metrics API
properties:
- type: Documentation
  url: https://help.pluralsight.com/hc/en-us/articles/24286030333332-Collaboration-metrics-API
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/flow-collaboration-metrics.yml
provider_name: Pluralsight
provider_slug: pluralsight
slug: flow-collaboration-metrics-api
source_filename: flow-collaboration-metrics.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Pluralsight Flow Collaboration Metrics API\n  description: REST API for accessing pull request and collaboration metrics for engineering teams with date range filtering.\n  version: 1.0.0\n  contact:\n    name: Pluralsight API Support\n    email: support@pluralsight.com\n    url: https://help.pluralsight.com\n  license:\n    name: Proprietary\n    url: https://www.pluralsight.com/terms\nservers:\n- url: https://api.appfireflow.com\n  description: Production\nexternalDocs:\n  description: Collaboration Metrics API Documentation\n  url: https://help.pluralsight.com/hc/en-us/articles/24286030333332-Collaboration-metrics-API\ntags:\n- name: Collaboration Metrics\n  description: Pull request and collaboration metrics operations\npaths:\n  /collaboration/pullrequest/metrics:\n    get:\n      summary: Pluralsight Get Collaboration Metrics\n      description: Retrieve pull request and collaboration metrics for engineering teams with date range filtering.\n\
  \      operationId: getCollaborationMetrics\n      tags:\n      - Collaboration Metrics\n      security:\n      - bearerAuth: []\n      parameters:\n      - name: start_date\n        in: query\n        description: Start date for the metrics period\n        schema:\n          type: string\n          format: date\n        example: '2026-04-17T12:00:00Z'\n      - name: end_date\n        in: query\n        description: End date for the metrics period\n        schema:\n          type: string\n          format: date\n        example: '2026-04-17T12:00:00Z'\n      responses:\n        '200':\n          description: Successful response with collaboration metrics\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    type: object\n                    description: Collaboration metrics data\n        '401':\n          description: Unauthorized - Invalid or missing authentication\
  \ token\n        '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: JWT\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/flow-collaboration-metrics.yml
tags:
- Collaboration
- Engineering Metrics
- Pull Requests
---
