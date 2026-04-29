---
aid: zendesk:sessions
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Sessions API lets you audit and control users active sign-in sessions in your Zendesk account. It provides endpoints to list current sessions (for the authenticated user or a specified user) and returns metadata such as device/user agent, IP, creation time, and last activity. You can revoke an individual session or all sessions for a user to force logouts across Zendesk web and mobile experiencesuseful for security incidents, offboarding, and SSO changes.
humanURL: https://developer.zendesk.com/api-reference/ticketing/account-configuration/sessions/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Sessions API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/account-configuration/sessions/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/sessions-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: sessions
source_yaml: "aid: zendesk:sessions\nname: Zendesk Sessions API\ntags:\n- Sessions\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://{subdomain}.zendesk.com\nhumanURL: https://developer.zendesk.com/api-reference/ticketing/account-configuration/sessions/\nproperties:\n- url: https://developer.zendesk.com/api-reference/ticketing/account-configuration/sessions/\n  type: Documentation\n- url: openapi/sessions-openapi-original.yml\n  type: OpenAPI\ndescription: The Zendesk Sessions API lets you audit and control users active sign-in sessions in your\n  Zendesk account. It provides endpoints to list current sessions (for the authenticated user or a specified\n  user) and returns metadata such as device/user agent, IP, creation time, and last activity. You can\n  revoke an individual session or all sessions for a user to force logouts across Zendesk web and mobile\n  experiencesuseful for security incidents, offboarding, and SSO changes.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/apis.yml
tags:
- Sessions
---
