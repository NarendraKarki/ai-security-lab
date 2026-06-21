# Module 05 — Agentic AI & API Security

**Duration:** Week 3 · Days 18–21 (32 hours)
**Status:** 🔄 In progress
**Tools:** LangChain (0.1.20 — classic ReAct agent API) · Ollama (llama3:latest) · OWASP API Top 10

## Objective
Evaluate the security posture of agentic AI systems — LLM agents that can autonomously call tools, browse the web, write and execute code, and interact with external APIs. Map attack scenarios to OWASP API Top 10 and design human-in-the-loop governance controls.

## Scenario

**FinAssist** — a simulated internal LangChain agent for SecureBank's
customer support team, with tool access to three backend APIs:
read-only balance lookup, read-only transaction history, and a
write-action refund tool (`initiate_refund`) built *without* an
authorization check binding the requested account to the
authenticated support session. This deliberate, documented gap is
the subject of this module's attack exercises (OWASP API1 — Broken
Object Level Authorization, API5 — Broken Function Level
Authorization).

Architecture choice: `llama3:latest` has no native tool-calling
support (`"capabilities": ["completion"]` per Ollama's `/api/tags`),
so the agent uses a ReAct (text-parsed) tool-call pattern rather than
structured function-calling — making the parsing layer itself part
of the threat surface under test, not just the model's reasoning.

## Exercises

| # | Exercise | Day | Hours | Status | Report |
|---|---|---|---|---|---|
| 01 | Build a LangChain financial agent | 18 | 4 | ✅ Complete | [ex01-langchain-financial-agent.md](./reports/ex01-langchain-financial-agent.md) |
| 02 | Tool misuse attack scenarios | 18-19 | 4 | ⏳ Pending | — |
| 03 | OWASP API Top 10 testing | 19-20 | 4 | ⏳ Pending | — |
| 04 | HiTL control design | 20 | 4 | ⏳ Pending | — |
| 05 | Agentic security governance doc | 21 | 4 | ⏳ Pending | — |

*Module starts: Day 18 · Target completion: Day 21*

## Evidence integrity note

Exercise 01's evidence folder (`evidence/runs/`) intentionally
preserves a run that produced a false-positive `API1-BOLA` finding
due to a tool-input parsing bug, alongside the corrected run that
followed the fix. Both are indexed in `evidence/runs/INDEX.md`. This
is a deliberate documentation choice, not an oversight — see Section
7 of the Exercise 01 report for the reasoning. Evidence in this
module is structured per `EVIDENCE-SCHEMA.md`, with every tool
invocation cross-checked against the mock backend's own independent
call log (`mock_backend.py`), so that findings reflect what actually
executed rather than what the agent's text output claims happened.
