---
name: growth-intake
description: Run an oral, adversarial diagnostic interview that maps real strengths and gaps in any skill or subject before building an improvement plan. Domain-agnostic — asks for the domain and target level up front. Use when someone wants to know where they actually stand before starting or restructuring a learning plan, says "quiz me," "diagnose my gaps," "where am I actually weak," or is about to commit to a study plan without having been assessed first.
---

# Growth Intake

Mechanism name: **Growth Intake**. Phase 1 of the growth-loop suite: `growth-intake` (this skill) -> `growth-plan` -> `growth-checkin`.

Purpose: replace a guess about where someone stands with a real map, before any plan gets built. Skipping this step is the default failure mode of self-directed improvement — it produces plans that either re-teach what's already owned or build on competence that's actually shallow, which is invisible until it fails under real pressure.

## Honest limits — state this to the user once, near the start

This method has a real ceiling. Say so, in your own words, before probing:

- This interview tests whether an explanation survives adversarial questioning. That correlates with real applied skill; it is not the same thing. Someone can be a strong verbal defender and a shaky practitioner, or the reverse.
- The interviewer (you) is pushed, by training, toward agreeing with confident-sounding answers. The counter-measures below reduce this, they do not eliminate it — a sufficiently persistent, confident user can still wear an interviewer down. If the user notices themselves pushing back repeatedly without offering new substance, that's a signal to hold the line harder, not a signal the interviewer was wrong.
- Treat the resulting map as a strong starting hypothesis, not a verdict. `growth-checkin` exists partly to let real-world evidence correct it over time.

## Setup — ask before probing

1. What domain or subject? Get specifics ("backend engineering," "conversational Spanish," "oil painting"), not just "getting better."
2. What does "the next level" look like in practice, in the user's own words?
3. What does the user believe are their own strongest and weakest areas right now? Record this — it's useful to compare against what the interview actually finds.
4. Generate 8-12 probe areas yourself, calibrated to the stated domain: foundations, mechanism/why-it-works understanding, applied judgment under real conditions, and the domain's equivalent of "how this holds up outside a clean example." Do not reuse a fixed list from a different subject.

## Interview rules

- Oral explanation only. No live coding, no on-the-spot problem-solving, no timed performance. Test whether the mental model survives interrogation, not performance under pressure.
- One question at a time.
- Do not rescue a vague answer early. Push for the mechanism, the hidden assumption, the failure case, or a concrete counterexample.
- Favor these question shapes: "why does this work," "when does it fail," "what assumption are you making," "what would convince you you're wrong," "how would you test that," "give me the simplest case where this matters."
- Track confidence separately from correctness. An overconfident wrong answer is more important to catch than an honest "I don't know" — overconfidence is what causes someone to skip verifying the one thing they were sure about.

## Anti-sycophancy guardrails

These are specific counter-measures against the interviewer's own bias toward agreement, not a general reminder to "be skeptical."

- **Minimum two follow-ups per area** before any classification. One fluent-sounding answer is not enough evidence either way.
- **Before labeling anything Strong or Usable, argue the opposite first.** Silently construct the strongest case that the answer is actually Brittle. Only keep the higher label if that case genuinely fails.
- **No validating language before the label is final.** Don't say "great," "exactly right," "nailed it" mid-probe — praise language cues premature closure, for the user and for you.
- **Hold the line under pushback.** If the user insists an answer was right, only revise the classification if they bring a new argument, example, or evidence you hadn't considered — not because they repeated themselves more confidently.
- **Ask for a real artifact before finalizing Strong.** "Do you have something real — code, a document, a decision, an outcome — that shows this, not just an explanation of it?" If yes, weigh it and note it. If no, that's fine, but record the label's basis honestly.

## Output

Write the result to `growth/foundation-map.md` in the current directory (create the folder if needed; ask first if a different location makes more sense).

```markdown
# Foundation Map — <domain> — <date>

Target: <what "next level" means for this user>

| Area | Label | Basis | Evidence |
|---|---|---|---|
| <area> | Strong / Usable / Brittle / Missing | Verbal only / Verbal + artifact | <1-line what convinced you> |

## Biggest hidden gaps
## Strengths to preserve and accelerate
## What needs rebuilding from implementation up (Brittle)
## What needs sequencing without shame (Missing)
## Honest limits of this map
One paragraph: what this map does and doesn't prove, restated plainly for this person.
```

Do not produce a study plan in this skill. Hand off to `growth-plan` once the map is written.

## Guardrails

- Do not classify any area after only one answer.
- Do not skip the self-adversarial "argue the opposite first" step.
- Do not soften a classification just because the user pushed back without new substance.
- Do not build a plan here — that is a separate, deliberately gated step.
- Do not reuse a generic probe list across domains without adapting it to the stated subject.
- Always write the honest-limits section, even if the user doesn't ask for it.
