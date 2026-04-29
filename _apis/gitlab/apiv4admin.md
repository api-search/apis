---
aid: gitlab:apiv4admin
baseURL: https://gitlab.com/api/v4
description: The GitLab Admin API provides administrative endpoints for managing a GitLab instance. It includes operations for managing runners, CI/CD variables, Sidekiq queues, and other instance-level administrative tasks that require administrator privileges.
humanURL: https://docs.gitlab.com/api/admin/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Admin API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-admin-openapi-original.yml
- type: Documentation
  url: https://docs.gitlab.com/api/admin/
provider_name: GitLab
provider_slug: gitlab
slug: apiv4admin
source_yaml: "aid: gitlab:apiv4admin\nname: GitLab Admin API\ntags:\n- Admin\n- Administration\n- Management\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://gitlab.com/api/v4\nhumanURL: https://docs.gitlab.com/api/admin/\noverlays:\n- url: overlays/gitlab-api-v4-admin-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/gitlab-api-v4-admin-openapi-original.yml\n  type: OpenAPI\n- url: https://docs.gitlab.com/api/admin/\n  type: Documentation\ndescription: The GitLab Admin API provides administrative endpoints for managing a GitLab instance. It\n  includes operations for managing runners, CI/CD variables, Sidekiq queues, and other instance-level\n  administrative tasks that require administrator privileges.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/apis.yml
tags:
- Admin
- Administration
- Management
---
