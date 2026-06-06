---
layout: post
title: "What Zendesk's Marketplace Review Actually Teaches You About Building Secure Apps"
date: 2026-06-06
author: Vijitkumar Kunhikandi
categories: [product, escalationai, zendesk]
excerpt: "EscalationAI's first submission was rejected. Three blockers, one non-trivial fix. Here is what the review process exposed about secure app architecture — and why getting rejected was useful."
---

EscalationAI's first Zendesk Marketplace submission came back with three blockers yesterday. Not a full rejection. Just: fix these, resubmit, and we will approve.

It took about six hours to fix everything properly. Not because the changes were hard, but because one of the three blockers was pointing at something more structural — the way secure settings were being handled in the frontend.

Here is what happened, what was wrong, and what I changed.

## The Three Blockers

**1. Missing domainWhitelist in manifest.json**

When a Zendesk app uses secure parameters, you must declare which external domains the app calls. I had `api_key` marked as `secure: true` but no `domainWhitelist` defined. The fix is one line:

```json
"domainWhitelist": ["escalationai.vijit.in"]
```

Simple. But it forces you to think about something important: every domain your app touches needs to be declared. If you are calling multiple services, all of them go here. It is a useful audit of your own app's surface area.

**2. short_description over 80 characters**

The submitted file had 93 characters. Limit is 80. The version I thought I had submitted had 55. Turns out the file on disk was different from what I had been working on locally. The fix was trimming and resubmitting the correct file.

Lesson: always verify the exact file you are packaging, not the one open in your editor.

**3. Secure settings not coded correctly in index.html**

This was the real one.

## Why the Secure Settings Fix Matters

The original code was fetching the API key on the frontend using `client.metadata()`:

```javascript
const meta = await client.metadata();
const apiKey = meta.settings.api_key;
```

Zendesk's reviewer flagged this as incorrect. And they were right.

Here is why: when a parameter has `secure: true` in manifest.json, Zendesk intentionally prevents the frontend from reading it. The whole point of marking something secure is that it never touches the browser. If your frontend is trying to read a secure setting, you have designed the auth flow backwards.

The correct pattern is: the frontend does not handle credentials at all. Instead, it sends an `installationId` to your backend. Your backend resolves the actual API key from there.

In practice, this meant:

```javascript
// Frontend: send installationId, not the key itself
const context = await client.context();
const installationId = context.installationId;

fetch('https://escalation-ai-backend.vercel.app/api/score', {
  headers: {
    'X-Installation-Id': installationId
  }
});
```

The backend then looks up which API key maps to that `installationId` in Redis. The key never leaves the server.

This required a new Redis mapping (`installation:{id}` to `api_key`) and a new endpoint (`/api/resolve-installation`) that customers call once during setup to create that mapping.

It also required a setup page at `escalationai.vijit.in/setup` so customers can link their Zendesk installation to their API key without it ever passing through the browser during normal use.

## What the Review Process Actually Does

The Zendesk Marketplace review is not just a checkbox exercise. The three blockers they caught were all legitimate architectural concerns:

- The domainWhitelist forces you to think about your app's external dependencies
- The character limit forces you to write a concise description that actually communicates the product value
- The secure settings flag exposed a real flaw in the auth design

Getting flagged on the third one was useful. The app is more secure now than it was before submission.

## What Is Live Now

EscalationAI v1.1 is submitted and under review. Changes in this version:

- `domainWhitelist` added to manifest
- `short_description` corrected to 78 characters
- Frontend now uses `client.context()` installationId pattern
- Backend has shared auth library (`lib-auth.js`) that resolves installationId to api_key via Redis
- New `/api/resolve-installation` endpoint for one-time setup linking
- Setup page live at escalationai.vijit.in/setup

The ISO 42001 compliance features — audit trail, explainable AI, human override logging, bias monitoring — are all unchanged. The auth fix did not touch any of that.

If you are building a Zendesk Marketplace app, the documentation on secure settings is worth reading before you write a single line of frontend code. The constraint shapes the architecture in a good direction.

---

EscalationAI is a Zendesk sidebar app that scores every ticket for escalation risk in real time. Free 7-day trial at [escalationai.vijit.in](https://escalationai.vijit.in).
