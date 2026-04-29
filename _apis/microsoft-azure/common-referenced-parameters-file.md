---
aid: microsoft-azure-one:common-referenced-parameters-file
baseURL: ''
description: The Microsoft Azure Common Referenced Parameters File provides a centralized location for storing commonly used parameters that can be referenced in multiple Azure Resource Manager templates. This file helps streamline the deployment process by allowing users to define and manage parameters in one place, making it easier to update and maintain configurations across different resources and deployments.
humanURL: https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/parameter-files
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Microsoft Azure Common Referenced Parameters File
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/common-referenced-parameters-file-openapi-original.yml
- type: Documentation
  url: https://learn.microsoft.com/en-us/azure/azure-resource-manager/bicep/parameter-files
provider_name: Microsoft Azure
provider_slug: microsoft-azure
slug: common-referenced-parameters-file
source_filename: common-referenced-parameters-file-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "swagger: '2.0'\ninfo:\n  version: '2017-08-30'\n  title: Microsoft Azure Common Referenced Parameters File\n  description: File containing commonly referenced parameters.\npaths: {}\nparameters:\n  GlobalEndpoint:\n    name: Endpoint\n    description: >-\n      Supported Cognitive Services endpoints (protocol and hostname, for\n      example: \"https://westus.api.cognitive.microsoft.com\",\n      \"https://api.cognitive.microsoft.com\").\n    x-ms-parameter-location: client\n    required: true\n    type: string\n    in: path\n    x-ms-skip-url-encoding: true\n    default: https://api.cognitive.microsoft.com\n  ImageStream:\n    name: Image\n    in: body\n    required: true\n    x-ms-parameter-location: method\n    description: An image stream.\n    schema:\n      type: object\n      format: file\n  ImageUrl:\n    name: ImageUrl\n    in: body\n    required: true\n    x-ms-parameter-location: method\n    x-ms-client-flatten: true\n    description: A JSON document with a URL pointing\
  \ to the image that is to be analyzed.\n    schema:\n      $ref: '#/definitions/ImageUrl'\ndefinitions:\n  ImageUrl:\n    type: object\n    required:\n      - url\n    properties:\n      url:\n        description: Publicly reachable URL of an image\n        type: string\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure/refs/heads/main/openapi/common-referenced-parameters-file-openapi-original.yml
tags: []
---
