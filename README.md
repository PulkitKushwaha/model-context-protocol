# MCP Deep Dive
 
A structured, in-depth study of the **Model Context Protocol (MCP)**: the open standard by Anthropic that defines how AI agents connect to tools, data, and services.
 
This repository is organised as a learning path, not a reference dump. Each section builds on the last.
 
---
 
## Structure
 
```
mcp-deep-dive/
├── 01-why-is-it-needed/        ← The problem MCP solves
├── 02-what-it-actually-is/     ← The protocol, architecture, and data layer
└── 03-how-is-it-implemented/   ← Building, connecting, and deploying
```
 
---
 
## The Three Sections
 
### 01 · Why Is It Needed?
The problem that existed before MCP was the fragmented, per-agent tool integrations, tangled concerns, no reusability of tools, resources and prompts. Why the industry needed a standard and what it was designed to replace.
 
### 02 · What It Actually Is
The full protocol: JSON-RPC 2.0, the three-layer architecture (Host · Client · Server), the data layer (Tools · Resources · Prompts), transport types, and the MCP session lifecycle.
 
### 03 · How Is It Implemented
Hands-on: building MCP servers, connecting them to LangGraph agents via adapters, the Anthropic SDK's native MCP support, local vs remote deployment, and production patterns.
 
---
 
## Prerequisites
 
A working knowledge of:
- LLM APIs (tool/function calling)
- Basic Python
- The agent loop concept (perceive → plan → act → observe)
No prior MCP knowledge required.
 
---
 
## Why This Exists
 
Most MCP content either stays at the surface ("it's like a USB-C for AI tools") or jumps straight to code without explaining why the protocol is designed the way it is. This repository tries to do both — explain the reasoning, then show the implementation.
 
---
 
## Status
 
| Section | Status |
|---|---|
| 01 · Why Is It Needed? | 🔄 In progress |
| 02 · What It Actually Is? | 🔄 In progress |
| 03 · How Is It Implemented? | 🔄 In progress |
 
---
 
*Built as part of a structured Agentic AI study plan.*
