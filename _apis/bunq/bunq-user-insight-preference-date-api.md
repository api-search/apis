---
aid: bunq:bunq-user-insight-preference-date-api
baseURL: ''
description: The Bunq User Insight Preference Date API is a tool that allows users to access and manipulate their personal data preferences within the Bunq app. With this API, users can customize their preferences and settings to tailor their banking experience to their individual needs. This includes setting preferences for notifications, alerts, and other relevant information that the user may want to receive.
humanURL: ''
image: ''
layout: api
name: Bunq User Insight Preference Date API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-insight-preference-date-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-user-insight-preference-date-api
source_filename: bunq-user-userid-insight-preference-date-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq user/{userID}/insight-preference-date'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths:\n  /user/{userID}/insight-preference-date:\n    get:\n      tags:\n        - User\n      summary: ''\n      operationId: List_all_InsightPreferenceDate_for_User\n      description: Used to allow users to set insight/budget preferences.\n      parameters:\n        - in: path\n          name: userID\n          description:\
  \ ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: Used to allow users to set insight/budget preferences.\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/InsightPreferenceDateListing'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n      \
  \        $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: User\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-insight-preference-date-openapi-original.yml
tags:
- Dates
- Insights
- Preferences
- Users
---
