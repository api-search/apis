---
aid: apache-ofbiz:apache-ofbiz-rest-api
baseURL: https://localhost:8443/rest
description: REST API plugin for Apache OFBiz that exposes any exported OFBiz service as a RESTful endpoint. Clients authenticate via HTTP Basic Auth to obtain a JWT token, then invoke services via GET (with URL-encoded JSON parameters) or POST (with JSON request body). Swagger UI is available at /docs/swagger-ui.html when the plugin is installed.
humanURL: https://github.com/apache/ofbiz-plugins/tree/trunk/rest-api
image: ''
layout: api
name: Apache OFBiz REST API
properties:
- type: Documentation
  url: https://github.com/apache/ofbiz-plugins/blob/trunk/rest-api/src/docs/asciidoc/rest-api.adoc
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apache-ofbiz/refs/heads/main/openapi/apache-ofbiz-rest-api-openapi.yaml
- title: Token Response Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-ofbiz/refs/heads/main/json-schema/apache-ofbiz-token-response-schema.json
- title: Service Entry Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-ofbiz/refs/heads/main/json-schema/apache-ofbiz-service-entry-schema.json
- title: Service Response Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-ofbiz/refs/heads/main/json-schema/apache-ofbiz-service-response-schema.json
provider_name: Apache OFBiz
provider_slug: apache-ofbiz
slug: apache-ofbiz-rest-api
tags:
- REST
- JWT
- Service Engine
- ERP
---
