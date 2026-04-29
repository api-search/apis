---
aid: abstract-api:company-enrichment
baseURL: https://companyenrichment.abstractapi.com/v1/
description: Retrieve comprehensive details about businesses using their domain or email address, including name, logo, headcount, location, industry, and more.
humanURL: https://www.abstractapi.com/api/company-enrichment
image: ''
layout: api
name: Company Enrichment API
properties:
- type: Documentation
  url: https://docs.abstractapi.com/api/company-enrichment.md
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-company-enrichment.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/json-schema/company-enrichment-company-enrichment-response-schema.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/examples/company-enrichment-company-enrichment-response-example.json
provider_name: Abstract API
provider_slug: abstract-api
slug: company-enrichment
source_filename: abstract-api-company-enrichment.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Abstract API - Company Enrichment API\n  description: Retrieve comprehensive details about businesses using their domain or email address, including name, logo, headcount, location, industry, and more.\n  version: 1.0.0\n  contact:\n    url: https://www.abstractapi.com/\n  x-generated-from: documentation\nservers:\n  - url: https://companyenrichment.abstractapi.com/v1\n    description: Company Enrichment API v1\nsecurity:\n  - apiKey: []\ntags:\n  - name: Company Enrichment\n    description: Company data enrichment operations\npaths:\n  /:\n    get:\n      operationId: getCompanyEnrichment\n      summary: Abstract API Get Company Enrichment\n      description: Retrieve company data including name, logo, description, industry, headcount, and location using a domain name or email.\n      tags:\n        - Company Enrichment\n      parameters:\n        - name: api_key\n          in: query\n          required: true\n          description: Your unique\
  \ API key for the Company Enrichment API.\n          schema:\n            type: string\n          example: abc123def456\n        - name: domain\n          in: query\n          required: false\n          description: Company domain name to enrich (e.g., stripe.com). Use domain or email.\n          schema:\n            type: string\n          example: stripe.com\n        - name: email\n          in: query\n          required: false\n          description: Business email address to derive the company domain from. Use domain or email.\n          schema:\n            type: string\n            format: email\n          example: billing@stripe.com\n      responses:\n        '200':\n          description: Company enrichment data\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/CompanyEnrichmentResponse'\n              examples:\n                getCompanyEnrichment200Example:\n                  summary: Default getCompanyEnrichment\
  \ 200 response\n                  x-microcks-default: true\n                  value:\n                    name: Stripe\n                    domain: stripe.com\n                    country: US\n                    locality: San Francisco\n                    region: California\n                    linkedin_url: https://www.linkedin.com/company/stripe\n                    logo: https://logo.clearbit.com/stripe.com\n                    year_founded: 2010\n                    industry: Financial Services\n                    employees_count: 8000\n                    description: Stripe is a technology company that builds economic infrastructure for the internet.\n        '400':\n          description: Bad request\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '401':\n          description: Unauthorized\n          content:\n            application/json:\n              schema:\n                $ref:\
  \ '#/components/schemas/ErrorResponse'\n        '429':\n          description: Rate limit exceeded\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: query\n      name: api_key\n  schemas:\n    CompanyEnrichmentResponse:\n      type: object\n      description: Company enrichment data\n      properties:\n        name:\n          type: string\n          description: Company name\n          example: Stripe\n        domain:\n          type: string\n          description: Company domain\n          example: stripe.com\n        country:\n          type: string\n          description: ISO 3166-1 alpha-2 country code\n          example: US\n        locality:\n          type: string\n          description: City or locality\n          example: San Francisco\n    \
  \    region:\n          type: string\n          description: State or region\n          example: California\n        linkedin_url:\n          type: string\n          format: uri\n          description: LinkedIn company profile URL\n          example: https://www.linkedin.com/company/stripe\n        logo:\n          type: string\n          format: uri\n          description: URL to company logo image\n          example: https://logo.clearbit.com/stripe.com\n        year_founded:\n          type: integer\n          description: Year the company was founded\n          example: 2010\n        industry:\n          type: string\n          description: Industry classification\n          example: Financial Services\n        employees_count:\n          type: integer\n          description: Approximate number of employees\n          example: 8000\n        description:\n          type: string\n          description: Short company description\n          example: Stripe is a technology company that\
  \ builds economic infrastructure for the internet.\n    ErrorResponse:\n      type: object\n      properties:\n        message:\n          type: string\n          example: The provided API key is invalid\n        error:\n          type: string\n          example: invalid_api_key\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-company-enrichment.yaml
tags:
- Company Enrichment
- Business Data
- Data Enrichment
---
