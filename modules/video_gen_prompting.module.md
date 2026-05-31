# ── PROMPTOS MODULE: video_gen_prompting ─────────────────────────────────────────────
# Version: 1.0
# Kernel compatibility: PromptOS v2.0+
# Source: awesome-prompts/video_gen_prompting.txt
# ─────────────────────────────────────────────────────────────────────────────

## MODULE.IDENTITY
AI Video Generation Prompt Guide & Templates

## MODULE.PROCESS
1. Paint foreground with motion vector left (-3)
2. Paint background with vector right (+1)
3. Reinforce in text: "Camera trucking right, foreground moves past quickly"
- [Beat 1: specific action with count or timing]
- [Beat 2: distinct next beat]
- [Beat 3: resolution or reaction]
1. Generate audio in Suno or ElevenLabs
2. Export beat timestamps

## MODULE.TOOLING
**Checklist:**
- [Beat 1: specific action with count or timing]
- [Beat 2: distinct next beat]
- [Beat 3: resolution or reaction]

## MODULE.OUTPUT
min_v: 4

structured data and reference images
  Sora 2          → physics simulator; models cause, effect, and inertia

------------------------------------------------------------------
UNIVERSAL PROMPT STRUCTURE (works across all models):

[STYLE INTENT] — cinematic short film | documentary | commercial | music video
[SHOT TYPE + FRAMING] — wide establishing shot | medium close-up | aerial
[CAMERA MOVEMENT] — slow dolly-in | handheld ENG | crane boom up | static
[SUBJECT + ACTION] — described in beats/counts, not vague adjectives
[ENVIRONMENT] — foreground, midground, background, weather
[LIGHTING] —

## MODULE.COMMANDS
/video_gen_prompting:checklist — Run domain checklist against last response
/video_gen_prompting:deep — Expand current topic to V=5 exhaustive treatment

# ── END MODULE ────────────────────────────────────────────────────────────────
