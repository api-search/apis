---
aid: context-engineering:retrieval-augmented-generation
baseURL: https://arxiv.org
description: RAG is a context engineering pattern that augments LLM prompts with passages retrieved at inference time from a vector store, search index, or knowledge base. RAG keeps facts outside the model and is one of the most widely used context engineering techniques.
humanURL: https://arxiv.org/abs/2005.11401
image: ''
layout: api
name: Retrieval-Augmented Generation (RAG)
properties:
- type: Specification
  url: https://arxiv.org/abs/2005.11401
- type: Reference
  url: https://docs.llamaindex.ai/
- type: Reference
  url: https://python.langchain.com/docs/concepts/rag/
provider_name: Context Engineering
provider_slug: context-engineering
slug: retrieval-augmented-generation
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: context-engineering:retrieval-augmented-generation\nname: Retrieval-Augmented Generation (RAG)\ndescription: RAG is a context engineering pattern that augments LLM prompts with passages retrieved at\n  inference time from a vector store, search index, or knowledge base. RAG keeps facts outside the model\n  and is one of the most widely used context engineering techniques.\nhumanURL: https://arxiv.org/abs/2005.11401\nbaseURL: https://arxiv.org\ntags:\n- Embeddings\n- Knowledge Base\n- RAG\n- Retrieval\nproperties:\n- type: Specification\n  url: https://arxiv.org/abs/2005.11401\n- type: Reference\n  url: https://docs.llamaindex.ai/\n- type: Reference\n  url: https://python.langchain.com/docs/concepts/rag/\nx-features:\n- Pluggable retrievers over vector and keyword indexes\n- Pre-retrieval rewriting and post-retrieval re-ranking\n- Hybrid retrieval combining BM25 and dense vectors\n- Citations and grounding for answer auditing\nx-useCases:\n- Domain-specific question answering\
  \ over private documents\n- Customer support agents with up-to-date knowledge\n- Long-tail factual recall outside model training\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/context-engineering/refs/heads/main/apis.yml
tags:
- Embeddings
- Knowledge Base
- RAG
- Retrieval
---
