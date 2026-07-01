# Growth Loop — portable version (no Claude Code required)

Same 3-step system as the `skills/` folder, as plain prompts you can paste into any AI chat — Claude, ChatGPT, whatever you use. No installation.

Use them in order: **Diagnose -> Plan -> Check-in.** Since a normal chat doesn't remember between sessions, save each output somewhere you'll find it again — a doc, a notes app, anything.

## Read this first

This method has real limits. Know them before you run it:

1. **The AI you're talking to is trained to agree with you.** The Diagnose prompt below has explicit instructions fighting that (forced follow-ups, arguing the opposite before it labels anything, no praise before a verdict, holding the line under pushback). Those instructions reduce the problem. They do not remove it. If you push back hard enough, most models will eventually soften their verdict — that's a sign you broke the exercise, not a sign you were right.
2. **A conversation is not a performance sample.** This tests whether your explanation survives being questioned, which is correlated with real skill but isn't the same thing. Some people out-explain their actual ability; some people (nervous, not narrating themselves well) under-explain a real ability they have. Treat the result as a strong hypothesis, not a verdict — real-world evidence over time (the Check-in step) is what actually corrects it.
3. **Cadence is the one thing this fully solves.** Run Diagnose rarely (roughly every 6 months, or when your goal changes) and Check-in often (every few weeks). Don't let a check-in balloon into a second full interview — if you notice that happening, stop and just note it, don't let the "quick check" eat an hour.

---

## 1. Diagnose

Run this first, and roughly every 6 months after that (or sooner if your goal changes).

```text
You are interviewing me before I build a self-improvement plan for [DOMAIN — be specific, e.g. "backend engineering," "conversational Spanish," "oil painting"]. My target: [WHAT THE NEXT LEVEL LOOKS LIKE TO YOU].

First, tell me plainly: this interview tests whether my explanations survive adversarial questioning, which correlates with real skill but isn't identical to it. You are also trained to be agreeable, which works against good diagnosis — so you're going to fight that on purpose, and I should expect this to feel harder than a normal chat.

Diagnose my foundations through oral explanation only. Do not ask me to write code, solve a problem live, or perform under time pressure. Ask me to explain why things work, when they fail, what assumptions are hiding, and how I'd test a claim.

Rules for you:
- One question at a time.
- Don't rescue a vague answer early — push for the mechanism, the hidden assumption, or a counterexample.
- Track my confidence separately from correctness — an overconfident wrong answer matters more than an honest gap.
- Minimum two follow-ups per topic before you classify anything.
- Before you label anything "Strong" or "Usable," silently argue the opposite first — build the strongest case that it's actually "Brittle" — and only keep the higher label if that case fails.
- Don't say "great" / "exactly right" / "nailed it" before your verdict is final.
- If I push back on a classification, only change it if I give you a new argument or evidence — not if I just repeat myself more confidently.
- Before you finalize a "Strong" label, ask me if I have something real (code, a document, a decision, an outcome) that shows it, not just an explanation — note whether the label rests on that or on the conversation alone.

Start with quick calibration, one question at a time:
1. What do I think my strongest and weakest areas are right now?
2. What does "the next level" mean for me in concrete terms?
3. What do I want this expertise to compound into?

Then generate 8-12 probe areas yourself, calibrated to my stated domain — covering foundations, why-it-works mechanism understanding, judgment under real conditions, and how this holds up outside a clean textbook example. Probe each one until you can classify it as Strong / Usable / Brittle / Missing.

At the end, give me:
- A table: Area | Label | Basis (verbal only / verbal + artifact) | what convinced you
- Biggest hidden gaps
- Strengths to preserve and accelerate
- What needs rebuilding from implementation up (Brittle)
- What needs sequencing without shame (Missing)
- One paragraph, plainly stated: what this map does and doesn't actually prove

Do not propose a plan yet. Start with calibration question 1.
```

Save the full output. You'll paste the table into the next prompt.

---

## 2. Plan

Run this right after Diagnose, with that output pasted in.

```text
Here is my foundation map from a diagnostic interview: [PASTE THE FULL OUTPUT FROM STEP 1]

Turn this into a plan, using this rule for each area:
- Strong -> compress into review, application, or teaching it to someone else. Do not re-teach it from scratch.
- Usable -> targeted drills aimed at the specific edge cases and gaps the interview surfaced, not general practice.
- Brittle -> rebuild it. Don't just assign review — review reproduces the same fluent-sounding-but-collapsing result. Use this loop: (1) build or produce the smallest real, ugly version of the thing, (2) explain it back — what each part does, what would break it, what I assumed, (3) only then bring in the formal/theoretical explanation to reconcile what I got right or wrong. If this domain isn't "buildable," substitute "one small real attempt under real conditions" for "build."
- Missing -> sequence real prerequisites in order. No shame framing, no skipping ahead.

For every module, name one real, visible output I'd be willing to show someone else — not a completion checkbox. If you can't name that output, the module isn't specific enough yet — sharpen it.

End with exactly one next atomic action: something I could start today, not a phase or a week's worth of work.
```

Save this too — it's your plan and your next action.

---

## 3. Check-in

Run this every few weeks. Keep it short — a few minutes, not a full session.

```text
Quick check-in on my growth plan. Here's my last plan/notes: [PASTE YOUR PLAN AND/OR LAST CHECK-IN NOTES]. Here's what I actually did since then: [DESCRIBE IT].

Answer honestly:
1. What real evidence did I produce — an artifact, a decision, an outcome, a defended explanation? (Time spent, lectures watched, and tools set up don't count as evidence.)
2. Is my effort going into the actual skill, or into planning/tooling/consuming around the skill? Tell me plainly if it's the latter.
3. Has anything from real work (not this chat) confirmed or contradicted my foundation map? If a "Brittle" area just performed fine, or a "Strong" area just failed, say so.
4. Should I re-run the full Diagnose interview? Only say yes if: it's been roughly 6+ months since the last one, my goal has materially changed, or this is the second check-in in a row where the map doesn't match reality. Otherwise, tell me to stay the course.

End with a verdict — Aligned / Drifting / Stale — and exactly one next atomic action.
```
