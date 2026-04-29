---
aid: asana:asana-user-task-lists-api
baseURL: ''
description: Asana User Task Lists API is a tool that allows users to create, update, and manage task lists within the Asana platform. By using this API, users can access their task lists, view all the tasks within them, and make changes such as marking tasks as complete or updating task details. This API provides a seamless way for users to stay organized and on top of their tasks by offering a centralized platform for managing all their to-do lists.
humanURL: https://developers.asana.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Asana User Task Lists  API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/asana/refs/heads/main/openapi/asana-user-task-lists-api-openapi.yml
- type: Documentation
  url: https://developers.asana.com/reference/user-task-lists
provider_name: Asana
provider_slug: asana
slug: asana-user-task-lists-api
source_filename: asana-user-task-lists-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Asana User Task Lists API\n  description: >-\n    The Asana User Task Lists API manages user task lists, which represent\n    the tasks assigned to a particular user (their \"My Tasks\" view).\n  version: '1.0'\n  termsOfService: https://asana.com/terms\n  contact:\n    name: Asana Support\n    url: https://asana.com/support\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0\nservers:\n  - url: https://app.asana.com/api/1.0\n    description: Main endpoint.\nsecurity:\n  - personalAccessToken: []\n  - oauth2: []\ntags:\n  - name: User Task Lists\n    description: Manage user task lists (My Tasks).\npaths:\n  /user_task_lists/{user_task_list_gid}:\n    get:\n      summary: Asana Get a user task list\n      operationId: getUserTaskList\n      tags:\n        - User Task Lists\n      parameters:\n        - name: user_task_list_gid\n          in: path\n          required: true\n          schema:\n            type:\
  \ string\n      responses:\n        '200':\n          description: Successfully retrieved the user task list.\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    $ref: '#/components/schemas/UserTaskListResponse'\n  /users/{user_gid}/user_task_list:\n    get:\n      summary: Asana Get a user's task list\n      operationId: getUserTaskListForUser\n      tags:\n        - User Task Lists\n      parameters:\n        - name: user_gid\n          in: path\n          required: true\n          schema:\n            type: string\n        - name: workspace\n          in: query\n          required: true\n          schema:\n            type: string\n      responses:\n        '200':\n          description: Successfully retrieved the user's task list.\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n\
  \                  data:\n                    $ref: '#/components/schemas/UserTaskListResponse'\ncomponents:\n  securitySchemes:\n    personalAccessToken:\n      type: http\n      scheme: bearer\n    oauth2:\n      type: oauth2\n      flows:\n        authorizationCode:\n          authorizationUrl: https://app.asana.com/-/oauth_authorize\n          tokenUrl: https://app.asana.com/-/oauth_token\n          scopes:\n            default: Provides access to all endpoints documented in the API reference.\n  schemas:\n    UserTaskListResponse:\n      type: object\n      properties:\n        gid:\n          type: string\n          readOnly: true\n        resource_type:\n          type: string\n          readOnly: true\n          example: user_task_list\n        name:\n          type: string\n          example: My Tasks in My Workspace\n        owner:\n          type: object\n          readOnly: true\n          properties:\n            gid:\n              type: string\n            resource_type:\n\
  \              type: string\n            name:\n              type: string\n        workspace:\n          type: object\n          readOnly: true\n          properties:\n            gid:\n              type: string\n            resource_type:\n              type: string\n            name:\n              type: string\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/asana/refs/heads/main/openapi/asana-user-task-lists-api-openapi.yml
tags: []
---
