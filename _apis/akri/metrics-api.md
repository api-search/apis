---
aid: akri:metrics-api
baseURL: http://localhost:8080
description: Akri exposes Prometheus metrics on port 8080 at /metrics for the Agent, Controller, and broker pods. Metrics include instance count, discovery response results and latency, and broker pod count. Supports Prometheus Operator ServiceMonitor for metric scraping.
humanURL: https://docs.akri.sh/
image: ''
layout: api
name: Akri Metrics API
properties:
- type: Documentation
  url: https://docs.akri.sh/
- type: GitHubRepository
  url: https://github.com/project-akri/akri
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/openapi/akri-metrics-openapi.yaml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-schema/akri-prometheus-metrics-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-schema/akri-akri-instance-count-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-schema/akri-akri-discovery-response-result-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-schema/akri-akri-discovery-response-time-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-schema/akri-akri-broker-pod-count-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-schema/akri-akri-configuration-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-schema/akri-akri-instance-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-structure/akri-prometheus-metrics-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-structure/akri-akri-instance-count-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-structure/akri-akri-discovery-response-result-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-structure/akri-akri-discovery-response-time-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-structure/akri-akri-broker-pod-count-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-structure/akri-akri-configuration-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/json-structure/akri-akri-instance-structure.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/examples/akri-prometheus-metrics-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/examples/akri-akri-instance-count-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/examples/akri-akri-discovery-response-result-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/examples/akri-akri-discovery-response-time-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/examples/akri-akri-broker-pod-count-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/examples/akri-akri-configuration-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/examples/akri-akri-instance-example.json
provider_name: Akri
provider_slug: akri
slug: metrics-api
source_filename: akri-metrics-openapi.yaml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.3\ninfo:\n  title: Akri Metrics API\n  description: >-\n    Prometheus metrics endpoint exposed by Akri Agent, Controller, and broker\n    pods. Metrics include instance count, discovery response results and\n    latency, and broker pod count for monitoring Akri deployments.\n  version: 0.12.20\n  contact:\n    name: Akri Community\n    url: https://github.com/project-akri/akri\n  license:\n    name: Apache 2.0\n    url: https://github.com/project-akri/akri/blob/main/LICENSE\n  x-generated-from: documentation\nservers:\n  - url: http://localhost:8080\n    description: Akri Agent/Controller metrics server (default port)\npaths:\n  /metrics:\n    get:\n      operationId: getMetrics\n      summary: Akri Get Prometheus Metrics\n      description: >-\n        Returns Prometheus-formatted metrics for the Akri Agent, Controller, or\n        broker pods. Includes instance discovery counts, discovery response\n        results, discovery latency histograms, and broker pod\
  \ counts.\n      tags:\n        - Metrics\n      responses:\n        '200':\n          description: Prometheus metrics in text exposition format\n          content:\n            text/plain:\n              schema:\n                $ref: '#/components/schemas/PrometheusMetrics'\n              examples:\n                GetMetrics200Example:\n                  summary: Default getMetrics 200 response\n                  x-microcks-default: true\n                  value: |\n                    # HELP akri_instance_count Number of discovered Akri instances\n                    # TYPE akri_instance_count gauge\n                    akri_instance_count{configuration=\"onvif-camera\",shared=\"false\"} 3\n                    # HELP akri_discovery_response_result Discovery handler response results\n                    # TYPE akri_discovery_response_result counter\n                    akri_discovery_response_result{configuration=\"onvif-camera\",result=\"success\"} 42\n                    # HELP akri_discovery_response_time\
  \ Discovery handler response latency\n                    # TYPE akri_discovery_response_time histogram\n                    akri_discovery_response_time_bucket{configuration=\"onvif-camera\",le=\"0.005\"} 10\n                    # HELP akri_broker_pod_count Number of broker pods deployed\n                    # TYPE akri_broker_pod_count gauge\n                    akri_broker_pod_count{configuration=\"onvif-camera\",node=\"node-01\"} 1\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  schemas:\n    PrometheusMetrics:\n      title: PrometheusMetrics\n      type: string\n      description: >-\n        Prometheus text exposition format containing Akri metrics. Includes\n        akri_instance_count (gauge), akri_discovery_response_result (counter),\n        akri_discovery_response_time (histogram), and akri_broker_pod_count\n        (gauge) plus standard process metrics.\n      example: |\n        # HELP akri_instance_count Number of discovered Akri\
  \ instances\n        # TYPE akri_instance_count gauge\n        akri_instance_count{configuration=\"onvif-camera\",shared=\"false\"} 3\n    AkriInstanceCount:\n      title: AkriInstanceCount\n      type: object\n      description: Gauge tracking the number of discovered Akri instances per configuration\n      properties:\n        configuration:\n          type: string\n          description: Name of the Akri Configuration resource\n          example: onvif-camera\n        shared:\n          type: string\n          description: Whether the device is shared across multiple nodes\n          example: \"false\"\n        value:\n          type: number\n          description: Current count of discovered instances\n          example: 3\n    AkriDiscoveryResponseResult:\n      title: AkriDiscoveryResponseResult\n      type: object\n      description: Counter for Discovery Handler success and failure responses\n      properties:\n        configuration:\n          type: string\n          description:\
  \ Name of the Akri Configuration resource\n          example: onvif-camera\n        result:\n          type: string\n          description: Result of the discovery response\n          enum:\n            - success\n            - failure\n          example: success\n        value:\n          type: number\n          description: Total count of responses\n          example: 42\n    AkriDiscoveryResponseTime:\n      title: AkriDiscoveryResponseTime\n      type: object\n      description: Histogram of Discovery Handler response latency in seconds\n      properties:\n        configuration:\n          type: string\n          description: Name of the Akri Configuration resource\n          example: onvif-camera\n        le:\n          type: string\n          description: Histogram bucket upper bound in seconds\n          example: \"0.005\"\n        value:\n          type: number\n          description: Count of observations within this bucket\n          example: 10\n    AkriBrokerPodCount:\n   \
  \   title: AkriBrokerPodCount\n      type: object\n      description: Gauge tracking the number of broker pods per configuration and node\n      properties:\n        configuration:\n          type: string\n          description: Name of the Akri Configuration resource\n          example: onvif-camera\n        node:\n          type: string\n          description: Kubernetes node name\n          example: node-01\n        value:\n          type: number\n          description: Current count of broker pods\n          example: 1\n    AkriConfiguration:\n      title: AkriConfiguration\n      type: object\n      description: >-\n        Akri Configuration custom resource (configurations.akri.sh) that\n        specifies device discovery settings and optional broker workload\n        deployment specifications.\n      properties:\n        apiVersion:\n          type: string\n          description: API version of the Akri Configuration resource\n          example: akri.sh/v0\n        kind:\n     \
  \     type: string\n          description: Resource kind\n          example: Configuration\n        metadata:\n          type: object\n          description: Kubernetes object metadata\n          properties:\n            name:\n              type: string\n              description: Name of the configuration\n              example: onvif-camera\n            namespace:\n              type: string\n              description: Kubernetes namespace\n              example: default\n        spec:\n          type: object\n          description: Configuration specification\n          properties:\n            discoveryHandler:\n              type: object\n              description: Discovery Handler settings for device discovery\n              properties:\n                name:\n                  type: string\n                  description: Name of the Discovery Handler to use\n                  example: onvif\n                discoveryDetails:\n                  type: string\n                  description:\
  \ Protocol-specific discovery details as a string\n                  example: \"ipAddresses:\\\\n  action: Exclude\\\\n  items:\\\\n  - 10.0.0.1\"\n                discoveryProperties:\n                  type: array\n                  description: Additional key-value properties for Discovery Handler\n                  items:\n                    type: object\n                    properties:\n                      name:\n                        type: string\n                        example: USERNAME_LIST\n                      value:\n                        type: string\n                        example: admin\n            capacity:\n              type: integer\n              description: Maximum number of broker replicas per device\n              example: 1\n    AkriInstance:\n      title: AkriInstance\n      type: object\n      description: >-\n        Akri Instance custom resource (instances.akri.sh) representing a\n        single discovered device. Automatically created and destroyed\
  \ as\n        devices appear and disappear.\n      properties:\n        apiVersion:\n          type: string\n          description: API version of the Akri Instance resource\n          example: akri.sh/v0\n        kind:\n          type: string\n          description: Resource kind\n          example: Instance\n        metadata:\n          type: object\n          description: Kubernetes object metadata\n          properties:\n            name:\n              type: string\n              description: Instance name in format configuration-name-hash\n              example: onvif-camera-a1b2c3\n            namespace:\n              type: string\n              description: Kubernetes namespace\n              example: default\n        spec:\n          type: object\n          description: Instance specification\n          properties:\n            configurationName:\n              type: string\n              description: Name of the parent Configuration resource\n              example: onvif-camera\n\
  \            shared:\n              type: boolean\n              description: Whether device is shared across multiple nodes\n              example: false\n            nodes:\n              type: array\n              description: List of nodes that can access this device\n              items:\n                type: string\n              example:\n                - node-01\n                - node-02\n            deviceUsage:\n              type: object\n              description: Map of slot names to broker pod names\n              additionalProperties:\n                type: string\n            metadata:\n              type: object\n              description: Device-specific metadata from discovery\n              additionalProperties:\n                type: string\ntags:\n  - name: Metrics\n    description: Prometheus metrics endpoints for Akri Agent, Controller, and broker pods\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/akri/refs/heads/main/openapi/akri-metrics-openapi.yaml
tags:
- Monitoring
- Prometheus
- Metrics
- Observability
---
