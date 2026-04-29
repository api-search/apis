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
source_yaml: "aid: zendesk:job-statuses\nname: Zendesk Job Statuses\ntags:\n- Jobs\n- Statuses\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://{subdomain}.zendesk.com\nhumanURL: https://developer.zendesk.com/api-reference/ticketing/ticket-management/job_statuses/\nproperties:\n- url: https://developer.zendesk.com/api-reference/ticketing/ticket-management/job_statuses/\n  type: Documentation\n- url: openapi/job-statuses-openapi-original.yml\n  type: OpenAPI\ndescription: Zendesk Job Statuses is the mechanism and API resource that tracks long-running, asynchronous\n  tasks kicked off in Zendesksuch as bulk ticket updates, user or organization imports, and other create/update\n  many operations. Instead of waiting for a synchronous response, these endpoints return a job ID that\n  you can poll to see whether the work is queued, in progress, or completed, along with progress counts,\n  result details, and any errors.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/apis.yml
tags:
- Jobs
- Statuses
---
