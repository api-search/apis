---
aid: zendesk:oauth
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk OAuth API implements the OAuth 2.0 standard to let apps securely access Zendesk data on a users or accounts behalf without sharing passwords. Developers register an OAuth client in a Zendesk account, redirect users to Zendesk for signin and consent, and exchange the returned authorization code for access (and optionally refresh) tokens.
humanURL: https://developer.zendesk.com/api-reference/ticketing/oauth/oauth_tokens/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Oauth API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/oauth/oauth_tokens/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/oauth-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: oauth
source_yaml: "aid: zendesk:oauth\nname: Zendesk Oauth API\ntags:\n- Authentication\n- Authorization\n- Oauth\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://{subdomain}.zendesk.com\nhumanURL: https://developer.zendesk.com/api-reference/ticketing/oauth/oauth_tokens/\nproperties:\n- url: https://developer.zendesk.com/api-reference/ticketing/oauth/oauth_tokens/\n  type: Documentation\n- url: openapi/oauth-openapi-original.yml\n  type: OpenAPI\ndescription: The Zendesk OAuth API implements the OAuth 2.0 standard to let apps securely access Zendesk\n  data on a users or accounts behalf without sharing passwords. Developers register an OAuth client in\n  a Zendesk account, redirect users to Zendesk for signin and consent, and exchange the returned authorization\n  code for access (and optionally refresh) tokens.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/apis.yml
tags:
- Authentication
- Authorization
- Oauth
---
