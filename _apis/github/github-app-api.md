---
aid: github:github-app-api
baseURL: https://api.github.com
description: The GitHub App API is the set of REST/GraphQL endpoints and webhooks that lets a GitHub App securely integrate with and automate work across GitHub. Apps authenticate with a shortlived JSON Web Token and exchange it for installation access tokens to act on specific repositories or organizations with finegrained, leastprivilege permissions, or use user-to-server OAuth to act on behalf of a user when needed.
humanURL: https://docs.github.com/en/rest/apps?apiVersion=2022-11-28
image: ''
layout: api
name: GitHub App API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-app-api-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/rest/apps
provider_name: GitHub
provider_slug: github
slug: github-app-api
source_yaml: "aid: github:github-app-api\nname: GitHub App API\ntags:\n- Applications\nbaseURL: https://api.github.com\nhumanURL: https://docs.github.com/en/rest/apps?apiVersion=2022-11-28\noverlays:\n- url: overlays/github-app-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/github-app-api-openapi.yml\n  type: OpenAPI\n- url: https://docs.github.com/en/rest/apps\n  type: Documentation\ndescription: The GitHub App API is the set of REST/GraphQL endpoints and webhooks that lets a GitHub App\n  securely integrate with and automate work across GitHub. Apps authenticate with a shortlived JSON Web\n  Token and exchange it for installation access tokens to act on specific repositories or organizations\n  with finegrained, leastprivilege permissions, or use user-to-server OAuth to act on behalf of a user\n  when needed.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/apis.yml
tags:
- Applications
---
