---
aid: copilot-instructions-md:format
baseURL: ''
description: The copilot-instructions.md format is an unstructured Markdown file placed at .github/copilot-instructions.md. GitHub Copilot detects the file automatically and prepends its contents to prompts sent to the model in Copilot Chat, Copilot in the IDE, and the Copilot coding agent. The file accepts free-form natural language instructions, with whitespace between sections ignored, and is rendered as a reference in Copilot Chat replies so users can confirm it was consulted.
humanURL: https://docs.github.com/en/copilot/customizing-copilot/adding-repository-custom-instructions-for-github-copilot
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: copilot-instructions.md Format
properties:
- type: Documentation
  url: https://docs.github.com/en/copilot/customizing-copilot/adding-repository-custom-instructions-for-github-copilot
- type: Blog
  url: https://github.blog/changelog/2025-01-23-custom-instructions-for-github-copilot-in-vs-code-now-generally-available/
- type: Documentation
  url: https://docs.github.com/en/copilot/customizing-copilot/about-customizing-github-copilot-chat-responses
- type: Examples
  url: https://github.com/github/awesome-copilot
provider_name: copilot-instructions.md
provider_slug: copilot-instructions-md
slug: format
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: copilot-instructions-md:format\nname: copilot-instructions.md Format\ntags:\n- Convention\n- GitHub Copilot\n- Markdown\n- Repository\nimage: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://docs.github.com/en/copilot/customizing-copilot/adding-repository-custom-instructions-for-github-copilot\nproperties:\n- url: https://docs.github.com/en/copilot/customizing-copilot/adding-repository-custom-instructions-for-github-copilot\n  type: Documentation\n- url: https://github.blog/changelog/2025-01-23-custom-instructions-for-github-copilot-in-vs-code-now-generally-available/\n  type: Blog\n- url: https://docs.github.com/en/copilot/customizing-copilot/about-customizing-github-copilot-chat-responses\n  type: Documentation\n- url: https://github.com/github/awesome-copilot\n  type: Examples\ndescription: The copilot-instructions.md format is an unstructured Markdown file placed at .github/copilot-instructions.md.\n  GitHub Copilot detects\
  \ the file automatically and prepends its contents to prompts sent to the model\n  in Copilot Chat, Copilot in the IDE, and the Copilot coding agent. The file accepts free-form natural\n  language instructions, with whitespace between sections ignored, and is rendered as a reference in Copilot\n  Chat replies so users can confirm it was consulted.\nx-features:\n- Auto-loaded by GitHub Copilot Chat, IDE plugins, and coding agent\n- Resides at the canonical path .github/copilot-instructions.md\n- Plain Markdown - no required schema or front matter\n- Visible reference in Copilot Chat replies that consume the file\n- Pairs with .github prompt files and Copilot agent rulesets\n- Effective immediately upon save; no Copilot configuration step\nx-useCases:\n- Telling Copilot which test runner, linter, and build commands to use\n- Steering Copilot to preferred libraries or framework patterns\n- Communicating commit message and branch naming conventions\n- Documenting code style, naming, and comment\
  \ conventions\n- Reducing CI failures caused by Copilot generated code\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/copilot-instructions-md/refs/heads/main/apis.yml
tags:
- Convention
- GitHub Copilot
- Markdown
- Repository
---
