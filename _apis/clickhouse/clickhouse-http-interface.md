---
aid: clickhouse:clickhouse-http-interface
baseURL: http://localhost:8123
description: HTTP interface (default port 8123, HTTPS 8443) for executing SQL queries against ClickHouse. Supports SELECT via GET, mutations via POST, multiple output formats (JSON, CSV, XML, TabSeparated), and authentication via HTTP Basic, URL parameters, or X-ClickHouse-User/X-ClickHouse-Key headers. Helper paths include /ping and /replicas_status.
humanURL: https://clickhouse.com/docs/en/interfaces/http
image: ''
layout: api
name: ClickHouse HTTP Interface
properties:
- type: Documentation
  url: https://clickhouse.com/docs/en/interfaces/http
provider_name: ClickHouse
provider_slug: clickhouse
slug: clickhouse-http-interface
tags:
- Database
- HTTP
- SQL
---
