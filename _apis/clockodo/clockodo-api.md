---
aid: clockodo:clockodo-api
baseURL: https://my.clockodo.com/api
description: The Clockodo API is a REST interface at my.clockodo.com that lets developers automate time tracking and project management. v2 endpoints under /api/v2 cover entries, customers, projects, services, users, lump-sum services, and the stop-clock; legacy endpoints under /api cover absences and holiday quotas. Calls authenticate with X-ClockodoApiUser plus X-ClockodoApiKey (or HTTP Basic with the same credentials) and identify the calling app via X-Clockodo-External-Application; responses are JSON.
humanURL: https://www.clockodo.com/en/api/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Clockodo API
properties:
- type: Documentation
  url: https://www.clockodo.com/en/api/
- type: Authentication
  url: https://www.clockodo.com/en/api/authentication/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/clockodo/refs/heads/main/openapi/clockodo-openapi.yml
provider_name: Clockodo
provider_slug: clockodo
slug: clockodo-api
source_yaml: "aid: clockodo:clockodo-api\nname: Clockodo API\ntags:\n- Absence Management\n- Billing\n- Project Management\n- Stop Clock\n- Time Tracking\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://www.clockodo.com/en/api/\nbaseURL: https://my.clockodo.com/api\nproperties:\n- url: https://www.clockodo.com/en/api/\n  type: Documentation\n- url: https://www.clockodo.com/en/api/authentication/\n  type: Authentication\n- url: openapi/clockodo-openapi.yml\n  type: OpenAPI\ndescription: The Clockodo API is a REST interface at my.clockodo.com that lets developers automate time\n  tracking and project management. v2 endpoints under /api/v2 cover entries, customers, projects, services,\n  users, lump-sum services, and the stop-clock; legacy endpoints under /api cover absences and holiday\n  quotas. Calls authenticate with X-ClockodoApiUser plus X-ClockodoApiKey (or HTTP Basic with the same\n  credentials) and identify the calling app via X-Clockodo-External-Application;\
  \ responses are JSON.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/clockodo/refs/heads/main/apis.yml
tags:
- Absence Management
- Billing
- Project Management
- Stop Clock
- Time Tracking
---
