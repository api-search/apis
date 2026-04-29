---
aid: slack:slack-emoji-api
baseURL: https://slack.com/api
description: Slack's Emoji API lets apps discover and manage a workspace's custom emoji. The core method, emoji.list (requires the emoji:read scope), returns a name-to-URL map of all custom emoji along with aliases (noted as alias:other_name) and a cache timestamp to help clients sync efficiently. Apps can also subscribe to the emoji_changed event to stay up to date when emoji are added, renamed, or removed.
humanURL: https://docs.slack.dev/reference/methods
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Slack Emoji API
properties:
- type: Documentation
  url: https://docs.slack.dev/reference/methods
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/slack/refs/heads/main/openapi/slack-emoji-openapi.yml
provider_name: Slack
provider_slug: slack
slug: slack-emoji-api
source_yaml: "aid: slack:slack-emoji-api\nname: Slack Emoji API\ntags:\n- Emoji\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://slack.com/api\nhumanURL: https://docs.slack.dev/reference/methods\nproperties:\n- url: https://docs.slack.dev/reference/methods\n  type: Documentation\n- url: openapi/slack-emoji-openapi.yml\n  type: OpenAPI\ndescription: Slack's Emoji API lets apps discover and manage a workspace's custom emoji. The core method,\n  emoji.list (requires the emoji:read scope), returns a name-to-URL map of all custom emoji along with\n  aliases (noted as alias:other_name) and a cache timestamp to help clients sync efficiently. Apps can\n  also subscribe to the emoji_changed event to stay up to date when emoji are added, renamed, or removed.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/slack/refs/heads/main/apis.yml
tags:
- Emoji
---
