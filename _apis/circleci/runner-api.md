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
source_yaml: "aid: circleci:runner-api\nname: CircleCI Self-Hosted Runner API\ntags:\n- CI/CD\n- Infrastructure\n- Runners\n- Self-Hosted\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://runner.circleci.com\nhumanURL: https://circleci.com/docs/runner-api/\nproperties:\n- url: https://circleci.com/docs/runner-api/\n  type: Documentation\n- url: openapi/circleci-runner-api-openapi.yml\n  type: OpenAPI\ndescription: The CircleCI Self-Hosted Runner API enables management and execution of jobs on self-hosted\n  runner infrastructure. It provides endpoints for listing available runners, managing runner tasks, and\n  querying resource classes. The API is hosted separately from the main CircleCI API at runner.circleci.com\n  and supports multiple authentication methods depending on the endpoint. Developers can use this API\n  to integrate self-hosted runner management into their infrastructure automation workflows.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/circleci/refs/heads/main/apis.yml
tags:
- CI/CD
- Infrastructure
- Runners
- Self-Hosted
---
