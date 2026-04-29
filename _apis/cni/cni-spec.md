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
source_yaml: "aid: cni:cni-spec\nname: CNI Specification\ndescription: The CNI specification defines the interface between container runtimes and network plugins.\n  It specifies how runtimes invoke plugins via environment variables (CNI_COMMAND, CNI_CONTAINERID, CNI_NETNS,\n  CNI_IFNAME, CNI_PATH, CNI_ARGS) and stdin configuration, and how plugins respond on stdout with network\n  interface details. The spec covers ADD, DEL, CHECK, and VERSION operations for managing container network\n  attachments, and defines the plugin chaining model used by meta-plugins.\nhumanURL: https://www.cni.dev/docs/spec/\nproperties:\n- type: Documentation\n  url: https://www.cni.dev/docs/spec/\n- type: GitHubRepository\n  url: https://github.com/containernetworking/cni\n- type: JSONSchema\n  url: json-schema/cni-network-config-schema.json\n- type: JSONSchema\n  url: json-schema/cni-result-schema.json\n- type: JSONLDContext\n  url: json-ld/cni-context.jsonld\n- type: NaftikoCapabilities\n  url: capabilities/cni-spec-capabilities.yml\n\
  tags:\n- Network Plugins\n- Specification\nx-features:\n- name: ADD operation\n  description: Attach a container to a network and return a Result document with assigned interfaces,\n    IPs, routes, and DNS.\n- name: DEL operation\n  description: Detach a container from a network and tear down allocated resources.\n- name: CHECK operation\n  description: Verify the container's current attachment matches the prior ADD result.\n- name: VERSION operation\n  description: Report the CNI spec versions a plugin supports.\n- name: Plugin Chaining\n  description: Meta-plugin chaining model where a chain shares previous Result via prevResult.\n- name: Network Config Schema\n  description: Schema for the JSON document that describes a network and its plugin chain.\n- name: Result Schema\n  description: Schema for the Result document that plugins emit on stdout.\nx-useCases:\n- name: Kubernetes CNI Plugin\n  description: Implement a CNI plugin that integrates with Kubernetes / containerd / CRI-O.\n\
  - name: Network Validation\n  description: Validate network configurations and plugin Result documents against the spec.\n- name: Custom SDN\n  description: Build custom software-defined networks for containers using a portable plugin contract.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cni/refs/heads/main/apis.yml
tags:
- Network Plugins
- Specification
---
