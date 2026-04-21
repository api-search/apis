---
aid: apache-nutch:apache-nutch-rest-api
baseURL: http://localhost:8081
description: REST API for managing Apache Nutch crawl jobs, configurations, seed URL lists, database queries (CrawlDB and FetchDB), and data readers. Supports full crawl lifecycle management including inject, generate, fetch, parse, updatedb, and index operations. Secured via HTTP Basic Authentication.
humanURL: https://cwiki.apache.org/confluence/display/NUTCH/Nutch+1.X+REST+API
image: ''
layout: api
name: Apache Nutch REST API
properties:
- type: Documentation
  url: https://cwiki.apache.org/confluence/display/NUTCH/Nutch+1.X+REST+API
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/openapi/apache-nutch-openapi.yaml
- title: Nutch Config Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/json-schema/apache-nutch-nutch-config-schema.json
- title: Job Config Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/json-schema/apache-nutch-job-config-schema.json
- title: Job Info Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/json-schema/apache-nutch-job-info-schema.json
- title: Server Info Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/json-schema/apache-nutch-nutch-server-info-schema.json
- title: Seed List Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/json-schema/apache-nutch-seed-list-schema.json
- title: DB Query Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/json-schema/apache-nutch-db-query-schema.json
provider_name: Apache Nutch
provider_slug: apache-nutch
slug: apache-nutch-rest-api
tags:
- REST
- Crawl Management
- Job Management
- Configuration
---
