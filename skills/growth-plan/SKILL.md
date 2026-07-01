---
name: growth-plan
description: Turn a growth-intake foundation map into a phased improvement plan — compress what's strong, drill what's usable, rebuild what's brittle through build-then-explain-then-formalize, sequence what's missing without shame. Use after growth-intake has produced a foundation map, or when someone already has a self-assessment and wants it turned into an actual plan rather than a list of topics.
---

# Growth Plan

Mechanism name: **Growth Plan**. Phase 2 of the growth-loop suite: `growth-intake` -> `growth-plan` (this skill) -> `growth-checkin`.

Purpose: turn a foundation map into a plan whose shape is determined by the map, not by a generic curriculum. The same topic list produces a different plan depending on whether an area is Strong, Usable, Brittle, or Missing — treating them the same way wastes the diagnostic.

## Read first

Look for `growth/foundation-map.md` in the current directory. If it doesn't exist, say so and offer to run `growth-intake` first — do not invent a plan from an unstated self-assessment. A plan built without a real map is exactly the guess this suite exists to replace.

## Restructuring rule

For each area in the map:

- **Strong** -> compress into review, application, or teaching it to someone else. Do not re-teach it from scratch — that wastes time and signals the plan didn't actually use the map.
- **Usable** -> targeted drills aimed specifically at the edge cases and formal gaps the interview surfaced, not general practice.
- **Brittle** -> rebuild via the loop below. Review alone does not fix Brittle — the diagnostic finding was "sounds fluent, collapses under pressure," and re-reading the same material reproduces the same fluent-sounding-but-collapsing result.
- **Missing** -> sequence real prerequisites in order. No shame framing, no speed-running past a gap to look further along than the map supports.

## The build -> explain -> formalize loop (for Brittle and Missing areas)

1. Build or produce the smallest real, ugly version of the thing — code, a draft, a decision under simulated constraints, a rehearsed conversation, whatever "doing it badly in miniature" means in this domain.
2. Explain it back: what does each important part do, what would break it, what did you assume.
3. Only then bring in the formal/theoretical treatment (a text, a lecture, an expert explanation) to reconcile what the small build got right or wrong.

If the domain genuinely isn't "buildable" (a purely interpersonal or physical skill, say), substitute "produce one small real attempt under real conditions" for "build," and keep the explain-then-formalize order the same.

## Artifact standard

Every module in the plan should point at one real, visible output the person would be willing to show another person — not a completion checkbox, not "watched the lectures." If a module can't name that output, it isn't specific enough yet; sharpen it before adding it to the plan.

## Output

Write to `growth/plan.md`:

```markdown
# Growth Plan — <domain> — <date>
Built from: growth/foundation-map.md (<date of that map>)

## Compress (Strong)
## Drill (Usable)
## Rebuild (Brittle) — via build -> explain -> formalize
## Sequence (Missing)

## Next atomic action
One concrete, startable-today action. Not a phase, not a week — one session's worth.
```

Always end by handing back exactly **one** next atomic action, not a syllabus. A plan someone can't start today is a plan that will sit unused.

## Guardrails

- Refuse to build a plan with no foundation map present; redirect to `growth-intake` instead of guessing.
- Never assign a review-only fix to a Brittle area.
- Never output more than one next atomic action at a time.
- Keep each plan section to a few lines; if a section is ballooning, the map probably wasn't specific enough — that's a sign to revisit `growth-intake`, not to write more plan.
