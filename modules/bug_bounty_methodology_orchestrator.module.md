# ── PROMPTOS MODULE: bug_bounty_methodology_orchestrator ─────────────────────────────────────────────
# Version: 1.0
# Kernel compatibility: PromptOS v2.0+
# Source: awesome-prompts/bug_bounty_methodology_orchestrator.txt
# ─────────────────────────────────────────────────────────────────────────────

## MODULE.IDENTITY
name: bb-methodology

## MODULE.PROCESS
1. **Define**: "Today I target [feature/domain] to achieve [CIA impact]"
2. **Select**: Choose 1-2 vuln classes (IDOR, Race Condition, etc.)
3. **Execute**: Focus ONLY on selected techniques. No wandering.
1. **Confidentiality** -- steal data the attacker shouldn't see
2. **Integrity** -- modify data the attacker shouldn't change
3. **Availability** -- disrupt service (app-level DoS only)
4. **Account Takeover** -- control another user's account
5. **RCE** -- execute commands on the server

## MODULE.TOOLING
**Checklist:**
- [ ] Map all endpoints (Burp/Caido sitemap + JS analysis)
- [ ] Identify auth model (cookie, JWT, OAuth, SAML?)
- [ ] Find business-critical flows (payment, registration, password reset, data export)
- [ ] Download and analyze JS files for hidden routes, secrets, logic
- [ ] Identify roles and permissions (user, admin, API keys)
- [ ] Note "weird" behaviors (anomalies in naming, errors, timing)
- [ ] Can attack work with 0-1 clicks? (minimize prerequisites)
- [ ] Does it affect all users or specific role?
- [ ] What's the business $ impact?
- [ ] While waiting for triage: try to escalate further (A->B signal method)

## MODULE.OUTPUT
min_v: 4

deliverables | Nothing — even "no finding here" is reportable as a positive defensive observation |
| **Pentest** (signed SoW / WAPT) | Depends on SoW. Read scope explicitly. Usually accepts hygiene + impact + recon | Out-of-scope assets, unsigned testing |
| **Internal audit** | Compliance-mapped findings (PCI / ISO / NIST / DPDPA / GDPR) | Findings without a control-mapping |

**Hard rule:** Before Phase 0 runs, write the engagement type as the first line in your hunt notes. If you can't answer it from the user's instruction, ASK once. Don't assume — the mistake costs both you and the triage

## MODULE.COMMANDS
/bug_bounty_methodology_orchestrator:plan — Output agent decomposition plan before execution
/bug_bounty_methodology_orchestrator:status — Show current task delegation state

# ── END MODULE ────────────────────────────────────────────────────────────────
