---
aid: new-relic:new-relic-trace-api
baseURL: https://trace-api.newrelic.com/trace/v1
description: The New Relic Trace API allows distributed tracing data to be sent directly to New Relic in either New Relic format or Zipkin JSON v2 format. It is used by Telemetry SDKs, open source integrations, and custom tracing implementations that need to report span data without a full APM agent.
humanURL: https://docs.newrelic.com/docs/distributed-tracing/trace-api/introduction-trace-api/
image: https://newrelic.com/themes/custom/erno/assets/mediakit/new_relic_logo_horizontal.png
layout: api
name: New Relic Trace API
properties:
- type: Documentation
  url: https://docs.newrelic.com/docs/distributed-tracing/trace-api/introduction-trace-api/
- type: APIReference
  url: https://docs.newrelic.com/docs/distributed-tracing/trace-api/trace-api-general-requirements-limits/
- type: Authentication
  url: https://docs.newrelic.com/docs/apis/intro-apis/new-relic-api-keys/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/openapi/new-relic-trace-api-openapi.yml
- type: RateLimits
  url: https://docs.newrelic.com/docs/distributed-tracing/trace-api/trace-api-general-requirements-limits/
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/trace-api-new-relic-trace-payload-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/trace-api-accepted-response-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/trace-api-common-block-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/trace-api-zipkin-span-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/trace-api-span-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/trace-api-zipkin-trace-payload-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-schema/trace-api-span-batch-schema.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/json-ld/new-relic-trace-api-context.jsonld
provider_name: New Relic
provider_slug: new-relic
slug: new-relic-trace-api
source_yaml: "aid: new-relic:new-relic-trace-api\nname: New Relic Trace API\ndescription: The New Relic Trace API allows distributed tracing data to be sent directly to New Relic\n  in either New Relic format or Zipkin JSON v2 format. It is used by Telemetry SDKs, open source integrations,\n  and custom tracing implementations that need to report span data without a full APM agent.\nimage: https://newrelic.com/themes/custom/erno/assets/mediakit/new_relic_logo_horizontal.png\nhumanURL: https://docs.newrelic.com/docs/distributed-tracing/trace-api/introduction-trace-api/\nbaseURL: https://trace-api.newrelic.com/trace/v1\nproperties:\n- type: Documentation\n  url: https://docs.newrelic.com/docs/distributed-tracing/trace-api/introduction-trace-api/\n- type: APIReference\n  url: https://docs.newrelic.com/docs/distributed-tracing/trace-api/trace-api-general-requirements-limits/\n- type: Authentication\n  url: https://docs.newrelic.com/docs/apis/intro-apis/new-relic-api-keys/\n- type: OpenAPI\n\
  \  url: openapi/new-relic-trace-api-openapi.yml\n- type: RateLimits\n  url: https://docs.newrelic.com/docs/distributed-tracing/trace-api/trace-api-general-requirements-limits/\n- type: JSONSchema\n  url: json-schema/trace-api-new-relic-trace-payload-schema.json\n- type: JSONSchema\n  url: json-schema/trace-api-accepted-response-schema.json\n- type: JSONSchema\n  url: json-schema/trace-api-common-block-schema.json\n- type: JSONSchema\n  url: json-schema/trace-api-zipkin-span-schema.json\n- type: JSONSchema\n  url: json-schema/trace-api-span-schema.json\n- type: JSONSchema\n  url: json-schema/trace-api-zipkin-trace-payload-schema.json\n- type: JSONSchema\n  url: json-schema/trace-api-span-batch-schema.json\n- type: JSONLD\n  url: json-ld/new-relic-trace-api-context.jsonld\ntags:\n- Distributed Tracing\n- Ingest\n- Telemetry\n- Traces\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/apis.yml
tags:
- Distributed Tracing
- Ingest
- Telemetry
- Traces
---
