---
aid: github:github-notifications-api
baseURL: https://api.github.com/
description: This GitHub REST API allows you to programmatically manage your GitHub notifications, which include updates on issues, pull requests, and commits. The API requires authentication via a personal access token (classic) and needs either the notifications or repo scope to function.
humanURL: '

  https://docs.github.com/en/rest/activity/notifications?apiVersion=2022-11-28'
image: ''
layout: api
name: GitHub Notifications API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-notifications-api-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/rest/activity/notifications
provider_name: GitHub
provider_slug: github
slug: github-notifications-api
source_yaml: "aid: github:github-notifications-api\nname: GitHub Notifications API\ntags:\n- Notifications\nbaseURL: https://api.github.com/\nhumanURL: '\n\n  https://docs.github.com/en/rest/activity/notifications?apiVersion=2022-11-28'\noverlays:\n- url: overlays/github-notifications-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/github-notifications-api-openapi.yml\n  type: OpenAPI\n- url: https://docs.github.com/en/rest/activity/notifications\n  type: Documentation\ndescription: This GitHub REST API allows you to programmatically manage your GitHub notifications, which\n  include updates on issues, pull requests, and commits. The API requires authentication via a personal\n  access token (classic) and needs either the notifications or repo scope to function.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/apis.yml
tags:
- Notifications
---
