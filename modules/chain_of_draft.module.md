# ── PROMPTOS MODULE: chain_of_draft ─────────────────────────────────────────────
# Version: 1.0
# Kernel compatibility: PromptOS v2.0+
# Source: awesome-prompts/chain_of_draft.txt
# ─────────────────────────────────────────────────────────────────────────────

## MODULE.IDENTITY
Chain of Draft (CoD) Prompting Technique

## MODULE.PROCESS
- Best for: math word problems, logical reasoning, multi-step calculations
- Not ideal for: creative writing, open-ended generation, tasks requiring explanation
- Works with: GPT-4, Claude 3+, Gemini 1.5+
- Token savings: ~92% vs standard CoT; latency: up to 76% lower
- Accuracy tradeoff: ~4% below CoT on math benchmarks — acceptable for most real-world use

## MODULE.TOOLING
(See domain source for reference frameworks and checklists.)

## MODULE.OUTPUT
min_v: 2

formation. Do not explain; just note what you are doing.

After all steps, write #### on its own line, then give the final answer.

Example format:
Step 1: [≤5 words]
Step 2: [≤5 words]
Step 3: [≤5 words]

## MODULE.COMMANDS
/chain_of_draft:checklist — Run domain checklist against last response
/chain_of_draft:deep — Expand current topic to V=5 exhaustive treatment

# ── END MODULE ────────────────────────────────────────────────────────────────
