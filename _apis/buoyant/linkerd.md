---
aid: buoyant:linkerd
baseURL: ''
description: Linkerd is a CNCF-graduated service mesh for Kubernetes that transparently adds mutual TLS encryption, latency-aware load balancing, retries, timeouts, circuit breaking, and observability to any Kubernetes workload without code changes. Supports HTTP, HTTP/2, gRPC, and TCP traffic.
humanURL: https://linkerd.io/
image: ''
layout: api
name: Linkerd Service Mesh
properties:
- type: Documentation
  url: https://linkerd.io/2.x/overview/
- type: Website
  url: https://linkerd.io/
- type: Reference
  url: https://linkerd.io/2.x/reference/
- type: GitHub Repository
  url: https://github.com/linkerd/linkerd2
provider_name: Buoyant
provider_slug: buoyant
slug: linkerd
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: buoyant:linkerd\nname: Linkerd Service Mesh\ndescription: Linkerd is a CNCF-graduated service mesh for Kubernetes that transparently adds mutual TLS\n  encryption, latency-aware load balancing, retries, timeouts, circuit breaking, and observability to\n  any Kubernetes workload without code changes. Supports HTTP, HTTP/2, gRPC, and TCP traffic.\nhumanURL: https://linkerd.io/\ntags:\n- Kubernetes\n- mTLS\n- Observability\n- Service Mesh\n- Zero Trust\nproperties:\n- type: Documentation\n  url: https://linkerd.io/2.x/overview/\n- type: Website\n  url: https://linkerd.io/\n- type: Reference\n  url: https://linkerd.io/2.x/reference/\n- type: GitHub Repository\n  url: https://github.com/linkerd/linkerd2\nx-features:\n- Mutual TLS for transparent encryption and authentication\n- Cryptographic workload identity\n- Latency-aware load balancing\n- Automated retries, timeouts, and circuit breaking\n- Zone-aware routing (HAZL) to reduce cross-zone costs\n- Canary and blue-green deployment\
  \ support\n- AI/LLM observability for resource, tool, and prompt usage metrics\n- Multi-cluster failover\n- FIPS 140-2/140-3 validated encryption (Enterprise)\nx-use-cases:\n- Zero-trust Kubernetes networking\n- Service-to-service mutual TLS without code changes\n- Observability for microservices and AI workloads\n- Multi-cluster Kubernetes deployments\n- Migration between cloud providers\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/buoyant/refs/heads/main/apis.yml
tags:
- Kubernetes
- mTLS
- Observability
- Service Mesh
- Zero Trust
---
