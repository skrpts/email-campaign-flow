---
type: asset
id: email-template-html
title: Email Template HTML
description: "Base HTML template for email campaigns"
tags: [Production, Campaign, Communication]
connections: []
---

## Email Template Structure

### Header
- Logo (max width: 200px)
- Navigation links (optional, max 3)

### Hero Section
- Hero image (600px wide, 200-300px tall)
- Headline: {{headline}}
- Subheadline: {{subheadline}}

### Body Content
- Introduction paragraph: {{intro}}
- Key benefits (bullet points or icon grid)
- Supporting content: {{body}}

### Call-to-Action
- Primary CTA button: {{cta_text}}
- CTA link: {{cta_url}}
- Button style: Brand colour, min 44px tap target

### Footer
- Company address (GDPR/CAN-SPAM requirement)
- Unsubscribe link
- Privacy policy link
- Social media icons

### Template Variables

| Variable | Description | Example |
|----------|------------|---------|
| {{first_name}} | Subscriber first name | "Sarah" |
| {{company}} | Subscriber company | "Acme Ltd" |
| {{headline}} | Email headline | "Introducing..." |
| {{cta_text}} | Button text | "Get Started" |
| {{cta_url}} | Button destination | "https://..." |
