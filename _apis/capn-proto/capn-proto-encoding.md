---
aid: capn-proto:capn-proto-encoding
baseURL: ''
description: The Cap'n Proto encoding specification defines the binary wire format. The in-memory layout is the wire format, enabling zero-copy reads and writes, random field access, and safe memory-mapped access to messages stored on disk.
humanURL: https://capnproto.org/encoding.html
image: ''
layout: api
name: Cap'n Proto Encoding (Wire Format)
properties:
- type: Specification
  url: https://capnproto.org/encoding.html
provider_name: Cap'n Proto
provider_slug: capn-proto
slug: capn-proto-encoding
source_yaml: "aid: capn-proto:capn-proto-encoding\nname: Cap'n Proto Encoding (Wire Format)\ndescription: The Cap'n Proto encoding specification defines the binary wire format. The in-memory layout\n  is the wire format, enabling zero-copy reads and writes, random field access, and safe memory-mapped\n  access to messages stored on disk.\nhumanURL: https://capnproto.org/encoding.html\ntags:\n- Binary Format\n- Specification\n- Zero Copy\nproperties:\n- type: Specification\n  url: https://capnproto.org/encoding.html\nx-features:\n- In-memory layout equals the wire format\n- Zero-copy deserialization\n- Random field access without scanning\n- Support for mmap-based message storage\n- Packed encoding variant for bandwidth-constrained links\n- Canonicalization rules for deterministic encoding\nx-use-cases:\n- Ultra-low-latency inter-process communication\n- Large on-disk datasets with mmap access\n- Network protocols where parsing cost matters\n- Embedded or memory-constrained environments (packed\
  \ form)\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/capn-proto/refs/heads/main/apis.yml
tags:
- Binary Format
- Specification
- Zero Copy
---
