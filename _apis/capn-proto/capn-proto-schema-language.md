---
aid: capn-proto:capn-proto-schema-language
baseURL: ''
description: The Cap'n Proto schema language is used to define message types in .capnp files that are then compiled into native code for each supported language. The schema language defines structs, unions, enums, interfaces (for RPC), groups, generics, and annotations, and carefully specifies evolution rules so schemas can be extended without breaking forward or backward compatibility.
humanURL: https://capnproto.org/language.html
image: ''
layout: api
name: Cap'n Proto Schema Language
properties:
- type: Specification
  url: https://capnproto.org/language.html
- type: Documentation
  url: https://capnproto.org/language.html
- type: GitHub Repository
  url: https://github.com/capnproto/capnproto
provider_name: Cap'n Proto
provider_slug: capn-proto
slug: capn-proto-schema-language
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: capn-proto:capn-proto-schema-language\nname: Cap'n Proto Schema Language\ndescription: The Cap'n Proto schema language is used to define message types in .capnp files that are\n  then compiled into native code for each supported language. The schema language defines structs, unions,\n  enums, interfaces (for RPC), groups, generics, and annotations, and carefully specifies evolution rules\n  so schemas can be extended without breaking forward or backward compatibility.\nhumanURL: https://capnproto.org/language.html\ntags:\n- Code Generation\n- Schema\n- Specification\nproperties:\n- type: Specification\n  url: https://capnproto.org/language.html\n- type: Documentation\n  url: https://capnproto.org/language.html\n- type: GitHub Repository\n  url: https://github.com/capnproto/capnproto\nx-features:\n- Struct, union, enum, interface, and group definitions\n- Generic parameters for reusable types\n- Annotations for custom metadata\n- Schema evolution rules for forward and backward\
  \ compatibility\n- Compilation to native code in multiple languages\n- Cross-language ABI through a canonical wire format\nx-use-cases:\n- Defining message types for zero-copy IPC\n- Describing RPC interfaces across language boundaries\n- Long-lived storage formats with schema evolution\n- Replacing Protocol Buffers for latency-sensitive workloads\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/capn-proto/refs/heads/main/apis.yml
tags:
- Code Generation
- Schema
- Specification
---
