---
aid: coredns:coredns-dns-api
baseURL: ''
description: CoreDNS implements the standard DNS protocol (RFC 1035) serving both UDP and TCP queries. In Kubernetes, it resolves service names to cluster IPs, headless services to pod IPs, and supports SRV records for port discovery. The Kubernetes plugin watches the API server for service and endpoint changes to keep DNS records current. Additional protocol bindings include DNS-over-TLS (DoT), DNS-over-HTTPS (DoH), DNS-over-QUIC (DoQ), and gRPC.
humanURL: https://coredns.io/manual/toc/
image: ''
layout: api
name: CoreDNS DNS Interface
properties:
- type: Documentation
  url: https://coredns.io/manual/toc/
provider_name: CoreDNS
provider_slug: coredns
slug: coredns-dns-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: coredns:coredns-dns-api\nname: CoreDNS DNS Interface\ndescription: CoreDNS implements the standard DNS protocol (RFC 1035) serving both UDP and TCP queries.\n  In Kubernetes, it resolves service names to cluster IPs, headless services to pod IPs, and supports\n  SRV records for port discovery. The Kubernetes plugin watches the API server for service and endpoint\n  changes to keep DNS records current. Additional protocol bindings include DNS-over-TLS (DoT), DNS-over-HTTPS\n  (DoH), DNS-over-QUIC (DoQ), and gRPC.\nhumanURL: https://coredns.io/manual/toc/\nproperties:\n- type: Documentation\n  url: https://coredns.io/manual/toc/\ntags:\n- DNS\n- DoH\n- DoQ\n- DoT\n- Kubernetes\n- Service Discovery\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coredns/refs/heads/main/apis.yml
tags:
- DNS
- DoH
- DoQ
- DoT
- Kubernetes
- Service Discovery
---
