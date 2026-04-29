---
aid: consensus:paxos
baseURL: https://lamport.azurewebsites.net
description: Paxos is the classical crash-fault-tolerant consensus algorithm introduced by Leslie Lamport in 1989. Paxos and its derivatives (Multi-Paxos, Cheap Paxos, Vertical Paxos, EPaxos, Flexible Paxos) are foundational to distributed systems theory and are used in Google Chubby, Spanner, Megastore, and others.
humanURL: https://lamport.azurewebsites.net/pubs/paxos-simple.pdf
image: ''
layout: api
name: Paxos
properties:
- type: Specification
  url: https://lamport.azurewebsites.net/pubs/paxos-simple.pdf
- type: Reference
  url: https://www.cs.utexas.edu/users/lorenzo/corsi/cs380d/papers/paper2-1.pdf
- type: Reference
  url: https://en.wikipedia.org/wiki/Paxos_(computer_science)
provider_name: Consensus
provider_slug: consensus
slug: paxos
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: consensus:paxos\nname: Paxos\ndescription: Paxos is the classical crash-fault-tolerant consensus algorithm introduced by Leslie Lamport\n  in 1989. Paxos and its derivatives (Multi-Paxos, Cheap Paxos, Vertical Paxos, EPaxos, Flexible Paxos)\n  are foundational to distributed systems theory and are used in Google Chubby, Spanner, Megastore, and\n  others.\nhumanURL: https://lamport.azurewebsites.net/pubs/paxos-simple.pdf\nbaseURL: https://lamport.azurewebsites.net\ntags:\n- Lamport\n- Paxos\n- Replication\nproperties:\n- type: Specification\n  url: https://lamport.azurewebsites.net/pubs/paxos-simple.pdf\n- type: Reference\n  url: https://www.cs.utexas.edu/users/lorenzo/corsi/cs380d/papers/paper2-1.pdf\n- type: Reference\n  url: https://en.wikipedia.org/wiki/Paxos_(computer_science)\nx-features:\n- Tolerates up to f crash failures with 2f+1 acceptors\n- Phases prepare, promise, accept, accepted\n- Multi-Paxos pipelines decisions for log replication\n- Underlies Google Chubby\
  \ and Spanner\nx-useCases:\n- Replicated state machines\n- Distributed configuration services (Chubby, ZooKeeper-like)\n- Globally consistent databases\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/consensus/refs/heads/main/apis.yml
tags:
- Lamport
- Paxos
- Replication
---
