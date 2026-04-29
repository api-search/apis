---
aid: zendesk:job-statuses
baseURL: https://{subdomain}.zendesk.com
description: Zendesk Job Statuses is the mechanism and API resource that tracks long-running, asynchronous tasks kicked off in Zendesksuch as bulk ticket updates, user or organization imports, and other create/update many operations. Instead of waiting for a synchronous response, these endpoints return a job ID that you can poll to see whether the work is queued, in progress, or completed, along with progress counts, result details, and any errors.
humanURL: https://developer.zendesk.com/api-reference/ticketing/ticket-management/job_statuses/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Job Statuses
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/ticket-management/job_statuses/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/job-statuses-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: job-statuses
source_filename: job-statuses-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Job Statuses\n  description: Needs a description.\npaths:\n  /api/v2/job_statuses:\n    get:\n      operationId: ListJobStatuses\n      tags:\n        - Job Statuses\n      summary: Zendesk Get  Api V2 Job_statuses\n      description: >\n        Shows the statuses for background jobs. Statuses are sorted first by\n        completion date and then by creation date in descending order.\n\n\n        #### Allowed For:\n\n\n        * Agents\n\n\n        #### Pagination\n\n\n        * Cursor pagination\n\n\n        See [Pagination](/api-reference/introduction/pagination/).\n      responses:\n        '200':\n          description: Success Response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/JobStatusesResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/JobStatusesResponseExample'\n  /api/v2/job_statuses/{job_status_id}:\n\
  \    parameters:\n      - $ref: '#/components/parameters/JobStatusId'\n    get:\n      operationId: ShowJobStatus\n      tags:\n        - Job Statuses\n      summary: Zendesk Get  Api V2 Job_statuses Job_status_id\n      description: |\n        Shows the status of a background job.\n\n        #### Allowed For:\n\n        * Agents\n      responses:\n        '200':\n          description: Success Response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/JobStatusResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/ShowJobStatusResponseExample'\n  /api/v2/job_statuses/show_many:\n    get:\n      operationId: ShowManyJobStatuses\n      tags:\n        - Job Statuses\n      summary: Zendesk Get  Api V2 Job_statuses Show_many\n      description: |\n        Accepts a comma-separated list of job status ids.\n\n        #### Allowed For:\n\n        * Agents\n      parameters:\n\
  \        - name: ids\n          in: query\n          description: Comma-separated list of job status ids.\n          required: true\n          schema:\n            type: string\n          example: 8b726e606741012ffc2d782bcb7848fe,e7665094164c498781ebe4c8db6d2af5\n      responses:\n        '200':\n          description: Success Response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/JobStatusesResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/JobStatusesResponseExample'\ncomponents:\n  schemas:\n    JobStatusesResponse:\n      type: object\n      properties:\n        job_statuses:\n          type: array\n          items:\n            $ref: '#/components/schemas/JobStatusObject'\n      required:\n        - job_statuses\n    JobStatusResponse:\n      type: object\n      properties:\n        job_status:\n          $ref: '#/components/schemas/JobStatusObject'\n\
  tags:\n  - name: Job Statuses\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/job-statuses-openapi-original.yml
tags:
- Jobs
- Statuses
---
