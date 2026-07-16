---
type: prompt
id: email-campaign-writer
title: Email Campaign Writer
description: "Task prompt for generating email campaign copy"
tags: [Customer-Facing, Campaign, Communication]
inputs:
  brief:
    label: "Brief"
    description: "The full assignment or project brief including requirements, constraints, and expected deliverables"
    example: "Write a 2000-word analysis of competitive pricing strategies in the SaaS market"
    required: true
    type: text
connections:
  - target: audience-segmentation
    type: derived_from
---

## Purpose

Produces email copy variants tailored to audience segments and campaign objectives.

## Prompt

Write email campaign copy for the following audience segment and campaign objective. Include: 3 subject line variants for A/B testing, preview text, email body with personalization placeholders, primary CTA, and a P.S. line. Ensure the copy adheres to brand voice guidelines, is GDPR-compliant with unsubscribe language, and is optimized for mobile reading (short paragraphs, scannable format).

### Inputs

- **Audience segments:** {{steps.previous.output}}
- **Campaign brief:** {{input.brief}}

Use the audience segments and campaign brief above to write targeted copy for each segment.
