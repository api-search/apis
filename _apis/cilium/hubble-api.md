---
aid: cilium:hubble-api
baseURL: ''
description: The Hubble API is a gRPC-based observability API built on top of Cilium and eBPF that provides deep visibility into network flows, DNS queries, HTTP requests, and service communication within Kubernetes clusters. It exposes Observer and Peer gRPC services for querying flows, nodes, namespaces, and server status across single nodes or entire clusters via Hubble Relay.
humanURL: https://docs.cilium.io/en/stable/observability/hubble/index.html
image: ''
layout: api
name: Hubble API
properties:
- type: Documentation
  url: https://docs.cilium.io/en/stable/observability/hubble/index.html
- type: Reference
  url: https://docs.cilium.io/en/stable/internals/hubble/
- type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/cilium/refs/heads/main/asyncapi/cilium-hubble-asyncapi.yml
- type: GitHubRepository
  url: https://github.com/cilium/hubble
- type: Change Log
  url: https://github.com/cilium/hubble/releases
provider_name: Cilium
provider_slug: cilium
slug: hubble-api
source_yaml: "aid: cilium:hubble-api\nname: Hubble API\ntags:\n- eBPF\n- Kubernetes\n- Networking\n- Observability\nhumanURL: https://docs.cilium.io/en/stable/observability/hubble/index.html\nproperties:\n- url: https://docs.cilium.io/en/stable/observability/hubble/index.html\n  type: Documentation\n- url: https://docs.cilium.io/en/stable/internals/hubble/\n  type: Reference\n- url: asyncapi/cilium-hubble-asyncapi.yml\n  type: AsyncAPI\n- url: https://github.com/cilium/hubble\n  type: GitHubRepository\n- url: https://github.com/cilium/hubble/releases\n  type: Change Log\ndescription: The Hubble API is a gRPC-based observability API built on top of Cilium and eBPF that provides\n  deep visibility into network flows, DNS queries, HTTP requests, and service communication within Kubernetes\n  clusters. It exposes Observer and Peer gRPC services for querying flows, nodes, namespaces, and server\n  status across single nodes or entire clusters via Hubble Relay.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cilium/refs/heads/main/apis.yml
tags:
- eBPF
- Kubernetes
- Networking
- Observability
---
