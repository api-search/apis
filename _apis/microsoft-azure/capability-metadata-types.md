---
aid: microsoft-azure:capability-metadata-types
baseURL: ''
description: Microsoft Azure Capability Metadata Types provide detailed information about the capabilities and features of various Azure services. These metadata types help users understand the functionalities of each service and how they can be utilized to meet specific business needs.
humanURL: https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/cloud-scale-analytics/govern-metadata-standards
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Capability Metadata Types
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/capability-metadata-types-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/cloud-scale-analytics/govern-metadata-standards
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: capability-metadata-types
source_filename: capability-metadata-types-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  title: Microsoft Azure Capability Metadata Types\n  version: 2023-10-27-preview\npaths: {}\ndefinitions:\n  capabilityType:\n    type: object\n    description: Model that represents a Capability Type resource.\n    allOf:\n      - $ref: >-\n          ../../../../../../common-types/resource-management/v2/types.json#/definitions/Resource\n    properties:\n      systemData:\n        description: The system metadata properties of the capability type resource.\n        $ref: >-\n          ../../../../../../common-types/resource-management/v2/types.json#/definitions/systemData\n        readOnly: true\n      location:\n        type: string\n        description: Location of the Capability Type resource.\n      properties:\n        description: The properties of the capability type resource.\n        $ref: '#/definitions/capabilityTypeProperties'\n        x-ms-client-flatten: true\n        readOnly: true\n  capabilityTypeProperties:\n    type: object\n    description:\
  \ Model that represents the Capability Type properties model.\n    properties:\n      publisher:\n        type: string\n        description: String of the Publisher that this Capability Type extends.\n        readOnly: true\n      targetType:\n        type: string\n        description: String of the Target Type that this Capability Type extends.\n        readOnly: true\n      displayName:\n        type: string\n        description: Localized string of the display name.\n        readOnly: true\n      description:\n        type: string\n        description: Localized string of the description.\n        readOnly: true\n      parametersSchema:\n        $ref: ./common.json#/definitions/url\n        description: URL to retrieve JSON schema of the Capability Type parameters.\n        readOnly: true\n      urn:\n        $ref: ./common.json#/definitions/urn\n        description: String of the URN for this Capability Type.\n        readOnly: true\n      kind:\n        type: string\n        description:\
  \ String of the kind of this Capability Type.\n        readOnly: true\n      azureRbacActions:\n        type: array\n        description: Control plane actions necessary to execute capability type.\n        items:\n          type: string\n          description: Control plane action necessary to execute capability type.\n      azureRbacDataActions:\n        type: array\n        description: Data plane actions necessary to execute capability type.\n        items:\n          type: string\n          description: Data plane action necessary to execute capability type.\n      runtimeProperties:\n        type: object\n        description: Runtime properties of this Capability Type.\n        properties:\n          kind:\n            type: string\n            description: >-\n              String of the kind of the resource's action type (continuous or\n              discrete).\n            readOnly: true\n    additionalProperties: false\n  capabilityTypeListResult:\n    type: object\n    description:\
  \ >-\n      Model that represents a list of Capability Type resources and a link for\n      pagination.\n    properties:\n      value:\n        type: array\n        items:\n          $ref: '#/definitions/capabilityType'\n        description: List of Capability Type resources.\n        readOnly: true\n      nextLink:\n        $ref: ./common.json#/definitions/urlNullable\n        description: URL to retrieve the next page of Capability Type resources.\n        readOnly: true\n    additionalProperties: false\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/capability-metadata-types-openapi-original.yml
tags: []
---
