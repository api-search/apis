---
aid: bunq:bunq-user-schedule-api
baseURL: ''
description: The Bunq User Schedule API allows developers to create and manage scheduled transactions for Bunq users. This API enables users to set up automated payments, transfers, or other financial activities to occur at specified times and frequencies. With this functionality, users can easily plan and organize their finances, ensuring that important transactions are carried out on time without the need for manual intervention.
humanURL: ''
image: ''
layout: api
name: Bunq User Schedule API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-schedule-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-user-schedule-api
source_filename: bunq-user-userid-schedule-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq user/{userID}/schedule'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths:\n  /user/{userID}/schedule:\n    get:\n      tags:\n        - User\n      summary: ''\n      operationId: List_all_Schedule_for_User\n      description: >-\n        Get a collection of scheduled definition for all accessible monetary\n        accounts of the user. You can add the parameter type to filter the\n        response. When\n\
  \        type={SCHEDULE_DEFINITION_PAYMENT,SCHEDULE_DEFINITION_PAYMENT_BATCH} is\n        provided only schedule definition object that relate to these\n        definitions are returned.\n      parameters:\n        - in: path\n          name: userID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: view for reading the scheduled definitions.\n          content:\n            application/json:\n              schema:\n                type: array\n               \
  \ items:\n                  $ref: '#/components/schemas/ScheduleUserListing'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: User\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-schedule-openapi-original.yml
tags:
- Schedules
- Users
---
