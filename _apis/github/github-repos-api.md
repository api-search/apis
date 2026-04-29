---
aid: github:github-repos-api
baseURL: https://api.github.com/
description: The GitHub Repos API is a set of REST endpoints that let you programmatically create, read, update, and delete repositories and their resources, giving you control over a repos lifecycle and configuration.
humanURL: https://docs.github.com/en/rest/repos?apiVersion=2022-11-28
image: ''
layout: api
name: GitHub Repos API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-repos-api-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/rest/repos
provider_name: GitHub
provider_slug: github
slug: github-repos-api
source_yaml: "aid: github:github-repos-api\nname: GitHub Repos API\ntags:\n- Repos\nbaseURL: https://api.github.com/\nhumanURL: https://docs.github.com/en/rest/repos?apiVersion=2022-11-28\noverlays:\n- url: overlays/github-repos-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/github-repos-api-openapi.yml\n  type: OpenAPI\n- url: https://docs.github.com/en/rest/repos\n  type: Documentation\ndescription: The GitHub Repos API is a set of REST endpoints that let you programmatically create, read,\n  update, and delete repositories and their resources, giving you control over a repos lifecycle and configuration.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/apis.yml
tags:
- Repos
---
