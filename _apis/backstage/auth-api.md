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
tags:
- Authentication
- Developer Portal
- OAuth
---
