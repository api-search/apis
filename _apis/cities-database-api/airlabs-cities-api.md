---
aid: cities-database-api:airlabs-cities-api
baseURL: https://airlabs.co/api/v9
description: The AirLabs Cities API exposes a single GET /cities endpoint that returns a list of cities filterable by IATA city_code, ISO 2 country_code, or comma-separated _fields. Free-tier responses include name, city_code, latitude, longitude, and country_code; paid tiers add UN/LOCODE, elevation, timezone, population, multilingual names, Wikipedia links, and SEO slugs. Authentication uses the api_key query parameter.
humanURL: https://airlabs.co/docs/cities
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: AirLabs Cities API
properties:
- type: Documentation
  url: https://airlabs.co/docs/cities
- type: API Reference
  url: https://airlabs.co/docs
- type: Authentication
  url: https://airlabs.co/account/api-key
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cities-database-api/refs/heads/main/openapi/cities-database-api-openapi.yml
provider_name: Cities Database API
provider_slug: cities-database-api
slug: airlabs-cities-api
source_filename: cities-database-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: AirLabs Cities Database API\n  version: '9'\n  summary: Reference dataset of global cities keyed by IATA metropolitan codes.\n  description: >-\n    The AirLabs Cities Database API returns a list of global cities filterable\n    by IATA city_code, ISO 2 country_code, or selected fields. City data\n    complements and extends the AirLabs airports dataset for travel search,\n    mapping, and geocoding experiences.\n  contact:\n    name: AirLabs Support\n    url: https://airlabs.co/contact\n  license:\n    name: AirLabs Terms of Service\n    url: https://airlabs.co/terms\nservers:\n  - url: https://airlabs.co/api/v9\n    description: AirLabs production API\nsecurity:\n  - apiKey: []\npaths:\n  /cities:\n    get:\n      operationId: listCities\n      summary: List cities\n      description: >-\n        Returns a list of cities, optionally filtered by IATA metropolitan\n        city_code, ISO 2 country_code, or restricted to a specified set of\n \
  \       fields.\n      tags:\n        - Cities\n      parameters:\n        - in: query\n          name: api_key\n          description: AirLabs API key from the account dashboard.\n          required: true\n          schema:\n            type: string\n        - in: query\n          name: city_code\n          description: IATA metropolitan city code (e.g. NYC, LON, PAR).\n          schema:\n            type: string\n        - in: query\n          name: country_code\n          description: ISO 2 country code (e.g. US, GB, FR).\n          schema:\n            type: string\n        - in: query\n          name: _fields\n          description: Comma-separated list of fields to include in the response.\n          schema:\n            type: string\n      responses:\n        '200':\n          description: An array of city objects.\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  request:\n   \
  \                 type: object\n                    properties:\n                      lang:\n                        type: string\n                      currency:\n                        type: string\n                      time:\n                        type: integer\n                      id:\n                        type: string\n                      server:\n                        type: string\n                  response:\n                    type: array\n                    items:\n                      $ref: '#/components/schemas/City'\n        '401':\n          description: Invalid or missing API key.\n        '429':\n          description: Rate limit exceeded.\ncomponents:\n  securitySchemes:\n    apiKey:\n      type: apiKey\n      in: query\n      name: api_key\n  schemas:\n    City:\n      type: object\n      properties:\n        name:\n          type: string\n          description: English name of the city.\n        city_code:\n          type: string\n          description:\
  \ IATA metropolitan area code.\n        un_code:\n          type: string\n          description: UN/LOCODE for the city.\n        slug:\n          type: string\n          description: SEO-friendly slug.\n        country_code:\n          type: string\n          description: ISO 2 country code.\n        lat:\n          type: number\n          format: float\n          description: Latitude in decimal degrees.\n        lng:\n          type: number\n          format: float\n          description: Longitude in decimal degrees.\n        elevation:\n          type: integer\n          description: Elevation in meters.\n        timezone:\n          type: string\n          description: IANA timezone identifier.\n        population:\n          type: integer\n          description: Population count.\n        wikipedia:\n          type: string\n          format: uri\n          description: Wikipedia article URL for the city.\n        names:\n          type: object\n          additionalProperties:\n\
  \            type: string\n          description: Multilingual city names keyed by ISO 639-1 language code.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cities-database-api/refs/heads/main/openapi/cities-database-api-openapi.yml
tags:
- Cities
- Geography
- IATA
- Reference Data
- Travel
---
