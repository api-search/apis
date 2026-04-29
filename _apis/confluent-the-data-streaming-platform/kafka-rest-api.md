---
aid: confluent-the-data-streaming-platform:kafka-rest-api
baseURL: https://pkc-XXXXX.region.aws.confluent.cloud
description: The Kafka REST API (Confluent REST Proxy in self-managed deployments, Kafka REST in Cloud) provides HTTP access to Apache Kafka topics, consumers, partitions, brokers, and ACLs. Clients without a native Kafka library can produce and consume records, manage topics, and inspect metadata over HTTP. Cloud variants additionally enforce RBAC and Confluent Cloud authentication.
humanURL: https://docs.confluent.io/platform/current/kafka-rest/api.html
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Confluent Kafka REST API
properties:
- type: Documentation
  url: https://docs.confluent.io/platform/current/kafka-rest/api.html
- type: Cloud Documentation
  url: https://docs.confluent.io/cloud/current/kafka-rest/index.html
provider_name: Confluent | the Data Streaming Platform
provider_slug: confluent-the-data-streaming-platform
slug: kafka-rest-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: confluent-the-data-streaming-platform:kafka-rest-api\nname: Confluent Kafka REST API\ndescription: The Kafka REST API (Confluent REST Proxy in self-managed deployments, Kafka REST in Cloud)\n  provides HTTP access to Apache Kafka topics, consumers, partitions, brokers, and ACLs. Clients without\n  a native Kafka library can produce and consume records, manage topics, and inspect metadata over HTTP.\n  Cloud variants additionally enforce RBAC and Confluent Cloud authentication.\nhumanURL: https://docs.confluent.io/platform/current/kafka-rest/api.html\nbaseURL: https://pkc-XXXXX.region.aws.confluent.cloud\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\ntags:\n- Apache Kafka\n- Producer\n- Consumer\n- REST\nproperties:\n- type: Documentation\n  url: https://docs.confluent.io/platform/current/kafka-rest/api.html\n- type: Cloud Documentation\n  url: https://docs.confluent.io/cloud/current/kafka-rest/index.html\nx-features:\n- Topic Management\n\
  - Produce and Consume over HTTP\n- Partition Inspection\n- Consumer Group Management\n- Broker Metadata\n- ACL Management\nx-use-cases:\n- Produce events from clients without a Kafka library\n- Bridge legacy systems to Kafka over HTTP\n- Inspect topic and partition metadata from web tools\n- Manage ACLs from automation scripts\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/confluent-the-data-streaming-platform/refs/heads/main/apis.yml
tags:
- Apache Kafka
- Producer
- Consumer
- REST
---
