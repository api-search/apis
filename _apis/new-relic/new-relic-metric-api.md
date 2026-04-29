---
aid: new-relic:new-relic-metric-api
baseURL: https://metric-api.newrelic.com/metric/v1
description: The New Relic Metric API is an HTTP endpoint for ingesting dimensional metric data directly into the New Relic platform. It accepts JSON payloads via POST requests and is the underlying API used by Telemetry SDKs and open source exporters such as Prometheus and DropWizard.
humanURL: https://docs.newrelic.com/docs/data-apis/ingest-apis/metric-api/introduction-metric-api/
image: https://newrelic.com/themes/custom/erno/assets/mediakit/new_relic_logo_horizontal.png
layout: api
name: New Relic Metric API
properties:
- type: Documentation
  url: https://docs.newrelic.com/docs/data-apis/ingest-apis/metric-api/introduction-metric-api/
- type: APIReference
  url: https://docs.newrelic.com/docs/data-apis/ingest-apis/metric-api/report-metrics-metric-api/
- type: Authentication
  url: https://docs.newrelic.com/docs/apis/intro-apis/new-relic-api-keys/
- type: RateLimits
  url: https://docs.newrelic.com/docs/data-apis/ingest-apis/metric-api/metric-api-limits-restricted-attributes/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/openapi/new-relic-metric-api-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/new-relic-metric-payload-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/metric-api-common-block-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/metric-api-summary-value-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/metric-api-metric-data-object-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/metric-api-metric-data-point-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/metric-api-metric-payload-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/metric-api-accepted-response-schema.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-ld/new-relic-metric-api-context.jsonld
provider_name: New Relic
provider_slug: new-relic
slug: new-relic-metric-api
source_yaml: "aid: new-relic:new-relic-metric-api\nname: New Relic Metric API\ndescription: The New Relic Metric API is an HTTP endpoint for ingesting dimensional metric data directly\n  into the New Relic platform. It accepts JSON payloads via POST requests and is the underlying API used\n  by Telemetry SDKs and open source exporters such as Prometheus and DropWizard.\nimage: https://newrelic.com/themes/custom/erno/assets/mediakit/new_relic_logo_horizontal.png\nhumanURL: https://docs.newrelic.com/docs/data-apis/ingest-apis/metric-api/introduction-metric-api/\nbaseURL: https://metric-api.newrelic.com/metric/v1\nproperties:\n- type: Documentation\n  url: https://docs.newrelic.com/docs/data-apis/ingest-apis/metric-api/introduction-metric-api/\n- type: APIReference\n  url: https://docs.newrelic.com/docs/data-apis/ingest-apis/metric-api/report-metrics-metric-api/\n- type: Authentication\n  url: https://docs.newrelic.com/docs/apis/intro-apis/new-relic-api-keys/\n- type: RateLimits\n  url: https://docs.newrelic.com/docs/data-apis/ingest-apis/metric-api/metric-api-limits-restricted-attributes/\n\
  - type: OpenAPI\n  url: openapi/new-relic-metric-api-openapi.yml\n- type: JSONSchema\n  url: json-schema/new-relic-metric-payload-schema.json\n- type: JSONSchema\n  url: json-schema/metric-api-common-block-schema.json\n- type: JSONSchema\n  url: json-schema/metric-api-summary-value-schema.json\n- type: JSONSchema\n  url: json-schema/metric-api-metric-data-object-schema.json\n- type: JSONSchema\n  url: json-schema/metric-api-metric-data-point-schema.json\n- type: JSONSchema\n  url: json-schema/metric-api-metric-payload-schema.json\n- type: JSONSchema\n  url: json-schema/metric-api-accepted-response-schema.json\n- type: JSONLD\n  url: json-ld/new-relic-metric-api-context.jsonld\ntags:\n- Ingest\n- Metrics\n- Monitoring\n- Telemetry\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/apis.yml
tags:
- Ingest
- Metrics
- Monitoring
- Telemetry
---
