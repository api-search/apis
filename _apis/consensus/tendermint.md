---
aid: consensus:tendermint
baseURL: https://docs.cometbft.com
description: Tendermint (now CometBFT) is a Byzantine fault-tolerant consensus engine that powers Cosmos SDK chains. CometBFT decouples consensus from application logic via the Application Blockchain Interface (ABCI), allowing custom blockchain applications in Go, Rust, and other languages.
humanURL: https://docs.cometbft.com/
image: ''
layout: api
name: Tendermint / CometBFT
properties:
- type: Documentation
  url: https://docs.cometbft.com/
- type: GitHubRepository
  url: https://github.com/cometbft/cometbft
- type: Reference
  url: https://docs.cometbft.com/main/spec/consensus/consensus.html
provider_name: Consensus
provider_slug: consensus
slug: tendermint
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: consensus:tendermint\nname: Tendermint / CometBFT\ndescription: Tendermint (now CometBFT) is a Byzantine fault-tolerant consensus engine that powers Cosmos\n  SDK chains. CometBFT decouples consensus from application logic via the Application Blockchain Interface\n  (ABCI), allowing custom blockchain applications in Go, Rust, and other languages.\nhumanURL: https://docs.cometbft.com/\nbaseURL: https://docs.cometbft.com\ntags:\n- ABCI\n- BFT\n- Blockchain\n- CometBFT\n- Cosmos\nproperties:\n- type: Documentation\n  url: https://docs.cometbft.com/\n- type: GitHubRepository\n  url: https://github.com/cometbft/cometbft\n- type: Reference\n  url: https://docs.cometbft.com/main/spec/consensus/consensus.html\nx-features:\n- Round-based BFT consensus with leader rotation\n- ABCI protocol decouples consensus from application\n- Instant finality on commit\n- Powers Cosmos Hub, Osmosis, and other Cosmos SDK chains\nx-useCases:\n- Building permissioned and permissionless blockchains\n\
  - Custom application chains in the Cosmos ecosystem\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/consensus/refs/heads/main/apis.yml
tags:
- ABCI
- BFT
- Blockchain
- CometBFT
- Cosmos
---
