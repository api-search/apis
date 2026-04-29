---
aid: microsoft-azure-one:common-monitoring-types
baseURL: ''
description: Microsoft Azure Common Monitoring Types offers various types of monitoring capabilities for users to track the performance and health of their Azure resources.
humanURL: https://learn.microsoft.com/en-us/azure/azure-monitor/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Common Monitoring Types
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/common-monitoring-types-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/azure-monitor/
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: common-monitoring-types
source_filename: common-monitoring-types-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  version: '2021-05-01'\n  title: Microsoft Azure Common Monitoring types\npaths: {}\ndefinitions:\n  LocalizableString:\n    type: object\n    required:\n      - value\n    properties:\n      value:\n        type: string\n        description: the invariant value.\n      localizedValue:\n        type: string\n        description: the locale specific value.\n    description: The localizable string class.\n  MetricUnit:\n    type: string\n    description: The unit of the metric.\n    enum:\n      - Count\n      - Bytes\n      - Seconds\n      - CountPerSecond\n      - BytesPerSecond\n      - Percent\n      - MilliSeconds\n      - ByteSeconds\n      - Unspecified\n      - Cores\n      - MilliCores\n      - NanoCores\n      - BitsPerSecond\n    x-ms-enum:\n      name: MetricUnit\n      modelAsString: true\n  ErrorContract:\n    title: Error Response\n    description: >-\n      Common error response for all Azure Resource Manager APIs to return error\n   \
  \   details for failed operations. (This also follows the OData error response\n      format.)\n    type: object\n    properties:\n      error:\n        description: The error object.\n        $ref: '#/definitions/ErrorResponse'\n  ErrorResponse:\n    description: Describes the format of Error response.\n    type: object\n    properties:\n      code:\n        description: Error code\n        type: string\n      message:\n        description: Error message indicating why the operation failed.\n        type: string\nparameters:\n  ResourceUriParameter:\n    name: resourceUri\n    in: path\n    required: true\n    type: string\n    description: The identifier of the resource.\n    x-ms-parameter-location: method\n    x-ms-skip-url-encoding: true\n  RegionParameter:\n    name: region\n    in: query\n    required: true\n    type: string\n    description: The region where the metrics you want reside.\n    x-ms-parameter-location: method\n  MetricNamespaceParameter:\n    name: metricnamespace\n\
  \    in: query\n    required: false\n    type: string\n    description: Metric namespace where the metrics you want reside.\n    x-ms-parameter-location: method\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/common-monitoring-types-openapi-original.yml
tags: []
---
