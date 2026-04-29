---
aid: consensus:hotstuff
baseURL: https://arxiv.org
description: HotStuff is a leader-based BFT consensus protocol with linear view change and three-chain commit, designed by Yin et al. HotStuff is the foundation for Diem/Libra BFT and inspired modern protocols like Aptos AptosBFT and Sui's Mysticeti.
humanURL: https://arxiv.org/abs/1803.05069
image: ''
layout: api
name: HotStuff
properties:
- type: Specification
  url: https://arxiv.org/abs/1803.05069
- type: Reference
  url: https://github.com/hot-stuff/libhotstuff
- type: Reference
  url: https://github.com/aptos-labs/aptos-core
provider_name: Consensus
provider_slug: consensus
slug: hotstuff
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: consensus:hotstuff\nname: HotStuff\ndescription: HotStuff is a leader-based BFT consensus protocol with linear view change and three-chain\n  commit, designed by Yin et al. HotStuff is the foundation for Diem/Libra BFT and inspired modern protocols\n  like Aptos AptosBFT and Sui's Mysticeti.\nhumanURL: https://arxiv.org/abs/1803.05069\nbaseURL: https://arxiv.org\ntags:\n- BFT\n- HotStuff\n- Linear\nproperties:\n- type: Specification\n  url: https://arxiv.org/abs/1803.05069\n- type: Reference\n  url: https://github.com/hot-stuff/libhotstuff\n- type: Reference\n  url: https://github.com/aptos-labs/aptos-core\nx-features:\n- Linear view change (O(n) message complexity)\n- Three-chain commit rule\n- Optimistic responsiveness\n- Foundation for Diem, Aptos, Sui consensus\nx-useCases:\n- Modern blockchain consensus designs\n- High-throughput, low-latency BFT systems\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/consensus/refs/heads/main/apis.yml
tags:
- BFT
- HotStuff
- Linear
---
