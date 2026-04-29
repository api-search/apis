---
aid: asana:asana-jobs-api
baseURL: ''
description: Asana Jobs API is an application programming interface that allows developers to access and interact with job-related data and functionality within the Asana platform. This API enables users to programmatically create, retrieve, update, and delete job postings, as well as access information about job applicants, interviews, and job statuses.
humanURL: https://developers.asana.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Asana Jobs  API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/asana/refs/heads/main/openapi/asana-jobs-api-openapi.yml
- type: Documentation
  url: https://developers.asana.com/reference/rest-api-reference
provider_name: Asana
provider_slug: asana
slug: asana-jobs-api
source_filename: asana-jobs-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Asana Jobs API\n  description: >-\n    The Asana Jobs API allows users to access job records representing\n    asynchronous processes such as project or task duplication.\n  version: '1.0'\n  termsOfService: https://asana.com/terms\n  contact:\n    name: Asana Support\n    url: https://asana.com/support\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0\nservers:\n  - url: https://app.asana.com/api/1.0\n    description: Main endpoint.\nsecurity:\n  - personalAccessToken: []\n  - oauth2: []\ntags:\n  - name: Jobs\n    description: Track asynchronous operations like project or task duplication.\npaths:\n  /jobs/{job_gid}:\n    get:\n      summary: Asana Get a job by id\n      description: Returns the full record for a job.\n      operationId: getJob\n      tags:\n        - Jobs\n      parameters:\n        - name: job_gid\n          in: path\n          required: true\n          schema:\n            type: string\n\
  \          example: '12345'\n      responses:\n        '200':\n          description: Successfully retrieved the record for a single job.\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    $ref: '#/components/schemas/JobResponse'\n        '400':\n          description: Bad request.\n        '401':\n          description: Unauthorized.\n        '403':\n          description: Forbidden.\n        '404':\n          description: Not found.\n        '500':\n          description: Internal server error.\ncomponents:\n  securitySchemes:\n    personalAccessToken:\n      type: http\n      scheme: bearer\n    oauth2:\n      type: oauth2\n      flows:\n        authorizationCode:\n          authorizationUrl: https://app.asana.com/-/oauth_authorize\n          tokenUrl: https://app.asana.com/-/oauth_token\n          scopes:\n            default: Provides access to all endpoints\
  \ documented in the API reference.\n  schemas:\n    JobResponse:\n      type: object\n      properties:\n        gid:\n          type: string\n          readOnly: true\n          example: '12345'\n        resource_type:\n          type: string\n          readOnly: true\n          example: job\n        resource_subtype:\n          type: string\n          readOnly: true\n          example: duplicate_task\n        status:\n          type: string\n          readOnly: true\n          enum:\n            - not_started\n            - in_progress\n            - succeeded\n            - failed\n          example: in_progress\n        new_project:\n          type: object\n          nullable: true\n          properties:\n            gid:\n              type: string\n            resource_type:\n              type: string\n            name:\n              type: string\n        new_task:\n          type: object\n          nullable: true\n          properties:\n            gid:\n              type: string\n\
  \            resource_type:\n              type: string\n            name:\n              type: string\n        new_project_template:\n          type: object\n          nullable: true\n          properties:\n            gid:\n              type: string\n            resource_type:\n              type: string\n            name:\n              type: string\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/asana/refs/heads/main/openapi/asana-jobs-api-openapi.yml
tags: []
---
