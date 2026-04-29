---
aid: github:github-scim-api
baseURL: https://api.github.com/
description: GitHubs SCIM API implements the SCIM 2.0 standard to automate user lifecycle management from an identity provider (such as Entra ID/Azure AD, Okta, or OneLogin) to GitHub Enterprise Cloud. It lets you provision, update, suspend/reactivate, and deprovision users, keeping their GitHub access in sync with your IdP.
humanURL: '

  https://docs.github.com/en/enterprise-cloud@latest/rest/scim?apiVersion=2022-11-28'
image: ''
layout: api
name: GitHub SCIM API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-scim-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/enterprise-cloud@latest/rest/scim
provider_name: GitHub
provider_slug: github
slug: github-scim-api
source_yaml: "aid: github:github-scim-api\nname: GitHub SCIM API\ntags:\n- SCIM\nbaseURL: https://api.github.com/\nhumanURL: '\n\n  https://docs.github.com/en/enterprise-cloud@latest/rest/scim?apiVersion=2022-11-28'\noverlays:\n- url: overlays/github-scim-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/github-scim-openapi.yml\n  type: OpenAPI\n- url: https://docs.github.com/en/enterprise-cloud@latest/rest/scim\n  type: Documentation\ndescription: GitHubs SCIM API implements the SCIM 2.0 standard to automate user lifecycle management from\n  an identity provider (such as Entra ID/Azure AD, Okta, or OneLogin) to GitHub Enterprise Cloud. It lets\n  you provision, update, suspend/reactivate, and deprovision users, keeping their GitHub access in sync\n  with your IdP.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/apis.yml
tags:
- SCIM
---
