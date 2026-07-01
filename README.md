# Growth Loop

A 3-step system for getting better at anything, on purpose: **diagnose where you actually stand -> build a plan the diagnosis actually justifies -> check in periodically so the plan doesn't go stale.**

Domain-agnostic. Built by generalizing a diagnostic-first ML self-study system; nothing about the mechanism is ML- or software-specific.

## Why this exists

Most self-improvement plans are a guess about where someone stands. The guess fails in one of two directions: re-teaching things already known (wastes time, kills motivation), or building on confidence that's actually shallow (invisible until it fails under real pressure). This fixes that by running a real diagnostic first, and refusing to build a plan until it exists.

## What's in here

- `skills/growth-intake/` — an oral, adversarial interview that produces a real map (Strong / Usable / Brittle / Missing) of where someone stands in any subject, before any plan gets built.
- `skills/growth-plan/` — turns that map into a plan: compress what's strong, drill what's usable, rebuild what's brittle (build small -> explain -> then read the theory), sequence what's missing.
- `skills/growth-checkin/` — a fast, periodic check on whether the plan is producing real evidence or just busywork, and whether it's time to re-run the diagnostic.
- `PORTABLE-PROMPT.md` — the same 3 steps as plain prompts, for anyone without Claude Code.

## Install (Claude Code)

Copy each folder under `skills/` into `~/.claude/skills/` (applies everywhere) or a project's `.claude/skills/` (applies to that project only). Then use `/growth-intake`, `/growth-plan`, `/growth-checkin` in order. State is kept in a `growth/` folder wherever you run them (`growth/foundation-map.md`, `growth/plan.md`, `growth/log.md`).

## No Claude Code? Use `PORTABLE-PROMPT.md`

Same mechanism, no install — copy-paste prompts into any AI chat. You carry the state yourself (save each output somewhere) instead of it living in a file.

## Read before you trust this — and before you hand it to anyone else

This method has real limits. Whoever uses this should know them, not just the person who built it:

1. **The interviewer is fighting its own training.** AI models are trained to be agreeable. `growth-intake` has explicit counter-instructions — forced follow-ups before any label, arguing the opposite before classifying something "Strong," no praise before the verdict, holding the line under pushback without new evidence. These measurably reduce premature agreement. They do not eliminate it. A confident, persistent person can still talk the interviewer into a softer verdict than they've earned — if you notice that happening, it's a sign you broke the exercise, not a sign you were right.
2. **A conversation is not a performance sample.** The intake tests whether an explanation survives adversarial questioning. That correlates with real applied skill; it is not the same thing. Someone can out-explain their actual ability, or under-explain a real ability they have (nerves, language, being a poor narrator of their own competence). The skill asks for real artifacts where they exist, but it can't manufacture outside evidence a conversation doesn't have access to. Treat the resulting map as a strong hypothesis, and let `growth-checkin`'s reality-check step correct it against real-world results over time.
3. **Cadence is the one caveat this fully solves.** Splitting Diagnose (rare) from Check-in (frequent), with explicit escalation triggers (roughly 6+ months, a changed goal, or repeated mismatch between the map and reality), removes the "one giant re-assessment or nothing" failure mode. No meaningful gap left here.
4. **Not everyone has Claude Code.** If someone you're sending this to doesn't, the `skills/` folders do nothing for them — send `PORTABLE-PROMPT.md` instead, or alongside.

Points 1 and 2 are mitigations, not fixes. Say so out loud to anyone you hand this to, the same way it's said here.
