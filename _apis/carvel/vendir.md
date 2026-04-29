---
aid: carvel:vendir
baseURL: ''
description: vendir declaratively states what files should be in a directory, syncing from upstream sources such as Git repositories, HTTP archives, Helm charts, and OCI images. Enables reproducible vendored configuration.
humanURL: https://carvel.dev/vendir/
image: ''
layout: api
name: vendir
properties:
- type: Documentation
  url: https://carvel.dev/vendir/docs/latest/
- type: GitHub Repository
  url: https://github.com/carvel-dev/vendir
provider_name: Carvel
provider_slug: carvel
slug: vendir
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: carvel:vendir\nname: vendir\ndescription: vendir declaratively states what files should be in a directory, syncing from upstream sources\n  such as Git repositories, HTTP archives, Helm charts, and OCI images. Enables reproducible vendored\n  configuration.\nhumanURL: https://carvel.dev/vendir/\ntags:\n- Configuration\n- Vendoring\nproperties:\n- type: Documentation\n  url: https://carvel.dev/vendir/docs/latest/\n- type: GitHub Repository\n  url: https://github.com/carvel-dev/vendir\nx-features:\n- Declarative sync from Git, HTTP, Helm, OCI\n- Lock files for reproducibility\n- Selective inclusion of files\n- Integration with overlays via ytt\nx-use-cases:\n- Vendoring third-party Kubernetes configuration\n- Pinning upstream Helm charts\n- Reproducible configuration builds\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/carvel/refs/heads/main/apis.yml
tags:
- Configuration
- Vendoring
---
