# Getting Started: build your second brain

This guide takes you from nothing to a working AI executive assistant. No coding. If you can install an app and fill in a form, you can do this.

Set aside about 30 to 45 minutes. By the end you'll have an assistant that knows who you are, what you're working on, and how you write, and that gets sharper every time you use it.

Here's the whole thing in five steps:

1. Install Claude Code (the app this runs on)
2. Download this template
3. Open the template in Claude Code
4. Make it yours (the important part)
5. Use it

---

## Step 1: Install Claude Code

Claude Code is an app from Anthropic (the company behind Claude). It's Claude with the ability to read and write files on your computer. That's what lets it hold a "second brain" instead of forgetting everything when you close the chat.

**The easy way (recommended if you're non-technical):**

1. Go to **[claude.com/claude-code](https://claude.com/claude-code)**.
2. Download the desktop app for your computer (Mac or Windows).
3. Install it like any other app and open it.
4. Sign in with your Claude account. (You need a paid Claude plan, or an Anthropic API key. The sign-in screen will walk you through it.)

That's it. Skip to Step 2.

**The other way (if you're comfortable with a terminal):** Claude Code also runs in the terminal and inside code editors like VS Code. If those words mean nothing to you, ignore this and use the desktop app above. If they do, the terminal install is one command: `npm install -g @anthropic-ai/claude-code` (you'll need [Node.js](https://nodejs.org) first), then run `claude`.

---

## Step 2: Download this template

This template is the skeleton of a second brain: a set of folders and files Claude reads to understand you. You're going to grab a copy.

1. Go to the template page: **[github.com/alexsidhu1/execassistant-template](https://github.com/alexsidhu1/execassistant-template)**.
2. Click the green **Code** button near the top.
3. Click **Download ZIP**.
4. Find the downloaded ZIP file (usually in your Downloads folder) and double-click it to unzip.
5. You now have a folder called `execassistant-template`. Move it somewhere you'll remember, like your Desktop or Documents. You can rename it to anything you like (for example, `my-assistant`).

No GitHub account needed. You're just downloading a folder.

---

## Step 3: Open the template in Claude Code

1. Open Claude Code.
2. Open the folder you just unzipped. (In the desktop app, point it at the `execassistant-template` folder. There's an "open folder" or "open project" option when you start.)

Claude can now see all the files in that folder. When you start chatting, it automatically reads `CLAUDE.md` first, which tells it everything else to look at.

To check it's working, type:

> Read CLAUDE.md and the files in the context folder, then tell me in one sentence what you understand about me so far.

Right now it'll say something about placeholders, because you haven't filled anything in yet. That's the next step.

---

## Step 4: Make it yours

This is where the value comes from. The assistant is only as good as what it knows about you. Two ways to do this. Pick one.

### Option A: Let Claude interview you (easiest)

You don't have to edit files by hand. Claude can do it for you. Paste this in:

> I want to set up my second brain. Read CLAUDE.md and every file in the context folder. Then interview me one question at a time to fill them in with my real details. Ask about who I am, what my business does, my team, my current priorities, and my goals. After each answer, update the right file. Keep going until the context folder reflects my real life.

Then just answer its questions in plain language. It writes the files for you. This is the fastest way, and honestly the best, because it asks about things you might not think to include.

### Option B: Edit the files yourself

If you'd rather type directly, open these files (in Claude Code, or any text editor) and replace the `[bracketed placeholders]` with your real information. Start here, in order of importance:

1. **`context/me.md`** — who you are, your role, how you work.
2. **`context/work.md`** — what your business does, your offers, your clients.
3. **`context/team.md`** — who's on your team and what to loop them in for.
4. **`context/current-priorities.md`** — what matters in the next 30 days.
5. **`context/goals.md`** — your targets for the quarter.
6. **`CLAUDE.md`** — change `[Your Name]` and the top description so it's working for you.
7. **`.claude/rules/communication-style.md`** — set the tone and formatting rules so it sounds like you, not generic AI.

Be specific. "I run a business" is useless. "I run a 4-person marketing agency in Austin, most revenue from retainer clients, trying to land bigger accounts" is gold. The detail is the whole point.

### One rule that matters

Don't put anything in here you wouldn't want a stranger reading, unless you keep this folder private (it is private by default on your own computer). The folder lives on your machine. It only goes public if you choose to upload it somewhere public. For most people, it just sits on your computer and stays yours.

---

## Step 5: Use it

Now it's an assistant. Talk to it like one. Some things to try:

- "Draft an email to a client who went quiet, in my voice."
- "What are my top priorities this week, and what should I ignore?"
- "I'm thinking about hiring a salesperson. Talk it through with me using what you know about my business."
- "Summarize this messy note into three clear next steps." (paste the note)

**Tell it to remember things.** When you correct it or state a preference, say "remember that." For example: "Remember that I never want emojis in client emails." It saves that and applies it next time.

**Log decisions.** When you make a real call, say "log this decision." It writes it to `decisions/log.md` with the reasoning, so future-you knows why.

**Build skills as you go.** The first time you do a repeatable task (a weekly review, a follow-up email, a content draft), do it once. The second time, say "turn this into a skill so we do it the same way every time." Now it's a reusable recipe. There's one example skill in `.claude/skills/weekly-review` to show you the shape.

---

## What "gets smarter over time" actually means

Nothing about this is automatic magic. It compounds because of you. Every time you correct it, add context, log a decision, or save a skill, the next conversation starts from a higher floor. After a few months it knows your business the way a good employee would, except it never forgets and it's there at midnight.

The hardest step is the first one: filling in the context honestly. Do that, and the rest takes care of itself.

---

## Stuck?

If something isn't working, ask Claude Code directly. It can see your files and your setup, so "I followed the getting started guide and X isn't working, help me debug it" usually sorts it out. That's the nice thing about an assistant that lives inside the tool: it can help you fix the tool.

Built by Alex Sidhu (Whitehorse AI). More at [alexsidhu.com](https://alexsidhu.com).
