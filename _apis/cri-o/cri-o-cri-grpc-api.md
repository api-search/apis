---
aid: cri-o:cri-o-cri-grpc-api
baseURL: ''
description: CRI-O implements the Kubernetes Container Runtime Interface (CRI) gRPC API that the kubelet uses to manage pod sandboxes, containers, image lifecycle, and runtime status. The CRI gRPC API is served over a Unix domain socket (default /var/run/crio/crio.sock) and includes services for RuntimeService and ImageService as defined by the upstream CRI protobuf specification.
humanURL: https://kubernetes.io/docs/concepts/architecture/cri/
image: ''
layout: api
name: CRI-O CRI gRPC API
properties:
- type: Documentation
  url: https://kubernetes.io/docs/concepts/architecture/cri/
- type: Specification
  url: https://github.com/kubernetes/cri-api
- type: GitHubRepository
  url: https://github.com/cri-o/cri-o
provider_name: CRI-O
provider_slug: cri-o
slug: cri-o-cri-grpc-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: cri-o:cri-o-cri-grpc-api\nname: CRI-O CRI gRPC API\ndescription: CRI-O implements the Kubernetes Container Runtime Interface (CRI) gRPC API that the kubelet\n  uses to manage pod sandboxes, containers, image lifecycle, and runtime status. The CRI gRPC API is served\n  over a Unix domain socket (default /var/run/crio/crio.sock) and includes services for RuntimeService\n  and ImageService as defined by the upstream CRI protobuf specification.\nhumanURL: https://kubernetes.io/docs/concepts/architecture/cri/\nproperties:\n- type: Documentation\n  url: https://kubernetes.io/docs/concepts/architecture/cri/\n- type: Specification\n  url: https://github.com/kubernetes/cri-api\n- type: GitHubRepository\n  url: https://github.com/cri-o/cri-o\ntags:\n- CRI\n- gRPC\n- Kubelet\n- Kubernetes\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cri-o/refs/heads/main/apis.yml
tags:
- CRI
- gRPC
- Kubelet
- Kubernetes
---
