---
aid: cohere:tokenize-api
baseURL: https://api.cohere.com
description: The Cohere Tokenize API splits input text into tokens using the tokenizer associated with a specified model. It returns both the token strings and their corresponding token IDs. This is useful for understanding how text will be processed by Cohere models, estimating token counts for billing purposes, and debugging input formatting issues.
humanURL: https://docs.cohere.com/reference/tokenize
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Cohere Tokenize API
properties:
- type: Documentation
  url: https://docs.cohere.com/reference/tokenize
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-tokenize-api-openapi.yml
provider_name: cohere
provider_slug: cohere
slug: tokenize-api
source_filename: cohere-tokenize-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Cohere Tokenize API\n  description: >-\n    The Cohere Tokenize API splits input text into tokens using the\n    tokenizer associated with a specified model. It returns both the token\n    strings and their corresponding token IDs. This is useful for\n    understanding how text will be processed by Cohere models, estimating\n    token counts for billing purposes, and debugging input formatting issues.\n  version: '1.0'\n  contact:\n    name: Cohere Support\n    url: https://support.cohere.com\n  termsOfService: https://cohere.com/terms-of-use\nexternalDocs:\n  description: Cohere Tokenize API Documentation\n  url: https://docs.cohere.com/reference/tokenize\nservers:\n  - url: https://api.cohere.com\n    description: Cohere Production Server\ntags:\n  - name: Tokenize\n    description: >-\n      Endpoints for splitting text into tokens using byte-pair encoding for\n      a specified Cohere model.\nsecurity:\n  - bearerAuth: []\npaths:\n  /v1/tokenize:\n\
  \    post:\n      operationId: tokenize\n      summary: Tokenize text\n      description: >-\n        Splits input text into smaller units called tokens using byte-pair\n        encoding (BPE) for the specified model. Returns both the token\n        strings and their corresponding integer token IDs. The text must be\n        between 1 and 65536 characters.\n      tags:\n        - Tokenize\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/TokenizeRequest'\n      responses:\n        '200':\n          description: Successful tokenization response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/TokenizeResponse'\n        '400':\n          description: Bad request due to invalid parameters\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Error'\n  \
  \      '401':\n          description: Unauthorized due to missing or invalid API key\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Error'\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      description: >-\n        Bearer authentication using a Cohere API key.\n  schemas:\n    TokenizeRequest:\n      type: object\n      required:\n        - text\n        - model\n      properties:\n        text:\n          type: string\n          description: >-\n            The string to be tokenized. Must be between 1 and 65536\n            characters.\n          minLength: 1\n          maxLength: 65536\n        model:\n          type: string\n          description: >-\n            The name of the model whose tokenizer will be used to tokenize\n            the input text.\n          example: command-r-plus\n    TokenizeResponse:\n      type: object\n      properties:\n        tokens:\n\
  \          type: array\n          description: >-\n            An array of token strings resulting from tokenizing the input\n            text.\n          items:\n            type: string\n        token_strings:\n          type: array\n          description: >-\n            An array of token strings corresponding to each token.\n          items:\n            type: string\n        meta:\n          type: object\n          description: >-\n            Metadata about the API request.\n          properties:\n            api_version:\n              type: object\n              properties:\n                version:\n                  type: string\n                  description: >-\n                    The API version used for the request.\n    Error:\n      type: object\n      properties:\n        message:\n          type: string\n          description: >-\n            A human-readable error message describing what went wrong.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-tokenize-api-openapi.yml
tags:
- Artificial Intelligence
- Natural Language Processing
- Text Processing
- Tokenization
---
