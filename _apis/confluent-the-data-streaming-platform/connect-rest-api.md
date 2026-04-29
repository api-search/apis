---
aid: confluent-the-data-streaming-platform:connect-rest-api
baseURL: https://localhost:8083
description: The Kafka Connect REST API manages connectors, tasks, and worker configuration. Operators use it to deploy, configure, pause, resume, and delete source and sink connectors, inspect task status, and restart failed tasks. In Confluent Cloud, managed connectors are provisioned through the Cloud REST API while runtime status is exposed via the Connect REST surface.
humanURL: https://docs.confluent.io/platform/current/connect/references/restapi.html
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Kafka Connect REST API
properties:
- type: Documentation
  url: https://docs.confluent.io/platform/current/connect/references/restapi.html
provider_name: Confluent | the Data Streaming Platform
provider_slug: confluent-the-data-streaming-platform
slug: connect-rest-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: confluent-the-data-streaming-platform:connect-rest-api\nname: Kafka Connect REST API\ndescription: The Kafka Connect REST API manages connectors, tasks, and worker configuration. Operators\n  use it to deploy, configure, pause, resume, and delete source and sink connectors, inspect task status,\n  and restart failed tasks. In Confluent Cloud, managed connectors are provisioned through the Cloud REST\n  API while runtime status is exposed via the Connect REST surface.\nhumanURL: https://docs.confluent.io/platform/current/connect/references/restapi.html\nbaseURL: https://localhost:8083\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\ntags:\n- Connectors\n- Kafka Connect\n- REST\nproperties:\n- type: Documentation\n  url: https://docs.confluent.io/platform/current/connect/references/restapi.html\nx-features:\n- Connector Lifecycle Management\n- Task Status and Restart\n- Plugin Discovery\n- Configuration Validation\nx-use-cases:\n- Deploy\
  \ and operate source/sink connectors\n- Restart failed tasks programmatically\n- Validate connector configurations in CI\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/confluent-the-data-streaming-platform/refs/heads/main/apis.yml
tags:
- Connectors
- Kafka Connect
- REST
---
