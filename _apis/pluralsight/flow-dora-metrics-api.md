---
aid: pluralsight:flow-dora-metrics-api
baseURL: https://flow-api.pluralsight.com/dora/build-release
description: REST API for accessing DORA engineering metrics including deployment frequency, lead time for changes, change failure rate, and time to restore service.
humanURL: https://help.pluralsight.com/hc/en-us/articles/27573677812884-DORA-metrics-API
image: https://www.pluralsight.com/content/dam/pluralsight2/general/headers/logo.png
layout: api
name: Pluralsight Flow DORA Metrics API
properties:
- type: Documentation
  url: https://help.pluralsight.com/hc/en-us/articles/27573677812884-DORA-metrics-API
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/flow-dora-metrics.yml
provider_name: Pluralsight
provider_slug: pluralsight
slug: flow-dora-metrics-api
source_filename: flow-dora-metrics.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Pluralsight Flow DORA Metrics API\n  description: REST API for accessing DORA engineering metrics including deployment frequency, lead time for changes, change failure rate, and time to restore service.\n  version: 1.0.0\n  contact:\n    name: Pluralsight API Support\n    email: support@pluralsight.com\n    url: https://help.pluralsight.com\n  license:\n    name: Proprietary\n    url: https://www.pluralsight.com/terms\nservers:\n- url: https://flow-api.pluralsight.com\n  description: Production\nexternalDocs:\n  description: DORA Metrics API Documentation\n  url: https://help.pluralsight.com/hc/en-us/articles/27573677812884-DORA-metrics-API\ntags:\n- name: DORA Metrics\n  description: DORA engineering metrics operations\npaths:\n  /dora/build-release:\n    get:\n      summary: Pluralsight Get DORA Metrics\n      description: Retrieve DORA engineering metrics including deployment frequency, lead time for changes, change failure rate, and time\
  \ to restore service.\n      operationId: getDoraMetrics\n      tags:\n      - DORA Metrics\n      security:\n      - bearerAuth: []\n      parameters:\n      - name: start_date\n        in: query\n        description: Start date for the metrics period\n        schema:\n          type: string\n          format: date\n        example: '2026-04-17T12:00:00Z'\n      - name: end_date\n        in: query\n        description: End date for the metrics period\n        schema:\n          type: string\n          format: date\n        example: '2026-04-17T12:00:00Z'\n      responses:\n        '200':\n          description: Successful response with DORA metrics\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    type: object\n                    description: DORA metrics data\n        '401':\n          description: Unauthorized - Invalid or missing authentication token\n \
  \       '429':\n          description: Too Many Requests - Rate limit exceeded\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      bearerFormat: JWT\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pluralsight/refs/heads/main/openapi/flow-dora-metrics.yml
tags:
- Change Failure Rate
- Deployment Frequency
- Dora
- Engineering Metrics
- Lead Time
---
