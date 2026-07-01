---
name: growth-checkin
description: Lightweight periodic check on whether a growth plan is still working — real evidence vs. drift — and whether it's actually time for a full growth-intake re-run. Use for a periodic "am I actually improving or just consuming" gut check, when someone asks if their plan needs updating, or when it's been a while since the last diagnostic.
---

# Growth Check-in

Mechanism name: **Growth Check-in**. Phase 3 of the growth-loop suite: `growth-intake` -> `growth-plan` -> `growth-checkin` (this skill), then loops back to whichever phase the verdict points to.

Purpose: the frequent, cheap counterpart to `growth-intake`. Most of the value of a diagnostic-first system is lost if the diagnostic only ever runs once — plans go stale, evidence gets ignored, and tooling/planning quietly substitutes for the actual skill. This skill exists so re-assessment is a habit, not a mega-event.

## Read first

- `growth/foundation-map.md`
- `growth/plan.md`
- `growth/log.md` if it exists (append-only history of past check-ins; create it if missing)

If none of these exist, say so and suggest starting with `growth-intake` instead of running a check-in on nothing.

## Protocol

1. **Orient**: what's the current plan section, what was the last logged action.
2. **Evidence check**: what real output was produced since the last check-in — a real artifact, a decision, an outcome, a defended explanation? Time spent, lectures watched, and tools configured are not evidence.
3. **Drift check**: is effort going into the actual skill, or into planning/tooling/consuming around the skill? Name it plainly if it's the latter.
4. **Reality check**: has anything from real work — not this chat — confirmed or contradicted the foundation map? A "Brittle" area that just performed fine in real use, or a "Strong" area that just failed, are both important signals and should feed back into the map.
5. **Staleness check** — decide whether to escalate to a full `growth-intake` re-run. Escalate only if at least one is true:
   - Roughly 6+ months since the last full intake, or
   - The goal, domain, or target level has materially changed, or
   - Two or more consecutive check-ins show the map's labels no longer match reality.

   If none apply, stay lightweight. Do not let a check-in quietly turn into a second full interview — that defeats the point of having a cheap, frequent option.

## Output

Append to `growth/log.md` and report:

```markdown
## Check-in — <date>
**Verdict:** Aligned — keep going / Drifting — correct / Stale — recommend full growth-intake re-run
**Evidence:** 2-4 bullets, grounded in real output, not effort
**Reality check:** did anything in real work confirm or contradict the map?
**Next atomic action:** exactly one
```

## Guardrails

- Do not count planning, tooling, or consumption time as progress.
- Do not escalate to a full re-intake unless a real trigger condition is met — most check-ins should stay short.
- Do not patch a plan that's actually wrong here; if the plan itself is off, route back to `growth-plan`, don't ad-hoc fix it mid-check-in.
- Keep the whole check-in short — a few minutes, not a session.
- Always ask the reality-check question; it's the only place real-world evidence re-enters the loop.
