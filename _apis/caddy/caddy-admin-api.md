---
aid: caddy:caddy-admin-api
baseURL: http://localhost:2019
description: Caddy exposes a RESTful administration API on localhost:2019 by default for dynamically loading and modifying server configuration at runtime without restarts. Endpoints support loading full JSON configs, traversing and mutating specific config paths, adapting Caddyfile to JSON, and querying PKI and reverse proxy state.
humanURL: https://caddyserver.com/docs/api
image: ''
layout: api
name: Caddy Admin API
properties:
- type: Documentation
  url: https://caddyserver.com/docs/api
- type: JSON Config Structure
  url: https://caddyserver.com/docs/json/
- type: Modules Reference
  url: https://caddyserver.com/docs/modules/
- type: API Tutorial
  url: https://caddyserver.com/docs/api-tutorial
provider_name: Caddy
provider_slug: caddy
slug: caddy-admin-api
source_yaml: "aid: caddy:caddy-admin-api\nname: Caddy Admin API\ndescription: Caddy exposes a RESTful administration API on localhost:2019 by default for dynamically loading\n  and modifying server configuration at runtime without restarts. Endpoints support loading full JSON\n  configs, traversing and mutating specific config paths, adapting Caddyfile to JSON, and querying PKI\n  and reverse proxy state.\nhumanURL: https://caddyserver.com/docs/api\nbaseURL: http://localhost:2019\ntags:\n- Admin API\n- Configuration\n- REST\nproperties:\n- type: Documentation\n  url: https://caddyserver.com/docs/api\n- type: JSON Config Structure\n  url: https://caddyserver.com/docs/json/\n- type: Modules Reference\n  url: https://caddyserver.com/docs/modules/\n- type: API Tutorial\n  url: https://caddyserver.com/docs/api-tutorial\nx-features:\n- POST /load for full config replacement\n- GET/POST/PUT/PATCH/DELETE /config/[path] for granular updates\n- POST /adapt to convert Caddyfile to JSON without loading\n\
  - POST /stop for graceful shutdown\n- GET /pki/ca/{id} for internal CA inspection\n- GET /reverse_proxy/upstreams for upstream status\n- ETag and If-Match concurrency control\nx-use-cases:\n- Dynamic configuration in orchestrated environments\n- Multi-tenant SaaS with per-tenant routes\n- Zero-downtime config changes\n- Integration with service discovery\n- Observability of upstream health\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/caddy/refs/heads/main/apis.yml
tags:
- Admin API
- Configuration
- REST
---
