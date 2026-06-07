# Module 01 — LLM Threat Modelling

**Duration:** Days 1–7 (56 hours)  
**Status:** 🔄 In Progress  
**Frameworks:** STRIDE · OWASP LLM Top 10 · MITRE ATLAS  

---

## Objective

Build a complete, reusable threat model for an LLM-powered application in a regulated financial services context. This module produces artefacts that underpin every subsequent module — understanding the threat landscape first ensures all defensive work is purposeful and traceable.

---

## Learning Outcomes

By the end of this module you will be able to:

1. Apply STRIDE threat modelling methodology to LLM-based systems
2. Map identified threats to OWASP Top 10 for LLMs (2025 edition)
3. Map identified threats to MITRE ATLAS tactics and techniques
4. Identify attack surfaces unique to agentic and RAG-based architectures
5. Produce a professional threat model document suitable for a financial services audience
6. Explain the difference between traditional application threat modelling and LLM-specific threat modelling

---

## Background Reading (Complete Before Exercises)

| Resource | Time | Priority |
|---|---|---|
| [OWASP LLM Top 10 — 2025](https://owasp.org/www-project-top-10-for-large-language-model-applications/) | 2 hrs | Essential |
| [MITRE ATLAS Matrix](https://atlas.mitre.org/matrices/ATLAS) | 2 hrs | Essential |
| [STRIDE Threat Modelling (Microsoft)](https://learn.microsoft.com/en-us/azure/security/develop/threat-modeling-tool-threats) | 1 hr | Essential |
| [NIST AI RMF Playbook](https://airc.nist.gov/Docs/2) | 1 hr | Recommended |
| [Gartner: AI TRiSM Framework](https://www.gartner.com/en/articles/what-is-ai-trism) | 30 min | Recommended |

---

## Exercises

| # | Exercise | Day | Hours | Report |
|---|---|---|---|---|
| 01 | [Environment Setup & Repo Initialisation](./exercises/EX-01-environment-setup.md) | 1 | 3 | [Report](./reports/REPORT-01-environment-setup.md) |
| 02 | [OWASP LLM Top 10 Deep Dive](./exercises/EX-02-owasp-llm-top10.md) | 1–2 | 4 | [Report](./reports/REPORT-02-owasp-llm-top10.md) |
| 03 | [MITRE ATLAS Mapping](./exercises/EX-03-mitre-atlas-mapping.md) | 2 | 3 | [Report](./reports/REPORT-03-mitre-atlas.md) |
| 04 | [Build a Vulnerable LLM Application](./exercises/EX-04-vulnerable-llm-app.md) | 3 | 4 | [Report](./reports/REPORT-04-vulnerable-app.md) |
| 05 | [STRIDE Threat Model — LLM Financial App](./exercises/EX-05-stride-threat-model.md) | 3–4 | 6 | [Report](./reports/REPORT-05-stride.md) |
| 06 | [Full Threat Model Document](./exercises/EX-06-threat-model-document.md) | 5–6 | 6 | [Report](./reports/REPORT-06-threat-model-final.md) |
| 07 | [Week 1 Review & LinkedIn Article](./exercises/EX-07-week1-review.md) | 7 | 8 | — |

---

## Key Deliverables

- [ ] `threat-model-llm-financial-services.md` — full threat model document
- [ ] `stride-mapping-table.xlsx` — STRIDE × OWASP × ATLAS cross-reference
- [ ] `vulnerable-llm-app/` — intentionally vulnerable Flask app used as target
- [ ] Lab reports for all 7 exercises
- [ ] LinkedIn article: *LLM Threat Modelling in Financial Services*

---

## Tools Used

| Tool | Purpose | Install |
|---|---|---|
| Python 3.11+ | All scripting | `brew install python` |
| Flask | Vulnerable LLM app | `pip install flask` |
| OpenAI / Ollama | LLM backend | Local via Ollama |
| draw.io / Eraser.io | Threat model diagrams | Web-based |
| VS Code | IDE | Already installed |

---

## OWASP LLM Top 10 Coverage

| OWASP ID | Name | Covered in Exercise |
|---|---|---|
| LLM01 | Prompt Injection | EX-04, EX-05 |
| LLM02 | Sensitive Information Disclosure | EX-05 |
| LLM03 | Supply Chain | EX-05 |
| LLM04 | Data and Model Poisoning | EX-05, M2 |
| LLM05 | Improper Output Handling | EX-04, EX-05 |
| LLM06 | Excessive Agency | EX-05, M5 |
| LLM07 | System Prompt Leakage | EX-04 |
| LLM08 | Vector and Embedding Weaknesses | EX-05 |
| LLM09 | Misinformation | EX-05 |
| LLM10 | Unbounded Consumption | EX-05 |

---

## MITRE ATLAS Coverage

| Tactic | Technique | Exercise |
|---|---|---|
| Initial Access | LLM Prompt Injection (AML.T0051) | EX-04 |
| Execution | LLM Jailbreak (AML.T0054) | EX-04 |
| Exfiltration | LLM Data Leakage (AML.T0057) | EX-05 |
| Impact | LLM Denial of Service | EX-05 |

---

## Notes & Observations

> Running log — add entries as you work through exercises.

---

*Module started: [DATE] · Target completion: Day 7*
