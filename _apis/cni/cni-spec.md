---
aid: cni:cni-spec
baseURL: ''
description: The CNI specification defines the interface between container runtimes and network plugins. It specifies how runtimes invoke plugins via environment variables (CNI_COMMAND, CNI_CONTAINERID, CNI_NETNS, CNI_IFNAME, CNI_PATH, CNI_ARGS) and stdin configuration, and how plugins respond on stdout with network interface details. The spec covers ADD, DEL, CHECK, and VERSION operations for managing container network attachments, and defines the plugin chaining model used by meta-plugins.
humanURL: https://www.cni.dev/docs/spec/
image: ''
layout: api
name: CNI Specification
properties:
- type: Documentation
  url: https://www.cni.dev/docs/spec/
- type: GitHubRepository
  url: https://github.com/containernetworking/cni
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cni/refs/heads/main/json-schema/cni-network-config-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cni/refs/heads/main/json-schema/cni-result-schema.json
- type: JSONLDContext
  url: https://raw.githubusercontent.com/api-evangelist/cni/refs/heads/main/json-ld/cni-context.jsonld
- type: NaftikoCapabilities
  url: https://raw.githubusercontent.com/api-evangelist/cni/refs/heads/main/capabilities/cni-spec-capabilities.yml
provider_name: Container Network Interface (CNI)
provider_slug: cni
slug: cni-spec
tags:
- Network Plugins
- Specification
---
