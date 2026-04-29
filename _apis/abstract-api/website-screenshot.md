---
aid: abstract-api:website-screenshot
baseURL: https://screenshot.abstractapi.com/v1/
description: Capture high-quality screenshots of any website with optional customizations including CSS injection, delay settings, and viewport configuration.
humanURL: https://www.abstractapi.com/api/website-screenshot-api
image: ''
layout: api
name: Website Screenshot API
properties:
- type: Documentation
  url: https://docs.abstractapi.com/api/screenshot.md
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-website-screenshot.yaml
provider_name: Abstract API
provider_slug: abstract-api
slug: website-screenshot
source_filename: abstract-api-website-screenshot.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Abstract API - Website Screenshot API\n  description: Capture high-quality screenshots of any website with optional customizations including CSS injection, delay settings, and viewport configuration.\n  version: 1.0.0\n  contact:\n    url: https://www.abstractapi.com/\n  x-generated-from: documentation\nservers:\n  - url: https://screenshot.abstractapi.com/v1\n    description: Website Screenshot API v1\nsecurity:\n  - apiKey: []\ntags:\n  - name: Website Screenshot\n    description: Website screenshot capture operations\npaths:\n  /:\n    get:\n      operationId: captureWebsiteScreenshot\n      summary: Abstract API Capture Website Screenshot\n      description: Capture a screenshot of any website URL with configurable viewport, delay, and CSS injection options.\n      tags:\n        - Website Screenshot\n      parameters:\n        - name: api_key\n          in: query\n          required: true\n          description: Your unique API key for the\
  \ Website Screenshot API.\n          schema:\n            type: string\n          example: abc123def456\n        - name: url\n          in: query\n          required: true\n          description: The URL of the website to screenshot.\n          schema:\n            type: string\n            format: uri\n          example: https://www.example.com\n        - name: capture_full_page\n          in: query\n          required: false\n          description: Whether to capture the full scrollable page. Defaults to false.\n          schema:\n            type: boolean\n          example: false\n        - name: width\n          in: query\n          required: false\n          description: Viewport width in pixels. Defaults to 1280.\n          schema:\n            type: integer\n          example: 1280\n        - name: height\n          in: query\n          required: false\n          description: Viewport height in pixels. Defaults to 720.\n          schema:\n            type: integer\n          example:\
  \ 720\n        - name: delay\n          in: query\n          required: false\n          description: Delay in milliseconds before taking the screenshot.\n          schema:\n            type: integer\n          example: 1000\n        - name: css_injection\n          in: query\n          required: false\n          description: CSS string to inject into the page before screenshotting.\n          schema:\n            type: string\n          example: 'body { background: white; }'\n        - name: export_format\n          in: query\n          required: false\n          description: Output format of the screenshot (jpeg or png). Defaults to jpeg.\n          schema:\n            type: string\n            enum:\n              - jpeg\n              - png\n          example: jpeg\n      responses:\n        '200':\n          description: Screenshot image binary\n          content:\n            image/jpeg:\n              schema:\n                type: string\n                format: binary\n      \
  \      image/png:\n              schema:\n                type: string\n                format: binary\n        '400':\n          description: Bad request\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '401':\n          description: Unauthorized\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: query\n      name: api_key\n  schemas:\n    ErrorResponse:\n      type: object\n      properties:\n        message:\n          type: string\n          example: The provided API key is invalid\n        error:\n          type: string\n          example: invalid_api_key\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-website-screenshot.yaml
tags:
- Screenshots
- Web Capture
- Images
---
