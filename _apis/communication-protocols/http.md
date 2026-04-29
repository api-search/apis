---
aid: communication-protocols:http
baseURL: https://httpwg.org
description: The application layer protocol that powers the World Wide Web and the majority of REST and HTTP APIs. HTTP/1.1 is defined in RFC 9110-9114, HTTP/2 in RFC 9113, and HTTP/3 in RFC 9114, the latter running over QUIC. HTTP defines methods, status codes, headers, content negotiation, caching, and conditional requests that underpin modern web APIs.
humanURL: https://httpwg.org/specs/
image: ''
layout: api
name: Hypertext Transfer Protocol (HTTP)
properties:
- type: Specification
  url: https://www.rfc-editor.org/rfc/rfc9110
- type: Specification
  url: https://www.rfc-editor.org/rfc/rfc9112
- type: Specification
  url: https://www.rfc-editor.org/rfc/rfc9113
- type: Specification
  url: https://www.rfc-editor.org/rfc/rfc9114
- type: Working Group
  url: https://datatracker.ietf.org/wg/httpbis/about/
provider_name: Communication Protocols
provider_slug: communication-protocols
slug: http
source_filename: apis.yml
source_heading: API entry from apis.yml
source_yaml: "aid: communication-protocols:http\nname: Hypertext Transfer Protocol (HTTP)\ndescription: The application layer protocol that powers the World Wide Web and the majority of REST and\n  HTTP APIs. HTTP/1.1 is defined in RFC 9110-9114, HTTP/2 in RFC 9113, and HTTP/3 in RFC 9114, the latter\n  running over QUIC. HTTP defines methods, status codes, headers, content negotiation, caching, and conditional\n  requests that underpin modern web APIs.\nhumanURL: https://httpwg.org/specs/\nbaseURL: https://httpwg.org\ntags:\n- Application Protocol\n- HTTP\n- IETF\n- REST\n- Web\nproperties:\n- type: Specification\n  url: https://www.rfc-editor.org/rfc/rfc9110\n- type: Specification\n  url: https://www.rfc-editor.org/rfc/rfc9112\n- type: Specification\n  url: https://www.rfc-editor.org/rfc/rfc9113\n- type: Specification\n  url: https://www.rfc-editor.org/rfc/rfc9114\n- type: Working Group\n  url: https://datatracker.ietf.org/wg/httpbis/about/\nx-features:\n- Stateless request/response model\n\
  - Methods, status codes, headers, content negotiation\n- HTTP/2 multiplexing and HPACK header compression\n- HTTP/3 over QUIC for low-latency, head-of-line-free transport\n- Strong caching semantics with conditional requests\nx-useCases:\n- REST and resource-oriented APIs\n- GraphQL and gRPC-Web transport\n- Webhook delivery\n- Browser-to-API communication\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/communication-protocols/refs/heads/main/apis.yml
tags:
- Application Protocol
- HTTP
- IETF
- REST
- Web
---
