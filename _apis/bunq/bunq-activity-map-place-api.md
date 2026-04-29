---
aid: bunq:bunq-activity-map-place-api
baseURL: https://public-api.sandbox.bunq.com/
description: The Bunq Activity Map Place API is a powerful tool that allows developers to easily integrate location-based information into their applications. With this API, users can access detailed information about various points of interest, such as restaurants, shops, and attractions, as well as real-time data on traffic and weather conditions.
humanURL: https://doc.bunq.com/#/activity-map-place-public
image: ''
layout: api
name: Bunq Activity Map Place API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-activity-map-place-public-itemid-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-activity-map-place-api
source_filename: bunq-activity-map-place-public-itemid-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq activity-map-place-public/{itemId}/'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths:\n  /activity-map-place-public/{itemId}:\n    get:\n      tags:\n        - Activity Map Place Public\n      summary: ''\n      operationId: READ_ActivityMapPlacePublic\n      description: Public endpoint for getting the place info.\n      parameters:\n        - in: path\n          name: itemId\n          description:\
  \ ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: Public endpoint for getting the place info.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ActivityMapPlacePublicRead'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n     \
  \       X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: Activity Map Place Public\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-activity-map-place-public-itemid-openapi-original.yml
tags: []
---
