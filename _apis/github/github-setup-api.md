---
aid: github:github-setup-api
baseURL: https://api.github.com/
description: The GitHub Setup API is the administrative interface for GitHub Enterprise Server that lets you automate tasks normally done in the Management Console during first-time and ongoing configuration. It provides endpoints to upload and apply your license, set the hostname and TLS certificates, configure system services like SMTP, create or reset the initial admin credentials, start and monitor reconfiguration runs, and query setup status and health.
humanURL: https://docs.github.com/en/rest/using-the-rest-api/getting-started-with-the-rest-api?apiVersion=2022-11-28
image: ''
layout: api
name: GitHub Setup API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-setup-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/rest/using-the-rest-api/getting-started-with-the-rest-api
provider_name: GitHub
provider_slug: github
slug: github-setup-api
source_yaml: "aid: github:github-setup-api\nname: GitHub Setup API\ntags:\n- Setup\nbaseURL: https://api.github.com/\nhumanURL: https://docs.github.com/en/rest/using-the-rest-api/getting-started-with-the-rest-api?apiVersion=2022-11-28\noverlays:\n- url: overlays/github-setup-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/github-setup-openapi.yml\n  type: OpenAPI\n- url: https://docs.github.com/en/rest/using-the-rest-api/getting-started-with-the-rest-api\n  type: Documentation\ndescription: The GitHub Setup API is the administrative interface for GitHub Enterprise Server that lets\n  you automate tasks normally done in the Management Console during first-time and ongoing configuration.\n  It provides endpoints to upload and apply your license, set the hostname and TLS certificates, configure\n  system services like SMTP, create or reset the initial admin credentials, start and monitor reconfiguration\n  runs, and query setup status and health.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/apis.yml
tags:
- Setup
---
