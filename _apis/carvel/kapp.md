---
aid: carvel:kapp
baseURL: ''
description: kapp is a CLI tool that installs, upgrades, and deletes multiple Kubernetes resources as a single application. It provides change set previews, resource ordering, and convergence detection for predictable deployments.
humanURL: https://carvel.dev/kapp/
image: ''
layout: api
name: kapp
properties:
- type: Documentation
  url: https://carvel.dev/kapp/docs/latest/
- type: GitHub Repository
  url: https://github.com/carvel-dev/kapp
provider_name: Carvel
provider_slug: carvel
slug: kapp
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: carvel:kapp\nname: kapp\ndescription: kapp is a CLI tool that installs, upgrades, and deletes multiple Kubernetes resources as\n  a single application. It provides change set previews, resource ordering, and convergence detection\n  for predictable deployments.\nhumanURL: https://carvel.dev/kapp/\ntags:\n- Deployment\n- Kubernetes\n- Lifecycle\nproperties:\n- type: Documentation\n  url: https://carvel.dev/kapp/docs/latest/\n- type: GitHub Repository\n  url: https://github.com/carvel-dev/kapp\nx-features:\n- Change-set preview before apply\n- Resource ordering and waiting\n- Label-based application grouping\n- Convergence detection on deploy\n- Garbage collection of removed resources\nx-use-cases:\n- Deploying Kubernetes applications atomically\n- Previewing infrastructure changes before apply\n- Managing application lifecycle without Helm\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/carvel/refs/heads/main/apis.yml
tags:
- Deployment
- Kubernetes
- Lifecycle
---
