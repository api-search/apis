---
aid: copa:scanner-plugins
baseURL: https://project-copacetic.github.io
description: Copa exposes a plugin interface that allows third-party vulnerability scanners to feed reports into the patcher. Out of the box, Copa supports Trivy JSON reports and provides documentation for adding new scanner plugins.
humanURL: https://project-copacetic.github.io/copacetic/website/scanner-plugins/
image: ''
layout: api
name: Copa Scanner Plugin Interface
properties:
- type: Documentation
  url: https://project-copacetic.github.io/copacetic/website/scanner-plugins/
- type: Reference
  url: https://github.com/project-copacetic/copacetic/tree/main/pkg/vex
provider_name: Copa (Project Copacetic)
provider_slug: copa
slug: scanner-plugins
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: copa:scanner-plugins\nname: Copa Scanner Plugin Interface\ndescription: Copa exposes a plugin interface that allows third-party vulnerability scanners to feed reports\n  into the patcher. Out of the box, Copa supports Trivy JSON reports and provides documentation for adding\n  new scanner plugins.\nhumanURL: https://project-copacetic.github.io/copacetic/website/scanner-plugins/\nbaseURL: https://project-copacetic.github.io\ntags:\n- Plugins\n- Scanners\n- Trivy\nproperties:\n- type: Documentation\n  url: https://project-copacetic.github.io/copacetic/website/scanner-plugins/\n- type: Reference\n  url: https://github.com/project-copacetic/copacetic/tree/main/pkg/vex\nx-features:\n- Trivy JSON parser built in\n- Pluggable interface for additional scanners\n- Standardized intermediate representation of vulnerability reports\nx-useCases:\n- Integrating internal vulnerability scanners with Copa\n- Using Grype, Snyk, or Anchore reports as Copa input\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/copa/refs/heads/main/apis.yml
tags:
- Plugins
- Scanners
- Trivy
---
