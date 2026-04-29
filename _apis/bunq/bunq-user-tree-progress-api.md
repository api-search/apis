---
aid: bunq:bunq-user-tree-progress-api
baseURL: ''
description: The Bunq User Tree Progress API is a tool that allows users to track their progress and activity within the Bunq app. By providing access to a comprehensive overview of their financial behavior and transactions, users can gain valuable insights into their spending habits, saving goals, and overall financial health. This API also enables users to set personalized goals and benchmarks, monitor their progress, and receive real-time notifications to help them stay on track.
humanURL: ''
image: ''
layout: api
name: Bunq User Tree Progress API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-tree-progress-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-user-tree-progress-api
source_filename: bunq-user-userid-tree-progress-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq user/{userID}/tree-progress'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths:\n  /user/{userID}/tree-progress:\n    get:\n      tags:\n        - User\n      summary: ''\n      operationId: List_all_TreeProgress_for_User\n      description: See how many trees this user has planted.\n      parameters:\n        - in: path\n          name: userID\n          description: ''\n          required: true\n   \
  \       schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: See how many trees this user has planted.\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/TreeProgressListing'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n\
  \            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: User\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-tree-progress-openapi-original.yml
tags:
- Progress
- Trees
- Users
---
