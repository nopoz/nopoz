I build operations tooling for containerized infrastructure, networking, and DNS, alongside AI agents that bring safe, supervised autonomy to that work, designed to run anywhere from a homelab to production.

### Projects

#### [hosaka](https://github.com/nopoz/hosaka)
[![release](https://img.shields.io/github/v/release/nopoz/hosaka)](https://github.com/nopoz/hosaka/releases) [![CI](https://img.shields.io/github/actions/workflow/status/nopoz/hosaka/ci.yml?label=CI)](https://github.com/nopoz/hosaka/actions/workflows/ci.yml)

Monitors container images across one or many hosts and drives controlled, health-aware updates: semver-aware classification, one-click upgrades with live console output, and notifications via Slack, Discord, Telegram, SMTP, and webhooks. On-demand AI analysis summarizes what changed between your current and target version and flags breaking changes before you upgrade.

#### [pfsense-dnscrypt-proxy](https://github.com/nopoz/pfsense-dnscrypt-proxy)
[![release](https://img.shields.io/github/v/release/nopoz/pfsense-dnscrypt-proxy)](https://github.com/nopoz/pfsense-dnscrypt-proxy/releases) [![CI](https://img.shields.io/github/actions/workflow/status/nopoz/pfsense-dnscrypt-proxy/ci.yml?label=CI)](https://github.com/nopoz/pfsense-dnscrypt-proxy/actions/workflows/ci.yml)

Brings encrypted DNS (DNSCrypt, DoH, Oblivious DoH, Anonymized DNS) to pfSense firewalls with a full management GUI. Signature-verified builds with SLSA provenance for supply-chain assurance.

#### [portrieve](https://github.com/nopoz/portrieve)
[![release](https://img.shields.io/github/v/release/nopoz/portrieve)](https://github.com/nopoz/portrieve/releases) [![CI](https://img.shields.io/github/actions/workflow/status/nopoz/portrieve/ci.yml?label=CI)](https://github.com/nopoz/portrieve/actions/workflows/ci.yml)

Backs up, restores, and migrates Portainer stacks as plain, version-controllable Docker Compose files. Supports GitOps workflows, disaster recovery, and environment migration without all-or-nothing database snapshots.

### Demos

#### [sentinel](https://github.com/nopoz/sentinel)

**Stack:** Python · LangGraph · claude-agent-sdk · FastAPI · Playwright · Docker · LangSmith

SecOps AI agent that investigates security alerts read-only and pauses for explicit human approval before executing any remediation. LangGraph orchestrates a plan/act/reflect loop with a structural approval gate: the only path to a state-changing action runs through a human decision, enforced by the graph rather than a prompt. Capability-separated tool policy keeps write actions physically out of reach during investigation, and a headline eval proves no remediation runs before approval. The agent drives a Dockerized Playwright browser through a mock SOC console.

#### [stiletto](https://gist.github.com/nopoz/79e070cc69f7e326cc3b283b87383006)

**Stack:** Python · LangGraph · Claude · FastAPI · Pydantic · Docker · LangSmith

Red-teaming AI agent that runs a full pentest campaign (recon, exploitation, post-exploitation, lateral movement, persistence, and a ranked report), with the model reasoning but never touching the network. Claude returns schema-validated JSON while a LangGraph state machine owns scope and runs every tool behind a fail-closed scope guard that denies by default; the reasoning layer holds no path to a subprocess. Human-approval gates are real checkpointed graph interrupts the model cannot skip, and the brain authors exploits for operator review before they run. The operator drives the whole campaign from a live web console (FastAPI + WebSocket) that streams tool activity in real time and is where every approval gate is cleared. Every phase is MITRE ATT&CK-aligned with per-tactic KPIs and audit trails in LangSmith, and any live run replays deterministically. Source is private; demo available on request.

### Security & CI/CD

I treat the pipeline as part of the product. Practices I apply across my projects and contributions:

- Default-deny GitHub Actions permissions (`permissions: {}`), with each job opting back into the least scope it needs.
- Third-party actions pinned to commit SHAs rather than mutable tags, to close supply-chain gaps.
- Layered scanning: secret detection (gitleaks), workflow auditing (actionlint, zizmor), dependency review, Dockerfile and image scanning (hadolint, Trivy), and CodeQL static analysis.
- Signed, attested release artifacts (SLSA provenance) so downstream users can verify what they install.

### Also contribute to

[Home Assistant](https://github.com/home-assistant/core) · [odysseus](https://github.com/pewdiepie-archdaemon/odysseus)

### Focus areas

Agentic AI systems · Human-in-the-loop autonomy · LLM tooling & evals · AI-driven security analysis & response · Container operations · Encrypted DNS · CI/CD supply-chain security
