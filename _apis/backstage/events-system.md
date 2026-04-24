---
aid: backstage:events-system
baseURL: ''
description: The Backstage Events system provides a publish-subscribe mechanism for broadcasting and consuming events within a Backstage instance. It enables plugins to emit events when significant actions occur (such as catalog entity changes, scaffolder task completions, or permission policy updates) and allows other plugins or external systems to subscribe to those events via HTTP webhooks or the internal event bus.
humanURL: https://backstage.io/docs/plugins/backends-and-plugins/
image: ''
layout: api
name: Backstage Events System
properties:
- type: Documentation
  url: https://backstage.io/docs/plugins/backends-and-plugins/
- type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/asyncapi/backstage-events-asyncapi.yml
provider_name: Backstage
provider_slug: backstage
slug: events-system
tags:
- Developer Portal
- Events
- Webhooks
---
