---
aid: gitlab:apiv4metadata
baseURL: https://gitlab.com/api/v4
description: The GitLab Metadata API provides information about the GitLab instance, including the version, revision, and other metadata about the running installation. It is useful for verifying connectivity and identifying the version of a GitLab instance programmatically.
humanURL: https://docs.gitlab.com/api/metadata/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Metadata API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-metadata-openapi-original.yml
- type: Documentation
  url: https://docs.gitlab.com/api/metadata/
provider_name: GitLab
provider_slug: gitlab
slug: apiv4metadata
source_yaml: "aid: gitlab:apiv4metadata\nname: GitLab Metadata API\ntags:\n- Instance Information\n- Metadata\n- System\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://gitlab.com/api/v4\nhumanURL: https://docs.gitlab.com/api/metadata/\noverlays:\n- url: overlays/gitlab-api-v4-metadata-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/gitlab-api-v4-metadata-openapi-original.yml\n  type: OpenAPI\n- url: https://docs.gitlab.com/api/metadata/\n  type: Documentation\ndescription: The GitLab Metadata API provides information about the GitLab instance, including the version,\n  revision, and other metadata about the running installation. It is useful for verifying connectivity\n  and identifying the version of a GitLab instance programmatically.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/apis.yml
tags:
- Instance Information
- Metadata
- System
---
