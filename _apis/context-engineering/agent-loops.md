---
aid: context-engineering:agent-loops
baseURL: https://docs.anthropic.com
description: 'Agentic loops are iterative reasoning patterns in which an LLM plans, calls tools, observes results, and refines its plan. Tool design is a central context engineering concern: tools must be token-efficient, have minimal overlap, and include clear, motivating descriptions.'
humanURL: https://docs.anthropic.com/en/docs/build-with-claude/tool-use/overview
image: ''
layout: api
name: Agentic Loops and Tool Use
properties:
- type: Documentation
  url: https://docs.anthropic.com/en/docs/build-with-claude/tool-use/overview
- type: Reference
  url: https://platform.openai.com/docs/guides/function-calling
- type: Reference
  url: https://arxiv.org/abs/2210.03629
provider_name: Context Engineering
provider_slug: context-engineering
slug: agent-loops
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: context-engineering:agent-loops\nname: Agentic Loops and Tool Use\ndescription: 'Agentic loops are iterative reasoning patterns in which an LLM plans, calls tools, observes\n  results, and refines its plan. Tool design is a central context engineering concern: tools must be token-efficient,\n  have minimal overlap, and include clear, motivating descriptions.'\nhumanURL: https://docs.anthropic.com/en/docs/build-with-claude/tool-use/overview\nbaseURL: https://docs.anthropic.com\ntags:\n- Agents\n- Function Calling\n- ReAct\n- Tool Use\nproperties:\n- type: Documentation\n  url: https://docs.anthropic.com/en/docs/build-with-claude/tool-use/overview\n- type: Reference\n  url: https://platform.openai.com/docs/guides/function-calling\n- type: Reference\n  url: https://arxiv.org/abs/2210.03629\nx-features:\n- Tool definitions with JSON Schema arguments\n- Iterative plan-act-observe loops\n- Parallel tool invocation\n- Server- and client-side tool execution\nx-useCases:\n- Building\
  \ task-completing AI agents\n- Wiring LLMs to internal APIs and databases\n- Decomposing complex problems with sub-tools\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/context-engineering/refs/heads/main/apis.yml
tags:
- Agents
- Function Calling
- ReAct
- Tool Use
---
