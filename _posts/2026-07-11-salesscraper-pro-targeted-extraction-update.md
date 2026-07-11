---
layout: post
title: "The Best Feature in This Update Wasn't My Idea"
subtitle: "Someone watched SalesScraper Pro pull an entire connections list during a demo and asked why it couldn't just work off a filtered search instead. That question is the whole update."
date: 2026-07-11
category: Sales Tools
slug: salesscraper-pro-targeted-extraction-update
cta_title: "Try SalesScraper Pro"
cta_text: "Install the Chrome extension and run Extract Contact Info against a filtered LinkedIn search instead of your full list. You'll feel the difference in the first run."
cta_url: "https://sspro.vijit.in"
cta_button: "Get SalesScraper Pro"
---

Until this update, Extract Contact Info did one thing: it worked through your entire LinkedIn connections list, start to finish. Say you had 3,000 connections and, for example, only wanted phone and email for the sixty who work as operations managers in Berlin — you were still processing all 3,000. There was no way to say "just these people."

I knew this was a limitation. I hadn't gotten around to fixing it, mostly because the obvious fix — build a filtering UI inside the extension, let people type in job titles and locations — felt like a bigger project than I had time for.

Then I ran a live demo yesterday, and someone in the room asked the question directly: why does this have to run against everyone? One of my ex colleagues watched the tool work through a full connections list in real time and pointed out the obvious gap. Not as a formal feature request. Just an observation, mid-demo, about something that was clearly inefficient to watch.

That question turned out to have a much simpler answer than I'd assumed. LinkedIn's own People Search already has the filtering built in: location, current company, industry, school, connection degree, all combinable in one search. I didn't need to build a filtering system. I needed the extension to trust a search someone had already filtered, instead of ignoring it and always defaulting to the full list.

So that's what shipped. Extract Contact Info now works two ways: your full Connections page, same as before, or a LinkedIn People Search you've filtered down yourself, scoped to first-degree connections only, which is the group LinkedIn actually shares phone and email for. Build the search you want on LinkedIn, then point the extension at it.

Alongside that, I also cleaned up a smaller but real problem: a couple of non-person rows had been sneaking into exported CSVs, entries for a location filter chip and a placeholder for a profile whose name LinkedIn hides. Not a security issue, just noise that shouldn't have been there. It's gone now.

None of this came from a roadmap I wrote alone. Twelve days ago, a first-degree connection tested the tool against his own network and found a bug I'd have taken much longer to catch on my own. This time, it was a demo attendee asking one plain question about something happening on screen in front of him. Both of those only happen because the product is out in front of real people instead of sitting in a private beta I control end to end.

If you're already using SalesScraper Pro, try running Extract Contact Info against a filtered search the next time you only need a specific group, instead of your whole list. If you're not using it yet, this is a reasonable time to start.
