---
aid: comeet:comeet-careers-api
baseURL: https://www.comeet.co/careers-api/2.0
description: Public, tokenized REST API that returns the list of published positions for a Comeet customer (and details for a single position). Used to power custom-branded careers websites, embed jobs into marketing pages, and syndicate openings to third-party job boards. Each company's data is scoped by a company UID and a public company token issued by Comeet.
humanURL: https://developers.comeet.com/reference/careers-api-overview
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Comeet Careers API
properties:
- type: Documentation
  url: https://developers.comeet.com/reference/careers-api-overview
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/comeet/refs/heads/main/openapi/comeet-careers-api-openapi.yml
provider_name: Comeet
provider_slug: comeet
slug: comeet-careers-api
source_filename: comeet-careers-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Comeet Careers API\n  description: >-\n    The Comeet (Spark Hire Recruit) Careers API exposes a company's published\n    job positions for embedding on a custom careers website. Clients pass a\n    company UID and a public company token to retrieve the list of open\n    positions or details for a single position. The API powers Comeet's\n    Careers Website Widget and is used by partners such as job boards and\n    aggregators that syndicate Comeet customers' jobs.\n  version: '2.0'\n  contact:\n    name: Spark Hire Recruit\n    url: https://developers.comeet.com/\nexternalDocs:\n  description: Careers API Overview\n  url: https://developers.comeet.com/reference/careers-api-overview\nservers:\n  - url: https://www.comeet.co/careers-api/2.0\n    description: Production\ntags:\n  - name: Positions\n    description: Published positions for a company.\nsecurity:\n  - companyToken: []\npaths:\n  /company/{company_uid}/positions:\n    get:\n     \
  \ operationId: listPositions\n      summary: List positions\n      description: >-\n        Retrieve the list of published positions for a company. The response\n        is empty when the company has no positions published.\n      tags:\n        - Positions\n      parameters:\n        - name: company_uid\n          in: path\n          required: true\n          description: The company UID assigned by Comeet.\n          schema:\n            type: string\n        - name: token\n          in: query\n          required: true\n          description: Public company token used to authorize the read.\n          schema:\n            type: string\n        - name: details\n          in: query\n          required: false\n          description: When true, include full position descriptions and requirements.\n          schema:\n            type: boolean\n            default: false\n      responses:\n        '200':\n          description: Array of published positions.\n          content:\n          \
  \  application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/Position'\n        '401':\n          description: Unauthorized (invalid or missing token).\n        '404':\n          description: Company not found.\n  /company/{company_uid}/positions/{position_uid}:\n    get:\n      operationId: getPosition\n      summary: Retrieve a position\n      description: Retrieve a single published position by its UID.\n      tags:\n        - Positions\n      parameters:\n        - name: company_uid\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: position_uid\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: token\n          in: query\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: A single position.\n          content:\n\
  \            application/json:\n              schema:\n                $ref: '#/components/schemas/Position'\n        '404':\n          description: Position not found.\ncomponents:\n  securitySchemes:\n    companyToken:\n      type: apiKey\n      in: query\n      name: token\n      description: Public company token issued by Comeet for the Careers API.\n  schemas:\n    Position:\n      type: object\n      properties:\n        uid:\n          type: string\n          description: Unique identifier for the position.\n        name:\n          type: string\n          description: Job title.\n        department:\n          type: string\n        location:\n          type: object\n          properties:\n            country:\n              type: string\n            city:\n              type: string\n            name:\n              type: string\n        company_department:\n          type: string\n        url_active_after:\n          type: string\n          format: date-time\n        url_comeet_hosted_page:\n\
  \          type: string\n          format: uri\n        time_id:\n          type: string\n        details:\n          type: object\n          properties:\n            description:\n              type: string\n              description: HTML or markdown job description.\n            requirements:\n              type: string\n        status:\n          type: string\n          enum: [published, draft, archived]\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/comeet/refs/heads/main/openapi/comeet-careers-api-openapi.yml
tags:
- Careers
- Jobs
- Recruiting
---
