---
aid: agco:agcommand-api
baseURL: https://api.agcocorp.com
description: The AGCO AgCommand API provides approved third-party developers and service providers with access to machine telemetry data from AGCO equipment. The API enables farming application developers to build management dashboards and mobile apps that access real-time machine data including location, performance metrics, and diagnostic information from AGCO Connect-ready machines. AGCO uses JSON API profiles for standardized filtering, search, and change events.
humanURL: https://get.agcoconnect.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: AGCO AgCommand API
properties:
- type: Portal
  url: https://get.agcoconnect.com/
- type: Documentation
  url: https://github.com/agco/agco-json-api-profiles
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/agco/refs/heads/main/openapi/agco-agcommand-api-openapi.yml
provider_name: agco
provider_slug: agco
slug: agcommand-api
source_filename: agco-agcommand-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: AGCO AgCommand API\n  description: >-\n    The AGCO AgCommand API provides approved third-party developers with access\n    to machine telemetry data from AGCO equipment. Enables building management\n    dashboards and mobile apps that access real-time machine data including\n    location, performance metrics, and diagnostics.\n  version: '1.0'\nservers:\n- url: https://api.agcocorp.com\ntags:\n- name: Locations\n  description: Access machine location and tracking data.\n- name: Machines\n  description: Access machine information and status.\n- name: Telemetry\n  description: Retrieve machine telemetry and sensor data.\npaths:\n  /machines:\n    get:\n      operationId: listMachines\n      summary: AGCO List Machines\n      description: >-\n        Retrieves a list of AGCO machines associated with the authenticated\n        account, including machine type, model, and connectivity status.\n      tags:\n      - Machines\n      responses:\n    \
  \    '200':\n          description: Success\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /machines/{machineId}/telemetry:\n    get:\n      operationId: getMachineTelemetry\n      summary: AGCO Get Machine Telemetry\n      description: >-\n        Retrieves telemetry data for a specific machine including engine hours,\n        fuel level, speed, and diagnostic codes.\n      tags:\n      - Telemetry\n      parameters:\n      - name: machineId\n        in: path\n        required: true\n        description: The unique machine identifier.\n        schema:\n          type: string\n        example: example_value\n      - name: startDate\n        in: query\n        description: Filter telemetry from this date.\n        schema:\n          type: string\n          format: date\n        example: '2025-03-15'\n      - name: endDate\n        in: query\n        description: Filter telemetry up to this date.\n        schema:\n          type: string\n          format:\
  \ date\n        example: '2025-03-15'\n      responses:\n        '200':\n          description: Success\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /machines/{machineId}/locations:\n    get:\n      operationId: getMachineLocations\n      summary: AGCO Get Machine Locations\n      description: >-\n        Retrieves location history for a specific machine including GPS\n        coordinates and timestamps.\n      tags:\n      - Locations\n      parameters:\n      - name: machineId\n        in: path\n        required: true\n        description: The unique machine identifier.\n        schema:\n          type: string\n        example: example_value\n      responses:\n        '200':\n          description: Success\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: header\n      name: Authorization\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/agco/refs/heads/main/openapi/agco-agcommand-api-openapi.yml
tags:
- Agriculture
- Farm Equipment
- IoT
- Precision Farming
- Telematics
---
