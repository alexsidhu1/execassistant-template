# Agents

Specialist subagents. The main assistant is the orchestrator: it routes work to the right specialist and never does their job itself.

Each agent is a markdown file with frontmatter (`name`, `description`, and a `tools` list scoping exactly which tools it can use) followed by its instructions. Scoping tools per agent keeps each one focused and safe (an email agent can't touch your calendar, a research agent can't send anything).

The files here (`email-agent`, `calendar-agent`, `research`) are examples. The tool names in them are MCP tools from one specific setup. Swap them for the MCP servers you connect.
