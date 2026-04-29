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
source_yaml: "aid: apache-httpd:apache-httpd-status-api\nname: Apache HTTP Server Status API\ndescription: Status and monitoring API for Apache HTTP Server (httpd) provided by mod_status, exposing\n  server metrics, worker state, and load balancer information via HTTP endpoints.\nhumanURL: https://httpd.apache.org/docs/current/mod/mod_status.html\nbaseURL: http://localhost:80\ntags:\n- Balancer\n- Metrics\n- Monitoring\n- REST\n- Status\nproperties:\n- type: Documentation\n  url: https://httpd.apache.org/docs/current/mod/mod_status.html\n- type: OpenAPI\n  url: openapi/apache-httpd-status-openapi.yml\n- type: JSONSchema\n  url: json-schema/httpd-serverstatus-schema.json\n- type: JSON-LD\n  url: json-ld/apache-httpd-status-context.jsonld\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apache-httpd/refs/heads/main/apis.yml
tags:
- Balancer
- Metrics
- Monitoring
- REST
- Status
---
