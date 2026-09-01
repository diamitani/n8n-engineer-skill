# n8n Engineer

**Enterprise-grade AI agent skill for production n8n workflows, MCP architecture, and GTM automation.**

[![Landing Page](https://img.shields.io/badge/Landing%20Page-Live-blue)](https://diamitani.github.io/n8n-engineer-landing/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## 🚀 Quick Start

### Install

```bash
# Clone the skill
git clone https://github.com/diamitani/n8n-engineer-skill.git ~/.hermes/skills/n8n-engineer

# Or via Hermes CLI
hermes skills install n8n-engineer
```

### Use

Say to your AI agent:

- "Build an n8n workflow that researches prospects and writes personalized outreach"
- "Set up an MCP server for my n8n instance"
- "Create a GTM automation that enrolls leads into sequences"

---

## 📦 What You Get

- **SKILL.md** — Complete skill specification
- **8 Reference Guides:**
  - architecture.md — MCP patterns, integration surfaces, decision framework
  - agents.md — AI agent patterns, tool design, evaluations
  - http-api.md — REST/API integration, auth, pagination
  - hard-nodes.md — Common traps and solutions
  - gtm.md — Revenue-focused workflow patterns
  - ops.md — Scaling, error handling, rollout
  - starter-pack.md — Bundled workflow templates
  - sources.md — Official n8n documentation index

---

## 🏗️ Capabilities

### MCP Architecture
- Instance-level MCP for multi-workflow control planes
- MCP Server Trigger for purpose-built tool servers
- MCP Client Tool for external tool consumption
- Call n8n Workflow Tool for internal capabilities

### AI Agent Runtime
- System goal definition and tool descriptions
- Human review gates for high-impact writes
- Evaluation datasets and rollback plans
- Adaptive paths vs. deterministic routing

### GTM Automation
- Prospect enrichment and account research
- CRM writeback with deduplication shields
- Outbound sequence enrollment and follow-up
- Meeting prep and deal unblocking automation

### HTTP & API Integration
- Native nodes vs. HTTP Request vs. custom nodes
- Auth strategies (OAuth2, API keys, bearer tokens)
- Pagination, rate limits, and retry logic
- n8n API for workflow management

---

## 🎯 When to Use

**Always:**
- Building or debugging n8n workflows
- Architecting MCP integrations
- Scaling production automation
- Revenue-generating GTM workflows

**Especially when:**
- You need MCP architecture guidance
- You're connecting AI agents to n8n
- You're building outbound or sales automation
- You need production-grade error handling

---

## 📖 Architecture Decision Framework

1. **Decide integration surface:**
   - Instance-level MCP → Multi-workflow control plane
   - MCP Server Trigger → Purpose-built tool server
   - MCP Client Tool → External tool consumption
   - Sub-workflows → Reusable business capabilities
   - Native nodes → Best when operation exists
   - HTTP Request → Unsupported operations
   - Custom nodes → Heavy reuse, complex auth

2. **Define the contract:**
   - Trigger and input schema
   - Normalization layer
   - Business logic
   - Tool and action layer
   - Logging and error path
   - Operator escalation path

3. **For agentic workflows:**
   - System goal
   - Tool descriptions
   - Allowed write actions
   - Human review gates
   - Evaluation dataset
   - Rollback plan

---

## 🔧 Build Patterns

- **Native node first** — Best when operation exists and credential UX matters
- **HTTP Request second** — Best for unsupported operations on known APIs
- **Custom community node third** — Best when reuse, auth complexity, or UX justify investment
- **Sub-workflow by default** — For shared business capabilities (enrichment, research, writeback)
- **AI Agent only when** — Tool selection, reasoning, or adaptive paths create real value

---

## 📚 Documentation Structure

```
n8n-engineer/
├── SKILL.md                    # Main skill specification
├── references/
│   ├── architecture.md         # MCP & integration patterns
│   ├── agents.md              # AI agent patterns
│   ├── http-api.md            # REST/API integration
│   ├── hard-nodes.md          # Common pitfalls
│   ├── gtm.md                 # Revenue workflows
│   ├── ops.md                 # Production operations
│   ├── starter-pack.md        # Workflow templates
│   └── sources.md             # Official docs index
├── agents/                     # Agent templates (optional)
└── assets/                     # Workflow JSON examples (optional)
```

---

## 🎨 GTM Workflow Shape

Proven revenue workflow pattern:

```
signal → enrich → qualify → personalize → approve → send → log → follow-up → feedback loop
```

Separate read-heavy research from write-heavy execution.  
Gate writes to CRM, email, sequencing with confidence thresholds or human review.

---

## 🔍 Validation Checklist

Before deploying workflows:

- [ ] The chosen surface is correct (instance MCP vs MCP Trigger vs sub-workflow)
- [ ] Workflow separates deterministic logic from agentic logic
- [ ] Credentials referenced through n8n credentials or approved secret stores
- [ ] Human review exists for high-impact writes
- [ ] Error handling and rollback are specified
- [ ] Pagination, batching, rate limits, and retries addressed
- [ ] User can tell what is reusable vs. environment-specific

---

## 🤝 Contributing

1. Fork the repo
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

---

## 📝 License

MIT License — see LICENSE for details

---

## 🙏 Credits

**Framework:** ROSTR (Runtime, Orchestration, State, Tools, Reference)  
**Author:** Patrick Diamitani  
**Organization:** Diamitani Industries

---

## 🔗 Links

- **Landing Page:** https://diamitani.github.io/n8n-engineer-landing/
- **GitHub:** https://github.com/diamitani/n8n-engineer-skill
- **Issues:** https://github.com/diamitani/n8n-engineer-skill/issues

---

**Master n8n like a systems engineer.** 🚀
