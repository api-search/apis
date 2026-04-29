---
aid: veritas-infoscale:rest-api
baseURL: https://{infoscale-server}:14149/api/v1
description: REST API for managing InfoScale clusters, storage resources, and high availability configurations. Supports storage configuration and management operations including disk groups, volumes, and file systems, as well as cluster configuration and management operations including service groups, resources, and heartbeats.
humanURL: https://www.veritas.com/support/en_US/doc/79638609-166315478-0/v151832379-166315478
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Veritas InfoScale REST API
properties:
- type: Documentation
  url: https://www.veritas.com/support/en_US/doc/79638609-166315478-0/v151832379-166315478
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/openapi/veritas-infoscale-rest-api.yaml
- type: Authentication
  url: https://www.veritas.com/support/en_US/doc/79638609-166315478-0/v151837041-166315478
- title: Cluster Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/json-schema/rest-api-cluster-schema.json
- title: Service Group Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/json-schema/rest-api-service-group-schema.json
- title: Disk Group Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/json-schema/rest-api-disk-group-schema.json
- title: Volume Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/json-schema/rest-api-volume-schema.json
- title: System Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/json-schema/rest-api-system-schema.json
- title: Alert Schema
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/json-schema/rest-api-alert-schema.json
- title: Cluster Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/json-structure/rest-api-cluster-structure.json
- title: Service Group Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/json-structure/rest-api-service-group-structure.json
- title: Disk Group Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/json-structure/rest-api-disk-group-structure.json
- title: Volume Structure
  type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/json-structure/rest-api-volume-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/json-ld/veritas-infoscale-rest-api-context.jsonld
- title: Cluster Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/examples/rest-api-cluster-example.json
- title: Service Group Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/examples/rest-api-service-group-example.json
- title: Disk Group Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/examples/rest-api-disk-group-example.json
- title: Volume Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/examples/rest-api-volume-example.json
- title: System Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/examples/rest-api-system-example.json
- title: Alert Example
  type: Example
  url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/examples/rest-api-alert-example.json
provider_name: Veritas InfoScale
provider_slug: veritas-infoscale
slug: rest-api
source_yaml: "aid: veritas-infoscale:rest-api\nname: Veritas InfoScale REST API\ndescription: REST API for managing InfoScale clusters, storage resources, and high availability configurations.\n  Supports storage configuration and management operations including disk groups, volumes, and file systems,\n  as well as cluster configuration and management operations including service groups, resources, and\n  heartbeats.\nimage: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://www.veritas.com/support/en_US/doc/79638609-166315478-0/v151832379-166315478\nbaseURL: https://{infoscale-server}:14149/api/v1\ntags:\n- Availability\n- Clustering\n- Storage\nproperties:\n- type: Documentation\n  url: https://www.veritas.com/support/en_US/doc/79638609-166315478-0/v151832379-166315478\n- type: OpenAPI\n  url: openapi/veritas-infoscale-rest-api.yaml\n- type: Authentication\n  url: https://www.veritas.com/support/en_US/doc/79638609-166315478-0/v151837041-166315478\n\
  - type: JSONSchema\n  url: json-schema/rest-api-cluster-schema.json\n  title: Cluster Schema\n- type: JSONSchema\n  url: json-schema/rest-api-service-group-schema.json\n  title: Service Group Schema\n- type: JSONSchema\n  url: json-schema/rest-api-disk-group-schema.json\n  title: Disk Group Schema\n- type: JSONSchema\n  url: json-schema/rest-api-volume-schema.json\n  title: Volume Schema\n- type: JSONSchema\n  url: json-schema/rest-api-system-schema.json\n  title: System Schema\n- type: JSONSchema\n  url: json-schema/rest-api-alert-schema.json\n  title: Alert Schema\n- type: JSONStructure\n  url: json-structure/rest-api-cluster-structure.json\n  title: Cluster Structure\n- type: JSONStructure\n  url: json-structure/rest-api-service-group-structure.json\n  title: Service Group Structure\n- type: JSONStructure\n  url: json-structure/rest-api-disk-group-structure.json\n  title: Disk Group Structure\n- type: JSONStructure\n  url: json-structure/rest-api-volume-structure.json\n  title: Volume\
  \ Structure\n- type: JSONLD\n  url: json-ld/veritas-infoscale-rest-api-context.jsonld\n- type: Example\n  url: examples/rest-api-cluster-example.json\n  title: Cluster Example\n- type: Example\n  url: examples/rest-api-service-group-example.json\n  title: Service Group Example\n- type: Example\n  url: examples/rest-api-disk-group-example.json\n  title: Disk Group Example\n- type: Example\n  url: examples/rest-api-volume-example.json\n  title: Volume Example\n- type: Example\n  url: examples/rest-api-system-example.json\n  title: System Example\n- type: Example\n  url: examples/rest-api-alert-example.json\n  title: Alert Example\ncontact:\n- FN: Veritas Support\n  email: support@veritas.com\n  url: https://www.veritas.com/support\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/veritas-infoscale/refs/heads/main/apis.yml
tags:
- Availability
- Clustering
- Storage
---
