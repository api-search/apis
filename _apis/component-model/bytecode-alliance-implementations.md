---
aid: component-model:bytecode-alliance-implementations
baseURL: https://bytecodealliance.org
description: A landscape of toolchains and runtimes that implement the Component Model, including Wasmtime, Jco, wit-bindgen language bindings, cargo-component for Rust, ComponentizeJS, and Spin for serverless Wasm. These implementations are largely stewarded by the Bytecode Alliance.
humanURL: https://bytecodealliance.org/
image: ''
layout: api
name: Component Model Implementations
properties:
- type: Reference
  url: https://github.com/bytecodealliance/wasmtime
- type: Reference
  url: https://github.com/bytecodealliance/wit-bindgen
- type: Reference
  url: https://github.com/bytecodealliance/cargo-component
- type: Reference
  url: https://github.com/bytecodealliance/jco
- type: Reference
  url: https://github.com/bytecodealliance/ComponentizeJS
- type: Reference
  url: https://github.com/fermyon/spin
provider_name: Component Model
provider_slug: component-model
slug: bytecode-alliance-implementations
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: component-model:bytecode-alliance-implementations\nname: Component Model Implementations\ndescription: A landscape of toolchains and runtimes that implement the Component Model, including Wasmtime,\n  Jco, wit-bindgen language bindings, cargo-component for Rust, ComponentizeJS, and Spin for serverless\n  Wasm. These implementations are largely stewarded by the Bytecode Alliance.\nhumanURL: https://bytecodealliance.org/\nbaseURL: https://bytecodealliance.org\ntags:\n- Bytecode Alliance\n- Implementations\n- Runtimes\n- Toolchains\nproperties:\n- type: Reference\n  url: https://github.com/bytecodealliance/wasmtime\n- type: Reference\n  url: https://github.com/bytecodealliance/wit-bindgen\n- type: Reference\n  url: https://github.com/bytecodealliance/cargo-component\n- type: Reference\n  url: https://github.com/bytecodealliance/jco\n- type: Reference\n  url: https://github.com/bytecodealliance/ComponentizeJS\n- type: Reference\n  url: https://github.com/fermyon/spin\nx-features:\n\
  - Wasmtime native runtime with component support\n- Jco JavaScript host and tooling\n- cargo-component for Rust component projects\n- wit-bindgen for cross-language bindings\nx-useCases:\n- Running components on the server, edge, or in browsers\n- Generating language bindings from WIT\n- Building serverless Wasm functions on Spin\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/component-model/refs/heads/main/apis.yml
tags:
- Bytecode Alliance
- Implementations
- Runtimes
- Toolchains
---
