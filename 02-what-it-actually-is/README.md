# 02 · What It Actually Is
 
> MCP is not a library or a framework. It is a protocol, a specification for how two processes communicate.
 
---
 
## The One-Line Definition
 
MCP (Model Context Protocol) is an open standard that defines how AI host applications connect to external tools and data sources through a uniform interface, using JSON-RPC 2.0 as its message format.
 
---
 
## The Big Picture
 
```
┌─────────────────────────────────────────────────────┐
│                     HOST                            │
│   (your app / Claude.ai / VS Code)                  │
│                                                     │
│   ┌────────────┐       ┌────────────┐               │
│   │  Client A  │       │  Client B  │               │
│   │ one per    │       │ one per    │               │
│   │ server     │       │ server     │               │
│   └─────┬──────┘       └─────┬──────┘               │
└─────────┼─────────────────────┼─────────────────────┘
          │ JSON-RPC 2.0        │ JSON-RPC 2.0
          │ over stdio          │ over SSE
          ▼                     ▼
   ┌─────────────┐       ┌─────────────┐
   │  Server A   │       │  Server B   │
   │  (GitHub)   │       │  (Postgres) │
   └─────────────┘       └─────────────┘
```
 
Three layers. Each with a single responsibility.
 
---
 
## Topics Covered in This Section
 
> *Full content coming — subtopics will be added here*
 
Planned coverage includes:
 
- JSON-RPC 2.0 — the wire protocol
- REST vs JSON-RPC — why MCP chose RPC
- The three-layer architecture — Host, Client, Server
- The data layer — Tools, Resources, Prompts
- Transport types — stdio and SSE
- The MCP session lifecycle — initialize, discover, call, respond
- Capabilities negotiation
- Error handling and error codes
---
 
*Previous: [01 · Why Is It Needed](../01-why-is-it-needed/README.md)*  
*Next: [03 · How Is It Implemented](../03-how-is-it-implemented/README.md)*
