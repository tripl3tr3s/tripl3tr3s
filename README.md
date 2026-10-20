# Triple Tres

**AI Engineer. Production LLM and agent systems in TypeScript.**

I build the unglamorous parts that make AI agents trustworthy in production: MCP servers, bounded agent loops, evaluation harnesses, observability, and human-in-the-loop gates. Solo-built and shipped a 46-tool MCP server and a 3-tier Claude orchestration layer, backed by 6,000+ tests, 91%+ coverage, and end-to-end Langfuse tracing. Open to AI engineering roles.

México (UTC-6, EST-aligned) · [tripl3.dev](https://tripl3.dev) · <hola@tripl3.dev> · [LinkedIn](https://www.linkedin.com/in/tripl3tr3s)

---

## What I've shipped

### Products

**SAT-MCP.** Production MCP server for Mexican tax compliance (CFDI 4.0). 46 tools across the full MCP primitive set plus 8 MCP-UI mini-apps, SSE and HTTP Streamable transport, multi-tenant CSD management, 5 PAC providers behind circuit breakers, and EFOS/EDOS blacklist monitoring. 6,000+ tests in strict TypeScript. Private commercial product; happy to walk through the architecture and code in an interview. An MIT-licensed open-source core (17 tools, schema-driven codegen, tests checked against SAT's own XSDs and XSLTs) is coming soon.

**DISAI-Conta.** AI-native fiscal platform built on SAT-MCP, live in private beta at [disai.mx](https://disai.mx). A Haiku router classifies 10 fiscal domains, Sonnet domain agents run native `tool_use` loops with self-correction, and Opus takes the highest-stakes domains (payments, compliance). An Expert Registry injects SAT catalog resources into context before the first call, removing an entire class of hallucinated catalog codes without RAG overhead. Langfuse traces everything; a HITL dashboard gates irreversible operations. _(Next.js 16, Anthropic SDK, SSE streaming)_

### Open source

**[efos-risk-graph](https://github.com/tripl3tr3s/efos-risk-graph)** [![npm](https://img.shields.io/npm/v/efos-risk-graph.svg?color=black)](https://www.npmjs.com/package/efos-risk-graph)
Directed-graph engine for SAT's Art. 69-B blacklist (EFOS/EDOS). Your direct supplier may be clean while _their_ supplier is a confirmed EFOS: the engine propagates risk across billing chains with per-hop attenuation, returns the path that explains each score, and detects invoicing carousels as graph cycles. Every design choice is derived and verified: BFS is provably optimal for max-score propagation, and the depth cutoff has a geometric error bound. Open-core by design: the engine is public, the billing edges stay private.

**[ai-reliability-eval-lab](https://github.com/tripl3tr3s/ai-reliability-eval-lab)**
Reproducible benchmark for bounded tool-using agents, comparing direct, routed, and resource-free configurations on synthetic Mexican fiscal data. Versioned datasets with scheduled faults and abstention cases; Wilson, Clopper-Pearson, exact McNemar and paired bootstrap statistics checked against scipy; a PASS / BLOCK / INCONCLUSIVE go-live gate; a hash-chained audit log; and provider-independent adapters. The whole pipeline runs without credentials. Results are pending the first full live run, and the repo says so rather than reporting numbers it doesn't have.

**Building blocks**, extracted from production and small enough to read in one sitting:

- **[agentic-tool-loop](https://github.com/tripl3tr3s/agentic-tool-loop)** - a bounded, self-correcting tool-use loop for the Anthropic Messages API in about 120 lines. Hard guards for iterations, refusals, and malformed follow-ups.
- **[llm-cost-router](https://github.com/tripl3tr3s/llm-cost-router)** - tiered model routing plus cost metering that prices prompt-cache reads and writes correctly. Pure, immutable, dependency-free. On [npm](https://www.npmjs.com/package/llm-cost-router).
- **[mcp-tool-idempotency](https://github.com/tripl3tr3s/mcp-tool-idempotency)** - exactly-once execution for MCP tool calls, so retries never fire side effects twice. Two-layer dedup (in-flight map plus atomic claim) with crash recovery.

---

## Writing

I write about what I actually build: the design decisions, and what breaks in production.

- [122,449 Operations Per Minute: Benchmarking a Production MCP Server](https://www.linkedin.com/posts/tripl3tr3s_hace-un-par-de-d%C3%ADas-alcanc%C3%A9-un-hito-que-me-ugcPost-7395001162833387520-A22X)
- [80% of Requests Never Hit the Expensive Model: 3-Tier Routing as Architecture](https://www.linkedin.com/posts/tripl3tr3s_mcp-aiengineering-buildinpublic-ugcPost-7457998591287054336-JkT-)
- [Building AI-Native Mexican Fiscal Compliance, 7 Months Solo](https://www.linkedin.com/posts/tripl3tr3s_mcp-aiengineering-buildinpublic-share-7457548155954475008-a6CF)
- [AI Strategy Is Not Business Strategy with AI Bolted On](https://www.linkedin.com/posts/tripl3tr3s_aistrategy-businessai-mlops-share-7437688675934789632-uTg5)

---

## Stack

**AI systems:** Anthropic Claude API (`tool_use`, streaming, adaptive thinking) · MCP (full primitive set, server and client) · multi-agent orchestration and model routing · Langfuse tracing · HITL approval patterns
**Evaluation:** versioned eval datasets · statistical comparison (confidence intervals, paired tests, bootstrap) · go-live gates · regression detection
**Backend:** TypeScript / Node.js · PostgreSQL (RLS, pgvector) · SQLite · Redis · Zod · Docker · Railway · CI/CD
**Frontend:** Next.js · React · Tailwind · SSE streaming UIs
**Also:** Python (codegen, data pipelines, verification scripts) · n8n

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

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=tripl3tr3s&show_icons=true&theme=radical&hide_border=true" alt="GitHub stats" height="165" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=tripl3tr3s&layout=compact&theme=radical&hide_border=true" alt="Top languages" height="165" />
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=tripl3tr3s&style=flat-square&color=fe428e" alt="Profile views" />
</p>
