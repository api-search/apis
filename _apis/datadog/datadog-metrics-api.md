---
aid: datadog:datadog-metrics-api
baseURL: https://api.datadoghq.com
description: The Metrics API allows you to post metrics data to be graphed on Datadog dashboards, query metrics from any time period as timeseries or scalar values, and modify tag configurations for metrics. It also supports viewing tags and volumes for metrics.
humanURL: https://docs.datadoghq.com/api/latest/metrics/
image: https://imgix.datadoghq.com/img/dd_logo_n_70x75.png
layout: api
name: Datadog Metrics API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-metrics-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/json-schema/datadog-metric-schema.json
- type: Documentation
  url: https://docs.datadoghq.com/api/latest/metrics/
- type: Reference
  url: https://docs.datadoghq.com/metrics/
provider_name: Datadog
provider_slug: datadog
slug: datadog-metrics-api
source_yaml: "aid: datadog:datadog-metrics-api\nname: Datadog Metrics API\ntags:\n- Metrics\n- Monitoring\n- Timeseries\nhumanURL: https://docs.datadoghq.com/api/latest/metrics/\nbaseURL: https://api.datadoghq.com\nimage: https://imgix.datadoghq.com/img/dd_logo_n_70x75.png\nproperties:\n- url: openapi/datadog-metrics-openapi.yml\n  type: OpenAPI\n- url: json-schema/datadog-metric-schema.json\n  type: JSONSchema\n- url: https://docs.datadoghq.com/api/latest/metrics/\n  type: Documentation\n- url: https://docs.datadoghq.com/metrics/\n  type: Reference\ndescription: The Metrics API allows you to post metrics data to be graphed on Datadog dashboards, query\n  metrics from any time period as timeseries or scalar values, and modify tag configurations for metrics.\n  It also supports viewing tags and volumes for metrics.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/apis.yml
tags:
- Metrics
- Monitoring
- Timeseries
---
