---
aid: datadog:datadog-logs-api
baseURL: https://api.datadoghq.com
description: The Logs API allows you to search and send log events to the Datadog platform over HTTP. It supports querying and aggregating log data from the Log Management product.
humanURL: https://docs.datadoghq.com/api/latest/logs/
image: https://imgix.datadoghq.com/img/dd_logo_n_70x75.png
layout: api
name: Datadog Logs API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-logs-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/json-schema/datadog-log-event-schema.json
- type: Documentation
  url: https://docs.datadoghq.com/api/latest/logs/
- type: Reference
  url: https://docs.datadoghq.com/logs/
provider_name: Datadog
provider_slug: datadog
slug: datadog-logs-api
source_yaml: "aid: datadog:datadog-logs-api\nname: Datadog Logs API\ntags:\n- Log Management\n- Logs\n- Search\nhumanURL: https://docs.datadoghq.com/api/latest/logs/\nbaseURL: https://api.datadoghq.com\nimage: https://imgix.datadoghq.com/img/dd_logo_n_70x75.png\nproperties:\n- url: openapi/datadog-logs-openapi.yml\n  type: OpenAPI\n- url: json-schema/datadog-log-event-schema.json\n  type: JSONSchema\n- url: https://docs.datadoghq.com/api/latest/logs/\n  type: Documentation\n- url: https://docs.datadoghq.com/logs/\n  type: Reference\ndescription: The Logs API allows you to search and send log events to the Datadog platform over HTTP.\n  It supports querying and aggregating log data from the Log Management product.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/apis.yml
tags:
- Log Management
- Logs
- Search
---
