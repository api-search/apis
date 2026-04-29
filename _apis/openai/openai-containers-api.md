---
aid: openai:openai-containers-api
baseURL: https://api.openai.com
description: The Containers API manages sandboxed containers used by Code Interpreter for running Python, data work, file transforms, and iterative debugging. Containers can be created explicitly or auto-managed, with configurable memory limits of 1g, 4g, 16g, or 64g. Container files can be uploaded, listed, retrieved, and downloaded. Containers expire after 20 minutes of inactivity.
humanURL: https://platform.openai.com/docs/api-reference/containers
image: ''
layout: api
name: OpenAI Containers API
properties:
- type: Documentation
  url: https://platform.openai.com/docs/api-reference/containers
- type: Documentation
  url: https://platform.openai.com/docs/api-reference/container-files
- type: Documentation
  url: https://developers.openai.com/api/docs/guides/tools-code-interpreter/
provider_name: OpenAI
provider_slug: openai
slug: openai-containers-api
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: openai:openai-containers-api\nname: OpenAI Containers API\ntags:\n- Code Interpreter\n- Containers\n- Sandbox\nscore: 100\nbaseURL: https://api.openai.com\nhumanURL: https://platform.openai.com/docs/api-reference/containers\nproperties:\n- url: https://platform.openai.com/docs/api-reference/containers\n  type: Documentation\n- url: https://platform.openai.com/docs/api-reference/container-files\n  type: Documentation\n- url: https://developers.openai.com/api/docs/guides/tools-code-interpreter/\n  type: Documentation\ndescription: The Containers API manages sandboxed containers used by Code Interpreter for running Python,\n  data work, file transforms, and iterative debugging. Containers can be created explicitly or auto-managed,\n  with configurable memory limits of 1g, 4g, 16g, or 64g. Container files can be uploaded, listed, retrieved,\n  and downloaded. Containers expire after 20 minutes of inactivity.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/apis.yml
tags:
- Code Interpreter
- Containers
- Sandbox
---
