# 03 · How Is It Implemented
 
> Theory lands when you build something. This section is hands-on.
 
---
 
## What You Will Build
 
By the end of this section you will have:
 
- A working MCP server exposing custom tools
- A LangGraph agent connected to it via `langchain-mcp-adapters`
- The same agent connected via the Anthropic SDK's native MCP support
- An understanding of when to use local (stdio) vs remote (SSE) deployment
---
 
## Prerequisites
 
Before this section, make sure you have covered:
 
- [01 · Why Is It Needed](../01-why-is-it-needed/README.md) — understanding the problem
- [02 · What It Actually Is](../02-what-it-actually-is/README.md) — understanding the protocol
And have installed:
 
```bash
pip install anthropic langchain-mcp-adapters langgraph
npm install -g @modelcontextprotocol/server-github   # example server
```
 
---
 
## Topics Covered in This Section
 
> *Full content coming — subtopics will be added here*
 
Planned coverage includes:
 
- Building your first MCP server in Python
- Exposing tools, resources, and prompts from a server
- Connecting to a server with `langchain-mcp-adapters`
- Using the Anthropic SDK's native MCP support
- Local servers — stdio transport
- Remote servers — SSE transport
- Connecting multiple servers to one agent
- MCP adapters — what they are and when you need them
- Production patterns — versioning, error handling, auth
- Integrating MCP servers into a LangGraph StateGraph
---
 
*Previous: [02 · What It Actually Is](../02-what-it-actually-is/README.md)*
