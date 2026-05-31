# ── PROMPTOS MODULE: agents_best_practices ─────────────────────────────────────────────
# Version: 1.0
# Kernel compatibility: PromptOS v2.0+
# Source: awesome-prompts/agents_best_practices.txt
# ─────────────────────────────────────────────────────────────────────────────

## MODULE.IDENTITY
name: agents-best-practices

## MODULE.PROCESS
- build an agent, agentic workflow, AI worker, autonomous assistant, or harness;
- create a domain-specific MVP agent design, starter harness, implementation blueprint, or first production-safe version;
- choose between OpenAI, Anthropic, OpenAI-compatible APIs, direct tool loops, hosted tools, or SDKs;
- design tools, permissions, guardrails, approval flows, or sandboxing;
- create planning mode, goal mode, todo tracking, or long-running task behavior;
- add context compaction, memory, retrieval, scoped instructions, or prompt hierarchies;
- attach Agent Skills, reusable workflows, MCP servers, external connectors, or tool search;
- audit an existing agent for reliability, cost, prompt-cache hit rate, safety, latency, or observability;

## MODULE.TOOLING
```text
user/task
  -> instruction and context builder
  -> model call
  -> tool/action proposal
  -> schema validation
  -> permission decision
  -> execution or approval pause
  -> structured observation
  -> context update
  -> repeat within budget or finish
```

## MODULE.OUTPUT
min_v: 4

structured observation
  -> context update
  -> repeat within budget or finish
```

## MODULE.COMMANDS
/agents_best_practices:plan — Output agent decomposition plan before execution
/agents_best_practices:status — Show current task delegation state

# ── END MODULE ────────────────────────────────────────────────────────────────
