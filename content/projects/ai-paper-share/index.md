---
title: AI Paper Xiaohongshu Sharing System
summary: An automated AI research content workflow built with OpenClaw, LangGraph, and FastMCP.
date: 2026-03-01
weight: 1
---

An automated workflow for turning AI research papers into reviewed and publishable Xiaohongshu content.

### Workflow

- Fetches and filters papers from arXiv.
- Scores papers and generates publication-ready copy and covers.
- Uses Feishu for review and revision before publishing.
- Publishes through the Xiaohongshu account “AI Frontier Share”.

### Architecture

- OpenClaw acts as the control center, coordinating multiple MCP plugins with separated responsibilities.
- FastMCP packages LangGraph workflows as callable MCP services.
- LangGraph manages paper selection, scoring, copywriting, cover generation, review, and rewriting as a stateful workflow.
- Multiple agents collaborate through chained calls and iterative review to improve copy quality.

The system has automatically shared 20 AI research papers.
