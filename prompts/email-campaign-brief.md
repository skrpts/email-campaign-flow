---
type: prompt
id: email-campaign-brief
title: "Email Campaign Brief"
description: "Collects email campaign details, audience, and goals"
tags: [Production]
inputs:
  campaign_brief:
    label: "Campaign Brief"
    description: "What this email campaign is about"
    example: "Nurture sequence for free trial users who haven't converted after 7 days"
    required: true
    type: text
  email_list:
    label: "Email List Description"
    description: "Who is on this list"
    example: "Free trial sign-ups from the last 30 days, mostly marketing managers"
    required: true
    type: text
  campaign_goal:
    label: "Campaign Goal"
    description: "What you want recipients to do"
    example: "Convert free trial to paid plan"
    required: true
    type: text
connections:
  - target: audience-segmentation
    type: derived_from
metadata:
  output_format: markdown
  prompt_type: task
---

You are an email marketing strategist. Segment the audience for this email campaign.

**Brief:** {{input.campaign_brief}}
**List:** {{input.email_list}}
**Goal:** {{input.campaign_goal}}

Segment into 3-4 groups with characteristics, email approach, subject line strategy, and CTA per segment.
