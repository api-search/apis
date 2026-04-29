---
aid: peoplesoft:search-framework-api
baseURL: https://{hostname}:{port}/psft/api/search/v1
description: Search indexing and query capabilities powered by OpenSearch (previously Elasticsearch) for full-text search, analytics dashboards, and PeopleSoft Insights.
humanURL: https://docs.oracle.com/cd/E52319_01/infoportal/search.html
image: https://www.oracle.com/a/ocom/img/cb71-psft-logo.jpg
layout: api
name: PeopleSoft Search Framework API
properties:
- type: Documentation
  url: https://docs.oracle.com/cd/E52319_01/infoportal/search.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/search-framework.yml
provider_name: PeopleSoft
provider_slug: peoplesoft
slug: search-framework-api
source_filename: search-framework.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: PeopleSoft Search Framework API\n  description: Search indexing and query capabilities powered by OpenSearch (previously Elasticsearch) for full-text search, analytics dashboards, and PeopleSoft Insights.\n  version: 1.0.0\n  contact:\n    name: Oracle Support\n    email: support@oracle.com\n    url: https://support.oracle.com\n  license:\n    name: Proprietary\n    url: https://www.oracle.com/contracts/\nservers:\n- url: https://{hostname}:{port}/psft/api/search/v1\n  description: PeopleSoft Instance\n  variables:\n    hostname:\n      description: PeopleSoft server hostname\n      default: localhost\n    port:\n      description: PeopleSoft server port\n      default: '8000'\nexternalDocs:\n  description: PeopleSoft Search Framework Documentation\n  url: https://docs.oracle.com/cd/E52319_01/infoportal/search.html\ntags:\n- name: Search\n  description: Search and indexing operations\npaths:\n  /search:\n    get:\n      summary: PeopleSoft Search\
  \ Content\n      description: Execute a full-text search across PeopleSoft indexed content.\n      operationId: searchContent\n      tags:\n      - Search\n      security:\n      - basicAuth: []\n      parameters:\n      - name: q\n        in: query\n        required: true\n        description: Search query string\n        schema:\n          type: string\n        example: example_value\n      - name: category\n        in: query\n        description: Search category to filter results\n        schema:\n          type: string\n        example: example_value\n      - name: maxResults\n        in: query\n        description: Maximum number of results to return\n        schema:\n          type: integer\n        example: 42\n      responses:\n        '200':\n          description: Search results\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  results:\n                    type: array\n    \
  \                items:\n                      type: object\n                  totalCount:\n                    type: integer\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n  /index:\n    post:\n      summary: PeopleSoft Trigger Index Build\n      description: Trigger a search index build or incremental update.\n      operationId: triggerIndexBuild\n      tags:\n      - Search\n      security:\n      - basicAuth: []\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                indexName:\n                  type: string\n                  description: Name of the search index\n                buildType:\n                  type: string\n                  enum:\n                  - full\n                  - incremental\n                  description: Type of index build\n      responses:\n\
  \        '202':\n          description: Index build initiated\n        '401':\n          description: Unauthorized\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  securitySchemes:\n    basicAuth:\n      type: http\n      scheme: basic\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/peoplesoft/refs/heads/main/openapi/search-framework.yml
tags:
- Analytics
- Insights
- OpenSearch
- Search
---
