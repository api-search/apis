---
aid: containerd:containerd-cri-api
baseURL: ''
description: Container Runtime Interface (CRI) implementation that enables Kubernetes to use containerd as its container runtime. Supports pod sandbox management, container lifecycle operations, image pulling, and streaming APIs for exec, attach, and port-forward.
humanURL: https://github.com/containerd/containerd/tree/main/pkg/cri
image: ''
layout: api
name: Containerd CRI API
properties:
- type: Documentation
  url: https://containerd.io/docs/
- type: Reference
  url: https://github.com/containerd/containerd/tree/main/pkg/cri
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/containerd/refs/heads/main/json-schema/containerd-config-schema.json
provider_name: Containerd
provider_slug: containerd
slug: containerd-cri-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: containerd:containerd-cri-api\nname: Containerd CRI API\ndescription: Container Runtime Interface (CRI) implementation that enables Kubernetes to use containerd\n  as its container runtime. Supports pod sandbox management, container lifecycle operations, image pulling,\n  and streaming APIs for exec, attach, and port-forward.\nhumanURL: https://github.com/containerd/containerd/tree/main/pkg/cri\nproperties:\n- type: Documentation\n  url: https://containerd.io/docs/\n- type: Reference\n  url: https://github.com/containerd/containerd/tree/main/pkg/cri\n- type: JSONSchema\n  url: json-schema/containerd-config-schema.json\ntags:\n- Container Runtime\n- CRI\n- Kubernetes\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/containerd/refs/heads/main/apis.yml
tags:
- Container Runtime
- CRI
- Kubernetes
---
