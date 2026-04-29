---
aid: copa:vex
baseURL: https://project-copacetic.github.io
description: Copa can emit a Vulnerability Exchange (VEX) document describing which CVEs were patched. VEX documents help security teams and downstream consumers verify that an image has been remediated and track residual risk.
humanURL: https://project-copacetic.github.io/copacetic/website/output/
image: ''
layout: api
name: Copa VEX Output
properties:
- type: Documentation
  url: https://project-copacetic.github.io/copacetic/website/output/
- type: Reference
  url: https://github.com/openvex/spec
provider_name: Copa (Project Copacetic)
provider_slug: copa
slug: vex
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: copa:vex\nname: Copa VEX Output\ndescription: Copa can emit a Vulnerability Exchange (VEX) document describing which CVEs were patched.\n  VEX documents help security teams and downstream consumers verify that an image has been remediated\n  and track residual risk.\nhumanURL: https://project-copacetic.github.io/copacetic/website/output/\nbaseURL: https://project-copacetic.github.io\ntags:\n- OpenVEX\n- SBOM\n- VEX\nproperties:\n- type: Documentation\n  url: https://project-copacetic.github.io/copacetic/website/output/\n- type: Reference\n  url: https://github.com/openvex/spec\nx-features:\n- Emits OpenVEX-compatible documents\n- Records patched CVE identifiers and statuses\n- Pairs with SBOMs for supply chain transparency\nx-useCases:\n- Communicating remediation status downstream\n- Reducing scanner noise from CVEs already patched in place\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/copa/refs/heads/main/apis.yml
tags:
- OpenVEX
- SBOM
- VEX
---
