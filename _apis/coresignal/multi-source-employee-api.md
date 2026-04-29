---
aid: coresignal:multi-source-employee-api
baseURL: https://api.coresignal.com/cdapi/v2/multi_source_employee
description: The Multi-source Employee API returns enriched employee profiles aggregated from multiple public sources with 300+ data fields covering experience, education, skills, certifications, and connections. Search uses Elasticsearch DSL with rich filter support, pagination, and collect/bulk_collect endpoints for retrieving full records by ID.
humanURL: https://docs.coresignal.com/multi-source-employee-api/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Coresignal Multi-source Employee API
properties:
- type: Documentation
  url: https://docs.coresignal.com/multi-source-employee-api/
- type: DataDictionary
  url: https://docs.coresignal.com/multi-source-employee-api/data-dictionary
- type: Sample
  url: https://docs.coresignal.com/multi-source-employee-api/sample
- type: SearchFilters
  url: https://docs.coresignal.com/multi-source-employee-api/search-filters
- type: ElasticsearchDSL
  url: https://docs.coresignal.com/multi-source-employee-api/search-with-es-dsl
- type: Collect
  url: https://docs.coresignal.com/multi-source-employee-api/collect
- type: BulkCollect
  url: https://docs.coresignal.com/multi-source-employee-api/bulk-collect
- type: Webhooks
  url: https://docs.coresignal.com/multi-source-employee-api/subscriptions
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/openapi/coresignal-multi-source-employee-api-openapi.yml
- type: Rules
  url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/rules/coresignal-multi-source-employee-api-rules.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/capabilities/coresignal-employee-data-collection-capabilities.yml
provider_name: Coresignal
provider_slug: coresignal
slug: multi-source-employee-api
source_filename: coresignal-multi-source-employee-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Coresignal Multi-source Employee API\n  version: '2.0'\n  description: >-\n    The Multi-source Employee API returns enriched employee profiles\n    aggregated from multiple public sources with 300+ fields. Search uses\n    Elasticsearch DSL or filters; Collect returns full records by ID.\n  contact:\n    name: Coresignal Support\n    url: https://coresignal.com/contact/\n  license:\n    name: Proprietary\n    url: https://coresignal.com/terms-and-conditions/\nservers:\n  - url: https://api.coresignal.com/cdapi/v2/multi_source_employee\n    description: Coresignal Multi-source Employee API production server\nsecurity:\n  - apiKey: []\ntags:\n  - name: Search\n    description: Search employee records.\n  - name: Collect\n    description: Retrieve full employee records.\n  - name: Subscriptions\n    description: Webhook subscriptions for employee record updates.\npaths:\n  /search/filter:\n    post:\n      operationId: searchEmployeesByFilter\n\
  \      summary: Search Employees (filter)\n      description: Search employee records using a structured filter.\n      tags:\n        - Search\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/EmployeeFilter'\n      responses:\n        '200':\n          description: Array of matching employee record IDs\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  type: integer\n                  format: int64\n  /search/es_dsl:\n    post:\n      operationId: searchEmployeesByEsDsl\n      summary: Search Employees (Elasticsearch DSL)\n      description: Search employee records using a full Elasticsearch DSL query body.\n      tags:\n        - Search\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n      responses:\n\
  \        '200':\n          description: Array of matching employee record IDs\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  type: integer\n                  format: int64\n  /collect/{id}:\n    get:\n      operationId: collectEmployee\n      summary: Collect an Employee record\n      description: Retrieve the full employee record for the given ID.\n      tags:\n        - Collect\n      parameters:\n        - name: id\n          in: path\n          required: true\n          schema:\n            type: integer\n            format: int64\n      responses:\n        '200':\n          description: Full employee record\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Employee'\n  /bulk_collect:\n    post:\n      operationId: bulkCollectEmployees\n      summary: Bulk Collect Employees\n      description: Retrieve multiple full\
  \ employee records by an array of IDs.\n      tags:\n        - Collect\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                ids:\n                  type: array\n                  items:\n                    type: integer\n                    format: int64\n      responses:\n        '200':\n          description: Array of employee records\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/Employee'\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: header\n      name: apikey\n  schemas:\n    Employee:\n      type: object\n      properties:\n        id:\n          type: integer\n          format: int64\n        full_name:\n          type: string\n        first_name:\n          type: string\n        last_name:\n \
  \         type: string\n        title:\n          type: string\n        headline:\n          type: string\n        summary:\n          type: string\n        country:\n          type: string\n        location:\n          type: string\n        industry:\n          type: string\n        connections:\n          type: integer\n        followers:\n          type: integer\n        experience:\n          type: array\n          items:\n            type: object\n            properties:\n              company_name:\n                type: string\n              title:\n                type: string\n              date_from:\n                type: string\n              date_to:\n                type: string\n              description:\n                type: string\n        education:\n          type: array\n          items:\n            type: object\n            properties:\n              school:\n                type: string\n              degree:\n                type: string\n              field:\n\
  \                type: string\n              date_from:\n                type: string\n              date_to:\n                type: string\n        skills:\n          type: array\n          items:\n            type: string\n        certifications:\n          type: array\n          items:\n            type: object\n        linkedin_url:\n          type: string\n        last_updated:\n          type: string\n          format: date-time\n    EmployeeFilter:\n      type: object\n      properties:\n        full_name:\n          type: string\n        title:\n          type: string\n        country:\n          type: string\n        location:\n          type: string\n        industry:\n          type: string\n        active_experience_company_name:\n          type: string\n        active_experience_title:\n          type: string\n        skills:\n          type: array\n          items:\n            type: string\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/openapi/coresignal-multi-source-employee-api-openapi.yml
tags:
- Employees
- Multi-source
- People Data
---
