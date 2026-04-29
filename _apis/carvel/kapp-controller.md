---
aid: carvel:kapp-controller
baseURL: ''
description: kapp-controller is a Kubernetes controller that provides GitOps-style continuous delivery for applications and packages using Carvel tools. It introduces PackageRepository, Package, PackageInstall, and App custom resources for package management.
humanURL: https://carvel.dev/kapp-controller/
image: ''
layout: api
name: kapp-controller
properties:
- type: Documentation
  url: https://carvel.dev/kapp-controller/docs/latest/
- type: GitHub Repository
  url: https://github.com/carvel-dev/kapp-controller
provider_name: Carvel
provider_slug: carvel
slug: kapp-controller
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: carvel:kapp-controller\nname: kapp-controller\ndescription: kapp-controller is a Kubernetes controller that provides GitOps-style continuous delivery\n  for applications and packages using Carvel tools. It introduces PackageRepository, Package, PackageInstall,\n  and App custom resources for package management.\nhumanURL: https://carvel.dev/kapp-controller/\ntags:\n- CRD\n- GitOps\n- Kubernetes\n- Package Management\nproperties:\n- type: Documentation\n  url: https://carvel.dev/kapp-controller/docs/latest/\n- type: GitHub Repository\n  url: https://github.com/carvel-dev/kapp-controller\nx-features:\n- App and Package CRDs\n- PackageRepository for distribution\n- GitOps continuous reconciliation\n- ytt, kbld, and kapp integration\n- Versioning and constraints for packages\nx-use-cases:\n- Kubernetes package management\n- GitOps-driven continuous delivery\n- Distributing internal platform packages\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/carvel/refs/heads/main/apis.yml
tags:
- CRD
- GitOps
- Kubernetes
- Package Management
---
