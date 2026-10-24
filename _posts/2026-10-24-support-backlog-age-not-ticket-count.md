---
layout: post
title: "Backlog Age: The Support Metric Your Ticket Count Hides"
subtitle: "Two teams can have the same number of open tickets and be in very different shape. Here is how to measure backlog age in your helpdesk, run a weekly review, and clear the tickets that are quietly costing you customers."
date: 2026-10-24
category: Support Operations
slug: support-backlog-age-not-ticket-count
cta_title: "Not sure what your Zendesk is hiding?"
cta_text: "Book a free 30-minute Zendesk review. We look at your SLAs, ticket flow and reporting together, and you leave with at least one thing worth fixing."
cta_url: "https://vijitlabs.com/services"
cta_button: "Book a free review"
---

Picture two support teams at the Monday stand-up. Both report 100 open tickets. Both managers nod and move on.

On the first team, almost every ticket arrived in the last three days. The work is fresh and flowing. On the second team, 30 of those tickets are more than two weeks old. A handful are past a month. Some of those customers have stopped chasing, which feels like good news but usually is not.

Same number. Very different week ahead.

That is the problem with ticket count as a health check. It tells you how much work is waiting. It says nothing about how long people have been waiting for it.

## Why ticket count hides the real risk

Ticket count is a snapshot, and snapshots are easy to read wrong. A team can close a lot of tickets every day and still have old ones sitting at the bottom of the queue, untouched.

This happens for ordinary reasons. Agents naturally pick the newest or the easiest tickets, because those can be solved quickly and feel productive. Hard tickets need a second team, a bug fix or a long reply, so they get skipped again and again. Each day the count looks stable, because new tickets come in and quick ones go out at roughly the same rate.

Meanwhile the oldest tickets get older. And old tickets are where the damage lives. They are the ones that turn into escalations, complaints to account managers and cancellation conversations.

Some helpdesk statuses make this harder to see. In Zendesk, a ticket set to Pending or On-hold is easy to leave out of the views agents work from each day, and some SLA targets pause while a ticket sits there. The ticket is still open. The customer is still waiting. It just stops looking urgent.

## The fix: measure age, not just volume

Backlog age is simply how long each unsolved ticket has been open, counted from the day the customer first asked. You do not need a new tool to track it. You need two habits.

**First, group unsolved tickets into age buckets.** Five buckets are enough for most teams:

| Age bucket | What it usually means | What to do |
|---|---|---|
| 0 to 2 days | Normal flow | Nothing special, work as usual |
| 3 to 7 days | Needs attention | Check each ticket has a clear next step |
| 8 to 14 days | At risk | Team lead reviews and assigns an owner by name |
| 15 to 30 days | Likely stuck | Escalate the blocker, update the customer |
| Over 30 days | Damage already happening | Manager reviews each one personally this week |

**Second, report the oldest ticket every week.** Not the average age. Averages hide the worst cases, because a pile of fresh tickets pulls the number down. The single oldest open ticket, with its age in days, is a number nobody can explain away.

Example: a team with 100 open tickets and an oldest ticket of 4 days is in a very different position from a team with 60 open tickets and an oldest ticket of 47 days. The second team looks better on count and is worse on risk.

## A weekly backlog age review you can start this week

This takes about 30 minutes once it is set up. Run it on the same day each week.

1. **Build an oldest-first list.** In Zendesk, create a shared view of all unsolved tickets (New, Open, Pending and On-hold) and sort it by the Requested date, oldest first. If you use another helpdesk, any list of unsolved tickets sorted by created date works.
2. **Count each bucket.** Note how many tickets fall into each of the five age buckets above. Write the numbers down in the same place every week so you can see the trend.
3. **Record the oldest ticket.** Write its ID, its age in days and the reason it is still open.
4. **Review everything over 14 days, one by one.** For each ticket ask three questions. Who owns it, by name? What is the next step? What is blocking it? If any answer is "not sure", that is the real problem.
5. **Clear oldest first.** Agree that each agent starts the day with their oldest ticket before taking new ones. Even one old ticket per agent per day changes the shape of the backlog within a couple of weeks.
6. **Check the trend, not the snapshot.** After four weeks, compare your bucket counts. You want the older buckets shrinking, even if the total count stays about the same.

If you want an early warning between reviews, Zendesk view conditions such as "Hours since created" let you build a separate view that only shows tickets older than a set limit. Put that view where team leads see it every day.

## Where this can go wrong

Backlog age is a useful number, and like any number, it can be gamed or misread. Three things to watch.

**Closing old tickets just to clear the list.** If you start reporting age, someone will be tempted to mark old tickets Solved without fixing anything. Watch your reopen rate alongside backlog age. If old tickets are getting solved and then reopened, the backlog has not shrunk, it has just been hidden.

**Treating every old ticket as a failure.** Some tickets are old for good reasons, such as a bug fix scheduled for next release or a customer who asked you to wait. These still belong on the list, but tag them so the review can separate "waiting by agreement" from "forgotten". The test is simple: does the customer know what is happening and when?

**Ignoring new tickets to chase old ones.** Clearing oldest first is a habit, not a rule that beats everything else. If you pull every agent onto old tickets, today's tickets become next week's old ones. A steady split, such as the first ticket of the day being the oldest one, usually works better than a big clean-up push.

There is also a reporting tradeoff. Counting age from the day the ticket was created includes time in Pending, which some teams feel is unfair, because the customer was the one who needed to reply. That is a fair point for measuring agents. It is the wrong lens for measuring customer experience. From the customer's side, the problem has been open the whole time. Use full age for the backlog review, and save the paused-clock view for agent performance if you need it.

## The takeaway

Ticket count tells you how busy you are. Backlog age tells you who is being let down. A team that only watches the first number will keep being surprised by escalations that "came out of nowhere", when they were sitting at the bottom of the queue for weeks.

**This week:** open an oldest-first list of every unsolved ticket, write down the age of the single oldest one, and bring that number to your next team meeting. Then ask who owns it. That one question will tell you more about your backlog than the total count ever has.

*I also share a short daily lesson on KPIs and processes on Instagram at [@vijitlabs](https://instagram.com/vijitlabs). Comment GUIDE on any reel for the free 2-page guide that goes with it.*
