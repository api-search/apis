---
aid: circleci:rest-api-v1
baseURL: https://circleci.com/api/v1.1
description: The CircleCI REST API v1 is the legacy API that provides access to build information, project details, and user data. While still available, CircleCI recommends migrating to the v2 API for newer features and improved functionality. The v1 API supports operations for retrieving build details, triggering builds, managing SSH keys, and accessing test metadata. Authentication is handled through API tokens passed as query parameters or HTTP headers.
humanURL: https://circleci.com/docs/api/v1/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CircleCI REST API V1
properties:
- type: Documentation
  url: https://circleci.com/docs/api/v1/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/circleci/refs/heads/main/openapi/circleci-rest-api-v1-openapi.yml
provider_name: CircleCI
provider_slug: circleci
slug: rest-api-v1
tags:
- Builds
- CI/CD
- Continuous Integration
- Legacy
---
