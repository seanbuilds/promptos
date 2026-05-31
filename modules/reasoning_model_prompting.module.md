# ── PROMPTOS MODULE: reasoning_model_prompting ─────────────────────────────────────────────
# Version: 1.0
# Kernel compatibility: PromptOS v2.0+
# Source: awesome-prompts/reasoning_model_prompting.txt
# ─────────────────────────────────────────────────────────────────────────────

## MODULE.IDENTITY
Reasoning / Extended Thinking Model Prompting Guide & Templates

## MODULE.PROCESS
- They self-plan. You do not need to tell them how to think.
- Explicit CoT instructions ("think step by step") interfere with their
- They excel on 5+ step problems. They are overkill for simple queries.
- They are slower and more expensive per token. Use them when it matters.
- Few-shot examples often hurt rather than help (they constrain the
- State the goal clearly and completely
- Provide all relevant context upfront (long context at TOP of prompt)
- Use XML tags or markdown sections to separate distinct inputs

## MODULE.TOOLING
**Checklist:**
- [Criterion 1]
- [Criterion 2]

## MODULE.OUTPUT
min_v: 4

output format constraints (what the final answer should look like)
  - Use "think thoroughly" or "reason carefully" over prescribed plans
  - For Claude: control depth via the effort parameter (low / medium / high / max)
  - For o3/o4: use developer messages to set role + boundaries + tool rules
  - Ask for self-verification: "Before finalizing, verify your answer against [criteria]"
  - Break multi-shot problems into well-defined sub-tasks

DON'T:
  - "Think step by step" — redundant, often harmful
  - "Let's think about this carefully before answering" — same problem
  - "First do X, then do

## MODULE.COMMANDS
/reasoning_model_prompting:checklist — Run domain checklist against last response
/reasoning_model_prompting:deep — Expand current topic to V=5 exhaustive treatment

# ── END MODULE ────────────────────────────────────────────────────────────────
