---
aid: context-engineering:long-horizon-strategies
baseURL: https://www.anthropic.com
description: Long-horizon strategies handle conversations and tasks that exceed the context window. Techniques include compaction (summarizing history into a smaller representation), structured note taking (persistent external memory), and multi-agent decomposition where sub-agents handle bounded subtasks and return condensed summaries.
humanURL: https://www.anthropic.com/news/contextual-retrieval
image: ''
layout: api
name: Long-Horizon Context Strategies
properties:
- type: Documentation
  url: https://www.anthropic.com/news/contextual-retrieval
- type: Reference
  url: https://www.anthropic.com/research/swe-bench-sonnet
- type: Reference
  url: https://github.com/microsoft/autogen
provider_name: Context Engineering
provider_slug: context-engineering
slug: long-horizon-strategies
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: context-engineering:long-horizon-strategies\nname: Long-Horizon Context Strategies\ndescription: Long-horizon strategies handle conversations and tasks that exceed the context window. Techniques\n  include compaction (summarizing history into a smaller representation), structured note taking (persistent\n  external memory), and multi-agent decomposition where sub-agents handle bounded subtasks and return\n  condensed summaries.\nhumanURL: https://www.anthropic.com/news/contextual-retrieval\nbaseURL: https://www.anthropic.com\ntags:\n- Compaction\n- Long Context\n- Memory\n- Multi-Agent\nproperties:\n- type: Documentation\n  url: https://www.anthropic.com/news/contextual-retrieval\n- type: Reference\n  url: https://www.anthropic.com/research/swe-bench-sonnet\n- type: Reference\n  url: https://github.com/microsoft/autogen\nx-features:\n- Conversation summarization for compaction\n- Persistent memory files for cross-session knowledge\n- Multi-agent decomposition with bounded\
  \ sub-agents\n- Hierarchical planning over long-running tasks\nx-useCases:\n- Long-running coding agents and SWE assistants\n- Multi-day customer engagements requiring memory\n- Complex research tasks decomposed across sub-agents\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/context-engineering/refs/heads/main/apis.yml
tags:
- Compaction
- Long Context
- Memory
- Multi-Agent
---
