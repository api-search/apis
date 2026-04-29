---
aid: apache-zipkin:apache-zipkin-api
baseURL: ''
description: The Zipkin REST API v2 provides endpoints for querying trace data, service names, span names, and dependencies. Key endpoints include GET /api/v2/services (list services), GET /api/v2/spans (list span names for a service), GET /api/v2/traces (search traces by service, span, tags, duration), GET /api/v2/trace/{traceId} (get a specific trace), and GET /api/v2/dependencies (service dependency graph). Span reporting uses POST /api/v2/spans for JSON format or POST /api/v2/spans for Thrift format.
humanURL: https://zipkin.io/zipkin-api/
image: ''
layout: api
name: Apache Zipkin REST API
properties:
- type: Documentation
  url: https://zipkin.io/zipkin-api/
- type: OpenAPI
  url: https://raw.githubusercontent.com/openzipkin/zipkin-api/master/zipkin2-api.yaml
provider_name: Apache Zipkin
provider_slug: apache-zipkin
slug: apache-zipkin-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: apache-zipkin:apache-zipkin-api\nname: Apache Zipkin REST API\ndescription: The Zipkin REST API v2 provides endpoints for querying trace data, service names, span names,\n  and dependencies. Key endpoints include GET /api/v2/services (list services), GET /api/v2/spans (list\n  span names for a service), GET /api/v2/traces (search traces by service, span, tags, duration), GET\n  /api/v2/trace/{traceId} (get a specific trace), and GET /api/v2/dependencies (service dependency graph).\n  Span reporting uses POST /api/v2/spans for JSON format or POST /api/v2/spans for Thrift format.\nhumanURL: https://zipkin.io/zipkin-api/\ntags:\n- REST\n- Distributed Tracing\n- Monitoring\n- Observability\nproperties:\n- type: Documentation\n  url: https://zipkin.io/zipkin-api/\n- type: OpenAPI\n  url: https://raw.githubusercontent.com/openzipkin/zipkin-api/master/zipkin2-api.yaml\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apache-zipkin/refs/heads/main/apis.yml
tags:
- REST
- Distributed Tracing
- Monitoring
- Observability
---
