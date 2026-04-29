---
aid: github:github-zen-api
baseURL: ''
description: The GitHub Zen API is a playful REST endpoint that returns a random aphorism from the Zen of GitHub, such as Keep it logically awesome. Each request to GET https://api.github.com/zen responds with a single plain-text line, making it useful for quick connectivity checks, demoing HTTP calls, or verifying authentication. It doesnt require auth, but you can include a token to benefit from higher rate limits.
humanURL: ''
image: ''
layout: api
name: GitHub Zen API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-zen-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/rest/meta/meta
provider_name: GitHub
provider_slug: github
slug: github-zen-api
source_yaml: "aid: github:github-zen-api\nname: GitHub Zen API\ntags:\n- Zen\noverlays:\n- url: overlays/github-zen-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/github-zen-openapi.yml\n  type: OpenAPI\n- url: https://docs.github.com/en/rest/meta/meta\n  type: Documentation\ndescription: The GitHub Zen API is a playful REST endpoint that returns a random aphorism from the Zen\n  of GitHub, such as Keep it logically awesome. Each request to GET https://api.github.com/zen responds\n  with a single plain-text line, making it useful for quick connectivity checks, demoing HTTP calls, or\n  verifying authentication. It doesnt require auth, but you can include a token to benefit from higher\n  rate limits.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/apis.yml
tags:
- Zen
---
