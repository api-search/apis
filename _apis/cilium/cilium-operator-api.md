---
aid: cilium:cilium-operator-api
baseURL: https://localhost/v1
description: The Cilium Operator API provides a REST interface for the Cilium operator component, which handles cluster-wide tasks such as garbage collection of Cilium endpoints and identities, node IPAM management, and coordination of cluster mesh operations. It exposes health and status endpoints for operator lifecycle management in Kubernetes deployments.
humanURL: https://docs.cilium.io/en/stable/internals/
image: ''
layout: api
name: Cilium Operator API
properties:
- type: Documentation
  url: https://docs.cilium.io/en/stable/internals/
- type: OpenAPI
  url: https://github.com/cilium/cilium/blob/main/api/v1/operator/openapi.yaml
- type: Change Log
  url: https://github.com/cilium/cilium/releases
provider_name: Cilium
provider_slug: cilium
slug: cilium-operator-api
source_yaml: "aid: cilium:cilium-operator-api\nname: Cilium Operator API\ntags:\n- eBPF\n- Kubernetes\n- Networking\n- Operations\nhumanURL: https://docs.cilium.io/en/stable/internals/\nbaseURL: https://localhost/v1\nproperties:\n- url: https://docs.cilium.io/en/stable/internals/\n  type: Documentation\n- url: https://github.com/cilium/cilium/blob/main/api/v1/operator/openapi.yaml\n  type: OpenAPI\n- url: https://github.com/cilium/cilium/releases\n  type: Change Log\ndescription: The Cilium Operator API provides a REST interface for the Cilium operator component, which\n  handles cluster-wide tasks such as garbage collection of Cilium endpoints and identities, node IPAM\n  management, and coordination of cluster mesh operations. It exposes health and status endpoints for\n  operator lifecycle management in Kubernetes deployments.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cilium/refs/heads/main/apis.yml
tags:
- eBPF
- Kubernetes
- Networking
- Operations
---
