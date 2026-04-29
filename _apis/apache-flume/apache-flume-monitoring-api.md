---
aid: apache-flume:apache-flume-monitoring-api
baseURL: http://localhost:41414
description: REST API for monitoring Apache Flume agents, retrieving component metrics for sources, channels, and sinks, and accessing agent health information.
humanURL: https://flume.apache.org/FlumeUserGuide.html
image: ''
layout: api
name: Apache Flume Monitoring API
properties:
- type: Documentation
  url: https://flume.apache.org/FlumeUserGuide.html
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apache-flume/refs/heads/main/openapi/apache-flume-monitoring-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-flume/refs/heads/main/json-schema/flume-monitoring-agent-metrics-schema.json
- type: JSON-LD
  url: https://raw.githubusercontent.com/api-evangelist/apache-flume/refs/heads/main/json-ld/apache-flume-monitoring-context.jsonld
provider_name: Apache Flume
provider_slug: apache-flume
slug: apache-flume-monitoring-api
source_filename: apache-flume-monitoring-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Apache Flume Monitoring API\n  version: \"1.11.0\"\n  description: REST API for monitoring Apache Flume agents, retrieving component metrics, and accessing agent health information.\n  contact:\n    email: user@flume.apache.org\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0\nservers:\n  - url: http://localhost:41414\n    description: Flume Agent Monitoring HTTP Server\n\npaths:\n  /metrics:\n    get:\n      operationId: getMetrics\n      summary: Apache Flume Get Agent Metrics\n      description: Retrieve all component metrics for the running Flume agent including source, channel, and sink statistics.\n      tags:\n        - Monitoring\n      responses:\n        '200':\n          description: Component metrics retrieved successfully\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/AgentMetrics'\n              examples:\n            \
  \    GetMetrics200Example:\n                  summary: Default getMetrics 200 response\n                  x-microcks-default: true\n                  value:\n                    SOURCE.avro-source:\n                      EventReceivedCount: \"1000\"\n                      EventAcceptedCount: \"998\"\n                      AppendBatchAcceptedCount: \"50\"\n                      AppendBatchReceivedCount: \"50\"\n                      Type: SOURCE\n                      StartTime: \"1718153645993\"\n                      StopTime: \"0\"\n                    CHANNEL.memory-channel:\n                      EventPutAttemptCount: \"998\"\n                      EventPutSuccessCount: \"998\"\n                      EventTakeAttemptCount: \"998\"\n                      EventTakeSuccessCount: \"997\"\n                      ChannelSize: \"1\"\n                      ChannelCapacity: \"1000\"\n                      Type: CHANNEL\n                    SINK.hdfs-sink:\n                      EventDrainAttemptCount:\
  \ \"997\"\n                      EventDrainSuccessCount: \"997\"\n                      ConnectionCreatedCount: \"5\"\n                      ConnectionClosedCount: \"4\"\n                      Type: SINK\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n\ncomponents:\n  schemas:\n    AgentMetrics:\n      type: object\n      description: All component metrics for a Flume agent indexed by component type and name\n      additionalProperties:\n        $ref: '#/components/schemas/ComponentMetrics'\n\n    ComponentMetrics:\n      type: object\n      description: Metrics for a specific Flume component (source, channel, or sink)\n      properties:\n        Type:\n          type: string\n          description: Component type (SOURCE, CHANNEL, or SINK)\n          enum: [SOURCE, CHANNEL, SINK]\n          example: SOURCE\n        StartTime:\n          type: string\n          description: Component start timestamp in milliseconds since epoch\n          example: \"1718153645993\"\
  \n        StopTime:\n          type: string\n          description: Component stop timestamp (0 if running)\n          example: \"0\"\n        EventReceivedCount:\n          type: string\n          description: Number of events received (sources only)\n          example: \"1000\"\n        EventAcceptedCount:\n          type: string\n          description: Number of events accepted (sources only)\n          example: \"998\"\n        AppendBatchReceivedCount:\n          type: string\n          description: Number of event batches received (sources only)\n          example: \"50\"\n        AppendBatchAcceptedCount:\n          type: string\n          description: Number of event batches accepted (sources only)\n          example: \"50\"\n        EventPutAttemptCount:\n          type: string\n          description: Number of event put attempts (channels only)\n          example: \"998\"\n        EventPutSuccessCount:\n          type: string\n          description: Number of successful event\
  \ puts (channels only)\n          example: \"998\"\n        EventTakeAttemptCount:\n          type: string\n          description: Number of event take attempts (channels only)\n          example: \"998\"\n        EventTakeSuccessCount:\n          type: string\n          description: Number of successful event takes (channels only)\n          example: \"997\"\n        ChannelSize:\n          type: string\n          description: Current number of events in channel\n          example: \"1\"\n        ChannelCapacity:\n          type: string\n          description: Maximum channel capacity in events\n          example: \"1000\"\n        EventDrainAttemptCount:\n          type: string\n          description: Number of drain attempts (sinks only)\n          example: \"997\"\n        EventDrainSuccessCount:\n          type: string\n          description: Number of successful drains (sinks only)\n          example: \"997\"\n        ConnectionCreatedCount:\n          type: string\n          description:\
  \ Number of connections created (sinks only)\n          example: \"5\"\n        ConnectionClosedCount:\n          type: string\n          description: Number of connections closed (sinks only)\n          example: \"4\"\n        ConnectionFailedCount:\n          type: string\n          description: Number of failed connections (sinks only)\n          example: \"0\"\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apache-flume/refs/heads/main/openapi/apache-flume-monitoring-openapi.yml
tags:
- Monitoring
- Metrics
- REST API
---
