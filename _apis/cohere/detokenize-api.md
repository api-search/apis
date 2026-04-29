---
aid: cohere:detokenize-api
baseURL: https://api.cohere.com
description: The Cohere Detokenize API converts a sequence of token IDs back into their corresponding text string using the tokenizer for a specified model. It is the inverse operation of the Tokenize API and is useful for inspecting model outputs at the token level, debugging tokenization behavior, and reconstructing text from token representations.
humanURL: https://docs.cohere.com/reference/detokenize
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Cohere Detokenize API
properties:
- type: Documentation
  url: https://docs.cohere.com/reference/detokenize
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-detokenize-api-openapi.yml
provider_name: cohere
provider_slug: cohere
slug: detokenize-api
source_filename: cohere-detokenize-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Cohere Detokenize API\n  description: >-\n    The Cohere Detokenize API converts a sequence of token IDs back into\n    their corresponding text string using the tokenizer for a specified\n    model. It is the inverse operation of the Tokenize API and is useful\n    for inspecting model outputs at the token level, debugging tokenization\n    behavior, and reconstructing text from token representations.\n  version: '1.0'\n  contact:\n    name: Cohere Support\n    url: https://support.cohere.com\n  termsOfService: https://cohere.com/terms-of-use\nexternalDocs:\n  description: Cohere Detokenize API Documentation\n  url: https://docs.cohere.com/reference/detokenize\nservers:\n  - url: https://api.cohere.com\n    description: Cohere Production Server\ntags:\n  - name: Detokenize\n    description: >-\n      Endpoints for converting token IDs back into text using a specified\n      Cohere model's tokenizer.\nsecurity:\n  - bearerAuth: []\npaths:\n \
  \ /v1/detokenize:\n    post:\n      operationId: detokenize\n      summary: Detokenize token IDs\n      description: >-\n        Takes a list of token IDs and converts them back into their\n        corresponding text string using byte-pair encoding for the specified\n        model. This is the inverse operation of the Tokenize endpoint.\n      tags:\n        - Detokenize\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/DetokenizeRequest'\n      responses:\n        '200':\n          description: Successful detokenization response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/DetokenizeResponse'\n        '400':\n          description: Bad request due to invalid parameters\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Error'\n        '401':\n\
  \          description: Unauthorized due to missing or invalid API key\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/Error'\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n      description: >-\n        Bearer authentication using a Cohere API key.\n  schemas:\n    DetokenizeRequest:\n      type: object\n      required:\n        - tokens\n        - model\n      properties:\n        tokens:\n          type: array\n          description: >-\n            The list of token IDs to be detokenized.\n          items:\n            type: integer\n        model:\n          type: string\n          description: >-\n            The name of the model whose tokenizer will be used to\n            detokenize the input tokens.\n          example: command-r-plus\n    DetokenizeResponse:\n      type: object\n      properties:\n        text:\n          type: string\n          description: >-\n\
  \            The text string resulting from detokenizing the input token IDs.\n        meta:\n          type: object\n          description: >-\n            Metadata about the API request.\n          properties:\n            api_version:\n              type: object\n              properties:\n                version:\n                  type: string\n                  description: >-\n                    The API version used for the request.\n    Error:\n      type: object\n      properties:\n        message:\n          type: string\n          description: >-\n            A human-readable error message describing what went wrong.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-detokenize-api-openapi.yml
tags:
- Artificial Intelligence
- Natural Language Processing
- Text Processing
- Tokenization
---
