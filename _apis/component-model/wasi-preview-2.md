---
aid: component-model:wasi-preview-2
baseURL: https://wasi.dev
description: WASI Preview 2 is the first WASI release built on the Component Model. It defines a set of interfaces such as wasi:filesystem, wasi:io, wasi:http, wasi:cli, and wasi:sockets that components can import to interact with the host system in a portable, capability-based way.
humanURL: https://wasi.dev/
image: ''
layout: api
name: WebAssembly System Interface Preview 2
properties:
- type: Documentation
  url: https://wasi.dev/
- type: GitHub Organization
  url: https://github.com/WebAssembly/WASI
- type: Reference
  url: https://github.com/WebAssembly/wasi-http
- type: Reference
  url: https://github.com/WebAssembly/wasi-filesystem
provider_name: Component Model
provider_slug: component-model
slug: wasi-preview-2
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: component-model:wasi-preview-2\nname: WebAssembly System Interface Preview 2\ndescription: WASI Preview 2 is the first WASI release built on the Component Model. It defines a set of\n  interfaces such as wasi:filesystem, wasi:io, wasi:http, wasi:cli, and wasi:sockets that components can\n  import to interact with the host system in a portable, capability-based way.\nhumanURL: https://wasi.dev/\nbaseURL: https://wasi.dev\ntags:\n- System Interface\n- WASI\n- Capabilities\nproperties:\n- type: Documentation\n  url: https://wasi.dev/\n- type: GitHub Organization\n  url: https://github.com/WebAssembly/WASI\n- type: Reference\n  url: https://github.com/WebAssembly/wasi-http\n- type: Reference\n  url: https://github.com/WebAssembly/wasi-filesystem\nx-features:\n- Capability-based system access\n- Defined as a collection of WIT worlds\n- wasi:http provides a portable HTTP server interface\n- Worlds for CLI, HTTP proxy, and embedder customization\nx-useCases:\n- Building portable\
  \ WebAssembly server functions\n- Running components in Wasmtime, Jco, WasmEdge, and Spin\n- Implementing capability-secure host bindings\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/component-model/refs/heads/main/apis.yml
tags:
- System Interface
- WASI
- Capabilities
---
