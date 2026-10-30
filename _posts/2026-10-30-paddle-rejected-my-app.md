---
layout: post
title: "Paddle Rejected My App. They Were Right."
subtitle: "Why I removed agent scoring from CallLensAI, and what support teams should measure instead: the call, not the person."
date: 2026-10-30
category: Building in Public
slug: paddle-rejected-my-app
cta_title: "Try CallLensAI on one call"
cta_text: "Upload one recorded support call and see the knowledge base gaps, call reasons and product feedback it finds. Then tell me which output you would actually use."
cta_url: "https://calllens.vijit.in"
cta_button: "Try CallLensAI"
---

Last week, Paddle turned down CallLensAI for checkout.

The reason was one line from their Acceptable Use Policy. They do not support "AI systems which make, or materially influence, decisions about a natural person."

My first reaction was irritation. CallLensAI analyses customer support calls. It is not a hiring tool. It does not approve loans. Then I reread my own feature list, slowly, the way a reviewer would. And I saw what they saw.

## The feature I was proudest of

One of CallLensAI's headline features was agent scoring. You uploaded a call, and the app rated how well the support agent handled it.

It felt like the obvious thing to build. I spent 22 years in IT service delivery and support. Call quality reviews were part of my working life for most of that time. Every support manager I have worked with wanted a faster way to know who needs coaching. So I built a number that answered that question.

Here is the problem I had not thought through. A score about a person is a decision about a person. The moment a manager uses that number in an appraisal, a warning or a termination, the AI has materially influenced a decision about a human being. That is exactly the line Paddle drew.

## Why they were right

Payment policy was only the trigger. The deeper reasons hold even if no payment provider ever asked.

**One call is a bad sample.** An agent can handle a furious customer with real skill and still score poorly, because the call ran long or the customer never calmed down. A single number hides all of that context.

**Scores change behaviour in the wrong direction.** When people know they are being scored, they work for the score. Calls get shorter. Empathy turns into a scripted line. The metric improves while the customer experience does not.

**The risk lands on the buyer.** The EU AI Act already places AI used to evaluate worker performance in its high-risk category. A careful CX leader will think twice before putting an AI-generated agent score in front of HR. I was building a feature that my best customers would be most nervous to use.

## What I built instead

I removed agent scoring completely. In its place, CallLensAI now looks at the call, not the person. Four features replaced it:

- **Knowledge base gap finder.** It flags questions the agent could not answer from documentation. Those gaps are usually a content problem, not a people problem, and they are cheap to fix.
- **Follow-up email draft.** It drafts the summary email the agent would otherwise write by hand after the call. That time goes back to the next customer.
- **Call reasons and trends.** It groups why customers are calling. If one reason suddenly grows, you see it before it becomes a backlog.
- **Product feedback extractor.** It pulls out what customers say about the product itself. That feedback usually dies in call recordings nobody replays.

I resubmitted the domain on 24 October. Paddle approved it the next day.

## The honest part

CallLensAI has no active users yet. So this is not a success story. It is a correction I made before a design mistake could hurt anyone.

I would rather learn this from a policy reviewer than from a support agent who lost a bonus because of a number my software produced.

## What to take from this

If you are building AI for support teams, ask one question about every output: **who is this a decision about?**

If the answer is a customer's problem, a product gap or a process, you are probably on solid ground. If the answer is a named employee, slow down. Look for a version that measures the work instead of the worker. In my case, that version turned out to be more useful anyway.

If you run a support team, try one recorded call through [CallLensAI](https://calllens.vijit.in). Then tell me which of the four outputs you would actually use on a Monday morning. That answer decides what I build next.
