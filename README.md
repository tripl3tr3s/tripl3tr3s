# Triple Tres

**AI Engineer. Production LLM and agent systems in TypeScript.**

I build the unglamorous parts that make AI agents trustworthy in production: MCP servers, multi-agent orchestration, observability, and human-in-the-loop gates. Solo-built and shipped a 43-tool MCP server and a 3-tier Claude orchestration layer, backed by 6,000+ tests, 91%+ coverage, and end-to-end Langfuse tracing. Open to AI engineering roles.

📍 México (UTC-6, EST-aligned) · 🌐 [tripl3.dev](https://tripl3.dev) · ✉️ <hola@tripl3.dev> · [LinkedIn](https://www.linkedin.com/in/tripl3tr3s)

---

## What I've shipped

**SAT-MCP.** Production MCP server for Mexican tax compliance (CFDI 4.0). Full MCP primitive set plus 8 MCP-UI mini-apps, SSE and HTTP Streamable transport, multi-tenant CSD management, 5 PAC providers behind circuit breakers, and EFOS/EDOS blacklist monitoring. 6,000+ tests in strict TypeScript. Private commercial product; happy to walk through the architecture and code in an interview.

**DISAI-Conta.** AI-native fiscal platform built on SAT-MCP, live in private beta at [disai.mx](https://disai.mx). A Haiku router classifies 10 fiscal domains in about 100ms, Sonnet domain agents run native `tool_use` loops with self-correction, and an Expert Registry injects SAT catalog resources into context before the first call, removing an entire class of hallucinated catalog codes without RAG overhead. Langfuse traces everything; a HITL dashboard gates irreversible operations. _(Next.js 16, Anthropic SDK, SSE streaming)_

**[Crypto/TradFi Analytics Terminal](https://github.com/RetailDAO/website).** Real-time dashboard over dual WebSockets: Node.js backend, Redis caching, circuit breakers, and graceful degradation. (Live demo Archived)

**[n8n Freelancer Starter](https://github.com/tripl3tr3s/n8n-freelancer-starter).** One-click Railway template for production-configured self-hosted n8n. Replaces a $20 to $30 per month Zapier/Make dependency for small teams.

---

## Writing

I write about what I actually build: the design decisions, and what breaks in production.

- [122,449 Operations Per Minute: Benchmarking a Production MCP Server](https://www.linkedin.com/posts/tripl3tr3s_hace-un-par-de-d%C3%ADas-alcanc%C3%A9-un-hito-que-me-ugcPost-7395001162833387520-A22X)
- [80% of Requests Never Hit the Expensive Model: 3-Tier Routing as Architecture](https://www.linkedin.com/posts/tripl3tr3s_mcp-aiengineering-buildinpublic-ugcPost-7457998591287054336-JkT-)
- [Building AI-Native Mexican Fiscal Compliance, 7 Months Solo](https://www.linkedin.com/posts/tripl3tr3s_mcp-aiengineering-buildinpublic-share-7457548155954475008-a6CF)
- [AI Strategy Is Not Business Strategy with AI Bolted On](https://www.linkedin.com/posts/tripl3tr3s_aistrategy-businessai-mlops-share-7437688675934789632-uTg5)

---

## Stack

**AI systems:** Anthropic Claude API (`tool_use`, streaming, multi-turn) · MCP (full primitive set, server and client) · multi-agent orchestration · Langfuse tracing and evals · HITL approval patterns
**Backend:** TypeScript / Node.js · PostgreSQL (RLS, pgvector) · SQLite · Redis · Zod · Docker · Railway · CI/CD
**Frontend:** Next.js · React · Tailwind · SSE streaming UIs
**Also:** n8n (self-hosted, multi-client) · Python (growing: data pipelines, verification scripts)

## Credentials

- **Model Context Protocol: Advanced Topics**, Anthropic
- **Claude Code in Action**, Anthropic
- **Building Scalable Agentic Systems**, DataCamp
- **n8n Self-Hosted for Enterprises**, n8n

Full credential history on [LinkedIn](https://www.linkedin.com/in/tripl3tr3s).

---

## Background

Before AI engineering: 13 years running a tattoo studio and working as a graphic designer, then two years writing deep technical research on protocol architecture and market microstructure ([research archive](https://tripl3.dev/#projects)). Precision, pattern recognition, and reading unfamiliar systems fast. The same rigor now goes into AI infrastructure.

> Reliability and observability · Evaluation over assumption · Pragmatism over hype
