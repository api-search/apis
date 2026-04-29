---
aid: alphabet:google-cloud-api
baseURL: https://cloud.google.com
description: The Google Cloud API provides programmatic access to Google Cloud Platform services including compute, storage, networking, machine learning, and data analytics. Developers can provision resources, manage infrastructure, and integrate GCP services into their applications.
humanURL: https://cloud.google.com/apis/docs/overview
image: ''
layout: api
name: Google Cloud API
properties:
- type: Documentation
  url: https://cloud.google.com/apis/docs/overview
- type: Portal
  url: https://cloud.google.com/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alphabet/refs/heads/main/openapi/alphabet-google-cloud-api-openapi.yml
provider_name: Alphabet
provider_slug: alphabet
slug: google-cloud-api
source_filename: alphabet-google-cloud-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Google Cloud API\n  description: >-\n    The Google Cloud API provides programmatic access to Google Cloud Platform services including compute, storage, networking, machine learning, and data analytics. Developers can provision resources, manage infrastructure, and integrate GCP services into their applications.\n  version: '1.0'\n  contact:\n    name: Alphabet Developer Support\n    url: https://cloud.google.com/apis/docs/overview\nexternalDocs:\n  description: Documentation\n  url: https://cloud.google.com/apis/docs/overview\nservers:\n  - url: https://cloud.google.com/apis\n    description: Production\ntags:\n  - name: Cloud\n    description: Cloud operations\nsecurity:\n  - bearerAuth: []\npaths:\n  /status:\n    get:\n      operationId: getStatus\n      summary: Get API status\n      description: >-\n        Returns the current status of the API.\n      tags:\n        - Cloud\n      responses:\n        '200':\n          description: Success\n\
  \          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  status:\n                    type: string\n                  version:\n                    type: string\n        '401':\n          description: Unauthorized\n        '429':\n          description: Too many requests\ncomponents:\n  securitySchemes:\n    bearerAuth:\n      type: http\n      scheme: bearer\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/alphabet/refs/heads/main/openapi/alphabet-google-cloud-api-openapi.yml
tags:
- Cloud
- Compute
- Machine Learning
- Storage
---
