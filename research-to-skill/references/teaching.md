# Teaching the user

Goal: after the build, the user can tell a good output from a bad one and knows where to deepen their knowledge. Teach at the three gates in SKILL.md only. Brief by default; depth on request.

## Non-obvious facts (the most valuable teaching)
A non-obvious fact is something the design depends on that a non-expert in the domain likely doesn't know. Typical kinds:
- platform or format constraints (a feature only exists via a specific file type or upload path)
- legal, safety or age limits
- conventions of the field ("practitioners always do X first")
- numbers that set the design (lengths, sizes, frequencies)
- common beliefs that are wrong

Rule: if removing the fact would change the design, and the user's brief didn't mention it, flag it. Format, one line each:
`Did you know: <fact> · why it matters for the skill: <effect> · source: <name> (verified / from knowledge)`
Max. 5 per research document. If you have more, keep the ones that change the design most.

## Why-lines (design section of the research document)
For each design decision, one line: `<decision> — because <reason>; without it <what breaks>`.
Skip why-lines for things that are obvious from the brief. A why-line the user can't disagree with is noise.

## Reviewer card (human-in-the-loop)
5–7 yes/no checks, derived from the expert profile's quality criteria. Only include what the human can judge better than the AI:
- domain correctness (would an expert sign this?)
- fit to the user's real context, audience and constraints
- edge cases and inputs the skill will meet in practice
- tone and voice
- the cost of an error (what happens if this output is wrong, and who notices)
Each check: question · what "no" looks like · what to do if "no" (fix the input, correct the output, or record a lesson).
Use yes/no, not 1–5 scales: binary checks force a decision and are easier to act on.
Tell the user: read several real outputs and write down every failure in plain words before inventing new rules — patterns appear after 5–10 outputs.

## Where to learn more
Two layers, max. 3 sources each, each with type, label and what to look for there.

**Domain layer** — search at runtime, never hardcode in a shared skill. Prefer, in order: official documentation or standards → practitioners (talks, case studies, newsletters) → community (forums, subreddits, Discords) for niche tips and failure stories. Label verified / from knowledge.

**Meta layer (skill authoring)** — stable, may be offered as is (verify before quoting specifics):
Status labels: "listed" = found in search results on 2026-11-09, page not opened; "unchecked" = from knowledge. Re-verify before the user relies on one.
- Anthropic docs: Agent Skills best practices (platform.claude.com, Agent Skills section) — official rules for structure, description, progressive disclosure. [listed]
- Anthropic Engineering blog post on Agent Skills — the design rationale: start from evaluation, iterate from real use. [unchecked]
- Practitioner write-ups on skill pitfalls (e.g. smcleod.net, "Writing and Reviewing Agent Skills – Common Pitfalls") — trigger evals, scripts vs. instructions, cutting lines. [listed]
- Hamel Husain's work on LLM evals (hamel.dev, posts on error analysis) — error analysis on real outputs, binary pass/fail, one domain expert as the judge. [listed; the pass/fail and domain-expert points unchecked]
- Community: the Anthropic skills repository on GitHub (github.com/anthropics/skills, examples) [listed]; r/ClaudeAI and the Anthropic Discord (niche tips) [unchecked, treat as unverified].

## Depth levels
- Brief (default): gates only, one line per item.
- Deeper (on request): add a sentence of reasoning per why-line and a "how an expert would check this" note per reviewer-card item.
