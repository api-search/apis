---
aid: apache-druid:apache-druid-rest-api
baseURL: ''
description: Druid exposes REST APIs for Druid SQL (POST /druid/v2/sql), native JSON queries (POST /druid/v2), batch and streaming data ingestion tasks, supervisor management for Kafka/Kinesis ingestion, data segment management, coordinator and overlord operations, process status, and dynamic configuration. A JDBC driver is also available for SQL access via JDBC clients.
humanURL: https://druid.apache.org/docs/latest/api-reference/
image: ''
layout: api
name: Apache Druid REST API
properties:
- type: Documentation
  url: https://druid.apache.org/docs/latest/api-reference/
- type: GettingStarted
  url: https://druid.apache.org/docs/latest/tutorials/tutorial-batch-hadoop
- type: APIReference
  url: https://druid.apache.org/docs/latest/api-reference/
- type: GitHubRepository
  url: https://github.com/apache/druid
- title: Kubernetes Operator
  type: Tools
  url: https://github.com/apache/druid-operator
- title: JDBC Driver (Maven)
  type: SDK
  url: https://mvnrepository.com/artifact/org.apache.druid/druid-sql
- title: pydruid Python Client
  type: SDK
  url: https://pypi.org/project/pydruid/
- title: Ingestion Task
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-schema/apache-druid-ingestion-task-schema.json
- title: Sql Query Request
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-schema/apache-druid-sql-query-request-schema.json
- title: Sql Query Response
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-schema/apache-druid-sql-query-response-schema.json
- title: Supervisor
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-schema/apache-druid-supervisor-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-structure/apache-druid-ingestion-task-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-structure/apache-druid-sql-query-request-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-structure/apache-druid-sql-query-response-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-structure/apache-druid-supervisor-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-ld/apache-druid-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/examples/apache-druid-ingestion-task-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/examples/apache-druid-sql-query-request-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/examples/apache-druid-sql-query-response-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/examples/apache-druid-supervisor-example.json
provider_name: Apache Druid
provider_slug: apache-druid
slug: apache-druid-rest-api
source_yaml: "aid: apache-druid:apache-druid-rest-api\nname: Apache Druid REST API\ndescription: Druid exposes REST APIs for Druid SQL (POST /druid/v2/sql), native JSON queries (POST /druid/v2),\n  batch and streaming data ingestion tasks, supervisor management for Kafka/Kinesis ingestion, data segment\n  management, coordinator and overlord operations, process status, and dynamic configuration. A JDBC driver\n  is also available for SQL access via JDBC clients.\nhumanURL: https://druid.apache.org/docs/latest/api-reference/\ntags:\n- Analytics\n- Data Ingestion\n- Datasources\n- JSON Query\n- Kafka\n- OLAP\n- REST\n- SQL\n- Segments\n- Supervisors\nproperties:\n- type: Documentation\n  url: https://druid.apache.org/docs/latest/api-reference/\n- type: GettingStarted\n  url: https://druid.apache.org/docs/latest/tutorials/tutorial-batch-hadoop\n- type: APIReference\n  url: https://druid.apache.org/docs/latest/api-reference/\n- type: GitHubRepository\n  url: https://github.com/apache/druid\n\
  - type: Tools\n  url: https://github.com/apache/druid-operator\n  title: Kubernetes Operator\n- type: SDK\n  url: https://mvnrepository.com/artifact/org.apache.druid/druid-sql\n  title: JDBC Driver (Maven)\n- type: SDK\n  url: https://pypi.org/project/pydruid/\n  title: pydruid Python Client\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-schema/apache-druid-ingestion-task-schema.json\n  title: Ingestion Task\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-schema/apache-druid-sql-query-request-schema.json\n  title: Sql Query Request\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-schema/apache-druid-sql-query-response-schema.json\n  title: Sql Query Response\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-schema/apache-druid-supervisor-schema.json\n\
  \  title: Supervisor\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-structure/apache-druid-ingestion-task-structure.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-structure/apache-druid-sql-query-request-structure.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-structure/apache-druid-sql-query-response-structure.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-structure/apache-druid-supervisor-structure.json\n- type: JSONLD\n  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/json-ld/apache-druid-context.jsonld\n- type: Example\n  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/examples/apache-druid-ingestion-task-example.json\n- type: Example\n\
  \  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/examples/apache-druid-sql-query-request-example.json\n- type: Example\n  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/examples/apache-druid-sql-query-response-example.json\n- type: Example\n  url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/examples/apache-druid-supervisor-example.json\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apache-druid/refs/heads/main/apis.yml
tags:
- Analytics
- Data Ingestion
- Datasources
- JSON Query
- Kafka
- OLAP
- REST
- SQL
- Segments
- Supervisors
---
