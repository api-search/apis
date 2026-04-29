---
aid: air-quality-programmatic-apis:air-quality-programmatic-apis
baseURL: ''
description: Real-time and forecast air quality data from 11,000+ monitoring stations globally. Returns AQI measurements for PM2.5, PM10, NO2, CO, SO2, and ozone pollutants by city, station, geographic coordinates, or IP geolocation. Includes weather data and 3-8 day air quality forecasts.
humanURL: https://aqicn.org/api/
image: ''
layout: api
name: AQICN Real-Time Air Quality API
properties:
- type: Documentation
  url: https://aqicn.org/api/
- title: JSON API Reference
  type: APIReference
  url: https://aqicn.org/json-api/doc/
- title: Map Tile API
  type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/air-quality-programmatic-apis/refs/heads/main/openapi/air-quality-programmatic-apis-openapi.yml
- title: API Token Request
  type: Authentication
  url: https://aqicn.org/data-platform/token/
provider_name: Air Quality Programmatic APIs
provider_slug: air-quality-programmatic-apis
slug: air-quality-programmatic-apis
source_filename: air-quality-programmatic-apis-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Air Quality Programmatic APIs Real-time Air Quality Tile API\n  description: API providing real-time air quality data as map tiles.\n  version: 1.0.0\nservers:\n- url: https://tiles.aqicn.org/tiles\n  description: Production server\npaths:\n  /{aqi}/{z}/{x}/{y}.png:\n    get:\n      summary: Air Quality Programmatic APIs Get Air Quality Tile\n      description: >-\n        Retrieves a tile image representing air quality data for a specific\n        location and zoom level.\n      parameters:\n      - name: aqi\n        in: path\n        required: true\n        description: Type of air quality marker to display\n        schema:\n          type: string\n          enum:\n          - usepa-aqi\n          - usepa-pm25\n          - usepa-10\n          - usepa-o3\n          - usepa-no2\n          - usepa-so2\n          - usepa-co\n          - asean-pm10\n      - name: z\n        in: path\n        required: true\n        description: Zoom level of the\
  \ tile\n        schema:\n          type: integer\n      - name: x\n        in: path\n        required: true\n        description: X coordinate of the tile\n        schema:\n          type: integer\n      - name: 'y'\n        in: path\n        required: true\n        description: Y coordinate of the tile\n        schema:\n          type: integer\n      - name: token\n        in: query\n        required: true\n        description: API token for authentication\n        schema:\n          type: string\n      responses:\n        '200':\n          description: Tile image retrieved successfully\n          content:\n            image/png: {}\n        '400':\n          description: Bad request (invalid parameters)\n        '403':\n          description: Unauthorized (invalid or missing token)\n        '503':\n          description: Service unavailable (due to maintenance or high traffic)\n      security:\n      - ApiKeyAuth: []\ncomponents:\n  securitySchemes:\n    ApiKeyAuth:\n      type: apiKey\n\
  \      in: query\n      name: token\n      description: API key for authentication\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/air-quality-programmatic-apis/refs/heads/main/openapi/air-quality-programmatic-apis-openapi.yml
tags:
- Air Quality
- AQI
- PM2.5
- EPA
- Environment
- Public Health
- Real-Time
- Open Data
---
