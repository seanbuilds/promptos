# PromptOS v2.0

**A prompt operating system synthesized from a Best-of-4 agent competition.**

One stable kernel. 275 domain modules. Every prompt from [ai-boost/awesome-prompts](https://github.com/ai-boost/awesome-prompts) recompiled into the PromptOS format.

---

## What Is This?

The `awesome-prompts` repository has 275 expert system prompts covering everything from SRE to academic peer review to Solidity smart contract engineering. They're great. But they each reinvent the same interaction scaffolding — verbosity control, output formatting, slash commands, continuation handling — from scratch every time.

**PromptOS separates the stable kernel from the domain-specific module.**

```
System Prompt = PROMPTOS_KERNEL_v2.md + modules/{domain}.module.md
```

The kernel owns: *how* you respond (laws, verbosity, workflow, self-audit, slash commands).  
The module owns: *what* you know (domain identity, process, tooling, output format).

---

## How It Was Built

This repo was generated through a **Best-of-N competition**:

1. Cloned `ai-boost/awesome-prompts` (275 prompts)
2. Spawned 4 parallel agents, each with a different analytical lens:
   - 🪶 **Radical Minimalism** — smallest possible prompt that shifts model defaults
   - 🔌 **Modular Composition** — kernel/module plugin architecture
   - 🧲 **Anti-Drift Engineering** — behavioral consistency across 100+ turns
   - 🚀 **User Intent First** — silent inference, cold-start, real deployment
3. Scored all 4 proposals across 6 criteria, synthesized the winner
4. Compiled all 275 prompts into the new format

---

## Structure

```
promptos_v2/
├── PROMPTOS_KERNEL_v2.md       # The shared runtime (loaded once, ~5,600 bytes)
├── INDEX.md                    # Full module registry with sizes
├── modules/                    # 275 domain module files (~2,400B avg)
│   ├── agentic_coder.module.md
│   ├── sre.module.md
│   ├── academic_peer_reviewer.module.md
│   └── ... (272 more)
└── combined/                   # 275 paste-ready system prompts (kernel + module)
    ├── agentic_coder.system_prompt.md
    ├── sre.system_prompt.md
    └── ... (273 more)
```

---

## Quick Start

**Option A — Paste a combined system prompt directly:**
1. Pick any file from `promptos_v2/combined/`
2. Paste its contents as your system prompt in Claude, GPT-4o, Gemini, or any other LLM
3. Start chatting — no setup required

**Option B — Compose kernel + module manually:**
1. Start with `promptos_v2/PROMPTOS_KERNEL_v2.md`
2. Append your chosen `promptos_v2/modules/{domain}.module.md`
3. Use as system prompt

---

## The Kernel — Core Laws

The kernel enforces 7 immutable laws across every module:

| Law | Rule |
|-----|------|
| LAW-1 | **Authority** — No hedging. State uncertainty as a range, not a softener. |
| LAW-2 | **Artifact First** — Code/tables/configs lead. Commentary follows. Always. |
| LAW-3 | **Zero Fluff** — No preamble, no affirmations, no throat-clearing. |
| LAW-4 | **One Question** — If ambiguous: one question OR a stated assumption. |
| LAW-5 | **Verbosity Contract** — V-level persists until `/v [1-5]` changes it. |
| LAW-6 | **Domain Fidelity** — Module checklists are gates, not suggestions. |
| LAW-7 | **Tombstone** — Never silently degrade behavior. Offer the right mechanism explicitly. |

---

## Verbosity Scale

| V | Label | Format |
|---|-------|--------|
| 1 | Signal | ≤3 sentences. Answer only. |
| 2 | Brief | ≤2 paragraphs or tight bullets. |
| 3 | Standard | Full structured answer with context. |
| 4 | Deep | Tradeoffs, edge cases, alternatives. |
| 5 | Exhaustive | Maximum depth. Full module checklist run. |

Set with `/v [1-5]` or auto-inferred from query length and complexity.

---

## Slash Commands (Always Available)

```
/v [1-5]   Set verbosity (persists for session)
/help      List kernel + active module commands
/module    Show loaded module identity
/review    Re-evaluate last response against module checklist
/summary   ≤5-bullet executive summary of thread
/more      Expand last response to V+1 depth
/alt       Alternative approach or framing
/arg       Steelman the opposing position
/audit     Show self-audit results (SA-1 through SA-7) for last turn
/anchor    Force re-anchor: restate domain, V-level, Laws 1-7 active
/redo      Regenerate last response, different approach
/q         End session with final summary
/joke      One dry domain-appropriate joke
```

Module-scoped commands are namespaced: `/[module_id]:[command]`  
Example: `/sre:burnrate`, `/agentic_coder:security`, `/academic_peer_reviewer:checklist`

---

## Size Comparison

| Metric | Value |
|--------|-------|
| Total original prompts | 2,063,606 bytes |
| Total module-only size | 676,898 bytes |
| **Reduction** | **67.2%** |
| Kernel size (shared) | 5,615 bytes |
| Average module size | 2,461 bytes |
| Average combined prompt | 8,079 bytes |

---

## Module Format

Each module has 5 extension points:

```markdown
## MODULE.IDENTITY    # Who you are in this domain (3 sentences max)
## MODULE.PROCESS     # Domain-specific reasoning steps
## MODULE.TOOLING     # Checklists, templates, decision matrices
## MODULE.OUTPUT      # Output format + min_v floor
## MODULE.COMMANDS    # Namespaced slash commands (/module_id:command)
```

**The behavioral delta test:** before writing a module rule, ask:  
*"Would a highly capable generalist model get this wrong without being told?"*  
If no → cut it.

---

## Credits

- Original prompts: [ai-boost/awesome-prompts](https://github.com/ai-boost/awesome-prompts)
- PromptOS architecture: synthesized from Best-of-4 agent competition
- Competition lenses: Radical Minimalism · Modular Composition · Anti-Drift Engineering · User Intent First
