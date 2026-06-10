---

## Day 2 — 2026-06-09

### What I worked on today
- Completed EX-02 — OWASP LLM Top 10 deep dive
- Added personal notes for all 10 entries with financial services context
- Fixed git commit identity to Narendra Karki
- Resolved SSH key issues for NarendraKarki GitHub account

### What worked
- All 10 OWASP LLM entries documented with attack scenarios
- GitHub pushing cleanly with correct identity

### What didn't work and how I fixed it
- SSH key was missing — generated new ed25519 key and added to GitHub
- Commits showing as diveinme — fixed with git config global user settings

### Things I want to understand better
- Embedding inversion techniques for LLM08
- RLHF poisoning detection methods for LLM04

### Questions for further research
- How do current financial regulators (FCA, CBB) address LLM-specific risks?
- What SIEM detection rules exist for excessive agency attacks?

---

## Day 3 — 2026-06-10

### What I worked on today
- EX-03 — MITRE ATLAS mapping — FinBot attack chain completed
- EX-04 — VulnFinBot built and running on localhost:5001
- Four live attacks executed — LLM01, LLM02, LLM06, LLM07 all confirmed
- Full lab report with findings and recommendations committed
- Workflow and LinkedIn carousel diagrams generated and saved

### What worked
- All four attacks succeeded against VulnFinBot
- Attack 3 was most surprising — no injection needed, just a direct question
- MITRE ATLAS attack chain maps cleanly to traditional APT kill chain

### What didn't work and how I fixed it
- Port 5000 taken by another app— switched to port 5001
- Email tool did not fire — model generated email as text not TOOL_CALL JSON

### Things I want to understand better
- How LangChain tool binding would make Attack 4 fire automatically
- Llama Guard implementation for prompt injection classification

### Questions for further research
- What detection rules would catch these attacks in Microsoft Sentinel?
- How do production LLM deployments handle PII filtering at output layer?