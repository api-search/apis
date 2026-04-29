---
aid: slack:slack-tests-api
baseURL: https://slack.com/api
description: I'm not aware of an official Slack product literally called Tests API. Typically, when people say Slack Tests API, they mean using Slack's existing APIs and SDK tooling to automate tests for Slack apps. In practice, developers call Slack's Web API to set up test data (channels, users, messages), craft Events API and interactive payloads to exercise handlers, and use SDK-provided mocks to assert responses and error handling in CI.
humanURL: https://docs.slack.dev/reference/methods
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Slack Tests API
properties:
- type: Documentation
  url: https://docs.slack.dev/reference/methods
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/slack/refs/heads/main/openapi/slack-test-api-openapi.yml
provider_name: Slack
provider_slug: slack
slug: slack-tests-api
source_filename: slack-test-api-openapi.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Slack Tests API\n  description: \"I\\x19m not aware of an official Slack product literally called \\x1CTests API.\\x1D Typically, when people say \\x1CSlack Tests API,\\x1D they mean using Slack\\x19s existing APIs and SDK tooling\n    to automate tests for Slack apps. In practice, developers call Slack\\x19s Web API to set up test data (channels, users, messages), craft Events API and interactive payloads to exercise handlers, and\n    use SDK-provided mocks to assert responses and error handling in CI. This approach lets teams verify permissions, rate-limit behavior, and message/Block Kit rendering, so bots, workflows, and functions\n    behave correctly before deployment. If you meant a specific third-party tool or a particular Slack feature by that name, let me know and I can tailor the description.\"\npaths:\n  /api.test:\n    get:\n      tags:\n      - Get\n      - Tests\n      description: Checks API calling code.\n      externalDocs:\n\
  \        description: API method documentation\n        url: https://api.slack.com/methods/api.test\n      operationId: getApiTest\n      parameters:\n      - name: error\n        in: query\n        description: Error response to return\n        schema:\n          type: string\n      - name: foo\n        in: query\n        description: example property to return\n        schema:\n          type: string\n      responses:\n        '200':\n          description: Standard success response\n          content:\n            application/json:\n              schema:\n                title: api.test success schema\n                required:\n                - ok\n                type: object\n                properties:\n                  ok:\n                    $ref: '#/components/schemas/defs_ok_true'\n                additionalProperties:\n                  type: object\n                  properties: {}\n                description: Schema for successful response api.test method\n          \
  \    example:\n                ok: true\n        default:\n          description: Artificial error response\n          content:\n            application/json:\n              schema:\n                title: api.test error schema\n                required:\n                - error\n                - ok\n                type: object\n                properties:\n                  error:\n                    type: string\n                  ok:\n                    $ref: '#/components/schemas/defs_ok_false'\n                additionalProperties:\n                  type: object\n                  properties: {}\n                description: Schema for error response api.test method\n              example:\n                args:\n                  error: my_error\n                error: my_error\n                ok: false\n      security:\n      - slackAuth:\n        - none\n      summary: Slack Get Api Test\n      x-api-evangelist-processing:\n        GenerateOperationSummariesFromPath: true\n\
  \        PascalCaseOperationSummaries: true\n        CaselCaseOperationIds: true\n        PullTagsFromSummary: true\n        ChooseTags: true\n      x-microcks-operation:\n        delay: 0\n        dispatcher: FALLBACK\ncomponents:\n  schemas: {}\ntags:\n- name: Get\n- name: Tests\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/slack/refs/heads/main/openapi/slack-test-api-openapi.yml
tags:
- Tests
---
