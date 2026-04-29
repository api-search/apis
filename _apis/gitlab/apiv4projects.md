---
aid: gitlab:apiv4projects
baseURL: https://gitlab.com/api/v4
description: The GitLab Projects API provides programmatic access to GitLab projects, enabling you to create, list, update, and delete projects. It supports managing project settings, members, forks, stars, and other project-level resources across GitLab.com and self-managed instances.
humanURL: https://docs.gitlab.com/api/projects/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Projects API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-projects-openapi-original.yml
- type: Documentation
  url: https://docs.gitlab.com/api/projects/
- type: Authentication
  url: https://docs.gitlab.com/api/rest/authentication/
provider_name: GitLab
provider_slug: gitlab
slug: apiv4projects
source_yaml: "aid: gitlab:apiv4projects\nname: GitLab Projects API\ntags:\n- Projects\n- Repositories\n- Source Control\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://gitlab.com/api/v4\nhumanURL: https://docs.gitlab.com/api/projects/\noverlays:\n- url: overlays/gitlab-api-v4-projects-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/gitlab-api-v4-projects-openapi-original.yml\n  type: OpenAPI\n- url: https://docs.gitlab.com/api/projects/\n  type: Documentation\n- url: https://docs.gitlab.com/api/rest/authentication/\n  type: Authentication\ndescription: The GitLab Projects API provides programmatic access to GitLab projects, enabling you to\n  create, list, update, and delete projects. It supports managing project settings, members, forks, stars,\n  and other project-level resources across GitLab.com and self-managed instances.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/apis.yml
tags:
- Projects
- Repositories
- Source Control
---
