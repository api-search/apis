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
source_yaml: "aid: apache-nutch:apache-nutch-rest-api\nname: Apache Nutch REST API\ndescription: REST API for managing Apache Nutch crawl jobs, configurations, seed URL lists, database queries\n  (CrawlDB and FetchDB), and data readers. Supports full crawl lifecycle management including inject,\n  generate, fetch, parse, updatedb, and index operations. Secured via HTTP Basic Authentication.\nhumanURL: https://cwiki.apache.org/confluence/display/NUTCH/Nutch+1.X+REST+API\nbaseURL: http://localhost:8081\ntags:\n- REST\n- Crawl Management\n- Job Management\n- Configuration\nproperties:\n- type: Documentation\n  url: https://cwiki.apache.org/confluence/display/NUTCH/Nutch+1.X+REST+API\n- type: OpenAPI\n  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/openapi/apache-nutch-openapi.yaml\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/json-schema/apache-nutch-nutch-config-schema.json\n  title: Nutch Config\
  \ Schema\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/json-schema/apache-nutch-job-config-schema.json\n  title: Job Config Schema\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/json-schema/apache-nutch-job-info-schema.json\n  title: Job Info Schema\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/json-schema/apache-nutch-nutch-server-info-schema.json\n  title: Server Info Schema\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/json-schema/apache-nutch-seed-list-schema.json\n  title: Seed List Schema\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/json-schema/apache-nutch-db-query-schema.json\n  title: DB Query Schema\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apache-nutch/refs/heads/main/apis.yml
tags:
- REST
- Crawl Management
- Job Management
- Configuration
---
