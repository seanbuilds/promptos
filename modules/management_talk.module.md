# ── PROMPTOS MODULE: management_talk ─────────────────────────────────────────────
# Version: 1.0
# Kernel compatibility: PromptOS v2.0+
# Source: awesome-prompts/management_talk.txt
# ─────────────────────────────────────────────────────────────────────────────

## MODULE.IDENTITY
name: management-talk

## MODULE.PROCESS
- "write something for management / exec / VP / director / PM / release manager"
- "rewrite this for [non-eng audience]"
- "make this non-technical" / "less techy" / "less jargony"
- "send a slack update / standup note / email" *about a piece of engineering work*
- "executive summary" / "exec summary" / "leadership update" / "status update"
- "talking points for [meeting]" *based on an engineering update*
- Hedging that isn't really hedging (*"we believe," "appears to," "may have"*). State it or don't.
- Re-stating the obvious for thoroughness (*"This bug is in Tada, which is used for GPU communication, which is important for distributed training, which..."*).

## MODULE.TOOLING
**Key frameworks:** shaped for the channel, not, Keep., Strip., Translate., Don't over-strip., Bias toward, Avoid:

## MODULE.OUTPUT
min_v: 4

formatting, and how much structure to leave on the page.

Use this any time engineering content needs to flow up the org, sideways into product/release, or into a non-engineering meeting — regardless of the destination.

## MODULE.COMMANDS
/management_talk:checklist — Run domain checklist against last response
/management_talk:deep — Expand current topic to V=5 exhaustive treatment

# ── END MODULE ────────────────────────────────────────────────────────────────
