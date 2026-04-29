---
aid: canonical:lxd-api
baseURL: https://<host>:8443/1.0
description: The REST API exposed by LXD, Canonical's system-container and VM manager. All client–daemon communication happens over HTTPS (remote) or a Unix socket (local). Provides endpoints for instances, images, networks, storage pools, profiles, projects, cluster members, and events. Fully documented in an auto-generated OpenAPI (Swagger) spec.
humanURL: https://documentation.ubuntu.com/lxd/latest/rest-api/
image: ''
layout: api
name: LXD REST API
properties:
- type: Documentation
  url: https://documentation.ubuntu.com/lxd/latest/rest-api/
- type: OpenAPI
  url: https://github.com/canonical/lxd/blob/main/doc/rest-api.yaml
- type: Reference
  url: https://linuxcontainers.org/lxd/rest-api/
provider_name: Canonical
provider_slug: canonical
slug: lxd-api
source_yaml: "aid: canonical:lxd-api\nname: LXD REST API\ndescription: The REST API exposed by LXD, Canonical's system-container and VM manager. All client–daemon\n  communication happens over HTTPS (remote) or a Unix socket (local). Provides endpoints for instances,\n  images, networks, storage pools, profiles, projects, cluster members, and events. Fully documented in\n  an auto-generated OpenAPI (Swagger) spec.\nhumanURL: https://documentation.ubuntu.com/lxd/latest/rest-api/\nbaseURL: https://<host>:8443/1.0\ntags:\n- Containers\n- Virtualisation\n- OpenAPI\nproperties:\n- type: Documentation\n  url: https://documentation.ubuntu.com/lxd/latest/rest-api/\n- type: OpenAPI\n  url: https://github.com/canonical/lxd/blob/main/doc/rest-api.yaml\n- type: Reference\n  url: https://linuxcontainers.org/lxd/rest-api/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/canonical/refs/heads/main/apis.yml
tags:
- Containers
- Virtualisation
- OpenAPI
---
