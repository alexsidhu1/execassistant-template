---
name: weekly-review
description: Use when I ask for a weekly review, a Friday wrap, "where did the week go", or a summary of what moved this week. Pulls from calendar, tasks, and notes and produces a tight review plus next week's focus.
argument-hint: [optional week or date range]
---

## What This Skill Does

Produces a short, honest weekly review: what got done, what stalled, what needs a decision, and the two or three things that matter most next week. It is a thinking tool, not a status report for someone else. Keep it blunt.

This is an example skill. It shows the shape of a SKILL.md: when to trigger, what context to load, the steps, and the output format. Adapt it or delete it.

## Context To Load First

1. Read `.claude/rules/communication-style.md` so the review sounds like me.
2. Read `context/current-priorities.md` so "what matters next week" is measured against what I said actually matters.

## Steps

### Step 1: Gather the week
Pull the raw material for the week (or the range I gave):
- Calendar: what I actually spent time on.
- Tasks: what got closed, what's still open, what's overdue.
- Notes or decisions: anything logged in `decisions/log.md` this week.

If a source isn't connected, say so and work with what you have. Don't invent activity.

### Step 2: Find the signal
Don't list everything. Answer four questions:
- **What moved?** Real progress, not motion.
- **What stalled, and why?** Be specific about the blocker.
- **What needs me?** Decisions only I can make.
- **What did I spend time on that didn't matter?** The honest one.

### Step 3: Set next week
Name the two or three things that, if they happen, make next week a win. Tie them to current priorities. If this week revealed that priorities have shifted, say so and propose updating `context/current-priorities.md`.

## Output Format

Short. Four headed sections (Moved / Stalled / Needs me / Next week), bullets under each. Lead with the most important line. No filler, no pep talk.
