---
aid: abstract-api:image-processing
baseURL: https://images.abstractapi.com/v1/
description: Compress, convert, and optimize images by URL or direct upload. Supports format conversion, quality adjustment, and size reduction.
humanURL: https://www.abstractapi.com/api/image-processing-optimization-api
image: ''
layout: api
name: Image Processing API
properties:
- type: Documentation
  url: https://docs.abstractapi.com/api/images.md
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-image-processing.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/json-schema/image-processing-image-processing-response-schema.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/examples/image-processing-image-processing-response-example.json
provider_name: Abstract API
provider_slug: abstract-api
slug: image-processing
source_filename: abstract-api-image-processing.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Abstract API - Image Processing API\n  description: Compress, convert, and optimize images by URL or direct upload. Supports format conversion, quality adjustment, and size reduction.\n  version: 1.0.0\n  contact:\n    url: https://www.abstractapi.com/\n  x-generated-from: documentation\nservers:\n  - url: https://images.abstractapi.com/v1\n    description: Image Processing API v1\nsecurity:\n  - apiKey: []\ntags:\n  - name: Image Processing\n    description: Image compression and optimization operations\npaths:\n  /url:\n    get:\n      operationId: processImageByURL\n      summary: Abstract API Process Image by URL\n      description: Compress, convert, or optimize an image from a given URL.\n      tags:\n        - Image Processing\n      parameters:\n        - name: api_key\n          in: query\n          required: true\n          description: Your unique API key for the Image Processing API.\n          schema:\n            type: string\n\
  \          example: abc123def456\n        - name: url\n          in: query\n          required: true\n          description: URL of the image to process.\n          schema:\n            type: string\n            format: uri\n          example: https://www.example.com/image.png\n        - name: lossy\n          in: query\n          required: false\n          description: Whether to apply lossy compression. Defaults to true.\n          schema:\n            type: boolean\n          example: true\n        - name: quality\n          in: query\n          required: false\n          description: Image quality from 1 to 100 (for lossy compression).\n          schema:\n            type: integer\n            minimum: 1\n            maximum: 100\n          example: 80\n        - name: output_format\n          in: query\n          required: false\n          description: Target output format (jpeg, png, webp, gif).\n          schema:\n            type: string\n            enum:\n              - jpeg\n\
  \              - png\n              - webp\n              - gif\n          example: webp\n      responses:\n        '200':\n          description: Processed image result\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ImageProcessingResponse'\n              examples:\n                processImageByURL200Example:\n                  summary: Default processImageByURL 200 response\n                  x-microcks-default: true\n                  value:\n                    original_size: 102400\n                    new_size: 51200\n                    saved_bytes: 51200\n                    saved_percent: 50.0\n                    url: https://dl.abstractapi.com/processed/abc123.webp\n        '400':\n          description: Bad request\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '401':\n          description: Unauthorized\n \
  \         content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: query\n      name: api_key\n  schemas:\n    ImageProcessingResponse:\n      type: object\n      description: Image processing result\n      properties:\n        original_size:\n          type: integer\n          description: Original file size in bytes\n          example: 102400\n        new_size:\n          type: integer\n          description: Processed file size in bytes\n          example: 51200\n        saved_bytes:\n          type: integer\n          description: Bytes saved by processing\n          example: 51200\n        saved_percent:\n          type: number\n          description: Percentage of size reduction\n          example: 50.0\n        url:\n          type: string\n          format: uri\n\
  \          description: URL to download the processed image\n          example: https://dl.abstractapi.com/processed/abc123.webp\n    ErrorResponse:\n      type: object\n      properties:\n        message:\n          type: string\n          example: The provided API key is invalid\n        error:\n          type: string\n          example: invalid_api_key\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-image-processing.yaml
tags:
- Image Processing
- Images
- Optimization
---
