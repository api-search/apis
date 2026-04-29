---
aid: apache-doris:apache-doris
baseURL: ''
description: Apache Doris provides a MySQL-compatible protocol for SQL queries, a REST API for cluster management and monitoring, Stream Load HTTP API for real-time bulk data ingestion, Routine Load for continuous Kafka ingestion, and connectors for Flink, Spark, and Kafka. An MCP server is also available for AI-assisted analytics.
humanURL: https://doris.apache.org/docs/dev/summary/basic-summary
image: ''
layout: api
name: Apache Doris
properties:
- type: Documentation
  url: https://doris.apache.org/docs/dev/summary/basic-summary
- type: GettingStarted
  url: https://doris.apache.org/docs/dev/install/
- type: APIReference
  url: https://doris.apache.org/docs/dev/admin-manual/http-actions/
- type: GitHubRepository
  url: https://github.com/apache/doris
- title: MCP Server
  type: Tools
  url: https://github.com/apache/doris-mcp-server
- title: Flink Connector
  type: SDK
  url: https://github.com/apache/doris-flink-connector
- title: Spark Connector
  type: SDK
  url: https://github.com/apache/doris-spark-connector
- title: Kafka Connector
  type: SDK
  url: https://github.com/apache/doris-kafka-connector
- title: Kubernetes Operator
  type: Tools
  url: https://github.com/apache/doris-operator
- title: Stream Loader CLI
  type: Tools
  url: https://github.com/apache/doris-streamloader
- title: Routine Load Job
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-schema/apache-doris-routine-load-job-schema.json
- title: Stream Load Response
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-schema/apache-doris-stream-load-response-schema.json
- title: Table Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-schema/apache-doris-table-schema-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-structure/apache-doris-routine-load-job-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-structure/apache-doris-stream-load-response-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-structure/apache-doris-table-schema-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-ld/apache-doris-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/examples/apache-doris-routine-load-job-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/examples/apache-doris-stream-load-response-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/examples/apache-doris-table-schema-example.json
provider_name: Apache Doris
provider_slug: apache-doris
slug: apache-doris
source_yaml: "aid: apache-doris:apache-doris\nname: Apache Doris\ndescription: Apache Doris provides a MySQL-compatible protocol for SQL queries, a REST API for cluster\n  management and monitoring, Stream Load HTTP API for real-time bulk data ingestion, Routine Load for\n  continuous Kafka ingestion, and connectors for Flink, Spark, and Kafka. An MCP server is also available\n  for AI-assisted analytics.\nhumanURL: https://doris.apache.org/docs/dev/summary/basic-summary\ntags:\n- Analytics\n- Connectors\n- Data Ingestion\n- Flink\n- Kafka\n- MySQL\n- REST\n- SQL\n- Spark\n- Stream Load\nproperties:\n- type: Documentation\n  url: https://doris.apache.org/docs/dev/summary/basic-summary\n- type: GettingStarted\n  url: https://doris.apache.org/docs/dev/install/\n- type: APIReference\n  url: https://doris.apache.org/docs/dev/admin-manual/http-actions/\n- type: GitHubRepository\n  url: https://github.com/apache/doris\n- type: Tools\n  url: https://github.com/apache/doris-mcp-server\n  title:\
  \ MCP Server\n- type: SDK\n  url: https://github.com/apache/doris-flink-connector\n  title: Flink Connector\n- type: SDK\n  url: https://github.com/apache/doris-spark-connector\n  title: Spark Connector\n- type: SDK\n  url: https://github.com/apache/doris-kafka-connector\n  title: Kafka Connector\n- type: Tools\n  url: https://github.com/apache/doris-operator\n  title: Kubernetes Operator\n- type: Tools\n  url: https://github.com/apache/doris-streamloader\n  title: Stream Loader CLI\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-schema/apache-doris-routine-load-job-schema.json\n  title: Routine Load Job\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-schema/apache-doris-stream-load-response-schema.json\n  title: Stream Load Response\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-schema/apache-doris-table-schema-schema.json\n\
  \  title: Table Schema\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-structure/apache-doris-routine-load-job-structure.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-structure/apache-doris-stream-load-response-structure.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-structure/apache-doris-table-schema-structure.json\n- type: JSONLD\n  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/json-ld/apache-doris-context.jsonld\n- type: Example\n  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/examples/apache-doris-routine-load-job-example.json\n- type: Example\n  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/examples/apache-doris-stream-load-response-example.json\n- type: Example\n\
  \  url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/examples/apache-doris-table-schema-example.json\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apache-doris/refs/heads/main/apis.yml
tags:
- Analytics
- Connectors
- Data Ingestion
- Flink
- Kafka
- MySQL
- REST
- SQL
- Spark
- Stream Load
---
