---
aid: bunq:bunq-device-server-api
baseURL: ''
description: The Bunq Device Server API is a platform that allows developers to easily integrate and communicate with Bunq's banking services. This API enables users to securely access their accounts, make payments, and retrieve transaction information all through a simple and efficient interface.
humanURL: ''
image: ''
layout: api
name: Bunq Device Server API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-device-server--openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-device-server-api
source_filename: bunq-device-server--openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq device-server/'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas:\n    DeviceServerRead:\n      type: object\n      properties:\n        id:\n          type: integer\n          description: The id of the DeviceServer as created on the server.\n          readOnly: true\n          writeOnly: false\n        created:\n          type: string\n          description: The timestamp of the DeviceServer's creation.\n    \
  \      readOnly: true\n          writeOnly: false\n        updated:\n          type: string\n          description: The timestamp of the DeviceServer's last update.\n          readOnly: true\n          writeOnly: false\n        description:\n          type: string\n          description: The description of the DeviceServer.\n          readOnly: true\n          writeOnly: false\n        ip:\n          type: string\n          description: The ip address which was used to create the DeviceServer.\n          readOnly: true\n          writeOnly: false\n        status:\n          type: string\n          description: >-\n            The status of the DeviceServer. Can be ACTIVE, BLOCKED,\n            NEEDS_CONFIRMATION or OBSOLETE.\n          readOnly: true\n          writeOnly: false\npaths:\n  /device-server/{itemId}:\n    get:\n      tags:\n        - Device Server\n      summary: ''\n      operationId: READ_DeviceServer\n      description: Get one of your DeviceServers.\n      parameters:\n\
  \        - in: path\n          name: itemId\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: >-\n            After having created an Installation you can now create a\n            DeviceServer. A DeviceServer is needed to do a login call with\n            session-server.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/DeviceServerRead'\n          headers:\n            X-Bunq-Client-Response-Id:\n\
  \              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: Device Server\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-device-server--openapi-original.yml
tags:
- Device
- Items
- Servers
---
