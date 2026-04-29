---
aid: communication-protocols:grpc
baseURL: https://grpc.io
description: A high-performance, contract-first RPC framework built on HTTP/2 with Protocol Buffers as the default IDL. gRPC supports unary, server streaming, client streaming, and bidirectional streaming and is widely used for microservice-to-microservice communication and for polyglot APIs across cloud-native platforms.
humanURL: https://grpc.io/
image: ''
layout: api
name: gRPC
properties:
- type: Documentation
  url: https://grpc.io/docs/
- type: Specification
  url: https://github.com/grpc/grpc/blob/master/doc/PROTOCOL-HTTP2.md
- type: GitHub Organization
  url: https://github.com/grpc
provider_name: Communication Protocols
provider_slug: communication-protocols
slug: grpc
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: communication-protocols:grpc\nname: gRPC\ndescription: A high-performance, contract-first RPC framework built on HTTP/2 with Protocol Buffers as\n  the default IDL. gRPC supports unary, server streaming, client streaming, and bidirectional streaming\n  and is widely used for microservice-to-microservice communication and for polyglot APIs across cloud-native\n  platforms.\nhumanURL: https://grpc.io/\nbaseURL: https://grpc.io\ntags:\n- CNCF\n- HTTP/2\n- Protocol Buffers\n- RPC\n- Streaming\nproperties:\n- type: Documentation\n  url: https://grpc.io/docs/\n- type: Specification\n  url: https://github.com/grpc/grpc/blob/master/doc/PROTOCOL-HTTP2.md\n- type: GitHub Organization\n  url: https://github.com/grpc\nx-features:\n- HTTP/2 multiplexed transport with Protobuf payloads\n- Four streaming modes (unary, server, client, bidi)\n- Polyglot code generation across 11+ languages\n- Pluggable authentication, deadlines, and interceptors\nx-useCases:\n- Internal microservice communication\n\
  - Mobile-to-backend APIs with low latency\n- High-throughput streaming workloads\n- Polyglot service interfaces\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/communication-protocols/refs/heads/main/apis.yml
tags:
- CNCF
- HTTP/2
- Protocol Buffers
- RPC
- Streaming
---
