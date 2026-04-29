---
aid: github:github-org-api
baseURL: https://api.github.com/
description: The GitHub Organization API lets you programmatically administer and integrate with organizations on GitHub, spanning both REST and GraphQL. It covers core governance tasks such as reading and updating org settings and policies, managing members and outside collaborators, sending invitations and assigning roles, organizing teams and their permissions, and controlling repository access at scale.
humanURL: https://docs.github.com/en/rest/orgs?apiVersion=2022-11-28
image: ''
layout: api
name: GitHub Organization API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-org-api-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/rest/orgs
provider_name: GitHub
provider_slug: github
slug: github-org-api
source_yaml: "aid: github:github-org-api\nname: GitHub Organization API\ntags:\n- Organizations\nbaseURL: https://api.github.com/\nhumanURL: https://docs.github.com/en/rest/orgs?apiVersion=2022-11-28\noverlays:\n- url: overlays/github-org-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/github-org-api-openapi.yml\n  type: OpenAPI\n- url: https://docs.github.com/en/rest/orgs\n  type: Documentation\ndescription: The GitHub Organization API lets you programmatically administer and integrate with organizations\n  on GitHub, spanning both REST and GraphQL. It covers core governance tasks such as reading and updating\n  org settings and policies, managing members and outside collaborators, sending invitations and assigning\n  roles, organizing teams and their permissions, and controlling repository access at scale.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/apis.yml
tags:
- Organizations
---
