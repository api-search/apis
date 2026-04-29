---
aid: gitlab:apiv4avatar
baseURL: https://gitlab.com/api/v4
description: The GitLab Avatar API allows you to retrieve avatar images for users and groups. It returns avatar URLs based on user email addresses, enabling applications to display profile images for GitLab users without requiring authentication.
humanURL: https://docs.gitlab.com/api/avatar/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Avatar API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-avatar-openapi-original.yml
- type: Documentation
  url: https://docs.gitlab.com/api/avatar/
provider_name: GitLab
provider_slug: gitlab
slug: apiv4avatar
source_yaml: "aid: gitlab:apiv4avatar\nname: GitLab Avatar API\ntags:\n- Avatars\n- Profile\n- Users\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://gitlab.com/api/v4\nhumanURL: https://docs.gitlab.com/api/avatar/\noverlays:\n- url: overlays/gitlab-api-v4-avatar-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/gitlab-api-v4-avatar-openapi-original.yml\n  type: OpenAPI\n- url: https://docs.gitlab.com/api/avatar/\n  type: Documentation\ndescription: The GitLab Avatar API allows you to retrieve avatar images for users and groups. It returns\n  avatar URLs based on user email addresses, enabling applications to display profile images for GitLab\n  users without requiring authentication.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/apis.yml
tags:
- Avatars
- Profile
- Users
---
