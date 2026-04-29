---
aid: bunq:bunq-installation-api
baseURL: ''
description: The Bunq Installation API is a tool that allows developers to easily integrate Bunq's banking services into their applications. It provides access to features such as creating users, setting up accounts, and linking payment methods. By using this API, developers can streamline the process of incorporating Bunq's services into their products, saving time and effort.
humanURL: ''
image: ''
layout: api
name: Bunq Installation API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-installation--openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-installation-api
source_filename: bunq-installation--openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq installation/'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas:\n    InstallationRead:\n      type: object\n      properties:\n        id:\n          type: integer\n          description: >-\n            The id of the Installation as created on the server. You can use\n            this id to request the server's public key again.\n          readOnly: true\n          writeOnly: false\npaths:\n  /installation/{itemId}:\n\
  \    get:\n      tags:\n        - Installation\n      summary: ''\n      operationId: READ_Installation\n      description: >-\n        You must have an active session to make this call. This call is used to\n        check whether the Id you provide is the Id of your current installation\n        or not.\n      parameters:\n        - in: path\n          name: itemId\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: >-\n            Installation is used to tell\
  \ the server about the public key of your\n            key pair. The server uses this key to verify your subsequent calls,\n            which need to be signed with your own private key. Additionally, you\n            can use the token you get from an Installation to authenticate the\n            registration of a new device.\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/InstallationRead'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\n  /installation/{installationID}/server-public-key:\n    get:\n      tags:\n        - Installation\n      summary: ''\n\
  \      operationId: List_all_ServerPublicKey_for_Installation\n      description: Show the ServerPublicKey for this Installation.\n      parameters:\n        - in: path\n          name: installationID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: >-\n            Using /installation/_/server-public-key you can request the\n            ServerPublicKey again. This is done by referring to the id of the\n            Installation.\n          content:\n         \
  \   application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/InstallationServerPublicKeyListing'\n          headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: Installation\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-installation--openapi-original.yml
tags:
- Installations
- Items
- Keys
- Public
- Servers
---
