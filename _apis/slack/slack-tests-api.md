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
source_yaml: "aid: slack:slack-tests-api\nname: Slack Tests API\ntags:\n- Tests\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://slack.com/api\nhumanURL: https://docs.slack.dev/reference/methods\nproperties:\n- url: https://docs.slack.dev/reference/methods\n  type: Documentation\n- url: openapi/slack-test-api-openapi.yml\n  type: OpenAPI\ndescription: I'm not aware of an official Slack product literally called Tests API. Typically, when people\n  say Slack Tests API, they mean using Slack's existing APIs and SDK tooling to automate tests for Slack\n  apps. In practice, developers call Slack's Web API to set up test data (channels, users, messages),\n  craft Events API and interactive payloads to exercise handlers, and use SDK-provided mocks to assert\n  responses and error handling in CI.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/slack/refs/heads/main/apis.yml
tags:
- Tests
---
