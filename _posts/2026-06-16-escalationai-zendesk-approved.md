---
layout: post
title: "EscalationAI Has Been Approved by Zendesk. Public Listing Is Coming."
subtitle: "After multiple submissions and a complete authentication rebuild, EscalationAI has cleared Zendesk Marketplace review. Early access is open now."
date: 2026-06-16
category: Customer Support
slug: escalationai-zendesk-approved
cta_title: "Get Early Access to EscalationAI"
cta_text: "EscalationAI is approved by Zendesk and heading to public listing. Request early access and get it installed in your Zendesk account before the public listing opens."
cta_url: "https://escalationai.vijit.in"
cta_button: "Request Early Access"
---

EscalationAI has cleared the Zendesk Marketplace review process. The public listing is on its way. Early access is open right now for support teams who want in before it goes live.

Getting here was not straightforward. This post covers what the journey actually looked like, because most product announcements skip the part where things did not work.

## What EscalationAI Does

EscalationAI is a Zendesk app that scores every support ticket for escalation risk in real time. It reads the ticket content and conversation history, evaluates it across more than 25 signals, and returns a risk score directly inside the Zendesk ticket view.

The signals include things like legal language in the customer's message, repeated contacts on the same issue, sentiment deterioration across the conversation, manager requests, churn indicators, and response time gaps. The score is accompanied by the specific signals that drove it, so agents know exactly why a ticket was flagged, not just that it was.

The goal is simple. Catch the tickets that are about to escalate before they do, while there is still time to intervene.

## The Zendesk Marketplace Review Process

Zendesk takes its marketplace seriously. Every app goes through a manual review that checks code quality, security implementation, API handling, data privacy compliance, and adherence to Zendesk's developer standards.

For EscalationAI, it took multiple submissions to get through.

The first submission was rejected with three specific blockers. The domain whitelist implementation was missing. The short description exceeded the character limit. And the secure settings implementation did not follow Zendesk's required pattern.

Each blocker was legitimate. None of them were vague. Zendesk's reviewer was specific about what needed to change and why.

The fixes required a complete rebuild of the authentication layer. The correct pattern for Zendesk apps requires the frontend to retrieve the installation context via the ZAF SDK, send it to the backend, and resolve the API key from there. A shared authentication library was built, a new endpoint was added to handle installation resolution, and a setup page was created to manage the configuration flow.

That submission passed review. EscalationAI is now approved by Zendesk and the public listing is being processed.

## What ISO 42001 Alignment Means in Practice

EscalationAI was built to align with ISO/IEC 42001:2023, the international standard for AI management systems. This was a deliberate design decision, not an afterthought.

In practice it means:

Every AI decision is logged. Every risk score has an audit trail. The signals that drove the score are always surfaced to the agent, not hidden inside a black box. Human agents remain in control at every point. The app assists judgment, it does not replace it.

For support teams operating under compliance requirements or with leadership that wants accountability over AI-assisted decisions, this matters. Most AI tools in the Zendesk ecosystem do not address governance at all.

## What Early Access Means

The public listing on the Zendesk Marketplace is being processed and will go live shortly. This is a manual process handled by the Zendesk Partner team.

In the meantime, early access is open. If you manage a Zendesk support team and want EscalationAI installed before the public listing opens, reach out directly through the product page. Setup takes under 30 minutes and does not require changes to your existing Zendesk configuration.

Early access users get direct input into what gets built next and access before the general Zendesk user base.

## What Comes Next

Once the public listing is live on the Zendesk Marketplace, EscalationAI will be discoverable by any Zendesk customer searching for escalation management tools. The app will continue to be actively developed with improvements informed by real usage feedback.

If you are running a support team on Zendesk and escalations are a recurring problem, now is the right time to get in. Early access is open and the public listing is coming shortly.
