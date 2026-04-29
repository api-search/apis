---
aid: amplitude:export-api
baseURL: https://amplitude.com
description: The Amplitude Export API enables bulk export of raw event data for a given project within a specified date range. Results are returned as zipped archives of JSON files containing complete event records with timestamps, user properties, device information, and attribution data. This API is commonly used for data warehousing, offline analysis, and feeding event data into external processing pipelines.
humanURL: https://amplitude.com/docs/apis/analytics/export
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Amplitude Export API
properties:
- type: Documentation
  url: https://amplitude.com/docs/apis/analytics/export
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-export-api-openapi.yml
provider_name: Amplitude
provider_slug: amplitude
slug: export-api
source_filename: amplitude-export-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Amplitude Export API\n  description: >-\n    The Amplitude Export API enables bulk export of raw event data for a\n    given project within a specified date range. Results are returned as\n    zipped archives of JSON files containing complete event records with\n    timestamps, user properties, device information, and attribution data.\n    This API is commonly used for data warehousing, offline analysis, and\n    feeding event data into external processing pipelines.\n  version: '2'\n  contact:\n    name: Amplitude Support\n    url: https://amplitude.com/contact\n  termsOfService: https://amplitude.com/terms\nexternalDocs:\n  description: Amplitude Export API Documentation\n  url: https://amplitude.com/docs/apis/analytics/export\nservers:\n- url: https://amplitude.com\n  description: Amplitude Production Server\ntags:\n- name: Export\n  description: Raw event data export operations\nsecurity:\n- basicAuth: []\npaths:\n  /api/2/export:\n    get:\n\
  \      operationId: exportEvents\n      summary: Amplitude Export Raw Event Data\n      description: >-\n        Export raw event data for the specified date range as a zipped archive\n        of JSON files. The maximum queryable period is 365 days and the\n        maximum response size is 4 GB. Data is available for export at a\n        minimum within 2 hours of server ingestion. Dates older than 30 days\n        before the current date may not be available.\n      tags:\n      - Export\n      parameters:\n      - name: start\n        in: query\n        required: true\n        description: >-\n          The start date and hour in YYYYMMDDTHH format, for example\n          20220101T00. For multi-day exports, the format YYYYMMDD is also\n          accepted.\n        schema:\n          type: string\n          pattern: '^\\d{8}(T\\d{2})?$'\n      - name: end\n        in: query\n        required: true\n        description: >-\n          The end date and hour in YYYYMMDDTHH format, for example\n\
  \          20220101T23. For multi-day exports, the format YYYYMMDD is also\n          accepted.\n        schema:\n          type: string\n          pattern: '^\\d{8}(T\\d{2})?$'\n      responses:\n        '200':\n          description: Success - returns a zipped archive of JSON event files\n          content:\n            application/zip:\n              schema:\n                type: string\n                format: binary\n        '400':\n          description: >-\n            Bad request - the exported data exceeds the 4 GB size limit\n        '401':\n          description: Unauthorized - invalid or missing credentials\n        '404':\n          description: >-\n            No data found for the requested date range\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n      description: >-\n        Use your Amplitude API key as the username and your secret key as the\n    \
  \    password. Encode them as base64 in the format api_key:secret_key.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-export-api-openapi.yml
tags:
- Analytics
- Data
- Events
- Export
---
