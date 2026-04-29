---
aid: databricks:clusters-api
baseURL: ''
description: The Databricks Clusters API allows you to create, start, edit, list, terminate, and delete clusters. Clusters are managed cloud resources that enable you to run data engineering and data science workloads on Apache Spark in the cloud. The API provides programmatic control over cluster lifecycle management, configuration, and monitoring.
humanURL: https://docs.databricks.com/api/workspace/clusters
image: ''
layout: api
name: Databricks Clusters API
properties:
- type: Documentation
  url: https://docs.databricks.com/api/workspace/clusters
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/openapi/databricks-openapi.yml
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/json-schema/databricks-cluster-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/json-schema/databricks-create-cluster-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/json-schema/databricks-edit-cluster-request-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/json-schema/databricks-cluster-details-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/json-schema/databricks-spark-node-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/json-schema/databricks-auto-scale-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/json-schema/databricks-aws-attributes-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/json-schema/databricks-azure-attributes-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/json-schema/databricks-gcp-attributes-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/json-schema/databricks-init-script-info-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/json-schema/databricks-cluster-event-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/json-schema/databricks-error-response-schema.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/json-ld/databricks-context.jsonld
provider_name: Databricks
provider_slug: databricks
slug: clusters-api
source_yaml: "aid: databricks:clusters-api\nname: Databricks Clusters API\ntags:\n- Clusters\n- Compute\n- Infrastructure\nhumanURL: https://docs.databricks.com/api/workspace/clusters\nproperties:\n- url: https://docs.databricks.com/api/workspace/clusters\n  type: Documentation\n- url: openapi/databricks-openapi.yml\n  type: OpenAPI\n- url: json-schema/databricks-cluster-schema.json\n  type: JSONSchema\n- url: json-schema/databricks-create-cluster-request-schema.json\n  type: JSONSchema\n- url: json-schema/databricks-edit-cluster-request-schema.json\n  type: JSONSchema\n- url: json-schema/databricks-cluster-details-schema.json\n  type: JSONSchema\n- url: json-schema/databricks-spark-node-schema.json\n  type: JSONSchema\n- url: json-schema/databricks-auto-scale-schema.json\n  type: JSONSchema\n- url: json-schema/databricks-aws-attributes-schema.json\n  type: JSONSchema\n- url: json-schema/databricks-azure-attributes-schema.json\n  type: JSONSchema\n- url: json-schema/databricks-gcp-attributes-schema.json\n\
  \  type: JSONSchema\n- url: json-schema/databricks-init-script-info-schema.json\n  type: JSONSchema\n- url: json-schema/databricks-cluster-event-schema.json\n  type: JSONSchema\n- url: json-schema/databricks-error-response-schema.json\n  type: JSONSchema\n- url: json-ld/databricks-context.jsonld\n  type: JSONLD\ndescription: The Databricks Clusters API allows you to create, start, edit, list, terminate, and delete\n  clusters. Clusters are managed cloud resources that enable you to run data engineering and data science\n  workloads on Apache Spark in the cloud. The API provides programmatic control over cluster lifecycle\n  management, configuration, and monitoring.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/apis.yml
tags:
- Clusters
- Compute
- Infrastructure
---
