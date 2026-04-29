---
aid: conventions-md:related-conventions
baseURL: ''
description: 'CONVENTIONS.md sits alongside several closely related AI coding conventions. CLAUDE.md is used by Claude Code for repository memory. .cursor/rules and .cursorrules are used by Cursor. .github/copilot- instructions.md is used by GitHub Copilot. Each follows a similar pattern: a Markdown or text file describing repository-specific rules that gets injected into the AI assistant prompt context. CONVENTIONS.md is the most tool-agnostic option and is widely adopted across multiple AI coding agents.'
humanURL: https://docs.anthropic.com/en/docs/claude-code/memory
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: AI Coding Conventions Ecosystem
properties:
- type: Documentation
  url: https://docs.anthropic.com/en/docs/claude-code/memory
- type: Documentation
  url: https://docs.cursor.com/context/rules-for-ai
- type: Documentation
  url: https://docs.github.com/en/copilot/customizing-copilot/adding-repository-custom-instructions-for-github-copilot
- type: Documentation
  url: https://aider.chat/docs/usage/conventions.html
provider_name: CONVENTIONS.md
provider_slug: conventions-md
slug: related-conventions
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: conventions-md:related-conventions\nname: AI Coding Conventions Ecosystem\ntags:\n- AI Coding\n- Comparison\n- Conventions\nimage: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://docs.anthropic.com/en/docs/claude-code/memory\nproperties:\n- url: https://docs.anthropic.com/en/docs/claude-code/memory\n  type: Documentation\n- url: https://docs.cursor.com/context/rules-for-ai\n  type: Documentation\n- url: https://docs.github.com/en/copilot/customizing-copilot/adding-repository-custom-instructions-for-github-copilot\n  type: Documentation\n- url: https://aider.chat/docs/usage/conventions.html\n  type: Documentation\ndescription: 'CONVENTIONS.md sits alongside several closely related AI coding conventions. CLAUDE.md is\n  used by Claude Code for repository memory. .cursor/rules and .cursorrules are used by Cursor. .github/copilot-\n  instructions.md is used by GitHub Copilot. Each follows a similar pattern: a Markdown or text file\
  \ describing\n  repository-specific rules that gets injected into the AI assistant prompt context. CONVENTIONS.md is\n  the most tool-agnostic option and is widely adopted across multiple AI coding agents.'\nx-features:\n- Tool-agnostic file naming compared to CLAUDE.md or .cursorrules\n- Often committed to repo root for visibility to humans and AI\n- Frequently referenced by other agent files such as CLAUDE.md\n- Composable with .editorconfig, .prettierrc, and lint configurations\nx-useCases:\n- Sharing one set of rules across aider, Cursor, Cline, and Claude Code\n- Consolidating coding standards for human and AI contributors\n- Documenting cross-cutting concerns separate from tool-specific config\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/conventions-md/refs/heads/main/apis.yml
tags:
- AI Coding
- Comparison
- Conventions
---
