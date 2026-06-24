# Resources
 
A curated collection of everything worth reading, watching, and exploring on MCP. Organised by type — not dumped alphabetically.
 
> Last updated: June 2026 · Spec version covered: 2025-11-25 (stable) · 2026-07-28 RC available
 
---
 
## Start Here
 
If you're new to MCP, hit these three in order before anything else.
 
| Resource | What it is |
|---|---|
| [modelcontextprotocol.io](https://modelcontextprotocol.io) | Official documentation site — architecture, guides, tutorials |
| [MCP Specification](https://github.com/modelcontextprotocol/modelcontextprotocol) | The actual spec — what's normative, what's optional, what's experimental |
| [Anthropic's original MCP announcement](https://www.anthropic.com/news/model-context-protocol) | Why it was built, the design philosophy, the original vision |
 
---
 
## Official GitHub Organisation
 
Everything Anthropic and the Linux Foundation maintain officially.
 
| Repo | What it is |
|---|---|
| [modelcontextprotocol/modelcontextprotocol](https://github.com/modelcontextprotocol/modelcontextprotocol) | Specification and documentation source |
| [modelcontextprotocol/python-sdk](https://github.com/modelcontextprotocol/python-sdk) | Official Python SDK — use this to build servers and clients in Python |
| [modelcontextprotocol/typescript-sdk](https://github.com/modelcontextprotocol/typescript-sdk) | Official TypeScript SDK — most widely used SDK in the ecosystem |
| [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) | Reference server implementations — filesystem, git, fetch, memory, sequential thinking |
| [modelcontextprotocol/inspector](https://github.com/modelcontextprotocol/inspector) | MCP Inspector — visual tool for testing and debugging MCP servers |
 
> **Note on SDKs:** The Python SDK v1.x is current stable. v2 (alpha) targets stable release 2026-07-27. The TypeScript SDK v2 is targeting Q3 2026. Pin your versions accordingly.
 
---
 
## Official Registry
 
| Resource | What it is |
|---|---|
| [registry.modelcontextprotocol.io](https://registry.modelcontextprotocol.io) | Official MCP server registry — searchable, verified |
| [modelcontextprotocol.io/examples](https://modelcontextprotocol.io/examples) | Curated server examples from the official docs |
 
---
 
## Awesome Lists — Community Curated
 
The ecosystem moves fast. These lists track what's available across the community.
 
| List | Stars | What makes it useful |
|---|---|---|
| [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) | ⭐ 5.6K+ | The most referenced community list — broad coverage, frequently updated |
| [wong2/awesome-mcp-servers](https://github.com/wong2/awesome-mcp-servers) | ⭐ High | Comprehensive directory — organised by category (databases, dev tools, web, etc.) |
| [appcypher/awesome-mcp-servers](https://github.com/appcypher/awesome-mcp-servers) | ⭐ Active | Focused on production-ready and experimental servers |
| [tolkonepiu/best-of-mcp-servers](https://github.com/tolkonepiu/best-of-mcp-servers) | ⭐ Ranked | Ranked list — updated weekly by GitHub activity and downloads |
| [hireblackout/awesome-mcp-servers](https://github.com/hireblackout/awesome-mcp-servers) | ⭐ Practical | Ranked by GitHub downloads, Reddit consensus, and real-world usage patterns |
| [Rodert/awesome-mcp](https://github.com/Rodert/awesome-mcp) | ⭐ Active | Servers + broader MCP resources including clients and frameworks |
| [nborwankar/awesome-mcp-servers-2](https://github.com/nborwankar/awesome-mcp-servers-2) | ⭐ 2K+ servers | Comprehensive — covers 2K+ servers as of early 2025 |
 
---
 
## Notable Servers Worth Knowing
 
These are referenced constantly in the community — worth understanding what they do.
 
| Server | Transport | What it does |
|---|---|---|
| `@modelcontextprotocol/server-filesystem` | stdio | Secure local file read/write with configurable path restrictions |
| `@modelcontextprotocol/server-github` | stdio | Create issues, list PRs, read files from GitHub repos |
| `@modelcontextprotocol/server-fetch` | stdio | Web content fetching — converts HTML to LLM-friendly markdown |
| `@modelcontextprotocol/server-memory` | stdio | Knowledge graph-based persistent memory across sessions |
| `@modelcontextprotocol/server-sequential-thinking` | stdio | Dynamic, reflective problem-solving through structured thought sequences |
| `@modelcontextprotocol/server-git` | stdio | Read, search, and manipulate local Git repositories |
| Supabase MCP | remote SSE | Full Supabase integration — DB queries, auth, storage |
| Microsoft 365 MCP | remote SSE | Read calendar, send emails, access OneDrive — used in Claude.ai |
| Playwright MCP | stdio | Browser automation — scraping, interaction, screenshot capture |
 
---
 
## Frameworks for Building MCP Servers
 
If the raw SDK feels low-level, these abstractions make server development faster.
 
| Framework | Language | What it adds |
|---|---|---|
| [FastMCP](https://github.com/jlowin/fastmcp) | Python | High-level decorators — define a tool in 3 lines instead of 15. Most popular Python abstraction. |
| [FastMCP (TS)](https://github.com/punkpeye/fastmcp) | TypeScript | Same idea — minimal boilerplate for TypeScript servers |
| [langchain-mcp-adapters](https://github.com/langchain-ai/langchain-mcp-adapters) | Python | Translates MCP tool format to LangChain/LangGraph format. Use this to connect MCP servers to LangGraph agents. |
 
---
 
## Clients That Support MCP
 
MCP servers are only useful if something connects to them. These clients have native MCP support.
 
| Client | Type | Notes |
|---|---|---|
| [Claude Desktop](https://claude.ai/download) | Desktop app | First MCP client — configure servers in `claude_desktop_config.json` |
| [Claude.ai](https://claude.ai) | Web | MCP connectors available in settings (Microsoft 365, Superhuman, etc.) |
| [Cursor](https://cursor.com) | IDE | MCP support via `.cursor/mcp.json` config |
| [VS Code + GitHub Copilot](https://code.visualstudio.com) | IDE | MCP support via `.vscode/mcp.json` config |
| [Windsurf](https://windsurf.ai) | IDE | MCP support built in |
| [Zed](https://zed.dev) | IDE | MCP context providers |
| LangGraph | Framework | Via `langchain-mcp-adapters` |
| Anthropic Python SDK | SDK | Native MCP support — pass `mcp_servers` param directly |
 
---
 
## Key Blog Posts & Articles
 
| Post | Author | Why it matters |
|---|---|---|
| [MCP: One Year In (Nov 2025 spec release)](https://blog.modelcontextprotocol.io/posts/2025-11-25-first-mcp-anniversary/) | MCP Core Maintainers | Full retrospective + details on the 2025-11-25 spec — Tasks, OAuth 2.1, structured output |
| [2026-07-28 Release Candidate](https://blog.modelcontextprotocol.io/posts/2026-07-28-release-candidate/) | David Soria Parra | Largest revision since launch — stateless core, Extensions framework, MCP Apps, Tasks extension |
| [MCP Developer Guide 2026](https://lushbinary.com/blog/mcp-model-context-protocol-developer-guide-2026/) | Lushbinary | Comprehensive guide — architecture, both SDKs, security, Streamable HTTP vs SSE |
| [Anthropic: Building effective agents](https://www.anthropic.com/research/building-effective-agents) | Anthropic | Not MCP-specific but essential context — the agent patterns MCP plugs into |
 
---
 
## Spec Versions — Quick Reference
 
The spec has evolved fast. Know what version you're working with.
 
| Version | Released | Key additions |
|---|---|---|
| Initial release | Nov 2024 | Core protocol — tools, resources, prompts, stdio + SSE |
| 2025-03-26 | Mar 2025 | Streamable HTTP replaces SSE as recommended remote transport |
| 2025-06-18 | Jun 2025 | Structured output for tools |
| 2025-11-25 | Nov 2025 | OAuth 2.1, Tasks (experimental), MCP Registry launch, structured output stable |
| 2026-07-28 RC | May 2026 | Stateless core, Extensions framework, MCP Apps, formal deprecation policy |
 
> **Practical note:** SSE still works but is deprecated for new projects. Use Streamable HTTP for remote servers. For local servers, stdio is unchanged and still the default.
 
---
 
## Tooling
 
| Tool | What it does |
|---|---|
| [MCP Inspector](https://github.com/modelcontextprotocol/inspector) | Visual debugger for MCP servers — test tools, resources, prompts interactively before connecting to a client |
| [FastMCP CLI](https://github.com/jlowin/fastmcp) | `fastmcp dev` — runs a server with hot reload and connects to the Inspector automatically |
 
---
 
## Community
 
| Channel | What it's for |
|---|---|
| [MCP GitHub Discussions](https://github.com/modelcontextprotocol/modelcontextprotocol/discussions) | Official — spec questions, feature proposals, implementation help |
| [MCP Discord](https://discord.gg/anthropic) | Community — fastest place for implementation questions |
| [r/mcp](https://reddit.com/r/mcp) | Reddit — use cases, server recommendations, community projects |
| [PulseMCP](https://pulsemcp.com) | Community newsletter + server discovery — tracks new servers and ecosystem news |
 
---
 
## JSON-RPC 2.0 — The Wire Protocol
 
MCP runs on JSON-RPC 2.0. These are the authoritative references.
 
| Resource | What it is |
|---|---|
| [JSON-RPC 2.0 Specification](https://www.jsonrpc.org/specification) | The full spec — four message types, error codes, batch requests |
| [JSON-RPC vs REST comparison](https://www.smashingmagazine.com/2016/09/understanding-rest-and-rpc-for-http-apis/) | Clear explanation of why RPC and REST are fundamentally different design philosophies |
