---
aid: asana:asana-rule-triggers-api
baseURL: ''
description: The Asana Rule Triggers API provides developers with the ability to create and manage custom rules in Asana, a popular project management tool. With this API, users can set up triggers that initiate certain actions or workflows based on specific conditions being met within their Asana projects. These triggers can automate repetitive tasks, streamline communication and collaboration, and increase overall productivity within a team or organization.
humanURL: https://developers.asana.com/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Asana Rule Triggers  API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/asana/refs/heads/main/openapi/asana-rule-triggers-api-openapi.yml
- type: Documentation
  url: https://developers.asana.com/reference/triggerrule
provider_name: Asana
provider_slug: asana
slug: asana-rule-triggers-api
source_filename: asana-rule-triggers-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Asana Rule Triggers API\n  description: >-\n    The Asana Rule Triggers API allows developers to trigger rules via incoming\n    web requests, enabling external applications to connect to Asana through\n    rule-based automation.\n  version: '1.0'\n  termsOfService: https://asana.com/terms\n  contact:\n    name: Asana Support\n    url: https://asana.com/support\n  license:\n    name: Apache 2.0\n    url: https://www.apache.org/licenses/LICENSE-2.0\nservers:\n  - url: https://app.asana.com/api/1.0\n    description: Main endpoint.\nsecurity:\n  - personalAccessToken: []\n  - oauth2: []\ntags:\n  - name: Rules\n    description: Trigger rules via incoming web requests.\npaths:\n  /rule_triggers/{rule_trigger_gid}/run:\n    post:\n      summary: Asana Trigger a rule\n      description: Trigger a rule which uses an incoming web request trigger.\n      operationId: triggerRule\n      tags:\n        - Rules\n      parameters:\n        - name: rule_trigger_gid\n\
  \          in: path\n          required: true\n          schema:\n            type: string\n      requestBody:\n        required: true\n        content:\n          application/json:\n            schema:\n              type: object\n              properties:\n                data:\n                  type: object\n                  properties:\n                    resource:\n                      type: string\n                      description: The ID of the resource (e.g. task) to trigger the rule on.\n                  required:\n                    - resource\n      responses:\n        '200':\n          description: Successfully triggered the rule.\n          content:\n            application/json:\n              schema:\n                type: object\n                properties:\n                  data:\n                    type: object\n                    properties:\n                      message:\n                        type: string\n        '400':\n          description: Bad request.\n\
  \        '401':\n          description: Unauthorized.\n        '403':\n          description: Forbidden.\n        '404':\n          description: Not found.\n        '500':\n          description: Internal server error.\ncomponents:\n  securitySchemes:\n    personalAccessToken:\n      type: http\n      scheme: bearer\n    oauth2:\n      type: oauth2\n      flows:\n        authorizationCode:\n          authorizationUrl: https://app.asana.com/-/oauth_authorize\n          tokenUrl: https://app.asana.com/-/oauth_token\n          scopes:\n            default: Provides access to all endpoints documented in the API reference.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/asana/refs/heads/main/openapi/asana-rule-triggers-api-openapi.yml
tags: []
---
