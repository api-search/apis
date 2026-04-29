---
aid: bunq:bunq-user-feature-announcement-api
baseURL: ''
description: The Bunq User Feature Announcement API is a tool that allows developers to stay up-to-date with the latest features and updates released by Bunq, a mobile banking platform. With this API, developers can access information about new features, bug fixes, and enhancements as soon as they are announced. This enables them to integrate these updates into their own applications quickly and efficiently, ensuring that their users have access to the most current and innovative banking solutions.
humanURL: ''
image: ''
layout: api
name: Bunq User Feature Announcement API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-feature-announcement-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-user-feature-announcement-api
source_filename: bunq-user-userid-feature-announcement-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq user/{userID}/feature-announcement'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas:\n    FeatureAnnouncementRead:\n      type: object\n      properties:\n        avatar:\n          type: object\n          description: The Avatar of the event overview.\n          readOnly: true\n          writeOnly: false\n          $ref: '#/components/schemas/Avatar'\n        title:\n          type: string\n          description:\
  \ The event overview title of the feature display\n          readOnly: true\n          writeOnly: false\n        sub_title:\n          type: string\n          description: The event overview subtitle of the feature display\n          readOnly: true\n          writeOnly: false\n        type:\n          type: string\n          description: >-\n            The type of the feature announcement so apps can override with their\n            own stuff if desired\n          readOnly: true\n          writeOnly: false\npaths:\n  /user/{userID}/feature-announcement/{itemId}:\n    get:\n      tags:\n        - User\n      summary: ''\n      operationId: READ_FeatureAnnouncement_for_User\n      description: view for updating the feature display.\n      parameters:\n        - in: path\n          name: userID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - in: path\n          name: itemId\n          description: ''\n          required: true\n\
  \          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: view for updating the feature display.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/FeatureAnnouncementRead'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n      \
  \        $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: User\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-user-userid-feature-announcement-openapi-original.yml
tags:
- Announcement
- Feature
- Items
- Users
---
