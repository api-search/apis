---
aid: github:github-octocat-api
baseURL: https://api.github.com/
description: The GitHub Octocat API is a playful, non-functional endpoint in GitHubs REST API that returns an ASCII-art rendering of the Octocat mascot as plain text. Its primarily meant for fun and demospeople often use it to sanity-check connectivity, see how the API formats responses and headers, or showcase simple requests without touching real repository data. It doesnt manage or expose any GitHub resources, and in some clients you can even supply a short message that the Octocat says.
humanURL: https://github.com/octokit/octokit.js
image: ''
layout: api
name: GitHub Octocat API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-octocat-api-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/rest/meta/meta
provider_name: GitHub
provider_slug: github
slug: github-octocat-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: github:github-octocat-api\nname: GitHub Octocat API\ntags:\n- Octocat\nbaseURL: https://api.github.com/\nhumanURL: https://github.com/octokit/octokit.js\noverlays:\n- url: overlays/github-octocat-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/github-octocat-api-openapi.yml\n  type: OpenAPI\n- url: https://docs.github.com/en/rest/meta/meta\n  type: Documentation\ndescription: The GitHub Octocat API is a playful, non-functional endpoint in GitHubs REST API that returns\n  an ASCII-art rendering of the Octocat mascot as plain text. Its primarily meant for fun and demospeople\n  often use it to sanity-check connectivity, see how the API formats responses and headers, or showcase\n  simple requests without touching real repository data. It doesnt manage or expose any GitHub resources,\n  and in some clients you can even supply a short message that the Octocat says.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/apis.yml
tags:
- Octocat
---
