---
aid: gitlab:apiv4avatar
baseURL: https://gitlab.com/api/v4
description: The GitLab Avatar API allows you to retrieve avatar images for users and groups. It returns avatar URLs based on user email addresses, enabling applications to display profile images for GitLab users without requiring authentication.
humanURL: https://docs.gitlab.com/api/avatar/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Avatar API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-avatar-openapi-original.yml
- type: Documentation
  url: https://docs.gitlab.com/api/avatar/
provider_name: GitLab
provider_slug: gitlab
slug: apiv4avatar
source_filename: gitlab-api-v4-avatar-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.1\ninfo:\n  title: 'GitLab api/v4/avatar'\n  version: v4\n  description: Needs description.\n  termsOfService: https://about.gitlab.com/terms/\n  license:\n    name: CC BY-SA 4.0\n    url: https://gitlab.com/gitlab-org/gitlab/-/blob/master/LICENSE\nservers:\n- url: https://www.gitlab.com/api/\nsecurity:\n- ApiKeyAuth: []\ntags:\n- name: Avatar\npaths:\n  /api/v4/avatar:\n    get:\n      tags:\n      - Avatar\n      description: Return avatar url for a user\n      operationId: getApiV4Avatar\n      parameters:\n      - name: email\n        in: query\n        description: Public email address of the user\n        required: true\n        schema:\n          type: string\n        example: user@example.com\n      - name: size\n        in: query\n        description: Single pixel dimension for Gravatar images\n        schema:\n          type: integer\n          format: int32\n        example: 42\n      responses:\n        '200':\n          description: Return avatar url\
  \ for a user\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/API_Entities_Avatar'\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  schemas:\n    API_Entities_Avatar:\n      type: object\n      properties:\n        avatar_url:\n          type: string\n          example: https://gitlab.com/example\n      description: API_Entities_Avatar model\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-avatar-openapi-original.yml
tags:
- Avatars
- Profile
- Users
---
