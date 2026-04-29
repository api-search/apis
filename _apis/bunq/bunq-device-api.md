---
aid: bunq:bunq-device-api
baseURL: ''
description: Bunq Device API is a tool that allows developers to access and interact with Bunq's financial services on various devices, such as smartphones, tablets, and computers. With this API, developers can create applications that enable users to manage their money, make payments, transfer funds, and more, all from the convenience of their preferred device.
humanURL: ''
image: ''
layout: api
name: Bunq Device API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-device--openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-device-api
source_filename: bunq-device--openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq device/'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas:\n    DeviceRead:\n      type: object\n      properties:\n        DeviceServer:\n          type: object\n          description: ''\n          readOnly: true\n          writeOnly: false\n          $ref: '#/components/schemas/DeviceServer'\npaths:\n  /device/{itemId}:\n    get:\n      tags:\n        - Device\n      summary: ''\n      operationId: READ_Device\n\
  \      description: Get a single Device. A Device is either a DevicePhone or a DeviceServer.\n      parameters:\n        - in: path\n          name: itemId\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: >-\n            Used to get a Device or a listing of Devices. Creating a\n            DeviceServer should happen via /device-server\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/DeviceRead'\n\
  \          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: Device\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-device--openapi-original.yml
tags:
- Device
- Items
---
