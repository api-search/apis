---
aid: abstract-api:avatars
baseURL: https://avatars.abstractapi.com/v1/
description: Create highly customizable avatar images using a person's name or initials. Supports color, font, and size customization for user profile images.
humanURL: https://www.abstractapi.com/api/user-avatar-api
image: ''
layout: api
name: Avatars API
properties:
- type: Documentation
  url: https://docs.abstractapi.com/api/avatars.md
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-avatars.yaml
provider_name: Abstract API
provider_slug: abstract-api
slug: avatars
source_filename: abstract-api-avatars.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Abstract API - Avatars API\n  description: Create highly customizable avatar images using a person's name or initials. Supports color, font, and size customization for user profile images.\n  version: 1.0.0\n  contact:\n    url: https://www.abstractapi.com/\n  x-generated-from: documentation\nservers:\n  - url: https://avatars.abstractapi.com/v1\n    description: Avatars API v1\nsecurity:\n  - apiKey: []\ntags:\n  - name: Avatars\n    description: User avatar generation operations\npaths:\n  /:\n    get:\n      operationId: generateAvatar\n      summary: Abstract API Generate Avatar\n      description: Generate a customizable avatar image using a person's name or initials with configurable colors, fonts, and sizes.\n      tags:\n        - Avatars\n      parameters:\n        - name: api_key\n          in: query\n          required: true\n          description: Your unique API key for the Avatars API.\n          schema:\n            type: string\n\
  \          example: abc123def456\n        - name: name\n          in: query\n          required: true\n          description: Full name or initials to use for the avatar.\n          schema:\n            type: string\n          example: Jane Smith\n        - name: size\n          in: query\n          required: false\n          description: Size of the avatar in pixels (square). Defaults to 128.\n          schema:\n            type: integer\n          example: 128\n        - name: color\n          in: query\n          required: false\n          description: Text color as a hex code (without #).\n          schema:\n            type: string\n          example: FFFFFF\n        - name: background_color\n          in: query\n          required: false\n          description: Background color as a hex code (without #).\n          schema:\n            type: string\n          example: 4F46E5\n        - name: font_size\n          in: query\n          required: false\n          description: Font size\
  \ as a fraction of the avatar size (0.1 to 0.9).\n          schema:\n            type: number\n          example: 0.5\n        - name: char_count\n          in: query\n          required: false\n          description: Number of characters to use from the name. Defaults to 2.\n          schema:\n            type: integer\n          example: 2\n      responses:\n        '200':\n          description: Avatar image\n          content:\n            image/png:\n              schema:\n                type: string\n                format: binary\n        '400':\n          description: Bad request\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n        '401':\n          description: Unauthorized\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ErrorResponse'\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n\
  \  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: query\n      name: api_key\n  schemas:\n    ErrorResponse:\n      type: object\n      properties:\n        message:\n          type: string\n          example: The provided API key is invalid\n        error:\n          type: string\n          example: invalid_api_key\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-avatars.yaml
tags:
- Avatars
- Images
- User Interface
---
