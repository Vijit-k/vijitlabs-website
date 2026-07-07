---
layout: post
title: "EscalationAI Is Now Live on the Zendesk Marketplace"
subtitle: "After multiple review cycles and a complete rebuild, EscalationAI is publicly listed. Here is what it does and why it exists."
date: 2026-07-07
category: Customer Support
slug: escalationai-live-zendesk-marketplace
cta_title: "Install EscalationAI"
cta_text: "Available now on the Zendesk Marketplace. Free 7-day trial, no credit card required. Setup takes under 30 minutes."
cta_url: "https://www.zendesk.com/marketplace/apps/support/1260706/escalationai/"
cta_button: "View on Zendesk Marketplace"
---

EscalationAI is now publicly listed on the Zendesk Marketplace.

That sentence took longer to write than expected. Not because the product was hard to build, but because the Zendesk review process is thorough, and getting through it as a solo founder while managing everything else takes time.

This post covers what EscalationAI does, why it exists, and what the journey to get here actually looked like.

## The Problem It Solves

If you manage a support team on Zendesk, you know this situation. An agent opens a ticket. It looks routine. But somewhere in the conversation history, the customer mentioned legal action. Or asked for a manager. Or has contacted you six times about the same unresolved issue.

The signals are there. But agents are processing volume. They are not reading every ticket looking for early warning signs.

By the time the escalation happens, you are already in damage control mode. The customer is angry, a supervisor is involved, and the window for a low-cost resolution has closed.

EscalationAI is built to catch those tickets before they escalate, not after.

## What It Actually Does

EscalationAI runs as a native sidebar app inside Zendesk. The moment an agent opens a ticket, the app analyses the content and conversation history against 25 escalation signals. Within two seconds it returns a risk score from 0 to 100, the specific signals that triggered it, and a recommended action.

The score appears directly in the ticket view. Not in a separate dashboard. Not in a weekly report. Right where the agent is already working.

High-risk tickets are automatically tagged in Zendesk so supervisors can monitor them in a dedicated queue. Optional Slack alerts notify the team immediately when a RED risk ticket is detected.

Every score is explainable. Agents see exactly which signals drove the result, not just a number. This matters for two reasons. First, agents can act on it without guessing. Second, every AI decision has an audit trail, which matters increasingly as companies face scrutiny over how AI is used in customer operations.

## Why ISO 42001 Alignment Matters

EscalationAI is built to align with ISO/IEC 42001:2023, the international standard for AI management systems.

In practice this means every AI decision is logged, every score is explainable, and human agents remain in control at every point. The app assists judgment. It does not replace it.

Most AI tools in the Zendesk ecosystem do not address governance at all. They produce outputs and you trust them or you do not. EscalationAI is designed for support teams that operate under compliance requirements or have leadership that wants accountability over AI-assisted decisions.

## The Journey to Get Here

The first submission was rejected. Three blockers: missing domain whitelist, description over the character limit, and secure settings implemented incorrectly.

The second submission required a complete rebuild of the authentication layer. Zendesk apps must retrieve the installation context via the ZAF SDK, pass it to the backend, and resolve the API key server-side. A shared authentication library was built from scratch, a new endpoint was added to handle installation resolution, and a setup page was created to manage the configuration flow.

The third submission introduced a new blocker: an XSS vulnerability in signal rendering where `innerHTML` was being used to display backend data. Fixed by replacing it with DOM API using `textContent`.

Each rejection came with specific, actionable feedback from the Zendesk review team. The product that passed review is more secure and better architected than the one first submitted. The process worked as intended.

## What Comes Next

EscalationAI is live and available for any Zendesk customer to install directly from the marketplace. A free 7-day trial is available with no credit card required.

The product is actively developed. The next version includes stronger ticket handling, improved signal detection, and performance improvements under review.

If you manage a support team on Zendesk and escalations are a recurring cost, install it, run it for a week, and see what it surfaces. The link is below.
