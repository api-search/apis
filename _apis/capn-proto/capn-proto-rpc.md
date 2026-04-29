---
aid: capn-proto:capn-proto-rpc
baseURL: ''
description: Cap'n Proto's RPC protocol is a capability-based RPC layer that supports promise pipelining, object references passed as arguments or return values, and time-travel optimizations that eliminate round trips. It is the foundation of Cloudflare Workers' inter- service communication and Sandstorm's capability-oriented sandbox.
humanURL: https://capnproto.org/rpc.html
image: ''
layout: api
name: Cap'n Proto RPC Protocol
properties:
- type: Specification
  url: https://capnproto.org/rpc.html
- type: Documentation
  url: https://capnproto.org/rpc.html
provider_name: Cap'n Proto
provider_slug: capn-proto
slug: capn-proto-rpc
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: capn-proto:capn-proto-rpc\nname: Cap'n Proto RPC Protocol\ndescription: Cap'n Proto's RPC protocol is a capability-based RPC layer that supports promise pipelining,\n  object references passed as arguments or return values, and time-travel optimizations that eliminate\n  round trips. It is the foundation of Cloudflare Workers' inter- service communication and Sandstorm's\n  capability-oriented sandbox.\nhumanURL: https://capnproto.org/rpc.html\ntags:\n- Capability-Based Security\n- Protocol\n- RPC\n- Specification\nproperties:\n- type: Specification\n  url: https://capnproto.org/rpc.html\n- type: Documentation\n  url: https://capnproto.org/rpc.html\nx-features:\n- Capability-based security model\n- Object (capability) references passed in messages\n- Promise pipelining to eliminate round trips\n- Bidirectional calls over a single connection\n- Time-travel / path-compression optimizations\n- Transport-agnostic (TCP, TLS, WebSocket, shared memory)\nx-use-cases:\n- Microservice\
  \ RPC with low round-trip overhead\n- Secure capability-oriented sandboxing (Sandstorm, Workers)\n- Bidirectional streaming between trusted peers\n- Inter-process communication with fine-grained authorization\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/capn-proto/refs/heads/main/apis.yml
tags:
- Capability-Based Security
- Protocol
- RPC
- Specification
---
