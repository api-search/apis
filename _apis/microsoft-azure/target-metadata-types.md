---
aid: microsoft-azure:target-metadata-types
baseURL: ''
description: Microsoft Azure Target Metadata Types is a feature that allows businesses to define various types of metadata for their Azure resources. This feature enables users to categorize and organize their resources in a more structured manner, making it easier to manage and track them. With Target Metadata Types, users can create custom metadata fields such as labels, tags, and properties to provide additional context and information about their resources.
humanURL: https://learn.microsoft.com/en-us/azure/data-factory/control-flow-get-metadata-activity
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Target Metadata Types
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/target-metadata-types-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/data-factory/control-flow-get-metadata-activity
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: target-metadata-types
source_filename: target-metadata-types-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  title: Microsoft Azure Target Metadata Types\n  version: 2023-10-27-preview\npaths: {}\ndefinitions:\n  targetType:\n    type: object\n    description: Model that represents a Target Type resource.\n    allOf:\n      - $ref: >-\n          ../../../../../../common-types/resource-management/v2/types.json#/definitions/Resource\n    properties:\n      systemData:\n        description: The system metadata properties of the target type resource.\n        $ref: >-\n          ../../../../../../common-types/resource-management/v2/types.json#/definitions/systemData\n        readOnly: true\n      location:\n        type: string\n        description: Location of the Target Type resource.\n      properties:\n        description: The properties of the target type resource.\n        x-ms-client-flatten: true\n        $ref: '#/definitions/targetTypeProperties'\n    required:\n      - properties\n  targetTypeProperties:\n    type: object\n    description: Model that\
  \ represents the base Target Type properties model.\n    properties:\n      displayName:\n        type: string\n        description: Localized string of the display name.\n        readOnly: true\n      description:\n        type: string\n        description: Localized string of the description.\n        readOnly: true\n      propertiesSchema:\n        $ref: ./common.json#/definitions/url\n        description: URL to retrieve JSON schema of the Target Type properties.\n        readOnly: true\n      resourceTypes:\n        type: array\n        items:\n          type: string\n        description: List of resource types this Target Type can extend.\n        readOnly: true\n    additionalProperties: false\n  targetTypeListResult:\n    type: object\n    description: >-\n      Model that represents a list of Target Type resources and a link for\n      pagination.\n    properties:\n      value:\n        type: array\n        items:\n          $ref: '#/definitions/targetType'\n        description:\
  \ List of Target Type resources.\n        readOnly: true\n      nextLink:\n        $ref: ./common.json#/definitions/urlNullable\n        description: URL to retrieve the next page of Target Type resources.\n        readOnly: true\n    additionalProperties: false\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/target-metadata-types-openapi-original.yml
tags: []
---
