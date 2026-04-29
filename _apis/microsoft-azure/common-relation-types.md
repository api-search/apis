---
aid: microsoft-azure:common-relation-types
baseURL: ''
description: Microsoft Azure Common Relation Types is a feature that allows users to establish relationships between different data entities in their Azure environment. These relationships can be defined in various ways, such as one-to-one, one-to-many, or many-to-many. With these relation types, users can easily connect and reference related data across different Azure services, making it easier to manage and analyze complex data structures.
humanURL: https://learn.microsoft.com/en-us/azure/storage/tables/table-storage-design-modeling
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Common Relation Types
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/common-relation-types-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/storage/tables/table-storage-design-modeling
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: common-relation-types
source_filename: common-relation-types-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  version: 2024-01-01-preview\n  title: Microsoft Azure Common Relation types\npaths: {}\ndefinitions:\n  ThreatIntelligence:\n    description: ThreatIntelligence property bag.\n    properties:\n      confidence:\n        description: Confidence (must be between 0 and 1)\n        format: double\n        readOnly: true\n        type: number\n      providerName:\n        description: >-\n          Name of the provider from whom this Threat Intelligence information\n          was received\n        readOnly: true\n        type: string\n      reportLink:\n        description: Report link\n        readOnly: true\n        type: string\n      threatDescription:\n        description: Threat description (free text)\n        readOnly: true\n        type: string\n      threatName:\n        description: Threat name (e.g. \"Jedobot malware\")\n        readOnly: true\n        type: string\n      threatType:\n        description: Threat type (e.g. \"Botnet\")\n     \
  \   readOnly: true\n        type: string\n    type: object\nparameters: {}\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/common-relation-types-openapi-original.yml
tags: []
---
