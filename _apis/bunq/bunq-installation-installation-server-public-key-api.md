---
aid: bunq:bunq-installation-installation-server-public-key-api
baseURL: ''
description: The Bunq Installation Installation Server Public Key API allows users to securely register and authenticate their devices with the Bunq installation server. By generating a unique public key for each device, users can securely communicate with the server, ensuring that their data remains private and protected. This API streamlines the process of setting up a new device and provides a secure method for users to access their Bunq accounts.
humanURL: ''
image: ''
layout: api
name: Bunq Installation Installation Server Public Key API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-installation-installationid-server-public-key-openapi-original.yml
- type: Documentation
  url: https://doc.bunq.com/
provider_name: Bunq
provider_slug: bunq
slug: bunq-installation-installation-server-public-key-api
source_filename: bunq-installation-installationid-server-public-key-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.0\ninfo:\n  title: 'Bunq installation/{installationID}/server-public-key'\n  description: Needs description.\n  termsOfService: http://bunq.com/terms-api/\n  contact:\n    name: bunq Developer Support\n    url: http://bunq.com/developer\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0.html\n  version: '1.0'\nservers:\n  - url: https://public-api.sandbox.bunq.com/{basePath}\n    description: Sandbox server\n    variables:\n      basePath:\n        default: v1\n  - url: https://api.bunq.com/{basePath}\n    description: Production server\n    variables:\n      basePath:\n        default: v1\ncomponents:\n  schemas: {}\npaths:\n  /installation/{installationID}/server-public-key:\n    get:\n      tags:\n        - Installation\n      summary: ''\n      operationId: List_all_ServerPublicKey_for_Installation\n      description: Show the ServerPublicKey for this Installation.\n      parameters:\n        - in: path\n          name:\
  \ installationID\n          description: ''\n          required: true\n          schema:\n            type: integer\n        - $ref: '#/components/parameters/Cache-Control'\n        - $ref: '#/components/parameters/User-Agent'\n        - $ref: '#/components/parameters/X-Bunq-Language'\n        - $ref: '#/components/parameters/X-Bunq-Region'\n        - $ref: '#/components/parameters/X-Bunq-Client-Request-Id'\n        - $ref: '#/components/parameters/X-Bunq-Geolocation'\n        - $ref: '#/components/parameters/X-Bunq-Client-Authentication'\n      responses:\n        '200':\n          description: >-\n            Using /installation/_/server-public-key you can request the\n            ServerPublicKey again. This is done by referring to the id of the\n            Installation.\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/InstallationServerPublicKeyListing'\n   \
  \       headers:\n            X-Bunq-Client-Response-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Response-Id'\n            X-Bunq-Client-Request-Id:\n              $ref: '#/components/headers/X-Bunq-Client-Request-Id'\n            X-Bunq-Server-Signature:\n              $ref: '#/components/headers/X-Bunq-Server-Signature'\n        '400':\n          $ref: '#/components/responses/GenericError'\ntags:\n  - name: Installation\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bunq/refs/heads/main/openapi/bunq-installation-installationid-server-public-key-openapi-original.yml
tags:
- Installations
- Keys
- Public
- Servers
---
