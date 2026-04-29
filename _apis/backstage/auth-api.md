---
aid: backstage:auth-api
baseURL: ''
description: The Backstage Auth API provides endpoints for authenticating users and services with the Backstage backend. It supports multiple authentication providers (GitHub, Google, Okta, SAML, etc.) and handles OAuth flows, token issuance, token refresh, and session management. The Auth API is used by the Backstage frontend to initiate login flows and by backend plugins to verify caller identity via Backstage tokens.
humanURL: https://backstage.io/docs/auth/
image: ''
layout: api
name: Backstage Auth API
properties:
- type: Documentation
  url: https://backstage.io/docs/auth/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/openapi/backstage-auth-openapi.yml
provider_name: Backstage
provider_slug: backstage
slug: auth-api
source_yaml: "aid: backstage:auth-api\nname: Backstage Auth API\ntags:\n- Authentication\n- Developer Portal\n- OAuth\nhumanURL: https://backstage.io/docs/auth/\nproperties:\n- url: https://backstage.io/docs/auth/\n  type: Documentation\n- url: openapi/backstage-auth-openapi.yml\n  type: OpenAPI\ndescription: The Backstage Auth API provides endpoints for authenticating users and services with the\n  Backstage backend. It supports multiple authentication providers (GitHub, Google, Okta, SAML, etc.)\n  and handles OAuth flows, token issuance, token refresh, and session management. The Auth API is used\n  by the Backstage frontend to initiate login flows and by backend plugins to verify caller identity via\n  Backstage tokens.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/apis.yml
tags:
- Authentication
- Developer Portal
- OAuth
---
