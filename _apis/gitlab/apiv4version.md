---
aid: gitlab:apiv4version
baseURL: https://gitlab.com/api/v4
description: The GitLab Version API returns version and revision information for the GitLab instance. This endpoint is useful for verifying what version of GitLab is running and for checking compatibility with specific API features before making requests.
humanURL: https://docs.gitlab.com/api/version/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Version API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-version-openapi-original.yml
- type: Documentation
  url: https://docs.gitlab.com/api/version/
provider_name: GitLab
provider_slug: gitlab
slug: apiv4version
source_yaml: "aid: gitlab:apiv4version\nname: GitLab Version API\ntags:\n- Instance Information\n- System\n- Version\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://gitlab.com/api/v4\nhumanURL: https://docs.gitlab.com/api/version/\noverlays:\n- url: overlays/gitlab-api-v4-version-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/gitlab-api-v4-version-openapi-original.yml\n  type: OpenAPI\n- url: https://docs.gitlab.com/api/version/\n  type: Documentation\ndescription: The GitLab Version API returns version and revision information for the GitLab instance.\n  This endpoint is useful for verifying what version of GitLab is running and for checking compatibility\n  with specific API features before making requests.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/apis.yml
tags:
- Instance Information
- System
- Version
---
