---
aid: cosign:rekor-api
baseURL: https://rekor.sigstore.dev
description: Rekor is the Sigstore transparency log that cosign writes to and reads from when recording and verifying signing events. The public Rekor service exposes a REST API at rekor.sigstore.dev with operations for creating log entries, retrieving entries by index or UUID, fetching log info and proofs, and searching the index.
humanURL: https://docs.sigstore.dev/logging/overview/
image: ''
layout: api
name: Sigstore Rekor API (consumed)
properties:
- type: Documentation
  url: https://docs.sigstore.dev/logging/overview/
- type: OpenAPI
  url: https://raw.githubusercontent.com/sigstore/rekor/main/openapi.yaml
- type: GitHubRepository
  url: https://github.com/sigstore/rekor
provider_name: Cosign
provider_slug: cosign
slug: rekor-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: cosign:rekor-api\nname: Sigstore Rekor API (consumed)\ndescription: Rekor is the Sigstore transparency log that cosign writes to and reads from when recording\n  and verifying signing events. The public Rekor service exposes a REST API at rekor.sigstore.dev with\n  operations for creating log entries, retrieving entries by index or UUID, fetching log info and proofs,\n  and searching the index.\nhumanURL: https://docs.sigstore.dev/logging/overview/\nbaseURL: https://rekor.sigstore.dev\nproperties:\n- type: Documentation\n  url: https://docs.sigstore.dev/logging/overview/\n- type: OpenAPI\n  url: https://raw.githubusercontent.com/sigstore/rekor/main/openapi.yaml\n- type: GitHubRepository\n  url: https://github.com/sigstore/rekor\ntags:\n- Rekor\n- REST\n- Sigstore\n- Transparency Log\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cosign/refs/heads/main/apis.yml
tags:
- Rekor
- REST
- Sigstore
- Transparency Log
---
