---
aid: copa:cli
baseURL: https://project-copacetic.github.io
description: The copa command line interface used to patch container images. The core subcommand `copa patch` accepts an image reference and an optional vulnerability report and produces a new tagged image with OS-level package vulnerabilities remediated via BuildKit.
humanURL: https://project-copacetic.github.io/copacetic/website/
image: ''
layout: api
name: Copa CLI
properties:
- type: Documentation
  url: https://project-copacetic.github.io/copacetic/website/
- type: Reference
  url: https://project-copacetic.github.io/copacetic/website/quick-start/
- type: GitHubRepository
  url: https://github.com/project-copacetic/copacetic
- type: License
  url: https://github.com/project-copacetic/copacetic/blob/main/LICENSE
- type: Issue Tracker
  url: https://github.com/project-copacetic/copacetic/issues
provider_name: Copa (Project Copacetic)
provider_slug: copa
slug: cli
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: copa:cli\nname: Copa CLI\ndescription: The copa command line interface used to patch container images. The core subcommand `copa\n  patch` accepts an image reference and an optional vulnerability report and produces a new tagged image\n  with OS-level package vulnerabilities remediated via BuildKit.\nhumanURL: https://project-copacetic.github.io/copacetic/website/\nbaseURL: https://project-copacetic.github.io\ntags:\n- CLI\n- Patching\nproperties:\n- type: Documentation\n  url: https://project-copacetic.github.io/copacetic/website/\n- type: Reference\n  url: https://project-copacetic.github.io/copacetic/website/quick-start/\n- type: GitHubRepository\n  url: https://github.com/project-copacetic/copacetic\n- type: License\n  url: https://github.com/project-copacetic/copacetic/blob/main/LICENSE\n- type: Issue Tracker\n  url: https://github.com/project-copacetic/copacetic/issues\nx-features:\n- '`copa patch -i IMAGE` patches all outdated OS packages'\n- '`copa patch -r REPORT.json\
  \ -i IMAGE` patches based on a Trivy report'\n- Multi-platform image patching\n- Distroless image support\n- Pluggable scanner plugins\n- VEX (Vulnerability Exchange) document generation\nx-useCases:\n- Remediating OS-level CVEs in third-party container images\n- Continuously patching base images during security incidents\n- Inserting Copa into CI/CD pipelines after Trivy scans\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/copa/refs/heads/main/apis.yml
tags:
- CLI
- Patching
---
