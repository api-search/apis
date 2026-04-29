---
aid: zendesk:incremental
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Incremental API lets you export only the records that have changed since a specific point in time, making it easy to keep external systems in sync without repeatedly pulling full datasets. It supports core objects such as tickets, users, organizations, and ticket events, returning results in chronological order along with a checkpoint (an end_time or a cursor) you store and use on your next request to continue exactly where you left off.
humanURL: https://developer.zendesk.com/api-reference/ticketing/ticket-management/incremental_exports/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Incremental API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/ticket-management/incremental_exports/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/incremental-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: incremental
source_yaml: "aid: zendesk:incremental\nname: Zendesk Incremental API\ntags:\n- Incremental\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://{subdomain}.zendesk.com\nhumanURL: https://developer.zendesk.com/api-reference/ticketing/ticket-management/incremental_exports/\nproperties:\n- url: https://developer.zendesk.com/api-reference/ticketing/ticket-management/incremental_exports/\n  type: Documentation\n- url: openapi/incremental-openapi-original.yml\n  type: OpenAPI\ndescription: The Zendesk Incremental API lets you export only the records that have changed since a specific\n  point in time, making it easy to keep external systems in sync without repeatedly pulling full datasets.\n  It supports core objects such as tickets, users, organizations, and ticket events, returning results\n  in chronological order along with a checkpoint (an end_time or a cursor) you store and use on your next\n  request to continue exactly where you left off.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/apis.yml
tags:
- Incremental
---
