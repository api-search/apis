---
aid: component-model:wit
baseURL: https://component-model.bytecodealliance.org
description: WIT is the interface definition language for the Component Model. WIT describes the imports and exports of a component using interfaces and worlds. WIT is consumed by language toolchains to generate bindings and by runtimes to validate and link components at load time.
humanURL: https://component-model.bytecodealliance.org/design/wit.html
image: ''
layout: api
name: WebAssembly Interface Type (WIT)
properties:
- type: Documentation
  url: https://component-model.bytecodealliance.org/design/wit.html
- type: Specification
  url: https://github.com/WebAssembly/component-model/blob/main/design/mvp/WIT.md
- type: Reference
  url: https://github.com/bytecodealliance/wit-bindgen
provider_name: Component Model
provider_slug: component-model
slug: wit
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: component-model:wit\nname: WebAssembly Interface Type (WIT)\ndescription: WIT is the interface definition language for the Component Model. WIT describes the imports\n  and exports of a component using interfaces and worlds. WIT is consumed by language toolchains to generate\n  bindings and by runtimes to validate and link components at load time.\nhumanURL: https://component-model.bytecodealliance.org/design/wit.html\nbaseURL: https://component-model.bytecodealliance.org\ntags:\n- Bindings\n- IDL\n- Interface\n- WIT\nproperties:\n- type: Documentation\n  url: https://component-model.bytecodealliance.org/design/wit.html\n- type: Specification\n  url: https://github.com/WebAssembly/component-model/blob/main/design/mvp/WIT.md\n- type: Reference\n  url: https://github.com/bytecodealliance/wit-bindgen\nx-features:\n- Declarative IDL for components\n- Records, variants, enums, flags, options, results\n- Resources with methods for borrowed and owned references\n- Interfaces\
  \ compose into worlds\nx-useCases:\n- Authoring portable component interfaces\n- Generating language bindings via wit-bindgen\n- Defining stable contracts between platform and components\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/component-model/refs/heads/main/apis.yml
tags:
- Bindings
- IDL
- Interface
- WIT
---
