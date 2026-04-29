---
aid: apache-curator:apache-curator
baseURL: ''
description: Curator provides a high-level Java API with fluent builders for ZooKeeper operations, along with pre-built recipes for leader election, distributed locks (shared, reentrant, read-write, semaphore), barriers, caches (CuratorCache, PathCache, TreeCache), distributed counters, queues, group membership, and service discovery via curator-x-discovery.
humanURL: https://curator.apache.org/docs/about
image: ''
layout: api
name: Apache Curator
properties:
- type: Documentation
  url: https://curator.apache.org/docs/about
- type: APIReference
  url: https://curator.apache.org/apidocs/
- type: GettingStarted
  url: https://curator.apache.org/docs/getting-started
- type: GitHubRepository
  url: https://github.com/apache/curator
- title: curator-framework (Maven)
  type: SDK
  url: https://mvnrepository.com/artifact/org.apache.curator/curator-framework
- title: curator-recipes (Maven)
  type: SDK
  url: https://mvnrepository.com/artifact/org.apache.curator/curator-recipes
- title: curator-x-discovery (Maven)
  type: SDK
  url: https://mvnrepository.com/artifact/org.apache.curator/curator-x-discovery
- title: curator-async (Maven)
  type: SDK
  url: https://mvnrepository.com/artifact/org.apache.curator/curator-async
- title: curator-test (Testing)
  type: Tools
  url: https://mvnrepository.com/artifact/org.apache.curator/curator-test
- title: Distributed Lock
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-schema/apache-curator-distributed-lock-schema.json
- title: Leader Latch State
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-schema/apache-curator-leader-latch-state-schema.json
- title: Node Data
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-schema/apache-curator-node-data-schema.json
- title: Service Instance
  type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-schema/apache-curator-service-instance-schema.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-structure/apache-curator-distributed-lock-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-structure/apache-curator-leader-latch-state-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-structure/apache-curator-node-data-structure.json
- type: JSONStructure
  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-structure/apache-curator-service-instance-structure.json
- type: JSONLD
  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-ld/apache-curator-context.jsonld
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/examples/apache-curator-distributed-lock-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/examples/apache-curator-leader-latch-state-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/examples/apache-curator-node-data-example.json
- type: Example
  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/examples/apache-curator-service-instance-example.json
provider_name: Apache Curator
provider_slug: apache-curator
slug: apache-curator
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: apache-curator:apache-curator\nname: Apache Curator\ndescription: Curator provides a high-level Java API with fluent builders for ZooKeeper operations, along\n  with pre-built recipes for leader election, distributed locks (shared, reentrant, read-write, semaphore),\n  barriers, caches (CuratorCache, PathCache, TreeCache), distributed counters, queues, group membership,\n  and service discovery via curator-x-discovery.\nhumanURL: https://curator.apache.org/docs/about\ntags:\n- Barriers\n- Caches\n- Distributed Locks\n- Java\n- Leader Election\n- Maven\n- Queues\n- Service Discovery\n- ZooKeeper\nproperties:\n- type: Documentation\n  url: https://curator.apache.org/docs/about\n- type: APIReference\n  url: https://curator.apache.org/apidocs/\n- type: GettingStarted\n  url: https://curator.apache.org/docs/getting-started\n- type: GitHubRepository\n  url: https://github.com/apache/curator\n- type: SDK\n  url: https://mvnrepository.com/artifact/org.apache.curator/curator-framework\n\
  \  title: curator-framework (Maven)\n- type: SDK\n  url: https://mvnrepository.com/artifact/org.apache.curator/curator-recipes\n  title: curator-recipes (Maven)\n- type: SDK\n  url: https://mvnrepository.com/artifact/org.apache.curator/curator-x-discovery\n  title: curator-x-discovery (Maven)\n- type: SDK\n  url: https://mvnrepository.com/artifact/org.apache.curator/curator-async\n  title: curator-async (Maven)\n- type: Tools\n  url: https://mvnrepository.com/artifact/org.apache.curator/curator-test\n  title: curator-test (Testing)\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-schema/apache-curator-distributed-lock-schema.json\n  title: Distributed Lock\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-schema/apache-curator-leader-latch-state-schema.json\n  title: Leader Latch State\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-schema/apache-curator-node-data-schema.json\n\
  \  title: Node Data\n- type: JSONSchema\n  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-schema/apache-curator-service-instance-schema.json\n  title: Service Instance\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-structure/apache-curator-distributed-lock-structure.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-structure/apache-curator-leader-latch-state-structure.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-structure/apache-curator-node-data-structure.json\n- type: JSONStructure\n  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-structure/apache-curator-service-instance-structure.json\n- type: JSONLD\n  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/json-ld/apache-curator-context.jsonld\n\
  - type: Example\n  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/examples/apache-curator-distributed-lock-example.json\n- type: Example\n  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/examples/apache-curator-leader-latch-state-example.json\n- type: Example\n  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/examples/apache-curator-node-data-example.json\n- type: Example\n  url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/examples/apache-curator-service-instance-example.json\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apache-curator/refs/heads/main/apis.yml
tags:
- Barriers
- Caches
- Distributed Locks
- Java
- Leader Election
- Maven
- Queues
- Service Discovery
- ZooKeeper
---
