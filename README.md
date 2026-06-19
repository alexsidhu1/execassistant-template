# Executive Assistant / Second Brain (Claude Code template)

This is a template for turning [Claude Code](https://claude.com/claude-code) into a real executive assistant and second brain: a project that knows who you are, what you're working on, how you write, and gets sharper every time you use it.

It's the scaffolding from my own setup, stripped of anything personal and rebuilt as something you can clone and make your own. Everything here is placeholder content. Drop your own life into it.

## The idea

Most people use AI as a vending machine: ask a question, get an answer, the context dies when the chat closes. A second brain is different. You give the AI a persistent home for everything it should know about you, and it stops starting from zero every time.

Four things make that work:

1. **Context** it can always read (who you are, what the business is, who's on the team, what matters right now).
2. **Skills** for the workflows you repeat (so a good output becomes a repeatable recipe, not a lucky prompt).
3. **Agents** that specialize (one for email, one for calendar, one for research) with the main assistant routing between them.
4. **Memory and a decision log** so it learns your preferences and remembers why you decided things, without you re-explaining.

## How it's laid out

| Path | What it holds |
|---|---|
| `CLAUDE.md` | The orchestrator. The first thing Claude reads. Defines who it's working for, the rules, and how the rest of the project fits together. |
| `context/` | The facts about you: who you are, the business, the team, current priorities, goals. Update these as life changes. |
| `.claude/rules/` | Hard rules that apply to everything Claude writes (tone, formatting, words to never use). |
| `.claude/skills/` | Repeatable workflows. Each skill is a folder with a `SKILL.md` saying when to use it and how. |
| `.claude/agents/` | Specialist subagents. The main assistant delegates to these instead of doing everything itself. |
| `decisions/` | An append-only log of meaningful decisions and the reasoning behind them. |
| `projects/` | One folder per active workstream, each with a README that captures status and context. |
| `templates/` | Reusable scaffolds (e.g. an end-of-session summary). |
| `references/` | Standard operating procedures and example outputs. |

## New to this? Start here

If you're not technical, read **[GETTING-STARTED.md](GETTING-STARTED.md)**. It walks you from zero (installing the app) to a working assistant in about 30 minutes, no coding required.

## Make it yours

1. **Clone it** (or download the ZIP) and open the folder in Claude Code.
2. **Rewrite `context/`** with your real details. This is where most of the value comes from. Be specific. Vague context produces vague assistance.
3. **Edit `CLAUDE.md`** so the assistant is working for you, not the placeholder persona.
4. **Set the rules** in `.claude/rules/communication-style.md` to match how you actually write.
5. **Delete the example skill, agents, and project** and build your own as real workflows emerge. Don't build skills in advance. Build them the second time you do the same thing twice.
6. **Connect MCP servers** for the tools you live in (Gmail, Calendar, Slack, a CRM, etc.). The example agents show how to scope an agent to a specific set of tools.

## Requirements

- [Claude Code](https://claude.com/claude-code)
- Optional but recommended: MCP servers for the tools you want the assistant to touch. The agents in `.claude/agents/` reference specific MCP tools as an example; swap them for yours.

## Who made this

Built by Alex Sidhu, co-founder of Whitehorse AI. I write a weekly newsletter on AI, building, and the occasional bigger idea.

- Newsletter and writing: https://alexsidhu.com
- Whitehorse AI: https://whitehorseai.ai

If you build something with this, I'd like to see it.
