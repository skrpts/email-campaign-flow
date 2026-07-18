---
type: skill
id: email-campaign-composition
title: Email Campaign Composition
description: "Writing the email campaign copy variants that make up the deliverable, per audience segment and campaign objective"
tags: [Production, Campaign, Communication]
connections:
  - target: llm-service
    type: runs_on
metadata:
  estimated_duration: "5 minutes"
  avg_tokens: 3500
  trigger: manual
---

## Email Campaign Composition

This skill writes the actual email campaign copy — the deliverable the workflow exists to produce — turning the campaign brief, audience segments, and tested subject lines into ready-to-send email variants.

### Core Capability

Given the campaign brief, the audience segmentation, and the A/B-tested subject lines from upstream, this skill drafts targeted copy for each segment: subject-line variants, preview text, a mobile-optimised body with personalisation placeholders, a primary CTA, and a P.S. line — brand-aligned and GDPR-compliant throughout.

### Method

1. **Segment mapping:** Take each audience segment and its recommended approach, subject-line strategy, and CTA from the segmentation stage.
2. **Copy drafting:** For every segment, write the full email — subject-line variants for A/B testing, preview text, scannable body with personalisation placeholders, primary CTA, and a P.S. line.
3. **Compliance and readability:** Enforce brand voice, GDPR-compliant unsubscribe language, and mobile-first formatting (short paragraphs, scannable structure).

### Output Structure

One complete email per audience segment, each with its subject-line variants, preview text, body, CTA, and P.S. line. This is the campaign deliverable; the language-polish stage refines it into the final output.
