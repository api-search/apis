---
aid: containerfile:reference
baseURL: https://github.com
description: The official Containerfile reference shipped with the containers/common project. Documents every Containerfile instruction, syntax, and the ways Containerfile differs from Dockerfile, including secret mounts and platform-aware ARGs.
humanURL: https://github.com/containers/common/blob/main/docs/Containerfile.5.md
image: ''
layout: api
name: Containerfile Reference
properties:
- type: Specification
  url: https://github.com/containers/common/blob/main/docs/Containerfile.5.md
- type: Documentation
  url: https://docs.podman.io/en/latest/markdown/podman-build.1.html
- type: GitHubRepository
  url: https://github.com/containers/common
provider_name: Containerfile
provider_slug: containerfile
slug: reference
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: containerfile:reference\nname: Containerfile Reference\ndescription: The official Containerfile reference shipped with the containers/common project. Documents\n  every Containerfile instruction, syntax, and the ways Containerfile differs from Dockerfile, including\n  secret mounts and platform-aware ARGs.\nhumanURL: https://github.com/containers/common/blob/main/docs/Containerfile.5.md\nbaseURL: https://github.com\ntags:\n- Containerfile\n- Reference\n- containers/common\nproperties:\n- type: Specification\n  url: https://github.com/containers/common/blob/main/docs/Containerfile.5.md\n- type: Documentation\n  url: https://docs.podman.io/en/latest/markdown/podman-build.1.html\n- type: GitHubRepository\n  url: https://github.com/containers/common\nx-features:\n- Documents FROM, RUN, COPY, ADD, ARG, ENV, CMD, ENTRYPOINT, EXPOSE, USER, WORKDIR, VOLUME, LABEL, ONBUILD\n- RUN --mount support for bind, cache, secret, ssh, and tmpfs mounts\n- Platform-aware ARGs (TARGETARCH,\
  \ TARGETOS, TARGETPLATFORM, BUILDARCH, BUILDOS, BUILDPLATFORM)\n- HEREDOC syntax for inline RUN scripts\n- Multi-stage builds via FROM ... AS name\nx-useCases:\n- Authoring portable Containerfiles for Podman and Docker\n- Migrating between Docker and Podman build tooling\n- Defining cross-platform images with multi-arch support\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/containerfile/refs/heads/main/apis.yml
tags:
- Containerfile
- Reference
- containers/common
---
