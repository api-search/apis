---
aid: github:github-meta-api
baseURL: https://api.github.com/
description: Use the REST API to get meta information about GitHub, including the IP addresses of GitHub services.
humanURL: https://docs.github.com/en/rest/meta?apiVersion=2022-11-28
image: ''
layout: api
name: GitHub Meta API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-meta-api-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/rest/meta
provider_name: GitHub
provider_slug: github
slug: github-meta-api
source_yaml: "aid: github:github-meta-api\nname: GitHub Meta API\ntags:\n- Metadata\nbaseURL: https://api.github.com/\nhumanURL: https://docs.github.com/en/rest/meta?apiVersion=2022-11-28\noverlays:\n- url: overlays/github-meta-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/github-meta-api-openapi.yml\n  type: OpenAPI\n- url: https://docs.github.com/en/rest/meta\n  type: Documentation\ndescription: Use the REST API to get meta information about GitHub, including the IP addresses of GitHub\n  services.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/apis.yml
tags:
- Metadata
---
