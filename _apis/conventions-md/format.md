---
aid: conventions-md:format
baseURL: ''
description: The CONVENTIONS.md format is a free-form Markdown file describing the coding rules an AI coding agent should follow inside a repository. The file is loaded into the chat context, typically in read-only mode, and may be referenced via /read CONVENTIONS.md, the --read CLI flag, or a persistent read entry in .aider.conf.yml. Common content includes preferred libraries, language and version targets, type system rules, lint and format expectations, error handling style, and architectural patterns the project favors.
humanURL: https://aider.chat/docs/usage/conventions.html
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CONVENTIONS.md Format
properties:
- type: Documentation
  url: https://aider.chat/docs/usage/conventions.html
- type: Documentation
  url: https://aider.chat/docs/config/aider_conf.html
- type: Repository
  url: https://github.com/Aider-AI/aider
provider_name: CONVENTIONS.md
provider_slug: conventions-md
slug: format
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: conventions-md:format\nname: CONVENTIONS.md Format\ntags:\n- AI Coding\n- Convention\n- Markdown\n- Project Configuration\nimage: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://aider.chat/docs/usage/conventions.html\nproperties:\n- url: https://aider.chat/docs/usage/conventions.html\n  type: Documentation\n- url: https://aider.chat/docs/config/aider_conf.html\n  type: Documentation\n- url: https://github.com/Aider-AI/aider\n  type: Repository\ndescription: The CONVENTIONS.md format is a free-form Markdown file describing the coding rules an AI\n  coding agent should follow inside a repository. The file is loaded into the chat context, typically\n  in read-only mode, and may be referenced via /read CONVENTIONS.md, the --read CLI flag, or a persistent\n  read entry in .aider.conf.yml. Common content includes preferred libraries, language and version targets,\n  type system rules, lint and format expectations, error handling style,\
  \ and architectural patterns the\n  project favors.\nx-features:\n- Plain Markdown bullet list of project rules\n- Loaded into AI agent context per session or via config\n- Supports prompt caching when marked read-only\n- Composable alongside CLAUDE.md, .cursor/rules, and copilot-instructions\n- No required schema, allowing each project to define what matters\nx-useCases:\n- Steering AI agents toward preferred libraries and frameworks\n- Documenting type hint, naming, and lint requirements\n- Capturing architecture decisions for AI assisted refactors\n- Aligning human and AI contributors on a single source of conventions\n- Reducing rework caused by AI generated code that misses team norms\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/conventions-md/refs/heads/main/apis.yml
tags:
- AI Coding
- Convention
- Markdown
- Project Configuration
---
