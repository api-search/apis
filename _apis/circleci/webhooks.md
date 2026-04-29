---
aid: circleci:webhooks
baseURL: https://api.example.com
description: CircleCI Webhooks allow developers to receive real-time notifications about events in their CI/CD pipelines by configuring HTTP callbacks. Webhooks can be set up through project settings to notify external services when workflows and jobs complete, fail, or change status. This enables integration with monitoring systems, chat platforms, and custom automation workflows. Webhooks deliver JSON payloads containing event details to configured endpoint URLs.
humanURL: https://circleci.com/docs/webhooks/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CircleCI Webhooks
properties:
- type: Documentation
  url: https://circleci.com/docs/webhooks/
- type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/circleci/refs/heads/main/asyncapi/circleci-webhooks-asyncapi.yml
provider_name: CircleCI
provider_slug: circleci
slug: webhooks
source_yaml: "aid: circleci:webhooks\nname: CircleCI Webhooks\ntags:\n- CI/CD\n- Events\n- Notifications\n- Webhooks\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: https://api.example.com\nhumanURL: https://circleci.com/docs/webhooks/\nproperties:\n- url: https://circleci.com/docs/webhooks/\n  type: Documentation\n- url: asyncapi/circleci-webhooks-asyncapi.yml\n  type: AsyncAPI\ndescription: CircleCI Webhooks allow developers to receive real-time notifications about events in their\n  CI/CD pipelines by configuring HTTP callbacks. Webhooks can be set up through project settings to notify\n  external services when workflows and jobs complete, fail, or change status. This enables integration\n  with monitoring systems, chat platforms, and custom automation workflows. Webhooks deliver JSON payloads\n  containing event details to configured endpoint URLs.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/circleci/refs/heads/main/apis.yml
tags:
- CI/CD
- Events
- Notifications
- Webhooks
---
