# 🚀 AI Code Review & Auto-refactor Agent

An autonomous multi-agent pipeline designed to eliminate Pull Request bottlenecks and enforce architectural standards in small-scale development teams.

---

## 🔴 The Problem
In a 5-developer squad, manual code reviews often become a massive bottleneck.
- **Latency:** PRs sit for hours, causing developers to lose context and focus.
- **Complexity:** Merge conflicts accumulate while waiting for senior approval.
- **Gap:** Existing tools like GitHub Copilot focus on line-level suggestions but lack global codebase awareness, leading to missed architectural flaws and security anti-patterns.

## ⚙️ Core Architecture (Multi-Agent Pipeline)
The system operates through a specialized four-stage pipeline to ensure deep, context-aware reviews:

1. **Diff Analyzer:** Parses raw `git diff` into a clean, structured logical delta.
2. **Context Retriever (RAG):** Performs Semantic Search across the entire repository to fetch dependencies, naming conventions, and business logic context.
3. **Reasoning Engine (Long-Context):** Executes multi-pass reasoning on **Security, Performance, and Maintainability**. This stage utilizes **10k–30k tokens per request** to maintain full architectural context.
4. **Refactor Suggester:** Converts reasoning outputs into production-ready **Unified Diff patches**.

## 🛠 Tech Stack
- **LLM:** MiMo V2.5 Pro (via Xiaomi MiMo Orbit)
- **Framework:** LangGraph / CrewAI
- **Database:** ChromaDB (for RAG context)
- **Inference:** Long-Context Reasoning (32k+ Window)

## 📈 Key Impact
- **80% Reduction** in initial review latency.
- **Auto-refactoring** for repetitive styling and simple logic flaws.
- **Deep Security Audits** integrated directly into the CI/CD pipeline.
