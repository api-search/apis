---
aid: microsoft-azure:capability-types
baseURL: ''
description: Microsoft Azure Capability Types refer to the various features and functionalities that are offered by the Microsoft Azure cloud computing platform. These capabilities are categorized into different types such as compute, storage, networking, security, and database services. The compute capability type includes services for virtual machines, containers, and serverless computing options. The storage capability type includes services for storing and managing data in various formats and locations.
humanURL: https://learn.microsoft.com/en-us/azure/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Capability Types
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/capability-types-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: capability-types
source_filename: capability-types-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  title: Microsoft Azure Capability Types\n  version: 2023-10-27-preview\npaths: {}\ndefinitions:\n  capability:\n    type: object\n    description: Model that represents a Capability resource.\n    allOf:\n      - $ref: >-\n          ../../../../../../common-types/resource-management/v2/types.json#/definitions/Resource\n    properties:\n      systemData:\n        description: The standard system metadata of a resource type.\n        $ref: >-\n          ../../../../../../common-types/resource-management/v2/types.json#/definitions/systemData\n        readOnly: true\n      properties:\n        x-ms-client-flatten: true\n        description: The properties of a capability resource.\n        $ref: '#/definitions/capabilityProperties'\n        readOnly: true\n  capabilityProperties:\n    type: object\n    description: Model that represents the Capability properties model.\n    properties:\n      publisher:\n        type: string\n        description: String\
  \ of the Publisher that this Capability extends.\n        readOnly: true\n      targetType:\n        type: string\n        description: String of the Target Type that this Capability extends.\n        readOnly: true\n      description:\n        type: string\n        description: Localized string of the description.\n        readOnly: true\n      parametersSchema:\n        $ref: ./common.json#/definitions/url\n        description: URL to retrieve JSON schema of the Capability parameters.\n        readOnly: true\n      urn:\n        $ref: ./common.json#/definitions/urn\n        description: String of the URN for this Capability Type.\n        readOnly: true\n    additionalProperties: false\n  capabilityListResult:\n    type: object\n    description: >-\n      Model that represents a list of Capability resources and a link for\n      pagination.\n    properties:\n      value:\n        type: array\n        items:\n          $ref: '#/definitions/capability'\n        description: List of Capability\
  \ resources.\n        readOnly: true\n      nextLink:\n        $ref: ./common.json#/definitions/urlNullable\n        description: URL to retrieve the next page of Capability resources.\n        readOnly: true\n    additionalProperties: false\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/capability-types-openapi-original.yml
tags: []
---
