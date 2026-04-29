---
aid: charter-communications:bryte-iq-api
baseURL: https://api.charter.com
description: Bryte IQ is a Network-as-a-Service (NaaS) API platform from Charter Communications and CableLabs that provides developers with secure, privacy-friendly access to connected device and network capabilities. It is built on the Linux Foundation CAMARA project.
humanURL: https://corporate.charter.com/newsroom/charter-and-cablelabs-launch-bryte-iq-network-as-a-service-platform
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Charter Communications Bryte IQ API
properties:
- type: Documentation
  url: https://corporate.charter.com/newsroom/charter-and-cablelabs-launch-bryte-iq-network-as-a-service-platform
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/charter-communications/refs/heads/main/openapi/charter-communications-bryte-iq-api-openapi.yml
- type: CAMARA
  url: https://camaraproject.org/
provider_name: Charter Communications
provider_slug: charter-communications
slug: bryte-iq-api
source_filename: charter-communications-bryte-iq-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Charter Communications Bryte IQ API\n  description: >-\n    Bryte IQ is a Network-as-a-Service (NaaS) API platform launched by Charter\n    Communications and CableLabs, providing secure API access to network\n    capabilities based on the CAMARA project.\n  version: 1.0.0\n  contact:\n    name: Charter Communications\n    url: https://corporate.charter.com/\nservers:\n  - url: https://api.charter.com\n    description: Production\npaths:\n  /network/devices:\n    get:\n      operationId: getConnectedDevices\n      summary: Get Connected Devices\n      description: Retrieve a list of connected devices on the network.\n      tags:\n        - Devices\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ConnectedDeviceList'\n  /network/status:\n    get:\n      operationId: getNetworkStatus\n      summary:\
  \ Get Network Status\n      description: Retrieve current network status and health.\n      tags:\n        - Network\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/NetworkStatus'\ntags:\n  - name: Devices\n    description: Connected device operations\n  - name: Network\n    description: Network status operations\ncomponents:\n  schemas:\n    ConnectedDevice:\n      type: object\n      properties:\n        id:\n          type: string\n        name:\n          type: string\n        type:\n          type: string\n        status:\n          type: string\n        ipAddress:\n          type: string\n    ConnectedDeviceList:\n      type: object\n      properties:\n        devices:\n          type: array\n          items:\n            $ref: '#/components/schemas/ConnectedDevice'\n    NetworkStatus:\n      type: object\n      properties:\n       \
  \ status:\n          type: string\n        uptime:\n          type: number\n        bandwidth:\n          type: object\n          properties:\n            download:\n              type: number\n            upload:\n              type: number\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/charter-communications/refs/heads/main/openapi/charter-communications-bryte-iq-api-openapi.yml
tags:
- CAMARA
- NaaS
- Network as a Service
- Telecommunications
---
