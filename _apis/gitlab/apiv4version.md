---
aid: gitlab:apiv4version
baseURL: https://gitlab.com/api/v4
description: The GitLab Version API returns version and revision information for the GitLab instance. This endpoint is useful for verifying what version of GitLab is running and for checking compatibility with specific API features before making requests.
humanURL: https://docs.gitlab.com/api/version/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Version API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-version-openapi-original.yml
- type: Documentation
  url: https://docs.gitlab.com/api/version/
provider_name: GitLab
provider_slug: gitlab
slug: apiv4version
source_filename: gitlab-api-v4-version-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.1\ninfo:\n  title: 'GitLab api/v4/version'\n  version: v4\n  description: Needs description.\n  termsOfService: https://about.gitlab.com/terms/\n  license:\n    name: CC BY-SA 4.0\n    url: https://gitlab.com/gitlab-org/gitlab/-/blob/master/LICENSE\nservers:\n- url: https://www.gitlab.com/api/\nsecurity:\n- ApiKeyAuth: []\ntags:\n- name: Version\npaths:\n  /api/v4/version:\n    get:\n      tags:\n      - Version\n      summary: GitLab Retrieves Version Information for the GitLab Instance\n      description: >-\n        This feature was introduced in GitLab 8.13 and deprecated in 15.5. We\n        recommend you instead use the Metadata API.\n      operationId: getApiV4Version\n      responses:\n        '200':\n          description: Retrieves version information for the GitLab instance\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/API_Entities_Metadata'\n        '401':\n          description:\
  \ Unauthorized\n          content: {}\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  schemas:\n    API_Entities_Metadata:\n      type: object\n      properties:\n        version:\n          type: string\n          example: 15.2-pre\n        revision:\n          type: string\n          example: c401a659d0c\n        kas:\n          type: object\n          properties:\n            enabled:\n              type: boolean\n            externalUrl:\n              type: string\n              example: grpc://gitlab.example.com:8150\n            version:\n              type: string\n              example: 15.0.0\n        enterprise:\n          type: boolean\n          example: true\n      description: API_Entities_Metadata model\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-version-openapi-original.yml
tags:
- Instance Information
- System
- Version
---
