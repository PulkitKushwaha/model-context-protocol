# 01 · Why Is It Needed?
 
> Before understanding what MCP is, you need to understand the problem it was built to solve.
 
---
 
## The Problem
 
Every time a developer wanted to give an AI agent access to a new tool, like a database, a file system, Slack, GitHub, an internal API, they had to write custom integration code inside the agent itself.
 
This meant:
 
- **Auth logic** duplicated across every agent that needed the same service
- **Tool definitions** rewritten from scratch for each new agent
- **Tight coupling** between agent code and tool implementation — change the tool, touch every agent
- **No reusability** — an integration built for Agent A could not be used by Agent B without copy-paste
The deeper problem was architectural: tool integration code tangled two concerns that have nothing to do with each other.
 
```
Before MCP — two concerns tangled together inside the agent:
 
┌─────────────────────────────────────────────────┐
│                  Your Agent                     │
│                                                 │
│  CONCERN 1: When and why to use a tool          │
│  (reasoning, decision-making — agent's job)     │
│                                                 │
│  CONCERN 2: How to connect to the tool          │
│  (auth, API format, error handling — not        │
│   the agent's job, but it lived here anyway)    │
└─────────────────────────────────────────────────┘
```
 
The agent's job is to reason about *when* to use a tool. It should not need to know *how* the tool's API works, how to authenticate with it, or what its response format is. But without a standard, it had no choice.
 
---
 
## What This Led To
 
**Maintenance burden.** When an external API changed its format, every agent that used it needed updating — not just the integration code.
 
**No ecosystem.** There was no way to share integrations across teams or organisations. Every team rebuilt the same GitHub, Slack, and database connectors independently.
 
**Security complexity.** Auth tokens and credentials lived inside agent code or config, tightly coupled to agent logic rather than owned by a dedicated, auditable layer.
 
**Framework lock-in.** An integration written for LangChain couldn't be used in a raw Anthropic SDK agent, even though both agents were doing the same job.
 
---
 
## The Analogy That Makes It Click
 
Before USB-C, every device needed its own proprietary cable. A standard interface fixed this — not by changing what devices do, but by standardising *how they connect*.
 
MCP does the same thing for AI tools:
 
```
Before MCP:                     After MCP:
 
Agent ──custom──► GitHub        Agent ──MCP──► GitHub MCP server
Agent ──custom──► Slack         Agent ──MCP──► Slack MCP server
Agent ──custom──► Postgres      Agent ──MCP──► Postgres MCP server
 
Integration code lives           Integration code lives in
inside the agent.                the server. One per service.
No sharing. No reuse.            Any agent can connect.
```
 
---
 
## What MCP Separates
 
MCP draws a clean line between the two concerns:
 
| Concern | Owned by | Before MCP |
|---|---|---|
| When and why to use a tool | Agent (LLM) | Inside agent code |
| How to connect to the tool | MCP Server | Also inside agent code |
 
After MCP, the agent only thinks about reasoning. The server owns the integration. They communicate through a standard protocol neither side wrote.
 
---
 
## Topics Covered in This Section
 
> *Full content coming — subtopics will be added here*
 
---
 
*Next: [02 · What It Actually Is](../02-what-it-actually-is/README.md)*
