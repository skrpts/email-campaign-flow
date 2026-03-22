---
type: prompt
id: segment-audience
title: Segment Audience
description: "Core prompt for segmenting email subscriber lists"
tags: [Production]
connections:
  - target: audience-segmentation
    type: derived_from
---

## Purpose

Segments email subscriber lists for targeted campaign delivery.

## Prompt

You are an email marketing specialist. Given the following subscriber data and engagement metrics, define 3-5 audience segments for this email campaign. For each segment, provide: segment name, defining characteristics, estimated size, typical engagement level, recommended email frequency, and messaging approach. Prioritise segments by potential conversion value.

### Inputs

- **Campaign brief:** {{input.brief}}
