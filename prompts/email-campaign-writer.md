---
type: prompt
id: email-campaign-writer
title: Email Campaign Writer
description: "Task prompt for generating email campaign copy"
tags: [Customer-Facing, Campaign, Communication]
context_params:
  campaign_brief:
    label: "Campaign Brief"
    description: "The segmented campaign brief — audience segments with their approach, subject-line strategy, and CTA."
    required: false
  subject_lines:
    label: "Subject Lines"
    description: "The A/B-tested subject-line variants from the headline stage."
    required: false
    default_from_previous: true
connections:
  - target: audience-segmentation
    type: derived_from
  - target: headline-writing
    type: derived_from
---

## Purpose

Produces email copy variants tailored to audience segments and campaign objectives. This is the campaign deliverable — the emails themselves.

## Prompt

Write email campaign copy for the following audience segments and campaign objective. For each segment include: 3 subject line variants for A/B testing, preview text, email body with personalization placeholders, primary CTA, and a P.S. line. Ensure the copy adheres to brand voice guidelines, is GDPR-compliant with unsubscribe language, and is optimized for mobile reading (short paragraphs, scannable format).

### Inputs

- **Audience segments (campaign brief):** {{step.context.campaign_brief}}
- **Tested subject lines:** {{step.context.subject_lines}}

Use the segmented campaign brief and tested subject lines above to write targeted copy for each segment.
