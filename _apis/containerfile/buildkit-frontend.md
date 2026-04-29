---
aid: containerfile:buildkit-frontend
baseURL: https://github.com
description: Dockerfile and Containerfile parsing in modern Docker is performed by BuildKit's Dockerfile frontend, distributed as a container image (docker/dockerfile). The frontend version is selected via the `# syntax=` directive and adds new features without requiring a BuildKit upgrade.
humanURL: https://github.com/moby/buildkit/blob/master/frontend/dockerfile/docs/reference.md
image: ''
layout: api
name: BuildKit Dockerfile Frontend
properties:
- type: Documentation
  url: https://github.com/moby/buildkit/blob/master/frontend/dockerfile/docs/reference.md
- type: GitHubRepository
  url: https://github.com/moby/buildkit
- type: Reference
  url: https://hub.docker.com/r/docker/dockerfile
provider_name: Containerfile
provider_slug: containerfile
slug: buildkit-frontend
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: containerfile:buildkit-frontend\nname: BuildKit Dockerfile Frontend\ndescription: Dockerfile and Containerfile parsing in modern Docker is performed by BuildKit's Dockerfile\n  frontend, distributed as a container image (docker/dockerfile). The frontend version is selected via\n  the `# syntax=` directive and adds new features without requiring a BuildKit upgrade.\nhumanURL: https://github.com/moby/buildkit/blob/master/frontend/dockerfile/docs/reference.md\nbaseURL: https://github.com\ntags:\n- BuildKit\n- Frontend\n- Moby\nproperties:\n- type: Documentation\n  url: https://github.com/moby/buildkit/blob/master/frontend/dockerfile/docs/reference.md\n- type: GitHubRepository\n  url: https://github.com/moby/buildkit\n- type: Reference\n  url: https://hub.docker.com/r/docker/dockerfile\nx-features:\n- Versioned Dockerfile frontend images\n- Pluggable parser via `# syntax=` directive\n- Adds RUN --mount, secret, ssh, and cache features\n- Used by docker buildx and BuildKit-based\
  \ builders\nx-useCases:\n- Pinning the Dockerfile frontend version for reproducibility\n- Adopting new RUN features without upgrading the daemon\n- Authoring Dockerfile linting rules and tools\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/containerfile/refs/heads/main/apis.yml
tags:
- BuildKit
- Frontend
- Moby
---
