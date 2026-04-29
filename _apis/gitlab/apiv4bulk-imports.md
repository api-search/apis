---
aid: gitlab:apiv4bulk-imports
baseURL: https://gitlab.com/api/v4
description: The GitLab Bulk Imports API enables migration of groups and projects between GitLab instances. It provides endpoints for initiating bulk import operations and tracking their progress, facilitating large-scale data migrations between GitLab environments.
humanURL: https://docs.gitlab.com/api/bulk_imports/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Bulk Imports API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-bulk-imports-openapi-original.yml
- type: Documentation
  url: https://docs.gitlab.com/api/bulk_imports/
provider_name: GitLab
provider_slug: gitlab
slug: apiv4bulk-imports
source_yaml: "aid: gitlab:apiv4bulk-imports\nname: GitLab Bulk Imports API\ntags:\n- Bulk Imports\n- Data Transfer\n- Migration\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://gitlab.com/api/v4\nhumanURL: https://docs.gitlab.com/api/bulk_imports/\noverlays:\n- url: overlays/gitlab-api-v4-bulk-imports-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/gitlab-api-v4-bulk-imports-openapi-original.yml\n  type: OpenAPI\n- url: https://docs.gitlab.com/api/bulk_imports/\n  type: Documentation\ndescription: The GitLab Bulk Imports API enables migration of groups and projects between GitLab instances.\n  It provides endpoints for initiating bulk import operations and tracking their progress, facilitating\n  large-scale data migrations between GitLab environments.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/apis.yml
tags:
- Bulk Imports
- Data Transfer
- Migration
---
