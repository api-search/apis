---
aid: gitlab:apiv4application
baseURL: https://gitlab.com/api/v4
description: The GitLab Application Settings API provides access to instance-wide configuration settings for a GitLab installation. Administrators can retrieve and modify application settings such as sign-up restrictions, default project visibility, and other instance-level preferences.
humanURL: https://docs.gitlab.com/api/settings/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Application Settings API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-application-openapi-original.yml
- type: Documentation
  url: https://docs.gitlab.com/api/settings/
provider_name: GitLab
provider_slug: gitlab
slug: apiv4application
source_yaml: "aid: gitlab:apiv4application\nname: GitLab Application Settings API\ntags:\n- Administration\n- Application Settings\n- Configuration\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://gitlab.com/api/v4\nhumanURL: https://docs.gitlab.com/api/settings/\noverlays:\n- url: overlays/gitlab-api-v4-application-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/gitlab-api-v4-application-openapi-original.yml\n  type: OpenAPI\n- url: https://docs.gitlab.com/api/settings/\n  type: Documentation\ndescription: The GitLab Application Settings API provides access to instance-wide configuration settings\n  for a GitLab installation. Administrators can retrieve and modify application settings such as sign-up\n  restrictions, default project visibility, and other instance-level preferences.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/apis.yml
tags:
- Administration
- Application Settings
- Configuration
---
