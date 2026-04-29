---
aid: bunq:bunq-attachment-content-api
baseURL: ''
description: The Bunq Attachment Content API is a tool that allows developers to easily manage and access content attached to transactions within the Bunq banking system. This API enables users to retrieve, update, and delete various types of attachments, such as receipts, invoices, and images, linked to their transactions.
humanURL: https://doc.bunq.com/#/content
image: ''
layout: api
name: Bunq Attachment Content API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-attachment-public-attachment-publicuuid-content-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-attachment-content-api
source_filename: bunq-attachment-public-attachment-publicuuid-content-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq attachment-public/{attachment-publicUUID}/content'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths:\n  /attachment-public/{attachment-publicUUID}/content:\n    get:\n      tags:\n        - Attachment Public\n      summary: ''\n      operationId: List_all_Content_for_AttachmentPublic\n      description: Get the raw content of a specific attachment.\n      parameters:\n        - in: path\n          name:\
  \ attachment-publicUUID\n          description: ''\n          required: true\n          schema:\n            type: string\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: >-\n            Fetch the raw content of a public attachment with given ID. The raw\n            content is the binary representation of a file, without any JSON\n            wrapping.\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/AttachmentPublicContentListing'\n\
  \          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: Attachment Public\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-attachment-public-attachment-publicuuid-content-openapi-original.yml
tags:
- Attachments
- Content
- Public
---
