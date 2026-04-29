---
aid: slack:slack-dnd-api
baseURL: https://slack.com/api
description: Slack's Do Not Disturb (DND) API lets apps read and manage users' notification quiet time so they don't get pinged when they've paused alerts. With the dnd:read and dnd:write scopes, an app can check a user's current DND state and scheduled quiet hours, retrieve team-wide DND summaries (where permitted), start or extend a snooze for a specified duration, and end snooze or active DND. Key methods include dnd.info, dnd.teamInfo, dnd.setSnooze, dnd.endSnooze, and dnd.endDnd.
humanURL: https://docs.slack.dev/reference/methods
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Slack DND API
properties:
- type: Documentation
  url: https://docs.slack.dev/reference/methods
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/slack/refs/heads/main/openapi/slack-dnd-openapi.yml
provider_name: Slack
provider_slug: slack
slug: slack-dnd-api
source_yaml: "aid: slack:slack-dnd-api\nname: Slack DND API\ntags:\n- Do Not Disturb\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://slack.com/api\nhumanURL: https://docs.slack.dev/reference/methods\nproperties:\n- url: https://docs.slack.dev/reference/methods\n  type: Documentation\n- url: openapi/slack-dnd-openapi.yml\n  type: OpenAPI\ndescription: Slack's Do Not Disturb (DND) API lets apps read and manage users' notification quiet time\n  so they don't get pinged when they've paused alerts. With the dnd:read and dnd:write scopes, an app\n  can check a user's current DND state and scheduled quiet hours, retrieve team-wide DND summaries (where\n  permitted), start or extend a snooze for a specified duration, and end snooze or active DND. Key methods\n  include dnd.info, dnd.teamInfo, dnd.setSnooze, dnd.endSnooze, and dnd.endDnd.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/slack/refs/heads/main/apis.yml
tags:
- Do Not Disturb
---
