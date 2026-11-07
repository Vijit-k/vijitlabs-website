---
layout: post
title: "Why Average Resolution Time Hides Your Slowest Tickets"
subtitle: "An average can look healthy while a slice of customers waits for days. Here is how to report three simple numbers instead, the median, the 90th percentile and the oldest case, and set targets that protect the customers who are most likely to leave."
date: 2026-11-07
category: Support Operations
slug: average-resolution-time-median-90th-percentile
cta_title: "Not sure what your Zendesk is hiding?"
cta_text: "Book a free 30-minute Zendesk review. We look at your SLAs, ticket flow and reporting together, and you leave with at least one thing worth fixing."
cta_url: "https://vijitlabs.com/services"
cta_button: "Book a free review"
---

The weekly ops review is going well. Average resolution time is 9 hours, comfortably inside the 12-hour goal. Someone suggests tightening the goal next quarter.

Then an account manager forwards an email. A customer has been waiting five days for an answer on a billing problem, and they are asking about cancellation terms. The ticket is real. It is also inside that "9 hour average".

Nobody on the team was hiding anything. The average was simply doing what averages do: blending the fast tickets and the slow ones into one tidy number, and making the slow ones disappear.

## Why the average misleads support teams

Support data is lopsided. Most tickets are quick: a password reset, a how-to question, a simple refund. A smaller group takes much longer because they need another team, a bug fix, or several rounds of back and forth.

When the data looks like that, a few very slow tickets pull the average up, and a large number of quick tickets pull it back down. The result is a number that describes almost nobody. It is too slow for the typical customer and far too fast for the ones who are actually struggling.

There is a second problem. Averages can stay flat while the experience changes underneath. If the quick tickets get a little quicker and the slow tickets get a lot slower, the average may not move at all. Your dashboard says "stable". Your most frustrated customers say otherwise.

The customers in that slow group are usually the ones you can least afford to lose. They had a real problem, it took a long time, and they have had plenty of time to think about alternatives.

## The fix: report three numbers instead of one

Replace the single average with three numbers that each answer a different question.

1. **The median (the typical customer).** Sort every resolution time from fastest to slowest and take the one in the middle. Half your customers waited less than this, half waited more. Unlike the average, a handful of extreme tickets cannot drag it around.
2. **The 90th percentile (the slow end).** This is the time that 90% of tickets were resolved within. The remaining 10% took longer. It tells you how bad things get for the customers on the wrong side of your process.
3. **The maximum or oldest open ticket (the worst case).** One number, with a ticket number next to it, so someone can go and look at it today.

Here is why this matters. Two weeks of resolution times can share an average and still be very different weeks.

| Example | Week A | Week B |
|---|---|---|
| Average resolution time | 9 hours | 9 hours |
| Median (typical customer) | 7 hours | 3 hours |
| 90th percentile (slow 10%) | 15 hours | 28 hours |
| Slowest ticket | 1.5 days | 5 days |

On the average alone, these weeks look identical. With three numbers, Week B is clearly the riskier week: most customers got faster answers, but the slow group waited almost twice as long, and one customer waited five days. That is the week the cancellation email comes from.

## How to run a three-number check this week

You do not need a new tool for this. A weekly export and a spreadsheet are enough to start.

1. **Pick one time metric.** Start with the one leadership watches most, usually first reply time or full resolution time. Do one metric well before adding more.
2. **Pull last week's solved tickets.** In Zendesk, you can build an Explore report on the Tickets dataset with ticket ID, group and the resolution time metric, filtered to tickets solved last week. Explore offers median as well as average when you choose how a metric is aggregated, so you can switch the existing report and compare the two side by side.
3. **Export to a spreadsheet for the slow end.** Put the resolution times in one column, then use three formulas: `=MEDIAN(range)`, `=PERCENTILE(range, 0.9)` and `=MAX(range)`. Filter for the maximum and copy its ticket ID into your report.
4. **Split by group or channel.** Run the same three numbers for each major queue. A healthy overall median often hides one queue, such as billing or tier 2, that owns most of the slow tickets.
5. **Set the target on the slow end.** Keep a median goal if you like, but make the main goal about the 90th percentile. Example: "90% of tickets resolved within 24 hours." That target forces the team to deal with the slow tickets instead of speeding up the easy ones.
6. **Read the slowest five tickets.** Every week, someone opens the five slowest tickets and writes one line on why each was slow. Waiting on engineering, wrong group, missing information from the customer. After a few weeks, the pattern tells you what to fix.
7. **Track the three numbers as a trend.** Put them in a small weekly table. You are looking for the gap between the median and the 90th percentile. If the gap is growing, the slow group is drifting away from everyone else, even if the average looks fine.

Your Zendesk SLA policies already think this way, by the way. An SLA achievement rate counts how many tickets met the target, which is much closer to a percentile view than an average. If your SLA report and your average resolution time tell different stories, trust the SLA report and investigate.

## Where this can go wrong

**Small numbers are noisy.** If a queue only solves 30 tickets a week, the 90th percentile is decided by three tickets. One unusual case can swing it a lot. For small queues, look at a rolling four weeks instead of a single week, and always read the actual tickets before drawing conclusions.

**Pending and on-hold time can distort the picture.** Some resolution time metrics include time spent waiting on the customer. A ticket that sat for three days because the customer went quiet is not the same problem as one your team ignored. Check which version of the metric you are using and say so in the report. Zendesk Explore offers both calendar-hours and business-hours versions of several time metrics, and the choice matters.

**Targets on the slow end can be gamed.** If the only goal is the 90th percentile, a team may close slow tickets early or split them into new tickets to reset the clock. Watch your reopen rate alongside it. If the 90th percentile improves and reopens rise, the problem has moved, not gone.

**Three numbers take more explaining.** Leadership is used to one number. Expect a couple of review meetings where you walk through why the median and the 90th percentile tell different stories. A simple before-and-after table, like the one above, usually does the job faster than any definition.

The honest tradeoff is this: an average is easier to report and easier to hit. Three numbers are a little more work and they will sometimes show a problem you would rather not see. That is exactly why they are worth it.

## The takeaway

An average tells you what happened to a customer who does not exist. The median shows your typical customer, the 90th percentile shows the ones who are struggling, and the slowest ticket gives you a name and a number to act on today.

**This week:** take last week's solved tickets, calculate the median, the 90th percentile and the maximum for resolution time, and compare them with the average you already report. Then open the five slowest tickets and write one line on why each one took so long. That list is your next process fix.

*I also share a short daily lesson on KPIs and processes on Instagram at [@vijitlabs](https://instagram.com/vijitlabs). Comment GUIDE on any reel for the free 2-page guide that goes with it.*
