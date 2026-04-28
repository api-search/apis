---
aid: circleci:runner-api
baseURL: https://runner.circleci.com
description: The CircleCI Self-Hosted Runner API enables management and execution of jobs on self-hosted runner infrastructure. It provides endpoints for listing available runners, managing runner tasks, and querying resource classes. The API is hosted separately from the main CircleCI API at runner.circleci.com and supports multiple authentication methods depending on the endpoint. Developers can use this API to integrate self-hosted runner management into their infrastructure automation workflows.
humanURL: https://circleci.com/docs/runner-api/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CircleCI Self-Hosted Runner API
properties:
- type: Documentation
  url: https://circleci.com/docs/runner-api/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/circleci/refs/heads/main/openapi/circleci-runner-api-openapi.yml
provider_name: CircleCI
provider_slug: circleci
slug: runner-api
tags:
- CI/CD
- Infrastructure
- Runners
- Self-Hosted
---
