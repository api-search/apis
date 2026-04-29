---
aid: github:github-teams-api
baseURL: https://api.github.com/
description: The GitHub Teams API lets you programmatically manage organization teams and the access they grant. With it, you can create, update, and delete teams; organize parent/child team hierarchies; add or remove members and maintainers; send and manage invitations; and list or audit team membership. It also lets you grant, adjust, or revoke a teams permissions to repositories (and, where applicable, projects), enabling consistent, leastprivilege access control at scale.
humanURL: https://docs.github.com/en/rest/teams?apiVersion=2022-11-28
image: ''
layout: api
name: GitHub Teams API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/openapi/github-teams-openapi.yml
- type: Documentation
  url: https://docs.github.com/en/rest/teams
provider_name: GitHub
provider_slug: github
slug: github-teams-api
source_yaml: "aid: github:github-teams-api\nname: GitHub Teams API\ntags:\n- Teams\nbaseURL: https://api.github.com/\nhumanURL: https://docs.github.com/en/rest/teams?apiVersion=2022-11-28\noverlays:\n- url: overlays/github-teams-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/github-teams-openapi.yml\n  type: OpenAPI\n- url: https://docs.github.com/en/rest/teams\n  type: Documentation\ndescription: The GitHub Teams API lets you programmatically manage organization teams and the access they\n  grant. With it, you can create, update, and delete teams; organize parent/child team hierarchies; add\n  or remove members and maintainers; send and manage invitations; and list or audit team membership. It\n  also lets you grant, adjust, or revoke a teams permissions to repositories (and, where applicable, projects),\n  enabling consistent, leastprivilege access control at scale.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github/refs/heads/main/apis.yml
tags:
- Teams
---
