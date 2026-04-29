---
aid: gitlab:apiv4applications
baseURL: https://gitlab.com/api/v4
description: The GitLab Applications API allows you to manage OAuth applications registered in GitLab. You can create, list, and delete OAuth applications that enable third-party services to access GitLab resources on behalf of users using the OAuth 2.0 protocol.
humanURL: https://docs.gitlab.com/api/applications/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Applications API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-applications-openapi-original.yml
- type: Documentation
  url: https://docs.gitlab.com/api/applications/
provider_name: GitLab
provider_slug: gitlab
slug: apiv4applications
source_filename: gitlab-api-v4-applications-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.0.1\ninfo:\n  title: 'GitLab api/v4/applications'\n  version: v4\n  description: Needs description.\n  termsOfService: https://about.gitlab.com/terms/\n  license:\n    name: CC BY-SA 4.0\n    url: https://gitlab.com/gitlab-org/gitlab/-/blob/master/LICENSE\nservers:\n- url: https://www.gitlab.com/api/\nsecurity:\n- ApiKeyAuth: []\ntags:\n- name: Applications\npaths:\n  /api/v4/applications/{id}:\n    delete:\n      tags:\n      - Applications\n      summary: GitLab Delete an Application\n      description: Delete a specific application\n      operationId: deleteApiV4ApplicationsId\n      parameters:\n      - name: id\n        in: path\n        description: The ID of the application (not the application_id)\n        required: true\n        schema:\n          type: integer\n          format: int32\n        example: 42\n      responses:\n        '204':\n          description: Delete an application\n          content: {}\n      x-microcks-operation:\n        delay: 0\n\
  \        dispatcher: FALLBACK\n  /api/v4/applications:\n    get:\n      tags:\n      - Applications\n      summary: GitLab Get Applications\n      description: List all registered applications\n      operationId: getApiV4Applications\n      responses:\n        '200':\n          description: Get applications\n          content:\n            application/json:\n              schema:\n                type: array\n                items:\n                  $ref: '#/components/schemas/API_Entities_Application'\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\n    post:\n      tags:\n      - Applications\n      summary: GitLab Create a New Application\n      description: This feature was introduced in GitLab 10.5\n      operationId: postApiV4Applications\n      requestBody:\n        content:\n          application/json:\n            schema:\n              required:\n              - name\n              - redirect_uri\n              - scopes\n              properties:\n\
  \                name:\n                  type: string\n                  description: Name of the application.\n                redirect_uri:\n                  type: string\n                  description: Redirect URI of the application.\n                scopes:\n                  type: string\n                  description: >-\n                    Scopes of the application. You can specify multiple scopes\n                    by separating\\\n                                                     each scope using a space\n                confidential:\n                  type: boolean\n                  description: >-\n                    The application is used where the client secret can be kept\n                    confidential. Native mobile apps \\\n                                            and Single Page Apps are considered non-confidential. Defaults to true if not supplied\n                  default: true\n        required: true\n      responses:\n        '200':\n          description:\
  \ Create a new application\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/API_Entities_ApplicationWithSecret'\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  schemas:\n    API_Entities_ApplicationWithSecret:\n      type: object\n      properties:\n        id:\n          type: string\n          example: '123456'\n        application_id:\n          type: string\n          example: 5832fc6e14300a0d962240a8144466eef4ee93ef0d218477e55f11cf12fc3737\n        application_name:\n          type: string\n          example: MyApplication\n        callback_url:\n          type: string\n          example: https://redirect.uri\n        confidential:\n          type: boolean\n          example: true\n        secret:\n          type: string\n          example: ee1dd64b6adc89cf7e2c23099301ccc2c61b441064e9324d963c46902a85ec34\n      description: API_Entities_ApplicationWithSecret model\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-applications-openapi-original.yml
tags:
- Applications
- Authentication
- OAuth
---
