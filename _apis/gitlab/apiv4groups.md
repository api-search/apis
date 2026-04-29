---
aid: gitlab:apiv4groups
baseURL: https://gitlab.com/api/v4
description: The GitLab Groups API allows you to create, read, update, and delete groups and subgroups. Groups are used to manage access control and organize projects within a GitLab instance, enabling teams to collaborate with shared access permissions and settings.
humanURL: https://docs.gitlab.com/api/groups/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Groups API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-groups-openapi-original.yml
- type: Documentation
  url: https://docs.gitlab.com/api/groups/
- type: Authentication
  url: https://docs.gitlab.com/api/rest/authentication/
provider_name: GitLab
provider_slug: gitlab
slug: apiv4groups
source_yaml: "aid: gitlab:apiv4groups\nname: GitLab Groups API\ntags:\n- Access Control\n- Groups\n- Organizations\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://gitlab.com/api/v4\nhumanURL: https://docs.gitlab.com/api/groups/\noverlays:\n- url: overlays/gitlab-api-v4-groups-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/gitlab-api-v4-groups-openapi-original.yml\n  type: OpenAPI\n- url: https://docs.gitlab.com/api/groups/\n  type: Documentation\n- url: https://docs.gitlab.com/api/rest/authentication/\n  type: Authentication\ndescription: The GitLab Groups API allows you to create, read, update, and delete groups and subgroups.\n  Groups are used to manage access control and organize projects within a GitLab instance, enabling teams\n  to collaborate with shared access permissions and settings.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/apis.yml
tags:
- Access Control
- Groups
- Organizations
---
