---
aid: apache-httpd:apache-httpd-status-api
baseURL: http://localhost:80
description: Status and monitoring API for Apache HTTP Server (httpd) provided by mod_status, exposing server metrics, worker state, and load balancer information via HTTP endpoints.
humanURL: https://httpd.apache.org/docs/current/mod/mod_status.html
image: ''
layout: api
name: Apache HTTP Server Status API
properties:
- type: Documentation
  url: https://httpd.apache.org/docs/current/mod/mod_status.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apache-httpd/refs/heads/main/openapi/apache-httpd-status-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-httpd/refs/heads/main/json-schema/httpd-serverstatus-schema.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/apache-httpd/refs/heads/main/json-ld/apache-httpd-status-context.jsonld
provider_name: Apache HTTP Server
provider_slug: apache-httpd
slug: apache-httpd-status-api
tags:
- Balancer
- Metrics
- Monitoring
- REST
- Status
---
