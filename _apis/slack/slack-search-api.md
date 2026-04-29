---
aid: slack:slack-search-api
baseURL: https://slack.com/api
description: Slack's Search API lets apps programmatically find messages and files in a workspace using the same query syntax users have in Slack (e.g., in:, from:, has:, before:/after:, is:thread). Through endpoints like search.messages and search.files, it returns ranked matches with snippets and optional highlighting, plus rich metadata such as channel, timestamps, user, thread context, permalinks, and file details. You can sort by relevance or time, filter with operators, and page through results.
humanURL: https://docs.slack.dev/reference/methods
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Slack Search API
properties:
- type: Documentation
  url: https://docs.slack.dev/reference/methods
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/slack/refs/heads/main/openapi/slack-search-openapi.yml
provider_name: Slack
provider_slug: slack
slug: slack-search-api
source_yaml: "aid: slack:slack-search-api\nname: Slack Search API\ntags:\n- Search\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://slack.com/api\nhumanURL: https://docs.slack.dev/reference/methods\nproperties:\n- url: https://docs.slack.dev/reference/methods\n  type: Documentation\n- url: openapi/slack-search-openapi.yml\n  type: OpenAPI\ndescription: Slack's Search API lets apps programmatically find messages and files in a workspace using\n  the same query syntax users have in Slack (e.g., in:, from:, has:, before:/after:, is:thread). Through\n  endpoints like search.messages and search.files, it returns ranked matches with snippets and optional\n  highlighting, plus rich metadata such as channel, timestamps, user, thread context, permalinks, and\n  file details. You can sort by relevance or time, filter with operators, and page through results.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/slack/refs/heads/main/apis.yml
tags:
- Search
---
