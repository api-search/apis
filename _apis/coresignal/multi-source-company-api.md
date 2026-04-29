---
aid: coresignal:multi-source-company-api
baseURL: https://api.coresignal.com/cdapi/v2/multi_source_company
description: The Multi-source Company API returns enriched company records combining data from multiple public web sources, deduplicated and standardized with 500+ data fields covering firmographics, technographics, headcount, revenue, and locations. Search uses Elasticsearch DSL. Results are paginated and credits-priced per response.
humanURL: https://docs.coresignal.com/multi-source-company-api/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Coresignal Multi-source Company API
properties:
- type: Documentation
  url: https://docs.coresignal.com/multi-source-company-api/
- type: DataDictionary
  url: https://docs.coresignal.com/multi-source-company-api/data-dictionary
- type: Sample
  url: https://docs.coresignal.com/multi-source-company-api/sample
- type: SearchFilters
  url: https://docs.coresignal.com/multi-source-company-api/search-filters
- type: ElasticsearchDSL
  url: https://docs.coresignal.com/multi-source-company-api/search-with-es-dsl
- type: Collect
  url: https://docs.coresignal.com/multi-source-company-api/collect
- type: BulkCollect
  url: https://docs.coresignal.com/multi-source-company-api/bulk-collect
- type: Webhooks
  url: https://docs.coresignal.com/multi-source-company-api/subscriptions
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/openapi/coresignal-multi-source-company-api-openapi.yml
- type: Rules
  url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/rules/coresignal-multi-source-company-api-rules.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/capabilities/coresignal-company-data-collection-capabilities.yml
provider_name: Coresignal
provider_slug: coresignal
slug: multi-source-company-api
source_filename: coresignal-multi-source-company-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Coresignal Multi-source Company API\n  version: '2.0'\n  description: >-\n    The Multi-source Company API returns enriched company records combining\n    public web data sources, deduplicated and standardized with 500+ fields.\n    Search uses Elasticsearch DSL queries; Collect returns full records by\n    ID. Authentication uses the apikey HTTP header.\n  contact:\n    name: Coresignal Support\n    url: https://coresignal.com/contact/\n  license:\n    name: Proprietary\n    url: https://coresignal.com/terms-and-conditions/\nservers:\n  - url: https://api.coresignal.com/cdapi/v2/multi_source_company\n    description: Coresignal Multi-source Company API production server\nsecurity:\n  - apiKey: []\ntags:\n  - name: Search\n    description: Search and filter company records.\n  - name: Collect\n    description: Retrieve full company records by ID.\n  - name: Subscriptions\n    description: Manage webhook subscriptions for company data updates.\n\
  paths:\n  /search/filter:\n    post:\n      operationId: searchCompaniesByFilter\n      summary: Search Companies (filter)\n      description: Search company records using a structured filter object. Returns matching record IDs.\n      tags:\n        - Search\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/CompanyFilter'\n      responses:\n        '200':\n          description: Array of matching company record IDs\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  type: integer\n                  format: int64\n        '401':\n          $ref: '#/components/responses/Unauthorized'\n        '402':\n          $ref: '#/components/responses/CreditsExhausted'\n        '429':\n          $ref: '#/components/responses/RateLimited'\n  /search/es_dsl:\n    post:\n      operationId: searchCompaniesByEsDsl\n\
  \      summary: Search Companies (Elasticsearch DSL)\n      description: Search company records using a full Elasticsearch DSL query body.\n      tags:\n        - Search\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              description: Elasticsearch DSL query object\n      responses:\n        '200':\n          description: Array of matching company record IDs\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  type: integer\n                  format: int64\n  /collect/{id}:\n    get:\n      operationId: collectCompany\n      summary: Collect a Company record\n      description: Retrieve the full company record for the given ID.\n      tags:\n        - Collect\n      parameters:\n        - name: id\n          in: path\n          required: true\n          schema:\n            type: integer\n   \
  \         format: int64\n          description: Coresignal internal company ID\n      responses:\n        '200':\n          description: Full company record\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Company'\n        '404':\n          description: Company not found\n        '401':\n          $ref: '#/components/responses/Unauthorized'\n  /bulk_collect:\n    post:\n      operationId: bulkCollectCompanies\n      summary: Bulk Collect Companies\n      description: Retrieve multiple full company records by an array of IDs.\n      tags:\n        - Collect\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                ids:\n                  type: array\n                  items:\n                    type: integer\n                    format: int64\n      responses:\n        '200':\n          description:\
  \ Array of company records\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/Company'\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: header\n      name: apikey\n  parameters: {}\n  responses:\n    Unauthorized:\n      description: Missing or invalid apikey header\n    CreditsExhausted:\n      description: API credits exhausted for the account\n    RateLimited:\n      description: Rate limit exceeded\n  schemas:\n    Company:\n      type: object\n      properties:\n        id:\n          type: integer\n          format: int64\n        name:\n          type: string\n        website:\n          type: string\n          format: uri\n        domain:\n          type: string\n        industry:\n          type: string\n        type:\n          type: string\n        founded:\n          type: integer\n        size:\n          type: string\n    \
  \    employees_count:\n          type: integer\n        followers_count:\n          type: integer\n        description:\n          type: string\n        headquarters:\n          type: string\n        country:\n          type: string\n        region:\n          type: string\n        locality:\n          type: string\n        specialities:\n          type: array\n          items:\n            type: string\n        technologies:\n          type: array\n          items:\n            type: string\n        funding_total_amount:\n          type: number\n        last_funding_round:\n          type: object\n        linkedin_url:\n          type: string\n        twitter_url:\n          type: string\n        facebook_url:\n          type: string\n        crunchbase_url:\n          type: string\n        last_updated:\n          type: string\n          format: date-time\n    CompanyFilter:\n      type: object\n      properties:\n        name:\n          type: string\n        industry:\n          type:\
  \ string\n        size:\n          type: string\n        country:\n          type: string\n        region:\n          type: string\n        founded_from:\n          type: integer\n        founded_to:\n          type: integer\n        employees_count_from:\n          type: integer\n        employees_count_to:\n          type: integer\n        technologies:\n          type: array\n          items:\n            type: string\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coresignal/refs/heads/main/openapi/coresignal-multi-source-company-api-openapi.yml
tags:
- Companies
- Firmographics
- Multi-source
---
