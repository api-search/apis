---
aid: amazon-billing-and-cost-management:aws-cost-explorer-api
baseURL: https://ce.us-east-1.amazonaws.com
description: The AWS Cost Explorer API provides programmatic access to cost and usage data. Query aggregated or granular cost data, filter and group by service, account, tag, or region, and retrieve cost forecasts and rightsizing recommendations.
humanURL: https://docs.aws.amazon.com/cost-management/latest/userguide/ce-api.html
image: ''
layout: api
name: AWS Cost Explorer API
properties:
- type: Documentation
  url: https://docs.aws.amazon.com/cost-management/latest/userguide/ce-api.html
- type: APIReference
  url: https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/
- type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-billing-and-cost-management/refs/heads/main/openapi/aws-cost-explorer-api-openapi.yml
- type: SpectralRuleset
  url: https://raw.githubusercontent.com/api-evangelist/amazon-billing-and-cost-management/refs/heads/main/spectral/ruleset.yml
- type: Capabilities
  url: https://raw.githubusercontent.com/api-evangelist/amazon-billing-and-cost-management/refs/heads/main/capabilities/capabilities.yml
- type: Vocabulary
  url: https://raw.githubusercontent.com/api-evangelist/amazon-billing-and-cost-management/refs/heads/main/vocabulary/vocabulary.yml
provider_name: Amazon Billing And Cost Management
provider_slug: amazon-billing-and-cost-management
slug: aws-cost-explorer-api
source_yaml: "aid: amazon-billing-and-cost-management:aws-cost-explorer-api\nname: AWS Cost Explorer API\ndescription: The AWS Cost Explorer API provides programmatic access to cost and usage data. Query aggregated\n  or granular cost data, filter and group by service, account, tag, or region, and retrieve cost forecasts\n  and rightsizing recommendations.\nhumanURL: https://docs.aws.amazon.com/cost-management/latest/userguide/ce-api.html\nbaseURL: https://ce.us-east-1.amazonaws.com\ntags:\n- Cost Explorer\n- Cost Analysis\n- Forecasting\n- Cost Optimization\nproperties:\n- type: Documentation\n  url: https://docs.aws.amazon.com/cost-management/latest/userguide/ce-api.html\n- type: APIReference\n  url: https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/\n- type: OpenAPI\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-billing-and-cost-management/refs/heads/main/openapi/aws-cost-explorer-api-openapi.yml\n- type: SpectralRuleset\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-billing-and-cost-management/refs/heads/main/spectral/ruleset.yml\n\
  - type: Capabilities\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-billing-and-cost-management/refs/heads/main/capabilities/capabilities.yml\n- type: Vocabulary\n  url: https://raw.githubusercontent.com/api-evangelist/amazon-billing-and-cost-management/refs/heads/main/vocabulary/vocabulary.yml\ncontact:\n- FN: AWS Support\n  url: https://aws.amazon.com/contact-us/\nfeatures:\n- name: Cost and Usage Queries\n  description: Query cost and usage data with filtering by service, account, tag, region, and time range\n    at daily or monthly granularity.\n- name: Cost Forecasting\n  description: Generate cost forecasts for future time periods based on historical spending patterns.\n- name: Cost Anomaly Detection\n  description: ML-powered detection of unusual spending patterns with configurable alerts and root cause\n    analysis.\n- name: Rightsizing Recommendations\n  description: Identify EC2 instance rightsizing opportunities to reduce costs without impacting performance.\n\
  - name: Savings Plans Recommendations\n  description: Get recommendations for Savings Plans purchases to reduce compute costs based on usage\n    patterns.\n- name: Reservation Recommendations\n  description: Receive recommendations for Reserved Instance purchases across EC2, RDS, Redshift, and\n    other services.\nuseCases:\n- name: FinOps Cost Analysis\n  description: Build custom dashboards and reports querying cost and usage data by team, project, service,\n    or environment using cost allocation tags.\n- name: Budget Tracking Automation\n  description: Automate budget monitoring with programmatic budget creation, alert configuration, and\n    cost anomaly subscriptions.\n- name: Chargeback and Showback\n  description: Allocate and distribute AWS costs to internal teams and business units using cost categories\n    and split charge rules.\nintegrations:\n- name: AWS Organizations\n  description: Consolidated billing and multi-account cost analysis\n- name: Amazon QuickSight\n  description:\
  \ Visualize cost and usage data with QuickSight dashboards\n- name: Amazon SNS\n  description: Receive budget and anomaly alert notifications via SNS\n- name: AWS Lambda\n  description: Trigger automated cost remediation workflows from budget actions\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-billing-and-cost-management/refs/heads/main/apis.yml
tags:
- Cost Explorer
- Cost Analysis
- Forecasting
- Cost Optimization
---
