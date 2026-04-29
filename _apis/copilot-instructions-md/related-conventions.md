---
aid: copilot-instructions-md:related-conventions
baseURL: ''
description: Repository copilot-instructions.md is one layer in a stack of GitHub Copilot customization options. Personal custom instructions apply to a single user across all repositories. Organization custom instructions apply to every repository in a GitHub organization. Path-scoped .github/instructions/*.instructions.md files target specific files or globs. Prompt files in .github/prompts/ provide reusable named prompts. The copilot-instructions.md file sits at the repository tier and travels with the code, providing the same context to every collaborator.
humanURL: https://docs.github.com/en/copilot/customizing-copilot
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Copilot Instructions Ecosystem
properties:
- type: Documentation
  url: https://docs.github.com/en/copilot/customizing-copilot
- type: Documentation
  url: https://docs.github.com/en/copilot/customizing-copilot/adding-personal-custom-instructions-for-github-copilot
- type: Documentation
  url: https://docs.github.com/en/copilot/customizing-copilot/adding-organization-custom-instructions-for-github-copilot
- type: Documentation
  url: https://docs.github.com/en/copilot/customizing-copilot/adding-prompt-files-to-your-repository
provider_name: copilot-instructions.md
provider_slug: copilot-instructions-md
slug: related-conventions
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: copilot-instructions-md:related-conventions\nname: Copilot Instructions Ecosystem\ntags:\n- AI Coding\n- Conventions\n- GitHub Copilot\nimage: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nhumanURL: https://docs.github.com/en/copilot/customizing-copilot\nproperties:\n- url: https://docs.github.com/en/copilot/customizing-copilot\n  type: Documentation\n- url: https://docs.github.com/en/copilot/customizing-copilot/adding-personal-custom-instructions-for-github-copilot\n  type: Documentation\n- url: https://docs.github.com/en/copilot/customizing-copilot/adding-organization-custom-instructions-for-github-copilot\n  type: Documentation\n- url: https://docs.github.com/en/copilot/customizing-copilot/adding-prompt-files-to-your-repository\n  type: Documentation\ndescription: Repository copilot-instructions.md is one layer in a stack of GitHub Copilot customization\n  options. Personal custom instructions apply to a single user across all repositories.\
  \ Organization custom\n  instructions apply to every repository in a GitHub organization. Path-scoped .github/instructions/*.instructions.md\n  files target specific files or globs. Prompt files in .github/prompts/ provide reusable named prompts.\n  The copilot-instructions.md file sits at the repository tier and travels with the code, providing the\n  same context to every collaborator.\nx-features:\n- Composes with personal and organization-level instructions\n- Path-scoped .instructions.md files override repo-wide instructions\n- Reusable prompts in .github/prompts/*.prompt.md\n- Effective in Copilot Chat, Copilot in IDE, and Copilot coding agent\n- Versioned and reviewed alongside code through pull requests\nx-useCases:\n- Applying organization-wide guardrails across all repos\n- Layering repo-specific rules on top of organization defaults\n- Targeting language-specific conventions to subdirectories\n- Sharing reusable named prompts with all collaborators\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/copilot-instructions-md/refs/heads/main/apis.yml
tags:
- AI Coding
- Conventions
- GitHub Copilot
---
