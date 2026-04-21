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
tags:
- REST
- Distributed Tracing
- Monitoring
- Observability
---
