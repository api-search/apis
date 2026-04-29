---
aid: abstract-api:public-holidays
baseURL: https://holidays.abstractapi.com/v1/
description: Get public, local, religious, and other holidays for any country. Supports year and country filtering with comprehensive holiday metadata.
humanURL: https://www.abstractapi.com/api/holidays-api
image: ''
layout: api
name: Public Holidays API
properties:
- type: Documentation
  url: https://docs.abstractapi.com/api/holidays.md
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-public-holidays.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/json-schema/public-holidays-holiday-schema.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/examples/public-holidays-holiday-example.json
provider_name: Abstract API
provider_slug: abstract-api
slug: public-holidays
source_filename: abstract-api-public-holidays.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Abstract API - Public Holidays API\n  description: Get public, local, religious, and other holidays for any country. Supports year and country filtering with comprehensive holiday metadata.\n  version: 1.0.0\n  contact:\n    url: https://www.abstractapi.com/\n  x-generated-from: documentation\nservers:\n  - url: https://holidays.abstractapi.com/v1\n    description: Public Holidays API v1\nsecurity:\n  - apiKey: []\ntags:\n  - name: Public Holidays\n    description: Holiday lookup operations\npaths:\n  /:\n    get:\n      operationId: getPublicHolidays\n      summary: Abstract API Get Public Holidays\n      description: Retrieve public, local, religious, and other holidays for a given country and optional date filter.\n      tags:\n        - Public Holidays\n      parameters:\n        - name: api_key\n          in: query\n          required: true\n          description: Your unique API key for the Public Holidays API.\n          schema:\n    \
  \        type: string\n          example: abc123def456\n        - name: country\n          in: query\n          required: true\n          description: ISO 3166-1 alpha-2 two-letter country code.\n          schema:\n            type: string\n          example: US\n        - name: year\n          in: query\n          required: false\n          description: Year to query (required on free plan). Defaults to current year on paid.\n          schema:\n            type: string\n          example: '2026'\n        - name: month\n          in: query\n          required: false\n          description: Month to query (1-12, required on free plan). Defaults to current month.\n          schema:\n            type: string\n          example: '4'\n        - name: day\n          in: query\n          required: false\n          description: Day to query (1-31, required on free plan). Defaults to current day.\n          schema:\n            type: string\n          example: '19'\n      responses:\n        '200':\n\
  \          description: List of public holidays\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/Holiday'\n              examples:\n                getPublicHolidays200Example:\n                  summary: Default getPublicHolidays 200 response\n                  x-microcks-default: true\n                  value:\n                    - name: Easter Sunday\n                      name_local: Easter Sunday\n                      language: EN\n                      description: Easter Sunday marks the resurrection of Jesus Christ\n                      country: US\n                      location: ''\n                      type: National\n                      date: 04/20/2025\n                      date_year: '2025'\n                      date_month: '04'\n                      date_day: '20'\n                      week_day: Sunday\n        '400':\n          description:\
  \ Bad request\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '401':\n          description: Unauthorized\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: query\n      name: api_key\n  schemas:\n    Holiday:\n      type: object\n      description: A public holiday entry\n      properties:\n        name:\n          type: string\n          description: Holiday name in English\n          example: Easter Sunday\n        name_local:\n          type: string\n          description: Holiday name in local language\n          example: Paques\n        language:\n          type: string\n          description: Language of the local name\n          example: FR\n        description:\n\
  \          type: string\n          description: Additional details about the holiday\n          example: Easter Sunday marks the resurrection of Jesus Christ\n        country:\n          type: string\n          description: Country code\n          example: US\n        location:\n          type: string\n          description: Specific region where holiday applies\n          example: ''\n        type:\n          type: string\n          description: Holiday classification\n          example: National\n          enum:\n            - National\n            - Local\n            - Religious\n            - Observance\n            - Season\n            - Clock Change/Daylight Saving Time\n        date:\n          type: string\n          description: Holiday date in MM/DD/YYYY format\n          example: 04/20/2025\n        date_year:\n          type: string\n          description: Year of the holiday\n          example: '2025'\n        date_month:\n          type: string\n          description: Month\
  \ of the holiday\n          example: '04'\n        date_day:\n          type: string\n          description: Day of the holiday\n          example: '20'\n        week_day:\n          type: string\n          description: Day of the week\n          example: Sunday\n    ErrorResponse:\n      type: object\n      properties:\n        message:\n          type: string\n          example: The provided API key is invalid\n        error:\n          type: string\n          example: invalid_api_key\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-public-holidays.yaml
tags:
- Public Holidays
- Calendar
- Global Data
---
