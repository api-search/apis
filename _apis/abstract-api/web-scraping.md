---
aid: abstract-api:web-scraping
baseURL: https://scrape.abstractapi.com/v1/
description: Extract data from any website by providing the target URL. Handles JavaScript rendering and returns the full HTML content of any web page.
humanURL: https://www.abstractapi.com/api/web-scraping-api
image: ''
layout: api
name: Web Scraping API
properties:
- type: Documentation
  url: https://docs.abstractapi.com/api/scrape.md
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-web-scraping.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/json-schema/web-scraping-web-scraping-response-schema.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/examples/web-scraping-web-scraping-response-example.json
provider_name: Abstract API
provider_slug: abstract-api
slug: web-scraping
source_filename: abstract-api-web-scraping.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Abstract API - Web Scraping API\n  description: Extract data from any website by providing the target URL. Handles JavaScript rendering and returns the full HTML content of any web page.\n  version: 1.0.0\n  contact:\n    url: https://www.abstractapi.com/\n  x-generated-from: documentation\nservers:\n  - url: https://scrape.abstractapi.com/v1\n    description: Web Scraping API v1\nsecurity:\n  - apiKey: []\ntags:\n  - name: Web Scraping\n    description: Web content extraction operations\npaths:\n  /:\n    get:\n      operationId: scrapeWebPage\n      summary: Abstract API Scrape Web Page\n      description: Extract the full HTML content of any website URL, with support for JavaScript-rendered pages.\n      tags:\n        - Web Scraping\n      parameters:\n        - name: api_key\n          in: query\n          required: true\n          description: Your unique API key for the Web Scraping API.\n          schema:\n            type: string\n \
  \         example: abc123def456\n        - name: url\n          in: query\n          required: true\n          description: The URL of the webpage to scrape.\n          schema:\n            type: string\n            format: uri\n          example: https://www.example.com\n        - name: render_js\n          in: query\n          required: false\n          description: Whether to render JavaScript before returning HTML. Defaults to false.\n          schema:\n            type: boolean\n          example: false\n      responses:\n        '200':\n          description: Scraped HTML content\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/WebScrapingResponse'\n              examples:\n                scrapeWebPage200Example:\n                  summary: Default scrapeWebPage 200 response\n                  x-microcks-default: true\n                  value:\n                    body: '<html><head><title>Example Domain</title></head><body>...</body></html>'\n\
  \                    url: https://www.example.com\n                    status_code: 200\n        '400':\n          description: Bad request\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '401':\n          description: Unauthorized\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: query\n      name: api_key\n  schemas:\n    WebScrapingResponse:\n      type: object\n      description: Web scraping result\n      properties:\n        body:\n          type: string\n          description: Full HTML content of the page\n          example: '<html><head><title>Example Domain</title></head><body>...</body></html>'\n        url:\n          type: string\n          format:\
  \ uri\n          description: Final URL after redirects\n          example: https://www.example.com\n        status_code:\n          type: integer\n          description: HTTP status code of the scraped page\n          example: 200\n    ErrorResponse:\n      type: object\n      properties:\n        message:\n          type: string\n          example: The provided API key is invalid\n        error:\n          type: string\n          example: invalid_api_key\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-web-scraping.yaml
tags:
- Web Scraping
- Data Extraction
- HTML
---
