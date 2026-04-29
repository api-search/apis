---
aid: carvel:kbld
baseURL: ''
description: kbld builds or references container images in Kubernetes configuration in an immutable way by resolving image tags to digests and optionally building images from source during the deployment pipeline.
humanURL: https://carvel.dev/kbld/
image: ''
layout: api
name: kbld
properties:
- type: Documentation
  url: https://carvel.dev/kbld/docs/latest/
- type: GitHub Repository
  url: https://github.com/carvel-dev/kbld
provider_name: Carvel
provider_slug: carvel
slug: kbld
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: carvel:kbld\nname: kbld\ndescription: kbld builds or references container images in Kubernetes configuration in an immutable way\n  by resolving image tags to digests and optionally building images from source during the deployment\n  pipeline.\nhumanURL: https://carvel.dev/kbld/\ntags:\n- Container Images\n- Immutable\n- Kubernetes\nproperties:\n- type: Documentation\n  url: https://carvel.dev/kbld/docs/latest/\n- type: GitHub Repository\n  url: https://github.com/carvel-dev/kbld\nx-features:\n- Resolve image tags to digests\n- Build images from source with Docker/pack\n- Push to registries during deploy\n- Integration with ytt and kapp\nx-use-cases:\n- Ensuring immutable image references\n- Building and deploying images in one pipeline\n- Auditing which images are actually deployed\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/carvel/refs/heads/main/apis.yml
tags:
- Container Images
- Immutable
- Kubernetes
---
