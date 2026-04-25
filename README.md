# Cybercentry Verification — Claude Code Skill

A verification-first OWASP security review skill for [Claude Code](https://claude.com/claude-code). Threat-model driven, risk-prioritized, and anchored to the full OWASP standards suite — Top 10:2025, ASVS 5.0, API Security Top 10, and the Top 10 for LLM Applications 2025.

> **Cybercentry: AI Agent Cyber Security | Verification | Risk-Aware Systems.**

## What it does

Turns Claude into **Cybercentry** — a sharp security verifier that:

- **Threat-models first** — maps assets, entry points, trust boundaries, and data flows before reviewing code
- **Anchors every finding to OWASP** — Top 10:2025, ASVS 5.0, API Security, LLM Top 10 2025
- **Prioritizes by risk** — Critical and High first, with business/exploit impact
- **Delivers surgical fixes** — concrete diffs, config snippets, and exact tool commands (Semgrep, ZAP, Snyk, Trivy)
- **Covers AI/agent-specific risks** — prompt injection, supply chain, deserialization, vector/embedding weaknesses

Findings come back in a consistent format:

```
OWASP Ref | Severity | Finding | Location | Impact | Verification Steps | Recommended Fix
```

## Install

### Option 1 — Global install (recommended)

Available across every project on your machine.

**macOS / Linux:**
```bash
git clone https://github.com/Cybercentry/cybercentry-verification.git
mkdir -p ~/.claude/skills
cp -r cybercentry-verification/skills/cybercentry-verification ~/.claude/skills/
```

**Windows (PowerShell):**
```powershell
git clone https://github.com/Cybercentry/cybercentry-verification.git
New-Item -ItemType Directory -Force -Path "$HOME\.claude\skills" | Out-Null
Copy-Item -Recurse cybercentry-verification\skills\cybercentry-verification "$HOME\.claude\skills\"
```

### Option 2 — Project install

Scoped to one project only.

```bash
git clone https://github.com/Cybercentry/cybercentry-verification.git
mkdir -p .claude/skills
cp -r cybercentry-verification/skills/cybercentry-verification .claude/skills/
```

## Use

In a Claude Code session, either:

- Invoke directly: `/cybercentry-verification`
- Or ask in natural language: `Cybercentry, verify this codebase` / `run a security verification on this PR`

Claude will load the skill, confirm scope and threat model, and produce a risk-prioritized report.

## What's covered

**OWASP Top 10:2025**
- A01 Broken Access Control · A02 Security Misconfiguration · A03 Software Supply Chain Failures · A04 Cryptographic Failures · A05 Injection · A06 Insecure Design · A07 Authentication Failures · A08 Software or Data Integrity Failures · A09 Security Logging and Alerting Failures · A10 Mishandling of Exceptional Conditions

**Plus:**
- OWASP ASVS 5.0
- OWASP API Security Top 10
- OWASP Top 10 for LLM Applications 2025 (Gen AI Security Project)
- OWASP Cheat Sheet Series, WSTG, Code Review Guide

## Contributing

PRs welcome. If you spot stale OWASP wording, missing categories, or have improvements to the verification flow, open an issue or PR.

## License

[MIT](LICENSE) — fork freely.

---

Built by [Cybercentry](https://github.com/Cybercentry).
