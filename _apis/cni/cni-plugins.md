---
aid: cni:cni-plugins
baseURL: ''
description: A collection of reference and example networking plugins maintained by the containernetworking team that implement the CNI specification. Includes main plugins such as bridge, ipvlan, macvlan, ptp, host-device, and loopback, as well as meta plugins such as portmap, bandwidth, firewall, sbr, and tuning for additional networking functionality.
humanURL: https://www.cni.dev/plugins/current/
image: ''
layout: api
name: CNI Reference Plugins
properties:
- type: Documentation
  url: https://www.cni.dev/plugins/current/
- type: GitHubRepository
  url: https://github.com/containernetworking/plugins
- type: NaftikoCapabilities
  url: https://raw.githubusercontent.com/api-evangelist/cni/refs/heads/main/capabilities/cni-spec-capabilities.yml
provider_name: Container Network Interface (CNI)
provider_slug: cni
slug: cni-plugins
source_yaml: "aid: cni:cni-plugins\nname: CNI Reference Plugins\ndescription: A collection of reference and example networking plugins maintained by the containernetworking\n  team that implement the CNI specification. Includes main plugins such as bridge, ipvlan, macvlan, ptp,\n  host-device, and loopback, as well as meta plugins such as portmap, bandwidth, firewall, sbr, and tuning\n  for additional networking functionality.\nhumanURL: https://www.cni.dev/plugins/current/\nproperties:\n- type: Documentation\n  url: https://www.cni.dev/plugins/current/\n- type: GitHubRepository\n  url: https://github.com/containernetworking/plugins\n- type: NaftikoCapabilities\n  url: capabilities/cni-spec-capabilities.yml\ntags:\n- Containers\n- Kubernetes\n- Linux\n- Network Plugins\n- Networking\nx-features:\n- name: bridge\n  description: Linux-bridge plugin attaching container veth pairs to a bridge.\n- name: ipvlan\n  description: IPVLAN plugin for L2/L3 IPVLAN attachments.\n- name: macvlan\n  description:\
  \ MACVLAN plugin for MACVLAN attachments.\n- name: host-device\n  description: Plugin that moves an existing host device into a container netns.\n- name: ptp\n  description: Point-to-point veth-pair plugin.\n- name: loopback\n  description: Loopback interface configuration.\n- name: portmap\n  description: Meta-plugin that publishes container ports to the host via NAT.\n- name: bandwidth\n  description: Meta-plugin that applies ingress/egress traffic shaping with tc.\n- name: firewall\n  description: Meta-plugin that applies iptables/nftables rules for a container.\n- name: sbr\n  description: Source-based routing meta-plugin.\nx-useCases:\n- name: Kubernetes Pod Networking\n  description: Use bridge + portmap as a minimal Kubernetes pod networking stack.\n- name: Multi-Network Pods\n  description: Combine reference plugins via Multus or chains for multi-NIC pods.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cni/refs/heads/main/apis.yml
tags:
- Containers
- Kubernetes
- Linux
- Network Plugins
- Networking
---
