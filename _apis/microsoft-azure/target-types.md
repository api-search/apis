---
aid: microsoft-azure:target-types
baseURL: ''
description: Microsoft Azure Target Types allows users to define the specific targets they want to monitor and manage within their Azure environment. This feature provides a way to classify and organize different types of resources based on their function, location, or any other relevant criteria.
humanURL: https://learn.microsoft.com/en-us/rest/api/chaosstudio/target-types/list?view=rest-chaosstudio-2024-01-01
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Target Types
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/target-types-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/rest/api/chaosstudio/target-types/list?view=rest-chaosstudio-2024-01-01
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: target-types
source_filename: target-types-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  title: Microsoft Azure Target Types\n  version: 2023-10-27-preview\npaths: {}\ndefinitions:\n  target:\n    type: object\n    description: Model that represents a Target resource.\n    allOf:\n      - $ref: >-\n          ../../../../../../common-types/resource-management/v2/types.json#/definitions/Resource\n    properties:\n      systemData:\n        description: The system metadata of the target resource.\n        $ref: >-\n          ../../../../../../common-types/resource-management/v2/types.json#/definitions/systemData\n        readOnly: true\n      location:\n        type: string\n        description: Location of the target resource.\n      properties:\n        description: The properties of the target resource.\n        x-ms-client-flatten: true\n        $ref: '#/definitions/targetProperties'\n    required:\n      - properties\n  targetProperties:\n    type: object\n    description: Model that represents the base Target properties model.\n    properties:\
  \ {}\n    additionalProperties: true\n  targetListResult:\n    type: object\n    description: >-\n      Model that represents a list of Target resources and a link for\n      pagination.\n    properties:\n      value:\n        type: array\n        items:\n          $ref: '#/definitions/target'\n        description: List of Target resources.\n        readOnly: true\n      nextLink:\n        $ref: ./common.json#/definitions/urlNullable\n        description: URL to retrieve the next page of Target resources.\n        readOnly: true\n    additionalProperties: false\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/target-types-openapi-original.yml
tags: []
---
