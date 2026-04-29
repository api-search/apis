---
aid: cilium:hubble-relay-api
baseURL: ''
description: The Hubble Relay API is a gRPC service that aggregates and relays network flow data from multiple Hubble agents running across Kubernetes cluster nodes. It provides a single cluster-wide endpoint for the Hubble Observer service, enabling centralized queries of flow data, DNS events, and HTTP metrics from all nodes through Hubble Relay without connecting to each node individually.
humanURL: https://docs.cilium.io/en/stable/observability/hubble/index.html
image: ''
layout: api
name: Hubble Relay API
properties:
- type: Documentation
  url: https://docs.cilium.io/en/stable/observability/hubble/index.html
- type: Reference
  url: https://github.com/cilium/cilium/tree/main/api/v1/relay
- type: GitHubRepository
  url: https://github.com/cilium/cilium
- type: Change Log
  url: https://github.com/cilium/cilium/releases
provider_name: Cilium
provider_slug: cilium
slug: hubble-relay-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: cilium:hubble-relay-api\nname: Hubble Relay API\ntags:\n- gRPC\n- Kubernetes\n- Networking\n- Observability\nhumanURL: https://docs.cilium.io/en/stable/observability/hubble/index.html\nproperties:\n- url: https://docs.cilium.io/en/stable/observability/hubble/index.html\n  type: Documentation\n- url: https://github.com/cilium/cilium/tree/main/api/v1/relay\n  type: Reference\n- url: https://github.com/cilium/cilium\n  type: GitHubRepository\n- url: https://github.com/cilium/cilium/releases\n  type: Change Log\ndescription: The Hubble Relay API is a gRPC service that aggregates and relays network flow data from\n  multiple Hubble agents running across Kubernetes cluster nodes. It provides a single cluster-wide endpoint\n  for the Hubble Observer service, enabling centralized queries of flow data, DNS events, and HTTP metrics\n  from all nodes through Hubble Relay without connecting to each node individually.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cilium/refs/heads/main/apis.yml
tags:
- gRPC
- Kubernetes
- Networking
- Observability
---
