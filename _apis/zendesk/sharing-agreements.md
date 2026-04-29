---
aid: zendesk:sharing-agreements
baseURL: https://{subdomain}.zendesk.com
description: The Zendesk Sharing Agreements API lets you programmatically set up and manage ticketsharing relationships between separate Zendesk accounts so teams can collaborate on the same customer issues across instances. With it, you can create, list, update, and delete sharing agreements; send and respond to invitations; define rules and trust settings that control which tickets can be shared and what data is synchronized; and monitor or revoke agreements as needs change.
humanURL: https://developer.zendesk.com/api-reference/ticketing/tickets/sharing_agreements/
image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
layout: api
name: Zendesk Sharing Agreements API
properties:
- type: Documentation
  url: https://developer.zendesk.com/api-reference/ticketing/tickets/sharing_agreements/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/sharing-agreements-openapi-original.yml
provider_name: Zendesk
provider_slug: zendesk
slug: sharing-agreements
source_filename: sharing-agreements-openapi-original.yml
source_heading: OpenAPI Specification
source_yaml: "openapi: 3.1.0\ninfo:\n  title: Zendesk Sharing Agreements\n  description: Needs a description.\npaths:\n  /api/v2/sharing_agreements:\n    get:\n      operationId: ListSharingAgreements\n      tags:\n        - Sharing Agreements\n      summary: Zendesk Get  Api V2 Sharing_agreements\n      description: |\n        #### Allowed For\n\n        * Agents\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/SharingAgreementsResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/SharingAgreementsResponseExample'\n    post:\n      operationId: CreateSharingAgreement\n      tags:\n        - Sharing Agreements\n      summary: Zendesk Post  Api V2 Sharing_agreements\n      description: |\n        #### Allowed For\n\n        * Admins\n      responses:\n        '201':\n          description: Created\
  \ response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/SharingAgreementResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/SharingAgreementResponseExample'\n  /api/v2/sharing_agreements/{sharing_agreement_id}:\n    parameters:\n      - $ref: '#/components/parameters/SharingAgreementId'\n    get:\n      operationId: ShowSharingAgreement\n      tags:\n        - Sharing Agreements\n      summary: Zendesk Get  Api V2 Sharing_agreements Sharing_agreement_id\n      description: |\n        Returns a sharing agreement for your account.\n\n        #### Allowed For\n\n        * Agents\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/SharingAgreementResponse'\n              examples:\n                default:\n             \
  \     $ref: '#/components/examples/SharingAgreementResponseExample'\n    put:\n      operationId: UpdateSharingAgreement\n      tags:\n        - Sharing Agreements\n      summary: Zendesk Put  Api V2 Sharing_agreements Sharing_agreement_id\n      description: >\n        Returns an updated sharing agreement. Only `status` is allowed to be\n        updated.\n\n\n        #### Allowed For\n\n\n        * Admins\n      responses:\n        '200':\n          description: Success response\n          content:\n            application/json:\n              schema:\n                $ref: '#/components/schemas/SharingAgreementResponse'\n              examples:\n                default:\n                  $ref: '#/components/examples/SharingAgreementUpdateResponseExample'\n    delete:\n      operationId: DeleteSharingAgreement\n      tags:\n        - Sharing Agreements\n      summary: Zendesk Delete  Api V2 Sharing_agreements Sharing_agreement_id\n      description: |\n        Deletes a sharing agreement.\n\
  \n        #### Allowed For\n\n        * Admins\n      responses:\n        '204':\n          description: No Content response\ncomponents:\n  schemas:\n    SharingAgreementsResponse:\n      type: object\n      properties:\n        sharing_agreements:\n          type: array\n          items:\n            $ref: '#/components/schemas/SharingAgreementObject'\n    SharingAgreementResponse:\n      type: object\n      properties:\n        sharing_agreement:\n          $ref: '#/components/schemas/SharingAgreementObject'\ntags:\n  - name: Sharing Agreements\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zendesk/refs/heads/main/openapi/sharing-agreements-openapi-original.yml
tags:
- Sharing Agreements
---
