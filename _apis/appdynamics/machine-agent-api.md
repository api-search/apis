---
aid: appdynamics:machine-agent-api
baseURL: https://api.example.com
description: The AppDynamics Machine Agent API provides HTTP endpoints available at the machine agent for uploading custom metrics to the AppDynamics Controller. Developers can use this API to report custom infrastructure metrics, hardware metrics, and other machine-level data points that are not captured by the default agent instrumentation. This enables organizations to extend their monitoring coverage to include custom system-level metrics and integrate data from third-party monitoring tools.
humanURL: https://docs.appdynamics.com/appd/23.x/latest/en/extend-appdynamics/appdynamics-apis
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: AppDynamics Machine Agent API
properties:
- type: Documentation
  url: https://docs.appdynamics.com/appd/23.x/latest/en/extend-appdynamics/appdynamics-apis
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-machine-agent-api-openapi.yml
provider_name: AppDynamics
provider_slug: appdynamics
slug: machine-agent-api
source_filename: appdynamics-machine-agent-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: AppDynamics Machine Agent API\n  description: >-\n    The AppDynamics Machine Agent API provides HTTP endpoints available at\n    the machine agent for uploading custom metrics to the AppDynamics\n    Controller. Developers can use this API to report custom infrastructure\n    metrics, hardware metrics, and other machine-level data points that are\n    not captured by the default agent instrumentation. This enables\n    organizations to extend their monitoring coverage to include custom\n    system-level metrics and integrate data from third-party monitoring\n    tools. The HTTP listener must be enabled on the Machine Agent before\n    use.\n  version: '23.x'\n  contact:\n    name: Splunk AppDynamics Support\n    url: https://www.appdynamics.com/support\n  termsOfService: https://www.cisco.com/c/en/us/about/legal/cloud-and-software.html\nexternalDocs:\n  description: Machine Agent HTTP Listener Documentation\n  url: https://docs.appdynamics.com/appd/24.x/latest/en/infrastructure-visibility/machine-agent/extensions-and-custom-metrics/machine-agent-http-listener\n\
  servers:\n  - url: http://{machine-agent-host}:{port}\n    description: Machine Agent HTTP Listener\n    variables:\n      machine-agent-host:\n        default: localhost\n        description: >-\n          The hostname where the Machine Agent is running. Defaults to\n          localhost unless configured otherwise.\n      port:\n        default: '8293'\n        description: >-\n          The port for the Machine Agent HTTP listener.\ntags:\n  - name: Custom Metrics\n    description: >-\n      Upload custom metrics to the AppDynamics Controller through the Machine\n      Agent HTTP listener. Metrics must be uploaded at least once every 300\n      seconds to remain active.\nsecurity: []\npaths:\n  /api/v1/metrics:\n    post:\n      operationId: publishCustomMetrics\n      summary: Publish custom metrics\n      description: >-\n        Uploads one or more custom metrics to the AppDynamics Controller\n        through the Machine Agent. Metrics must be uploaded at least once\n        every\
  \ 300 seconds (5 minutes) to remain active in the metric\n        hierarchy. Each metric requires a name, aggregator type, and a 64-bit\n        integer value.\n      tags:\n        - Custom Metrics\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: array\n              description: >-\n                An array of custom metric objects to upload.\n              items:\n                $ref: '#/components/schemas/CustomMetric'\n      responses:\n        '200':\n          description: Metrics uploaded successfully\n        '400':\n          description: Bad request - invalid metric data\n        '503':\n          description: Service unavailable - Machine Agent HTTP listener not enabled\ncomponents:\n  schemas:\n    CustomMetric:\n      type: object\n      description: >-\n        A custom metric data point to upload to the Controller through the\n        Machine Agent HTTP listener.\n      required:\n    \
  \    - metricName\n        - aggregatorType\n        - value\n      properties:\n        metricName:\n          type: string\n          description: >-\n            The full metric path name using pipe delimiters for hierarchy\n            levels. For example, Custom Metrics|MyApp|RequestCount.\n        aggregatorType:\n          type: string\n          description: >-\n            The aggregation type that determines how metric values are rolled\n            up across time periods and cluster nodes.\n          enum:\n            - AVERAGE\n            - SUM\n            - OBSERVATION\n            - ADVANCED_AVERAGE\n        value:\n          type: integer\n          format: int64\n          description: >-\n            The metric value as a 64-bit integer.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-machine-agent-api-openapi.yml
tags:
- Custom Metrics
- Infrastructure
- Metrics
- Server Monitoring
---
