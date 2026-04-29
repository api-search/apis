---
aid: apache-http:apache-http-client-api
baseURL: ''
description: Java HTTP client library API for executing HTTP requests with connection pooling, async I/O, TLS/SSL, authentication, cookie management, and proxy support via Apache HttpComponents 5.x.
humanURL: https://hc.apache.org/httpcomponents-client-5.3.x/
image: ''
layout: api
name: Apache HttpComponents Client API
properties:
- type: Documentation
  url: https://hc.apache.org/httpcomponents-client-5.3.x/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apache-http/refs/heads/main/openapi/apache-http-client-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-http/refs/heads/main/json-schema/http-client-httprequest-schema.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/apache-http/refs/heads/main/json-ld/apache-http-client-context.jsonld
provider_name: Apache HttpComponents
provider_slug: apache-http
slug: apache-http-client-api
source_filename: apache-http-client-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Apache HttpComponents Client API\n  version: 5.3.0\n  description: Reference API specification for Apache HttpComponents HTTP client library,\n    covering request execution, connection management, authentication, and proxy configuration.\n  contact:\n    email: dev@hc.apache.org\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0\nservers:\n- url: https://api.example.com\n  description: Example target server for HttpComponents client\ntags:\n- name: Requests\n  description: HTTP request execution operations\n- name: Configuration\n  description: Client configuration operations\npaths:\n  /execute:\n    post:\n      operationId: executeRequest\n      summary: Apache HttpComponents Execute Request\n      description: Execute an HTTP request using the Apache HttpComponents client\n        with the provided request configuration.\n      tags:\n      - Requests\n      requestBody:\n        required: true\n    \
  \    content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/HttpRequest'\n      responses:\n        '200':\n          description: Request executed successfully\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/HttpResponse'\n  /configure/connection:\n    put:\n      operationId: configureConnection\n      summary: Apache HttpComponents Configure Connection\n      description: Update connection pool and timeout configuration for the HTTP client.\n      tags:\n      - Configuration\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/ConnectionConfig'\n      responses:\n        '200':\n          description: Configuration updated\n  /configure/proxy:\n    put:\n      operationId: configureProxy\n      summary: Apache HttpComponents Configure Proxy\n      description: Configure\
  \ an HTTP proxy for outbound requests from the HttpComponents\n        client.\n      tags:\n      - Configuration\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              $ref: '#/components/schemas/ProxyConfig'\n      responses:\n        '200':\n          description: Proxy configured\ncomponents:\n  schemas:\n    HttpRequest:\n      type: object\n      description: HTTP request configuration for Apache HttpComponents client\n      properties:\n        method:\n          type: string\n          description: HTTP method\n          example: GET\n        uri:\n          type: string\n          description: Request URI\n          example: https://api.example.com/data\n        headers:\n          type: object\n          description: Request headers as key-value pairs\n          example:\n            Accept: application/json\n            Authorization: Bearer token\n        body:\n          type: string\n          description:\
  \ Request body content\n          example: '{\"key\": \"value\"}'\n        contentType:\n          type: string\n          description: Content-Type header value\n          example: application/json\n    HttpResponse:\n      type: object\n      description: HTTP response from Apache HttpComponents client execution\n      properties:\n        statusCode:\n          type: integer\n          description: HTTP response status code\n          example: 200\n        reasonPhrase:\n          type: string\n          description: HTTP reason phrase\n          example: OK\n        headers:\n          type: object\n          description: Response headers as key-value pairs\n          example:\n            Content-Type: application/json\n        body:\n          type: string\n          description: Response body content\n          example: '{\"result\": \"ok\"}'\n        contentType:\n          type: string\n          description: Content-Type of the response body\n          example: application/json\n\
  \    ConnectionConfig:\n      type: object\n      description: Connection configuration for Apache HttpComponents client\n      properties:\n        connectTimeout:\n          type: integer\n          description: Connection timeout in milliseconds\n          example: 5000\n        socketTimeout:\n          type: integer\n          description: Socket read timeout in milliseconds\n          example: 30000\n        maxConnections:\n          type: integer\n          description: Maximum total connections in pool\n          example: 200\n        maxConnectionsPerRoute:\n          type: integer\n          description: Maximum connections per route\n          example: 20\n        keepAliveTimeout:\n          type: integer\n          description: Keep-alive timeout in milliseconds\n          example: 60000\n    ProxyConfig:\n      type: object\n      description: HTTP proxy configuration for Apache HttpComponents client\n      properties:\n        host:\n          type: string\n          description:\
  \ Proxy hostname\n          example: proxy.example.com\n        port:\n          type: integer\n          description: Proxy port\n          example: 8080\n        scheme:\n          type: string\n          description: Proxy scheme (http or https)\n          example: http\n        username:\n          type: string\n          description: Proxy authentication username\n          example: proxyuser\n        password:\n          type: string\n          description: Proxy authentication password\n          example: ''\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apache-http/refs/heads/main/openapi/apache-http-client-openapi.yml
tags:
- Authentication
- Connection Pooling
- HTTP Client
- Java
- TLS
---
