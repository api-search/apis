---
aid: communication-protocols:server-sent-events
baseURL: https://html.spec.whatwg.org
description: A simple, one-way, server-to-client streaming protocol defined as part of the HTML living standard. SSE runs over plain HTTP, supports automatic reconnection, and is widely used for live status feeds and LLM token streaming.
humanURL: https://html.spec.whatwg.org/multipage/server-sent-events.html
image: ''
layout: api
name: Server-Sent Events (SSE)
properties:
- type: Specification
  url: https://html.spec.whatwg.org/multipage/server-sent-events.html
- type: Documentation
  url: https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events
provider_name: Communication Protocols
provider_slug: communication-protocols
slug: server-sent-events
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: communication-protocols:server-sent-events\nname: Server-Sent Events (SSE)\ndescription: A simple, one-way, server-to-client streaming protocol defined as part of the HTML living\n  standard. SSE runs over plain HTTP, supports automatic reconnection, and is widely used for live status\n  feeds and LLM token streaming.\nhumanURL: https://html.spec.whatwg.org/multipage/server-sent-events.html\nbaseURL: https://html.spec.whatwg.org\ntags:\n- HTML\n- HTTP\n- Real-Time\n- Streaming\nproperties:\n- type: Specification\n  url: https://html.spec.whatwg.org/multipage/server-sent-events.html\n- type: Documentation\n  url: https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events\nx-features:\n- Plain HTTP text/event-stream responses\n- Automatic browser reconnection with Last-Event-ID\n- Simpler than WebSocket for one-way fan-out\nx-useCases:\n- LLM token streaming\n- Live status and activity feeds\n- Server-pushed dashboards\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/communication-protocols/refs/heads/main/apis.yml
tags:
- HTML
- HTTP
- Real-Time
- Streaming
---
