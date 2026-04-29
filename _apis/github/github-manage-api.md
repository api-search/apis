---
aid: github:github-manage-api
baseURL: https://api.github.com/
description: The GitHub Enterprise Management API lets administrators automate and integrate the operational and security management of their enterprise on GitHub. It covers tasks like provisioning and governing organizations, users, and teams; enforcing policies for repositories, security, and GitHub Actions; integrating identity and access management via SSO/SCIM; retrieving audit logs and usage data for compliance and billing; and managing self-hosted runners.
humanURL: https://docs.github.com/en/rest?apiVersion=2022-11-28
image: ''
layout: api
name: GitHub Enterprise Management API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-manage-api-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/rest/enterprise-admin
provider_name: GitHub
provider_slug: github
slug: github-manage-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: github:github-manage-api\nname: GitHub Enterprise Management API\ntags:\n- Management\nbaseURL: https://api.github.com/\nhumanURL: https://docs.github.com/en/rest?apiVersion=2022-11-28\noverlays:\n- url: overlays/github-manage-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/github-manage-api-openapi.yml\n  type: OpenAPI\n- url: https://docs.github.com/en/rest/enterprise-admin\n  type: Documentation\ndescription: The GitHub Enterprise Management API lets administrators automate and integrate the operational\n  and security management of their enterprise on GitHub. It covers tasks like provisioning and governing\n  organizations, users, and teams; enforcing policies for repositories, security, and GitHub Actions;\n  integrating identity and access management via SSO/SCIM; retrieving audit logs and usage data for compliance\n  and billing; and managing self-hosted runners.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/apis.yml
tags:
- Management
---
