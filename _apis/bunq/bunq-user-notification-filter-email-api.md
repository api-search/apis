---
aid: bunq:bunq-user-notification-filter-email-api
baseURL: ''
description: Bunq User Notification Filter Email API is a tool that allows users to filter and customize the emails they receive from Bunq, a mobile banking app. This API enables users to set up specific criteria and rules to only receive notifications about certain transactions, account updates, or other relevant information. By using this API, users can tailor their email notifications to suit their preferences and ensure they only receive the most important and relevant updates from Bunq.
humanURL: ''
image: ''
layout: api
name: Bunq User Notification Filter Email API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-notification-filter-email-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-user-notification-filter-email-api
source_filename: bunq-user-userid-notification-filter-email-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq user/{userID}/notification-filter-email'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas:\n    NotificationFilterEmailCreate:\n      type: object\n      properties:\n        Id:\n          type: object\n          description: The id of the created item\n          readOnly: true\n          writeOnly: false\n          $ref: '#/components/schemas/BunqId'\npaths:\n  /user/{userID}/notification-filter-email:\n    post:\n\
  \      tags:\n        - User\n      summary: ''\n      operationId: CREATE_NotificationFilterEmail_for_User\n      description: Manage the email notification filters for a user.\n      parameters:\n        - in: path\n          name: userID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      requestBody:\n        description: ''\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/NotificationFilterEmail'\n      responses:\n      \
  \  '200':\n          description: Manage the email notification filters for a user.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/NotificationFilterEmailCreate'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\n    get:\n      tags:\n        - User\n      summary: ''\n      operationId: List_all_NotificationFilterEmail_for_User\n      description: Manage the email notification filters for a user.\n      parameters:\n        - in: path\n          name: userID\n          description: ''\n          required: true\n          schema:\n            type: integer\n\
  \        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: Manage the email notification filters for a user.\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/NotificationFilterEmailListing'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n\
  \              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: User\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-notification-filter-email-openapi-original.yml
tags:
- Emails
- Filter
- Notifications
- Users
---
