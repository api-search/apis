---
aid: cilium:cilium-api
baseURL: https://localhost/v1
description: The Cilium REST API provides access to Cilium daemon and agent endpoints for managing Kubernetes network policy, security, and connectivity. The API is served by the cilium-agent process over a local Unix domain socket and HTTP interface, and covers endpoints, identities, cluster nodes, and health status.
humanURL: https://docs.cilium.io/en/stable/api/
image: ''
layout: api
name: Cilium API
properties:
- type: Documentation
  url: https://docs.cilium.io/en/stable/api/
- type: OpenAPI
  url: https://github.com/cilium/cilium/blob/main/api/v1/openapi.yaml
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cilium/refs/heads/main/openapi/cilium-api-openapi.yml
- type: Getting Started
  url: https://docs.cilium.io/en/stable/gettingstarted/
- type: Change Log
  url: https://github.com/cilium/cilium/releases
provider_name: Cilium
provider_slug: cilium
slug: cilium-api
source_yaml: "aid: cilium:cilium-api\nname: Cilium API\ntags:\n- eBPF\n- Kubernetes\n- Networking\n- Security\nhumanURL: https://docs.cilium.io/en/stable/api/\nbaseURL: https://localhost/v1\nproperties:\n- url: https://docs.cilium.io/en/stable/api/\n  type: Documentation\n- url: https://github.com/cilium/cilium/blob/main/api/v1/openapi.yaml\n  type: OpenAPI\n- url: openapi/cilium-api-openapi.yml\n  type: OpenAPI\n- url: https://docs.cilium.io/en/stable/gettingstarted/\n  type: Getting Started\n- url: https://github.com/cilium/cilium/releases\n  type: Change Log\ndescription: The Cilium REST API provides access to Cilium daemon and agent endpoints for managing Kubernetes\n  network policy, security, and connectivity. The API is served by the cilium-agent process over a local\n  Unix domain socket and HTTP interface, and covers endpoints, identities, cluster nodes, and health status.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cilium/refs/heads/main/apis.yml
tags:
- eBPF
- Kubernetes
- Networking
- Security
---
