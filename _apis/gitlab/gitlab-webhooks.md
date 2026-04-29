---
aid: gitlab:gitlab-webhooks
baseURL: https://gitlab.com/api/v4
description: GitLab Webhooks allow you to receive real-time HTTP POST notifications when events occur in GitLab projects or groups. Webhooks can be configured to trigger on events such as push events, merge requests, issues, comments, and pipeline status changes, enabling integrations with external systems.
humanURL: https://docs.gitlab.com/user/project/integrations/webhooks.html
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: GitLab Webhooks
properties:
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-webhooks-openapi.yml
- type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/asyncapi/gitlab-webhooks-asyncapi.yml
- type: Documentation
  url: https://docs.gitlab.com/user/project/integrations/webhooks.html
- type: APIReference
  url: https://docs.gitlab.com/api/project_webhooks/
provider_name: GitLab
provider_slug: gitlab
slug: gitlab-webhooks
source_yaml: "aid: gitlab:gitlab-webhooks\nname: GitLab Webhooks\ntags:\n- Events\n- Integrations\n- Webhooks\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://gitlab.com/api/v4\nhumanURL: https://docs.gitlab.com/user/project/integrations/webhooks.html\noverlays: []\nproperties:\n- url: openapi/gitlab-webhooks-openapi.yml\n  type: OpenAPI\n- url: asyncapi/gitlab-webhooks-asyncapi.yml\n  type: AsyncAPI\n- url: https://docs.gitlab.com/user/project/integrations/webhooks.html\n  type: Documentation\n- url: https://docs.gitlab.com/api/project_webhooks/\n  type: APIReference\ndescription: GitLab Webhooks allow you to receive real-time HTTP POST notifications when events occur\n  in GitLab projects or groups. Webhooks can be configured to trigger on events such as push events, merge\n  requests, issues, comments, and pipeline status changes, enabling integrations with external systems.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/apis.yml
tags:
- Events
- Integrations
- Webhooks
---
