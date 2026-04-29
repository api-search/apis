---
aid: cosign:fulcio-api
baseURL: https://fulcio.sigstore.dev
description: Fulcio is the Sigstore certificate authority that issues short-lived X.509 code-signing certificates bound to OIDC identities. Cosign calls the Fulcio public CA at fulcio.sigstore.dev during keyless signing to obtain a certificate for a verified identity.
humanURL: https://docs.sigstore.dev/certificate_authority/overview/
image: ''
layout: api
name: Sigstore Fulcio API (consumed)
properties:
- type: Documentation
  url: https://docs.sigstore.dev/certificate_authority/overview/
- type: GitHubRepository
  url: https://github.com/sigstore/fulcio
provider_name: Cosign
provider_slug: cosign
slug: fulcio-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: cosign:fulcio-api\nname: Sigstore Fulcio API (consumed)\ndescription: Fulcio is the Sigstore certificate authority that issues short-lived X.509 code-signing certificates\n  bound to OIDC identities. Cosign calls the Fulcio public CA at fulcio.sigstore.dev during keyless signing\n  to obtain a certificate for a verified identity.\nhumanURL: https://docs.sigstore.dev/certificate_authority/overview/\nbaseURL: https://fulcio.sigstore.dev\nproperties:\n- type: Documentation\n  url: https://docs.sigstore.dev/certificate_authority/overview/\n- type: GitHubRepository\n  url: https://github.com/sigstore/fulcio\ntags:\n- CA\n- Certificates\n- Fulcio\n- OIDC\n- Sigstore\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cosign/refs/heads/main/apis.yml
tags:
- CA
- Certificates
- Fulcio
- OIDC
- Sigstore
---
