---
aid: amnic:amnic-api
baseURL: ''
description: The Amnic API provides programmatic access to cloud cost data from saved Cost Analyzer charts, enabling automation of reporting and integration with other FinOps tools. Authenticate with an API key header to retrieve chart filters and cost data with custom filter parameters.
humanURL: https://amnic.com/
image: ''
layout: api
name: Amnic Cloud Cost Observability API
properties:
- type: Documentation
  url: https://docs.amnic.com/
- type: GettingStarted
  url: https://docs.amnic.com/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/openapi/amnic-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/json-schema/amnic-api-filter-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/json-schema/amnic-api-filter-list-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/json-schema/amnic-api-filter-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/json-schema/amnic-api-chart-data-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/json-structure/amnic-api-filter-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/json-structure/amnic-api-filter-list-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/json-structure/amnic-api-filter-request-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/json-structure/amnic-api-chart-data-structure.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/examples/amnic-api-filter-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/examples/amnic-api-filter-list-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/examples/amnic-api-filter-request-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/examples/amnic-api-chart-data-example.json
provider_name: Amnic
provider_slug: amnic
slug: amnic-api
source_filename: amnic-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Amnic Cloud Cost Observability API\n  description: >-\n    The Amnic API provides programmatic access to cloud cost data, enabling automation\n    of reporting and integration with other tools. Use this API to retrieve saved chart\n    data with custom filters for AWS, GCP, Azure, and Kubernetes cost analytics.\n  version: 1.0.0\n  contact:\n    name: Amnic Support\n    url: https://amnic.com/contact\n  x-generated-from: documentation\nservers:\n- url: https://api.amnic.com/orchestrator\n  description: Amnic Production API\nsecurity:\n- ApiKeyAuth: []\ntags:\n- name: Cost Analyzer\n  description: Operations for retrieving cost data and filters from saved charts in the Cost Analyzer.\npaths:\n  /v1/external/view/{uuid}/filters:\n    get:\n      operationId: getChartFilters\n      summary: Amnic Get Chart Filters\n      description: Returns the filters configured in a saved chart identified by its UUID.\n      tags:\n      - Cost Analyzer\n   \
  \   parameters:\n      - name: uuid\n        in: path\n        required: true\n        description: The unique identifier of the saved chart in the Cost Analyzer.\n        schema:\n          type: string\n          format: uuid\n        example: 550e8400-e29b-41d4-a716-446655440000\n      responses:\n        '200':\n          description: Filters retrieved successfully.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/FilterList'\n              examples:\n                GetChartFilters200Example:\n                  summary: Default getChartFilters 200 response\n                  x-microcks-default: true\n                  value:\n                  - filter_by: service\n                    values:\n                    - EC2\n                    - S3\n                  - filter_by: region\n                    values:\n                    - us-east-1\n        '400':\n          description: Bad request - missing or invalid\
  \ parameters.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '401':\n          description: Unauthorized - invalid or expired API key.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /v1/external/view/{uuid}:\n    post:\n      operationId: getChartData\n      summary: Amnic Get Chart Data\n      description: Retrieves saved chart data by providing additional custom filters to narrow the cost analysis results.\n      tags:\n      - Cost Analyzer\n      parameters:\n      - name: uuid\n        in: path\n        required: true\n        description: The unique identifier of the saved chart in the Cost Analyzer.\n        schema:\n          type: string\n          format: uuid\n        example: 550e8400-e29b-41d4-a716-446655440000\n \
  \     requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/FilterRequest'\n            examples:\n              GetChartDataRequestExample:\n                summary: Default getChartData request\n                x-microcks-default: true\n                value:\n                  filters:\n                  - filter_by: service\n                    values:\n                    - EC2\n      responses:\n        '200':\n          description: Chart data retrieved successfully.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ChartData'\n              examples:\n                GetChartData200Example:\n                  summary: Default getChartData 200 response\n                  x-microcks-default: true\n                  value:\n                    headers:\n                    - date\n                    - service\n        \
  \            - cost\n                    rows:\n                    - - '2025-03-01'\n                      - EC2\n                      - '1234.56'\n                    - - '2025-03-01'\n                      - S3\n                      - '98.76'\n        '400':\n          description: Bad request - missing or invalid parameters.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '401':\n          description: Unauthorized - invalid or expired API key.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    ApiKeyAuth:\n      type: apiKey\n      in: header\n      name: X-API-Key\n      description: API key for authenticating requests to the Amnic API. Obtain your API key from the Amnic dashboard.\n  schemas:\n\
  \    Filter:\n      type: object\n      description: A filter object specifying a dimension and its accepted values for cost data queries.\n      properties:\n        filter_by:\n          type: string\n          description: The dimension to filter by (e.g., service, region, account, team).\n          example: service\n        values:\n          type: array\n          description: The list of values to include for the specified filter dimension.\n          items:\n            type: string\n          example:\n          - EC2\n          - S3\n      required:\n      - filter_by\n      - values\n    FilterList:\n      type: array\n      description: A list of filters configured on a saved chart.\n      items:\n        $ref: '#/components/schemas/Filter'\n    FilterRequest:\n      type: object\n      description: Request body for retrieving chart data with additional custom filters.\n      properties:\n        filters:\n          type: array\n          description: Additional filters to apply\
  \ when retrieving chart data.\n          items:\n            $ref: '#/components/schemas/Filter'\n    ChartData:\n      type: object\n      description: Cost chart data returned as a 2D array with headers and rows.\n      properties:\n        headers:\n          type: array\n          description: Column headers for the cost data result set.\n          items:\n            type: string\n          example:\n          - date\n          - service\n          - cost\n        rows:\n          type: array\n          description: Rows of cost data values corresponding to the headers.\n          items:\n            type: array\n            items:\n              type: string\n    ErrorResponse:\n      type: object\n      description: Standard error response returned when a request fails.\n      properties:\n        message:\n          type: string\n          description: Human-readable description of the error.\n          example: Invalid or expired API key.\n        code:\n          type: integer\n\
  \          description: HTTP status code for the error.\n          example: 401\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amnic/refs/heads/main/openapi/amnic-openapi.yml
tags:
- Cloud Cost Observability
- FinOps
- Cost Analytics
---
