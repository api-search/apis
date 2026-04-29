---
aid: codeproject:codeproject-ai-server
baseURL: http://localhost:32168
description: Self-hosted AI service that exposes computer vision (object detection, scene, face, ALPR), image processing (background removal, cartoonise, portrait filter, super-resolution), audio classification, NLP (sentiment, summarization), and YOLOv5 training endpoints through a local HTTP REST API. All endpoints are POST and accept multipart uploads. The server runs on Windows, macOS, Linux, Raspberry Pi, Jetson, and OrangePi, plus Docker images, and integrates with Blue Iris, Home Assistant, and Agent DVR for surveillance use cases.
humanURL: https://www.codeproject.com/AI/
image: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: CodeProject.AI Server API
properties:
- name: CodeProject.AI Server Home
  type: Portal
  url: https://www.codeproject.com/AI/
- name: Documentation
  type: Documentation
  url: https://codeproject.github.io/codeproject.ai/
- name: API Reference
  type: APIReference
  url: https://codeproject.github.io/codeproject.ai/api/api_reference.html
- name: GitHub Repository
  type: SourceCode
  url: https://github.com/codeproject/CodeProject.AI-Server
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/codeproject/refs/heads/main/openapi/codeproject-ai-server-openapi.yml
provider_name: CodeProject
provider_slug: codeproject
slug: codeproject-ai-server
source_yaml: "aid: codeproject:codeproject-ai-server\nname: CodeProject.AI Server API\ntags:\n- AI\n- Audio\n- Computer Vision\n- Face Recognition\n- Image Processing\n- License Plate Recognition\n- Object Detection\n- On-Premise\n- Self-Hosted\n- Text\n- Training\ntype: REST\nimage: https://kinlane-productions.s3.amazonaws.com/apis-json/apis-json-logo.jpg\nbaseURL: http://localhost:32168\nhumanURL: https://www.codeproject.com/AI/\ndescription: Self-hosted AI service that exposes computer vision (object detection, scene, face, ALPR),\n  image processing (background removal, cartoonise, portrait filter, super-resolution), audio classification,\n  NLP (sentiment, summarization), and YOLOv5 training endpoints through a local HTTP REST API. All endpoints\n  are POST and accept multipart uploads. The server runs on Windows, macOS, Linux, Raspberry Pi, Jetson,\n  and OrangePi, plus Docker images, and integrates with Blue Iris, Home Assistant, and Agent DVR for surveillance\n  use cases.\nproperties:\n\
  - url: https://www.codeproject.com/AI/\n  name: CodeProject.AI Server Home\n  type: Portal\n- url: https://codeproject.github.io/codeproject.ai/\n  name: Documentation\n  type: Documentation\n- url: https://codeproject.github.io/codeproject.ai/api/api_reference.html\n  name: API Reference\n  type: APIReference\n- url: https://github.com/codeproject/CodeProject.AI-Server\n  name: GitHub Repository\n  type: SourceCode\n- url: openapi/codeproject-ai-server-openapi.yml\n  type: OpenAPI\nx-features:\n- Local-only HTTP REST API (no internet dependency)\n- YOLO-based object detection (80+ classes)\n- Custom YOLOv5 model loading and training\n- Face detection, registration, recognition, and matching\n- Automatic License Plate Recognition (ALPR)\n- Image background removal, cartoonise, portrait, super-resolution\n- Sound classification and NLP (sentiment, summarization)\n- Modular installer-based feature set\n- Cross-platform (Windows, macOS, Linux, Pi, Jetson, OrangePi, Docker)\nx-use-cases:\n\
  - On-premise CCTV/NVR object and person detection\n- License plate capture for parking and security\n- Privacy-preserving face recognition for home automation\n- Edge AI on Raspberry Pi and Jetson devices\n- Local image moderation and content classification\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/codeproject/refs/heads/main/apis.yml
tags:
- AI
- Audio
- Computer Vision
- Face Recognition
- Image Processing
- License Plate Recognition
- Object Detection
- On-Premise
- Self-Hosted
- Text
- Training
---
