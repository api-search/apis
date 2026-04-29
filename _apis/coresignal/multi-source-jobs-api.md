---
aid: coresignal:multi-source-jobs-api
baseURL: https://api.coresignal.com/cdapi/v2/multi_source_jobs
description: The Multi-source Jobs API returns enriched job posting records aggregated from multiple public sources with 85+ data fields covering title, location, company, salary, posted date, source URLs, and full job descriptions. Search uses Elasticsearch DSL with collect endpoints for retrieving full records by ID.
humanURL: https://docs.coresignal.com/multi-source-jobs-api/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Coresignal Multi-source Jobs API
properties:
- type: Documentation
  url: https://docs.coresignal.com/multi-source-jobs-api/
- type: DataDictionary
  url: https://docs.coresignal.com/multi-source-jobs-api/data-dictionary
- type: Sample
  url: https://docs.coresignal.com/multi-source-jobs-api/sample
- type: SearchFilters
  url: https://docs.coresignal.com/multi-source-jobs-api/search-filters
- type: ElasticsearchDSL
  url: https://docs.coresignal.com/multi-source-jobs-api/search-with-es-dsl
- type: Collect
  url: https://docs.coresignal.com/multi-source-jobs-api/collect
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/openapi/coresignal-multi-source-jobs-api-openapi.yml
- type: Rules
  url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/rules/coresignal-multi-source-jobs-api-rules.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/capabilities/coresignal-jobs-data-collection-capabilities.yml
provider_name: Coresignal
provider_slug: coresignal
slug: multi-source-jobs-api
source_filename: coresignal-multi-source-jobs-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Coresignal Multi-source Jobs API\n  version: '2.0'\n  description: >-\n    The Multi-source Jobs API returns enriched job posting records aggregated\n    from multiple public sources. Search supports filter and Elasticsearch\n    DSL queries; Collect retrieves full job records by ID.\n  contact:\n    name: Coresignal Support\n    url: https://coresignal.com/contact/\n  license:\n    name: Proprietary\n    url: https://coresignal.com/terms-and-conditions/\nservers:\n  - url: https://api.coresignal.com/cdapi/v2/multi_source_jobs\n    description: Coresignal Multi-source Jobs API production server\nsecurity:\n  - apiKey: []\ntags:\n  - name: Search\n    description: Search job posting records.\n  - name: Collect\n    description: Retrieve full job posting records by ID.\npaths:\n  /search/filter:\n    post:\n      operationId: searchJobsByFilter\n      summary: Search Jobs (filter)\n      description: Search job posting records using a structured\
  \ filter.\n      tags:\n        - Search\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/JobFilter'\n      responses:\n        '200':\n          description: Array of matching job posting record IDs\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  type: integer\n                  format: int64\n  /search/es_dsl:\n    post:\n      operationId: searchJobsByEsDsl\n      summary: Search Jobs (Elasticsearch DSL)\n      description: Search job posting records using a full Elasticsearch DSL query.\n      tags:\n        - Search\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n      responses:\n        '200':\n          description: Array of matching job posting record IDs\n          content:\n        \
  \    application/json:\n              schema:\n                type: array\n                items:\n                  type: integer\n                  format: int64\n  /collect/{id}:\n    get:\n      operationId: collectJob\n      summary: Collect a Job posting record\n      description: Retrieve the full job posting record for the given ID.\n      tags:\n        - Collect\n      parameters:\n        - name: id\n          in: path\n          required: true\n          schema:\n            type: integer\n            format: int64\n      responses:\n        '200':\n          description: Full job posting record\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Job'\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: header\n      name: apikey\n  schemas:\n    Job:\n      type: object\n      properties:\n        id:\n          type: integer\n          format: int64\n        title:\n          type:\
  \ string\n        description:\n          type: string\n        url:\n          type: string\n          format: uri\n        company_name:\n          type: string\n        company_url:\n          type: string\n        location:\n          type: string\n        country:\n          type: string\n        region:\n          type: string\n        seniority_level:\n          type: string\n        employment_type:\n          type: string\n        application_active:\n          type: boolean\n        time_posted:\n          type: string\n        date_posted:\n          type: string\n          format: date-time\n        salary_currency:\n          type: string\n        salary_min:\n          type: number\n        salary_max:\n          type: number\n        last_updated:\n          type: string\n          format: date-time\n    JobFilter:\n      type: object\n      properties:\n        title:\n          type: string\n        company_name:\n          type: string\n        country:\n          type:\
  \ string\n        location:\n          type: string\n        seniority_level:\n          type: string\n        employment_type:\n          type: string\n        date_posted_from:\n          type: string\n        date_posted_to:\n          type: string\n        application_active:\n          type: boolean\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/openapi/coresignal-multi-source-jobs-api-openapi.yml
tags:
- Jobs
- Multi-source
- Recruiting
---
