---
aid: github:github-networks-api
baseURL: https://api.github.com/
description: GitHubs Networks API lets you retrieve a stream of public activity that occurs across a repositorys network, meaning the original repo and all of its forks. Exposed via the Events API (for example, listing events for /networks/{owner}/{repo}/events), it returns the same event types you see in other GitHub event feedspushes, pull requests, issues, releases, and moreaggregated across every repo in that fork family.
humanURL: https://docs.github.com/en/rest?apiVersion=2022-11-28
image: ''
layout: api
name: GitHub Networks API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-networks-api-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/rest/activity/events
provider_name: GitHub
provider_slug: github
slug: github-networks-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: github:github-networks-api\nname: GitHub Networks API\ntags:\n- Networks\nbaseURL: https://api.github.com/\nhumanURL: https://docs.github.com/en/rest?apiVersion=2022-11-28\noverlays:\n- url: overlays/github-networks-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/github-networks-api-openapi.yml\n  type: OpenAPI\n- url: https://docs.github.com/en/rest/activity/events\n  type: Documentation\ndescription: GitHubs Networks API lets you retrieve a stream of public activity that occurs across a repositorys\n  network, meaning the original repo and all of its forks. Exposed via the Events API (for example, listing\n  events for /networks/{owner}/{repo}/events), it returns the same event types you see in other GitHub\n  event feedspushes, pull requests, issues, releases, and moreaggregated across every repo in that fork\n  family.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/apis.yml
tags:
- Networks
---
