---
aid: consensus:raft
baseURL: https://raft.github.io
description: Raft is a consensus algorithm designed for understandability, published by Ongaro and Ousterhout in 2014. Raft separates leader election, log replication, and safety into distinct concepts and is implemented widely in etcd, Consul, CockroachDB, TiKV, MongoDB, and many other production systems.
humanURL: https://raft.github.io/
image: ''
layout: api
name: Raft
properties:
- type: Specification
  url: https://raft.github.io/raft.pdf
- type: Documentation
  url: https://raft.github.io/
- type: Reference
  url: https://thesecretlivesofdata.com/raft/
provider_name: Consensus
provider_slug: consensus
slug: raft
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: consensus:raft\nname: Raft\ndescription: Raft is a consensus algorithm designed for understandability, published by Ongaro and Ousterhout\n  in 2014. Raft separates leader election, log replication, and safety into distinct concepts and is implemented\n  widely in etcd, Consul, CockroachDB, TiKV, MongoDB, and many other production systems.\nhumanURL: https://raft.github.io/\nbaseURL: https://raft.github.io\ntags:\n- etcd\n- Leader Election\n- Log Replication\n- Raft\nproperties:\n- type: Specification\n  url: https://raft.github.io/raft.pdf\n- type: Documentation\n  url: https://raft.github.io/\n- type: Reference\n  url: https://thesecretlivesofdata.com/raft/\nx-features:\n- Strong leader simplifies log replication\n- Randomized election timeouts\n- Membership changes via joint consensus\n- Snapshotting for log compaction\nx-useCases:\n- etcd, Consul, CockroachDB, TiKV, MongoDB replica sets\n- Replicated key-value stores\n- Configuration management for orchestrators\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/consensus/refs/heads/main/apis.yml
tags:
- etcd
- Leader Election
- Log Replication
- Raft
---
