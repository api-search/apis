---
aid: cert-manager:cert-manager-api
baseURL: ''
description: The cert-manager API extends the Kubernetes API with custom resources including Certificate, Issuer, ClusterIssuer, CertificateRequest, and Order. These resources allow declarative management of TLS certificates, automatic renewal, and integration with ACME and other certificate authorities directly through kubectl and Kubernetes manifests.
humanURL: https://cert-manager.io/docs/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: cert-manager Kubernetes API
properties:
- type: Documentation
  url: https://cert-manager.io/docs/
- type: Reference
  url: https://cert-manager.io/docs/reference/api-docs/
- type: Getting Started
  url: https://cert-manager.io/docs/getting-started/
- type: GitHubRepository
  url: https://github.com/cert-manager/cert-manager
- type: Change Log
  url: https://github.com/cert-manager/cert-manager/releases
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cert-manager/refs/heads/main/json-schema/cert-manager-certificate-schema.json
- type: JSONSchema
  url: https://raw.githubusercontent.com/api-evangelist/cert-manager/refs/heads/main/json-schema/cert-manager-issuer-schema.json
provider_name: Cert-Manager
provider_slug: cert-manager
slug: cert-manager-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: cert-manager:cert-manager-api\nname: cert-manager Kubernetes API\ndescription: The cert-manager API extends the Kubernetes API with custom resources including Certificate,\n  Issuer, ClusterIssuer, CertificateRequest, and Order. These resources allow declarative management of\n  TLS certificates, automatic renewal, and integration with ACME and other certificate authorities directly\n  through kubectl and Kubernetes manifests.\nhumanURL: https://cert-manager.io/docs/\nimage: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nproperties:\n- type: Documentation\n  url: https://cert-manager.io/docs/\n- type: Reference\n  url: https://cert-manager.io/docs/reference/api-docs/\n- type: Getting Started\n  url: https://cert-manager.io/docs/getting-started/\n- type: GitHubRepository\n  url: https://github.com/cert-manager/cert-manager\n- type: Change Log\n  url: https://github.com/cert-manager/cert-manager/releases\n- type: JSONSchema\n  url: json-schema/cert-manager-certificate-schema.json\n\
  - type: JSONSchema\n  url: json-schema/cert-manager-issuer-schema.json\ntags:\n- Certificates\n- Kubernetes API\n- TLS\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cert-manager/refs/heads/main/apis.yml
tags:
- Certificates
- Kubernetes API
- TLS
---
