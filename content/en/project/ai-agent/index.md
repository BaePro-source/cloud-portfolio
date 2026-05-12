---
title: LLM-Based AI Agent
summary: Autonomous task-executing AI Agent built with LangChain and OpenAI API
tags:
  - agent
  - ai
date: 2025-03-01
external_link: https://github.com/BaePro-source
image:
  caption: 'AI Agent Architecture'
  focal_point: Smart
  preview_only: false
---

## LLM-Based AI Agent Project

A project implementing an AI Agent that autonomously selects tools and executes tasks, powered by the LangChain framework and OpenAI GPT API.

### Key Features
- **Tool Calling**: Integration with external tools including web search, file I/O, and code execution
- **ReAct Pattern**: Agent loop implementing iterative Reasoning and Acting
- **Memory Management**: Context retention using conversation history and long-term memory stores
- **Multi-Agent**: Pipeline design with multiple agents collaborating across different roles

### Tech Stack
- Python, LangChain, OpenAI API
- ChromaDB (Vector Store)
- FastAPI (Agent Serving)
