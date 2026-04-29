---
aid: bunq:bunq-avatar-api
baseURL: ''
description: The Bunq Avatar API is a tool that allows users to easily add personalized avatars to their Bunq accounts. By utilizing this API, individuals can create unique and customizable avatars that represent their identity within the Bunq banking platform. This feature enhances the user experience by adding a personal touch to their accounts, making it easier to recognize their profile and engage with other users.
humanURL: https://doc.bunq.com/#/avatar
image: ''
layout: api
name: Bunq Avatar API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-avatar--openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-avatar-api
source_filename: bunq-avatar--openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq avatar/'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas:\n    AvatarRead:\n      type: object\n      properties:\n        uuid:\n          type: string\n          description: The UUID of the created avatar.\n          readOnly: true\n          writeOnly: false\n        image:\n          type: array\n          description: The content type of the image.\n          readOnly: true\n          writeOnly: false\n \
  \         items:\n            $ref: '#/components/schemas/Image'\npaths:\n  /avatar/{itemId}:\n    get:\n      tags:\n        - Avatar\n      summary: ''\n      operationId: READ_Avatar\n      description: >-\n        Avatars are public images used to represent you or your company. Avatars\n        are used to represent users, monetary accounts and cash registers.\n        Avatars cannot be deleted, only replaced. Avatars can be updated after\n        uploading the image you would like to use through AttachmentPublic.\n        Using the attachment_public_uuid which is returned you can update your\n        Avatar. Avatars used for cash registers and company accounts will be\n        reviewed by bunq.\n      parameters:\n        - in: path\n          name: itemId\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n\
  \        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: >-\n            Avatars are public images used to represent you or your company.\n            Avatars are used to represent users, monetary accounts and cash\n            registers. Avatars cannot be deleted, only replaced. Avatars can be\n            updated after uploading the image you would like to use through\n            AttachmentPublic. Using the attachment_public_uuid which is returned\n            you can update your Avatar. Avatars used for cash registers and\n            company accounts will be reviewed by bunq.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/AvatarRead'\n          headers:\n\
  \            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: Avatar\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-avatar--openapi-original.yml
tags:
- Avatars
- Items
---
