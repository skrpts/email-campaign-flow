---
type: workflow
id: email-campaign-flow
title: Email Campaign Flow
description: "Audience segmentation, copy, A/B test plan, and send schedule"
tags: [Production, Tested]
connections:
  - target: audience-segmentation
    type: uses
  - target: a-b-test-analysis
    type: uses
  - target: segment-audience
    type: uses
  - target: analyse-a-b-test
    type: uses
  - target: email-campaign-writer
    type: uses
---

## Overview

This workflow produces a complete email campaign from audience segmentation through to A/B test plan and optimised send schedule.

## Pipeline Stages

### Stage 1: Audience Segmentation

Invoke the **audience-segmentation** skill to define target segments for the email campaign based on subscriber data and behaviour.

### Stage 2: Email Copy Creation

Invoke the **email-campaign-writer** prompt to produce email copy variants for each audience segment.

### Stage 3: A/B Test Design

Invoke the **a-b-test-analysis** skill to design A/B test parameters for subject lines, copy, and send times.

### Stage 4: Results Analysis

Invoke the **analyse-a-b-test** prompt to interpret test results and recommend the winning variant for full deployment.

## Output

Complete email campaign package containing:

- Audience segment definitions
- Email copy variants per segment
- A/B test plan with hypothesis and success criteria
- Send schedule with optimised timing
