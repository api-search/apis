---
aid: comcast:authentication-api
baseURL: https://sat-prod.codebig2.net
description: The Comcast Security Access Token (SAT) endpoint issues short-lived bearer tokens used to authenticate calls to Comcast partner APIs such as the Open Ingest service. Clients exchange an x-client-id and x-client-secret pair for an OAuth-style access token valid for 24 hours, which is then attached to subsequent requests in the Authorization header.
humanURL: https://docs.developer.comcast.com/docs/081-core-authentication
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Comcast Authentication API (SAT)
properties:
- type: Documentation
  url: https://docs.developer.comcast.com/docs/081-core-authentication
provider_name: Comcast
provider_slug: comcast
slug: authentication-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: comcast:authentication-api\nname: Comcast Authentication API (SAT)\ntags:\n- Authentication\n- OAuth\n- Tokens\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://sat-prod.codebig2.net\nhumanURL: https://docs.developer.comcast.com/docs/081-core-authentication\nproperties:\n- url: https://docs.developer.comcast.com/docs/081-core-authentication\n  type: Documentation\ndescription: The Comcast Security Access Token (SAT) endpoint issues short-lived bearer tokens used to\n  authenticate calls to Comcast partner APIs such as the Open Ingest service. Clients exchange an x-client-id\n  and x-client-secret pair for an OAuth-style access token valid for 24 hours, which is then attached\n  to subsequent requests in the Authorization header.\nx-features:\n- Client-credential token exchange\n- 24-hour bearer token lifetime\n- x-client-id / x-client-secret request headers\nx-use-cases:\n- Authenticating against NBCUniversal partner ingest\
  \ workflows\n- Obtaining access tokens for Comcast media platform APIs\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/comcast/refs/heads/main/apis.yml
tags:
- Authentication
- OAuth
- Tokens
---
