---
aid: consensus:pbft
baseURL: http://pmg.csail.mit.edu
description: PBFT, by Castro and Liskov (1999), is a Byzantine fault-tolerant consensus protocol that tolerates up to f Byzantine failures with 3f+1 replicas. PBFT influenced subsequent BFT protocols including Tendermint and HotStuff.
humanURL: http://pmg.csail.mit.edu/papers/osdi99.pdf
image: ''
layout: api
name: Practical Byzantine Fault Tolerance (PBFT)
properties:
- type: Specification
  url: http://pmg.csail.mit.edu/papers/osdi99.pdf
- type: Reference
  url: https://en.wikipedia.org/wiki/Byzantine_fault
provider_name: Consensus
provider_slug: consensus
slug: pbft
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: consensus:pbft\nname: Practical Byzantine Fault Tolerance (PBFT)\ndescription: PBFT, by Castro and Liskov (1999), is a Byzantine fault-tolerant consensus protocol that\n  tolerates up to f Byzantine failures with 3f+1 replicas. PBFT influenced subsequent BFT protocols including\n  Tendermint and HotStuff.\nhumanURL: http://pmg.csail.mit.edu/papers/osdi99.pdf\nbaseURL: http://pmg.csail.mit.edu\ntags:\n- BFT\n- PBFT\nproperties:\n- type: Specification\n  url: http://pmg.csail.mit.edu/papers/osdi99.pdf\n- type: Reference\n  url: https://en.wikipedia.org/wiki/Byzantine_fault\nx-features:\n- Tolerates Byzantine (arbitrary) failures\n- Three-phase commit protocol (pre-prepare, prepare, commit)\n- Foundation for many blockchain BFT consensus algorithms\nx-useCases:\n- Permissioned blockchains\n- Hardened configuration systems\n- Research baseline for new BFT protocols\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/consensus/refs/heads/main/apis.yml
tags:
- BFT
- PBFT
---
