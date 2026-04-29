---
aid: gitlab:apiv4applications
baseURL: https://gitlab.com/api/v4
description: The GitLab Applications API allows you to manage OAuth applications registered in GitLab. You can create, list, and delete OAuth applications that enable third-party services to access GitLab resources on behalf of users using the OAuth 2.0 protocol.
humanURL: https://docs.gitlab.com/api/applications/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Applications API
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-applications-openapi-original.yml
- type: Documentation
  url: https://docs.gitlab.com/api/applications/
provider_name: GitLab
provider_slug: gitlab
slug: apiv4applications
source_yaml: "aid: gitlab:apiv4applications\nname: GitLab Applications API\ntags:\n- Applications\n- Authentication\n- OAuth\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://gitlab.com/api/v4\nhumanURL: https://docs.gitlab.com/api/applications/\noverlays:\n- url: overlays/gitlab-api-v4-applications-openapi-search.yml\n  type: OpenAPI\nproperties:\n- url: openapi/gitlab-api-v4-applications-openapi-original.yml\n  type: OpenAPI\n- url: https://docs.gitlab.com/api/applications/\n  type: Documentation\ndescription: The GitLab Applications API allows you to manage OAuth applications registered in GitLab.\n  You can create, list, and delete OAuth applications that enable third-party services to access GitLab\n  resources on behalf of users using the OAuth 2.0 protocol.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/apis.yml
tags:
- Applications
- Authentication
- OAuth
---
