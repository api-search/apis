---
aid: github:github-feeds-api
baseURL: https://api.github.com/
description: GitHubs Feeds API lets you programmatically discover the Atom feed URLs for GitHub activity thats relevant to you, such as the global timeline, a specific users activity, the authenticated users public and private activity, organization activity, and security advisories.
humanURL: https://docs.github.com/en/rest/activity/feeds?apiVersion=2022-11-28
image: ''
layout: api
name: GitHub Feeds API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-feeds-api-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/rest/activity/feeds
provider_name: GitHub
provider_slug: github
slug: github-feeds-api
source_yaml: "aid: github:github-feeds-api\nname: GitHub Feeds API\ntags:\n- Feeds\nbaseURL: https://api.github.com/\nhumanURL: https://docs.github.com/en/rest/activity/feeds?apiVersion=2022-11-28\noverlays:\n- url: overlays/github-feeds-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/github-feeds-api-openapi.yml\n  type: OpenAPI\n- url: https://docs.github.com/en/rest/activity/feeds\n  type: Documentation\ndescription: GitHubs Feeds API lets you programmatically discover the Atom feed URLs for GitHub activity\n  thats relevant to you, such as the global timeline, a specific users activity, the authenticated users\n  public and private activity, organization activity, and security advisories.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/apis.yml
tags:
- Feeds
---
