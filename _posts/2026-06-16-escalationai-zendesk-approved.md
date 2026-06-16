---
layout: post
title: "EscalationAI Just Cleared Zendesk Marketplace Review. Here Is What It Took."
subtitle: "Three submissions, two rejections, and one complete authentication rebuild later, EscalationAI is now in closed preview on the Zendesk Marketplace."
date: 2026-06-16
category: Customer Support
slug: escalationai-zendesk-approved
cta_title: "Get Early Access to EscalationAI"
cta_text: "EscalationAI is in closed preview on the Zendesk Marketplace. Request early access and get it installed in your Zendesk account before the public listing opens."
cta_url: "https://escalationai.vijit.in"
cta_button: "Request Early Access"
---

As of today, EscalationAI has cleared the Zendesk Marketplace review process and is now in closed preview. That means it has been reviewed, approved, and is being made available to early access users before the full public listing opens.

Getting here was not straightforward. This post covers what the journey actually looked like, because most product announcements skip the part where things did not work.

## What EscalationAI Does

EscalationAI is a Zendesk app that scores every support ticket for escalation risk in real time. It reads the ticket content and conversation history, evaluates it across more than 25 signals, and returns a risk score directly inside the Zendesk ticket view.

The signals include things like legal language in the customer's message, repeated contacts on the same issue, sentiment deterioration across the conversation, manager requests, churn indicators, and response time gaps. The score is accompanied by the specific signals that drove it, so agents know exactly why a ticket was flagged, not just that it was.

The goal is simple. Catch the tickets that are about to escalate before they do, while there is still time to intervene.

## The Zendesk Marketplace Review Process

Zendesk takes its marketplace seriously. Every app goes through a manual review that checks the code quality, security implementation, API handling, data privacy compliance, and adherence to Zendesk's developer standards.

For EscalationAI, it took three submissions to get through.

The first submission (v1.0) was rejected with three specific blockers. The domain whitelist implementation was missing. The short description exceeded the 80-character limit. And the secure settings implementation did not follow Zendesk's required pattern.

Each blocker was legitimate. None of them were vague. Zendesk's reviewer was specific about what needed to change and why.

The second submission (v1.1) fixed all three blockers. This required a complete rebuild of the authentication layer. The correct pattern for Zendesk apps requires the frontend to retrieve the installation context via the ZAF SDK, send it to the backend, and resolve the API key from there. A shared authentication library was built, a new endpoint was added to handle installation resolution, and a setup page was created to manage the configuration flow.

v1.1 passed review and is now in closed preview.

## What ISO 42001 Alignment Means in Practice

EscalationAI was built to align with ISO/IEC 42001:2023, the international standard for AI management systems. This was a deliberate design decision, not an afterthought.

In practice it means:

Every AI decision is logged. Every risk score has an audit trail. The signals that drove the score are always surfaced to the agent, not hidden inside a black box. Human agents remain in control at every point. The app assists judgment, it does not replace it.

For support teams operating under compliance requirements or with leadership that wants accountability over AI-assisted decisions, this matters. Most AI tools in the Zendesk ecosystem do not address governance at all.

## What Closed Preview Means

Closed preview is the stage between passing review and being publicly listed in the Zendesk Marketplace. The app has been approved. It is installable. But it is not yet discoverable by the general Zendesk user base.

During closed preview, specific Zendesk accounts can be invited to install the app. This is the right stage to gather early installs, get real usage feedback, and collect the first reviews that will accompany the public listing.

If you manage a Zendesk support team and want to be an early access user, this is the time to reach out. Early access users get direct input into what gets built next, and access before the public listing opens.

## What Comes Next

The next step is moving from closed preview to public listing. That requires gathering installs and reviews during the preview period.

A newer version of the app (v1.5.0) is also in the submission queue with five additional fixes including stronger ticket save handling, description length caps, and improved CORS safety for API calls. That version will go through the standard review process and will be submitted as an update once the public listing is live.

If you are running a support team on Zendesk and escalations are a recurring problem, EscalationAI is worth a look. Early access is open. Setup takes under 30 minutes.
