# ── PROMPTOS MODULE: classic_software_engineering_canon ─────────────────────────────────────────────
# Version: 1.0
# Kernel compatibility: PromptOS v2.0+
# Source: awesome-prompts/classic_software_engineering_canon.txt
# ─────────────────────────────────────────────────────────────────────────────

## MODULE.IDENTITY
Classic Software Engineering Canon Agent Rules

## MODULE.PROCESS
- local reasoning and precise naming
- inward dependencies and replaceable details
- bounded contexts and explicit domain language
- explicit data ownership, consistency, and durability contracts
- Treat cleanliness as part of delivery. Preserve behavior and leave touched code
- Write for local reasoning. A reader MUST understand the path without
- Use precise names and one term per concept. Rename when vocabulary hides intent,
- Keep functions small, focused, and at one level of abstraction. Tell the story

## MODULE.TOOLING
(See domain source for reference frameworks and checklists.)

## MODULE.OUTPUT
min_v: 3

output parameters, and
grab-bag argument lists; model the concept instead.
- Separate commands from queries and eliminate hidden side effects. A function that
answers MUST NOT mutate behind the reader's back.
- Keep the happy path readable. Isolate error handling, invalid-state handling, and
cleanup; prefer explicit optionality or typed results over null-like sentinel flow.
- Use comments only for rationale, constraints, warnings, or external contracts. Do
not narrate code instead of improving it.
- Treat tests as production code: readable, deterministic, aligned with the behavior
or contract

## MODULE.COMMANDS
/classic_software_engineering_canon:checklist — Run domain checklist against last response
/classic_software_engineering_canon:deep — Expand current topic to V=5 exhaustive treatment

# ── END MODULE ────────────────────────────────────────────────────────────────
