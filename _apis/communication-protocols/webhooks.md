---
aid: communication-protocols:webhooks
baseURL: https://webhooks.fyi
description: An HTTP-based pattern for delivering event notifications from one service to another by performing an outbound HTTP POST to a URL registered by the consumer. Webhooks are not a single specification but the broader pattern is increasingly governed by efforts such as the CloudEvents specification and the IETF Webhook security drafts.
humanURL: https://webhooks.fyi/
image: ''
layout: api
name: Webhooks
properties:
- type: Reference
  url: https://webhooks.fyi/
- type: Specification
  url: https://cloudevents.io/
- type: Documentation
  url: https://www.standardwebhooks.com/
provider_name: Communication Protocols
provider_slug: communication-protocols
slug: webhooks
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: communication-protocols:webhooks\nname: Webhooks\ndescription: An HTTP-based pattern for delivering event notifications from one service to another by performing\n  an outbound HTTP POST to a URL registered by the consumer. Webhooks are not a single specification but\n  the broader pattern is increasingly governed by efforts such as the CloudEvents specification and the\n  IETF Webhook security drafts.\nhumanURL: https://webhooks.fyi/\nbaseURL: https://webhooks.fyi\ntags:\n- Async\n- Events\n- HTTP\n- Push\nproperties:\n- type: Reference\n  url: https://webhooks.fyi/\n- type: Specification\n  url: https://cloudevents.io/\n- type: Documentation\n  url: https://www.standardwebhooks.com/\nx-features:\n- Outbound HTTP POST event delivery\n- Pluggable signing schemes (HMAC, JWT) for verification\n- Replay protection with timestamps and nonces\n- Aligns with CloudEvents and Standard Webhooks\nx-useCases:\n- Asynchronous event delivery between SaaS platforms\n- Build, deploy,\
  \ and CI pipeline notifications\n- Payment and billing event hooks\n- Third-party integrations without polling\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/communication-protocols/refs/heads/main/apis.yml
tags:
- Async
- Events
- HTTP
- Push
---
