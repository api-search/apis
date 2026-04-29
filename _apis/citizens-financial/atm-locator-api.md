---
aid: citizens-financial:atm-locator-api
baseURL: https://api.citizensbank.com
description: The Citizens Bank ATM Locator API enables users to locate all Citizens Bank ATMs throughout the USA. The API supports queries by zip code, street address, or latitude and longitude coordinates, returning ATM location details including hours of operation and whether the location is a standalone ATM or part of another entity.
humanURL: https://developer.citizensbank.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Citizens Bank ATM Locator API
properties:
- type: Documentation
  url: https://developer.citizensbank.com/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citizens-financial/refs/heads/main/openapi/citizens-bank-atm-locator-api-openapi.yml
provider_name: Citizens Financial
provider_slug: citizens-financial
slug: atm-locator-api
source_filename: citizens-bank-atm-locator-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Citizens Bank ATM Locator API\n  description: >-\n    The Citizens Bank ATM Locator API enables users to locate all Citizens\n    Bank ATMs throughout the USA. The API supports queries by zip code,\n    street address, or latitude and longitude coordinates, returning ATM\n    location details including hours of operation and whether the location\n    is a standalone ATM or part of another entity.\n  version: '1.0'\n  contact:\n    name: Citizens Bank Developer Support\n    url: https://developer.citizensbank.com/support\nexternalDocs:\n  description: Citizens Bank API Developer Portal\n  url: https://developer.citizensbank.com/\nservers:\n  - url: https://api.citizensbank.com\n    description: Production\n  - url: https://sandboxapi.citizensbank.com\n    description: Sandbox\ntags:\n  - name: ATM Locations\n    description: Search and retrieve ATM location data\npaths:\n  /atms:\n    get:\n      operationId: searchATMs\n      summary: Search\
  \ ATM locations\n      description: >-\n        Searches for Citizens Bank ATM locations by zip code, street\n        address, or geographic coordinates. Returns location details\n        including hours and facility type.\n      tags:\n        - ATM Locations\n      parameters:\n        - name: zipCode\n          in: query\n          schema:\n            type: string\n          description: ZIP code to search near\n        - name: address\n          in: query\n          schema:\n            type: string\n          description: Street address to search near\n        - name: latitude\n          in: query\n          schema:\n            type: number\n            format: double\n          description: Latitude coordinate\n        - name: longitude\n          in: query\n          schema:\n            type: number\n            format: double\n          description: Longitude coordinate\n        - name: radius\n          in: query\n          schema:\n            type: number\n          description:\
  \ Search radius in miles\n        - name: limit\n          in: query\n          schema:\n            type: integer\n          description: Maximum number of results to return\n      responses:\n        '200':\n          description: Successful response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/ATMList'\n        '400':\n          description: Bad request\ncomponents:\n  schemas:\n    ATMList:\n      type: object\n      properties:\n        atms:\n          type: array\n          items:\n            $ref: '#/components/schemas/ATM'\n        totalCount:\n          type: integer\n    ATM:\n      type: object\n      properties:\n        id:\n          type: string\n          description: Unique ATM identifier\n        name:\n          type: string\n          description: ATM location name\n        address:\n          type: object\n          properties:\n            street:\n              type: string\n            city:\n\
  \              type: string\n            state:\n              type: string\n            zipCode:\n              type: string\n        latitude:\n          type: number\n          format: double\n        longitude:\n          type: number\n          format: double\n        hoursOfOperation:\n          type: string\n          description: Operating hours description\n        locationType:\n          type: string\n          description: Standalone ATM or part of another entity\n        facilities:\n          type: array\n          items:\n            type: string\n          description: Available services at the ATM\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/citizens-financial/refs/heads/main/openapi/citizens-bank-atm-locator-api-openapi.yml
tags:
- ATMs
- Banking
- Geolocation
- Locations
---
