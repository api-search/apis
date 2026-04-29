---
aid: gitlab:apiv4metadata
baseURL: https://gitlab.com/api/v4
description: The GitLab Metadata API provides information about the GitLab instance, including the version, revision, and other metadata about the running installation. It is useful for verifying connectivity and identifying the version of a GitLab instance programmatically.
humanURL: https://docs.gitlab.com/api/metadata/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Metadata API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-metadata-openapi-original.yml
- type: Documentation
  url: https://docs.gitlab.com/api/metadata/
provider_name: GitLab
provider_slug: gitlab
slug: apiv4metadata
source_filename: gitlab-api-v4-metadata-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.1\ninfo:\n  title: 'GitLab api/v4/metadata'\n  version: v4\n  description: Needs description.\n  termsOfService: https://about.gitlab.com/terms/\n  license:\n    name: CC BY-SA 4.0\n    url: https://gitlab.com/gitlab-org/gitlab/-/blob/master/LICENSE\nservers:\n- url: https://www.gitlab.com/api/\nsecurity:\n- ApiKeyAuth: []\ntags:\n- name: Metadata\npaths:\n  /api/v4/metadata:\n    get:\n      tags:\n      - Metadata\n      summary: GitLab Retrieve Metadata Information for This GitLab Instance\n      description: This feature was introduced in GitLab 15.2.\n      operationId: getApiV4Metadata\n      responses:\n        '200':\n          description: Retrieve metadata information for this GitLab instance\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/API_Entities_Metadata'\n        '401':\n          description: Unauthorized\n          content: {}\n      x-microcks-operation:\n        delay:\
  \ 0\n        dispatcher: FALLBACK\ncomponents:\n  schemas:\n    API_Entities_Metadata:\n      type: object\n      properties:\n        version:\n          type: string\n          example: 15.2-pre\n        revision:\n          type: string\n          example: c401a659d0c\n        kas:\n          type: object\n          properties:\n            enabled:\n              type: boolean\n            externalUrl:\n              type: string\n              example: grpc://gitlab.example.com:8150\n            version:\n              type: string\n              example: 15.0.0\n        enterprise:\n          type: boolean\n          example: true\n      description: API_Entities_Metadata model\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-metadata-openapi-original.yml
tags:
- Instance Information
- Metadata
- System
---
