---
aid: caddy:caddy-web-server
baseURL: ''
description: Caddy is an open-source HTTP/2 and HTTP/3 web server and reverse proxy that obtains TLS certificates automatically via Let's Encrypt and ZeroSSL. Configured via a native JSON config, a human-friendly Caddyfile, or dynamically via the admin API. Built on a modular architecture that supports custom modules for virtually any HTTP behavior.
humanURL: https://caddyserver.com/
image: ''
layout: api
name: Caddy Web Server
properties:
- type: Documentation
  url: https://caddyserver.com/docs/
- type: Getting Started
  url: https://caddyserver.com/docs/getting-started
- type: GitHub Repository
  url: https://github.com/caddyserver/caddy
- type: Download
  url: https://caddyserver.com/download
provider_name: Caddy
provider_slug: caddy
slug: caddy-web-server
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: caddy:caddy-web-server\nname: Caddy Web Server\ndescription: Caddy is an open-source HTTP/2 and HTTP/3 web server and reverse proxy that obtains TLS certificates\n  automatically via Let's Encrypt and ZeroSSL. Configured via a native JSON config, a human-friendly Caddyfile,\n  or dynamically via the admin API. Built on a modular architecture that supports custom modules for virtually\n  any HTTP behavior.\nhumanURL: https://caddyserver.com/\ntags:\n- Automatic HTTPS\n- Go\n- Reverse Proxy\n- TLS\n- Web Server\nproperties:\n- type: Documentation\n  url: https://caddyserver.com/docs/\n- type: Getting Started\n  url: https://caddyserver.com/docs/getting-started\n- type: GitHub Repository\n  url: https://github.com/caddyserver/caddy\n- type: Download\n  url: https://caddyserver.com/download\nx-features:\n- Automatic HTTPS via Let's Encrypt and ZeroSSL\n- HTTP/1.1, HTTP/2, HTTP/3 (QUIC) support\n- Dynamic JSON configuration\n- Human-friendly Caddyfile format\n- Reverse proxy\
  \ with load balancing\n- Static file serving with automatic compression\n- Modular architecture with plugins\n- On-demand TLS certificates\n- Wildcard and DNS-01 challenge support\nx-use-cases:\n- Production web and API hosting\n- Zero-config HTTPS reverse proxy\n- Multi-tenant platforms with on-demand TLS\n- Static website hosting with SSL\n- Edge routing for microservices\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/caddy/refs/heads/main/apis.yml
tags:
- Automatic HTTPS
- Go
- Reverse Proxy
- TLS
- Web Server
---
