---
aid: apache-zookeeper:apache-zookeeper-admin-api
baseURL: http://localhost:8080/commands
description: The ZooKeeper Admin Server provides HTTP endpoints on port 8080 that expose the four-letter-word equivalent commands as REST endpoints for cluster monitoring, configuration, and diagnostics. Endpoints include /commands/conf (server configuration), /commands/stats (server statistics), /commands/mntr (monitoring metrics), /commands/envi (environment info), /commands/dump (session/ephemeral node dump), /commands/crst (connection reset), and /commands/leader (leader info for QuorumPeerMain).
humanURL: https://zookeeper.apache.org/doc/current/zookeeperAdmin.html#sc_4lw
image: ''
layout: api
name: Apache ZooKeeper Admin Server API
properties:
- type: Documentation
  url: https://zookeeper.apache.org/doc/current/zookeeperAdmin.html#sc_4lw
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/apache-zookeeper/refs/heads/main/openapi/zookeeper-admin-api.yml
provider_name: Apache ZooKeeper
provider_slug: apache-zookeeper
slug: apache-zookeeper-admin-api
tags:
- REST
- Admin
- Monitoring
- Cluster Management
---
