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
source_yaml: "aid: apache-ofbiz:apache-ofbiz-rest-api\nname: Apache OFBiz REST API\ndescription: REST API plugin for Apache OFBiz that exposes any exported OFBiz service as a RESTful endpoint.\n  Clients authenticate via HTTP Basic Auth to obtain a JWT token, then invoke services via GET (with URL-encoded\n  JSON parameters) or POST (with JSON request body). Swagger UI is available at /docs/swagger-ui.html\n  when the plugin is installed.\nhumanURL: https://github.com/apache/ofbiz-plugins/tree/trunk/rest-api\nbaseURL: https://localhost:8443/rest\ntags:\n- REST\n- JWT\n- Service Engine\n- ERP\nproperties:\n- type: Documentation\n  url: https://github.com/apache/ofbiz-plugins/blob/trunk/rest-api/src/docs/asciidoc/rest-api.adoc\n- type: OpenAPI\n  url: https://raw.githubusercontent.com/api-evangelist/apache-ofbiz/refs/heads/main/openapi/apache-ofbiz-rest-api-openapi.yaml\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-ofbiz/refs/heads/main/json-schema/apache-ofbiz-token-response-schema.json\n\
  \  title: Token Response Schema\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-ofbiz/refs/heads/main/json-schema/apache-ofbiz-service-entry-schema.json\n  title: Service Entry Schema\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-ofbiz/refs/heads/main/json-schema/apache-ofbiz-service-response-schema.json\n  title: Service Response Schema\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apache-ofbiz/refs/heads/main/apis.yml
tags:
- REST
- JWT
- Service Engine
- ERP
---
