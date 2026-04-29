---
aid: containerfile:oci-image-spec
baseURL: https://github.com
description: The Open Container Initiative Image Specification defines the format of the image artifacts that Containerfile and Dockerfile builds produce. The spec covers manifests, configuration, layers, and indexes consumed by container runtimes such as runc, crun, and containerd.
humanURL: https://github.com/opencontainers/image-spec
image: ''
layout: api
name: OCI Image Specification
properties:
- type: Specification
  url: https://github.com/opencontainers/image-spec
- type: GitHubRepository
  url: https://github.com/opencontainers/image-spec
- type: Reference
  url: https://opencontainers.org/
provider_name: Containerfile
provider_slug: containerfile
slug: oci-image-spec
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: containerfile:oci-image-spec\nname: OCI Image Specification\ndescription: The Open Container Initiative Image Specification defines the format of the image artifacts\n  that Containerfile and Dockerfile builds produce. The spec covers manifests, configuration, layers,\n  and indexes consumed by container runtimes such as runc, crun, and containerd.\nhumanURL: https://github.com/opencontainers/image-spec\nbaseURL: https://github.com\ntags:\n- Image\n- OCI\n- Standards\nproperties:\n- type: Specification\n  url: https://github.com/opencontainers/image-spec\n- type: GitHubRepository\n  url: https://github.com/opencontainers/image-spec\n- type: Reference\n  url: https://opencontainers.org/\nx-features:\n- Image manifest, configuration, and layer schema\n- Image index for multi-platform images\n- Foundational spec for OCI registries and runtimes\nx-useCases:\n- Building tools that produce OCI images directly\n- Verifying that Containerfile output conforms to OCI\n- Implementing\
  \ multi-arch image manifests\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/containerfile/refs/heads/main/apis.yml
tags:
- Image
- OCI
- Standards
---
