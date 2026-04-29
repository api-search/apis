---
aid: cat:cat-digital-marketplace-api
baseURL: ''
description: Explore the Cat Digital API catalog, subscribe to APIs, and execute calls against the Cat Digital products. Coverage includes fleet and asset management, telematics (VisionLink), fuel and utilization data, hours/odometer events, and geofencing.
humanURL: https://digital.cat.com/api-catalog-overview
image: ''
layout: api
name: CAT Digital Marketplace API
properties:
- type: Documentation
  url: https://digital.cat.com/api-catalog-overview
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cat/refs/heads/main/openapi/cat-openapi.yml
- type: Portal
  url: https://digital.cat.com/
- type: ChangeLog
  url: https://digital.cat.com/release-notes-manager
provider_name: CAT
provider_slug: cat
slug: cat-digital-marketplace-api
source_filename: cat-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: CAT Caterpillar Telematics API\n  description: API for Caterpillar-to-dealer data transfer\n  version: 1.0.0\nservers:\n  - url: https://services.cat.com/telematics/iso15143\n    description: Production server\npaths:\n  /{pageNumber}:\n    get:\n      summary: CAT Get fleet snapshot\n      description: Provides a snapshot view of the fleet.\n      parameters:\n        - name: pageNumber\n          in: path\n          required: true\n          schema:\n            type: integer\n      responses:\n        '200':\n          description: Successful response\n  /equipment/makeModelSerial/{make}/{model}/{serialNumber}:\n    get:\n      summary: CAT Get equipment snapshot\n      description: Returns snapshot data for a single piece of equipment.\n      parameters:\n        - name: make\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: model\n          in: path\n          required: true\n   \
  \       schema:\n            type: string\n        - name: serialNumber\n          in: path\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Successful response\n      tags:\n        - Equipment\n  /equipment/makeModelSerial/{make}/{model}/{serialNumber}/faults/{startDateUTC}/{endDateUTC}/{pageNumber}:\n    get:\n      summary: CAT Get fault codes\n      description: Retrieves fault code time-series data for an asset.\n      parameters:\n        - name: make\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: model\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: serialNumber\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: startDateUTC\n          in: path\n          required: true\n          schema:\n            type: string\n        \
  \    format: date-time\n        - name: endDateUTC\n          in: path\n          required: true\n          schema:\n            type: string\n            format: date-time\n        - name: pageNumber\n          in: path\n          required: true\n          schema:\n            type: integer\n      responses:\n        '200':\n          description: Successful response\n      tags:\n        - Equipment\n  /equipment/makeModelSerial/{make}/{model}/{serialNumber}/locations/{startDateUTC}/{endDateUTC}/{pageNumber}:\n    get:\n      summary: Get location data\n      description: Returns location details of a given asset.\n      parameters:\n        - name: make\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: model\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: serialNumber\n          in: path\n          required: true\n          schema:\n            type: string\n       \
  \ - name: startDateUTC\n          in: path\n          required: true\n          schema:\n            type: string\n            format: date-time\n        - name: endDateUTC\n          in: path\n          required: true\n          schema:\n            type: string\n            format: date-time\n        - name: pageNumber\n          in: path\n          required: true\n          schema:\n            type: integer\n      responses:\n        '200':\n          description: Successful response\n      tags:\n        - Equipment\n  /equipment/makeModelSerial/{make}/{model}/{serialNumber}/switchStatus/{startDateUTC}/{endDateUTC}/{pageNumber}:\n    get:\n      summary: CAT Get switch status\n      description: Retrieves switch status data of an asset.\n      parameters:\n        - name: make\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: model\n          in: path\n          required: true\n          schema:\n            type: string\n\
  \        - name: serialNumber\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: startDateUTC\n          in: path\n          required: true\n          schema:\n            type: string\n            format: date-time\n        - name: endDateUTC\n          in: path\n          required: true\n          schema:\n            type: string\n            format: date-time\n        - name: pageNumber\n          in: path\n          required: true\n          schema:\n            type: integer\n      responses:\n        '200':\n          description: Successful response\n      tags:\n        - Equipment\n  /equipment/makeModelSerial/{make}/{model}/{serialNumber}/fuelRemainingRatio/{startDateUTC}/{endDateUTC}/{pageNumber}:\n    get:\n      summary: CAT Get fuel remaining ratio\n      description: Retrieves the fuel remaining ratio details of an asset.\n      parameters:\n        - name: make\n          in: path\n          required: true\n    \
  \      schema:\n            type: string\n        - name: model\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: serialNumber\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: startDateUTC\n          in: path\n          required: true\n          schema:\n            type: string\n            format: date-time\n        - name: endDateUTC\n          in: path\n          required: true\n          schema:\n            type: string\n            format: date-time\n        - name: pageNumber\n          in: path\n          required: true\n          schema:\n            type: integer\n      responses:\n        '200':\n          description: Successful response\n      tags:\n        - Equipment\ntags:\n  - name: Equipment\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cat/refs/heads/main/openapi/cat-openapi.yml
tags:
- Assets
- Construction
- Heavy Equipment
- Telematics
- VisionLink
---
