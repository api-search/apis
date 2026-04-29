---
aid: consul-connect:consul-connect-config-entries
baseURL: https://developer.hashicorp.com
description: Consul Connect configuration entries (service-defaults, service-resolver, service-router, service-splitter, service-intentions, mesh, proxy-defaults) that declaratively configure mesh behavior. Configuration entries are managed via the /v1/config API and via Kubernetes Custom Resource Definitions when running on Kubernetes.
humanURL: https://developer.hashicorp.com/consul/docs/connect/config-entries
image: ''
layout: api
name: Consul Connect Configuration Entries
properties:
- type: Documentation
  url: https://developer.hashicorp.com/consul/docs/connect/config-entries
- type: Reference
  url: https://developer.hashicorp.com/consul/docs/connect/config-entries/service-defaults
- type: Reference
  url: https://developer.hashicorp.com/consul/docs/connect/config-entries/service-router
- type: Reference
  url: https://developer.hashicorp.com/consul/docs/connect/config-entries/service-splitter
provider_name: Consul Connect
provider_slug: consul-connect
slug: consul-connect-config-entries
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: consul-connect:consul-connect-config-entries\nname: Consul Connect Configuration Entries\ndescription: Consul Connect configuration entries (service-defaults, service-resolver, service-router,\n  service-splitter, service-intentions, mesh, proxy-defaults) that declaratively configure mesh behavior.\n  Configuration entries are managed via the /v1/config API and via Kubernetes Custom Resource Definitions\n  when running on Kubernetes.\nhumanURL: https://developer.hashicorp.com/consul/docs/connect/config-entries\nbaseURL: https://developer.hashicorp.com\ntags:\n- Configuration Entries\n- CRD\n- Kubernetes\n- L7 Routing\nproperties:\n- type: Documentation\n  url: https://developer.hashicorp.com/consul/docs/connect/config-entries\n- type: Reference\n  url: https://developer.hashicorp.com/consul/docs/connect/config-entries/service-defaults\n- type: Reference\n  url: https://developer.hashicorp.com/consul/docs/connect/config-entries/service-router\n- type: Reference\n  url:\
  \ https://developer.hashicorp.com/consul/docs/connect/config-entries/service-splitter\nx-features:\n- service-defaults to set protocol and timeouts\n- service-router for L7 path/header/method routing\n- service-splitter for canary and blue/green rollouts\n- service-resolver for failover and subsets\n- mesh-wide configuration via the mesh entry\n- Kubernetes CRDs for declarative mesh management\nx-useCases:\n- Implementing canary deployments via service-splitter\n- Routing traffic by header for tenant isolation\n- Centralizing TLS and protocol defaults\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/consul-connect/refs/heads/main/apis.yml
tags:
- Configuration Entries
- CRD
- Kubernetes
- L7 Routing
---
