---
aid: consul-connect:consul-connect-gateways
baseURL: https://developer.hashicorp.com
description: 'Consul Connect supports four gateway types for traffic flowing into and out of the mesh: mesh gateways for cross-datacenter and cross-partition traffic, ingress gateways for North-South entry, terminating gateways for access to non-mesh services, and the Consul API Gateway implementing the Kubernetes Gateway API.'
humanURL: https://developer.hashicorp.com/consul/docs/connect/gateways
image: ''
layout: api
name: Consul Connect Gateways
properties:
- type: Documentation
  url: https://developer.hashicorp.com/consul/docs/connect/gateways
- type: Reference
  url: https://developer.hashicorp.com/consul/docs/connect/gateways/mesh-gateway
- type: Reference
  url: https://developer.hashicorp.com/consul/docs/connect/gateways/ingress-gateway
- type: Reference
  url: https://developer.hashicorp.com/consul/docs/connect/gateways/terminating-gateway
- type: Reference
  url: https://developer.hashicorp.com/consul/docs/api-gateway
provider_name: Consul Connect
provider_slug: consul-connect
slug: consul-connect-gateways
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: consul-connect:consul-connect-gateways\nname: Consul Connect Gateways\ndescription: 'Consul Connect supports four gateway types for traffic flowing into and out of the mesh:\n  mesh gateways for cross-datacenter and cross-partition traffic, ingress gateways for North-South entry,\n  terminating gateways for access to non-mesh services, and the Consul API Gateway implementing the Kubernetes\n  Gateway API.'\nhumanURL: https://developer.hashicorp.com/consul/docs/connect/gateways\nbaseURL: https://developer.hashicorp.com\ntags:\n- API Gateway\n- Gateways\n- Ingress\n- Mesh Gateway\n- Terminating Gateway\nproperties:\n- type: Documentation\n  url: https://developer.hashicorp.com/consul/docs/connect/gateways\n- type: Reference\n  url: https://developer.hashicorp.com/consul/docs/connect/gateways/mesh-gateway\n- type: Reference\n  url: https://developer.hashicorp.com/consul/docs/connect/gateways/ingress-gateway\n- type: Reference\n  url: https://developer.hashicorp.com/consul/docs/connect/gateways/terminating-gateway\n\
  - type: Reference\n  url: https://developer.hashicorp.com/consul/docs/api-gateway\nx-features:\n- Mesh gateways for WAN federation and partition crossing\n- Ingress gateways for L4/L7 ingress with TLS\n- Terminating gateways for non-mesh service access\n- API Gateway implementing the Kubernetes Gateway API\nx-useCases:\n- Federate Consul across datacenters securely\n- Expose mesh services to external clients with TLS\n- Allow mesh services to call legacy non-mesh endpoints\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/consul-connect/refs/heads/main/apis.yml
tags:
- API Gateway
- Gateways
- Ingress
- Mesh Gateway
- Terminating Gateway
---
