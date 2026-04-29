---
aid: carvel:secretgen-controller
baseURL: ''
description: secretgen-controller provides CRDs to generate Kubernetes Secrets, export and import secrets across namespaces, and manage certificate and password creation declaratively.
humanURL: https://github.com/carvel-dev/secretgen-controller
image: ''
layout: api
name: secretgen-controller
properties:
- type: GitHub Repository
  url: https://github.com/carvel-dev/secretgen-controller
provider_name: Carvel
provider_slug: carvel
slug: secretgen-controller
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: carvel:secretgen-controller\nname: secretgen-controller\ndescription: secretgen-controller provides CRDs to generate Kubernetes Secrets, export and import secrets\n  across namespaces, and manage certificate and password creation declaratively.\nhumanURL: https://github.com/carvel-dev/secretgen-controller\ntags:\n- CRD\n- Kubernetes\n- Secrets\nproperties:\n- type: GitHub Repository\n  url: https://github.com/carvel-dev/secretgen-controller\nx-features:\n- Generate Certificates, Passwords, RSA Keys, SSH Keys\n- Cross-namespace secret export/import\n- Declarative secret management via CRDs\nx-use-cases:\n- Generating bootstrap credentials\n- Sharing secrets across namespaces\n- Declarative certificate management\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/carvel/refs/heads/main/apis.yml
tags:
- CRD
- Kubernetes
- Secrets
---
