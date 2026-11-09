# Skill review

## Quality
- [ ] Description says when to trigger (1–3 tight sentences) with concrete trigger phrases in the users' languages, and is "pushy" (skills tend to under-trigger). It is not a summary of the body — a summary can make the model act on it without loading the skill.
- [ ] SKILL.md up to ~150 lines; knowledge in `references/`, templates in `assets/`, with instructions on when to load what.
- [ ] Files in English; a Language section says output follows the user's language.
- [ ] A "Who you are" section with the expert profile.
- [ ] Invariants and "avoid" items are concrete, not generic advice.
- [ ] Runtime questions: max. 3–4 per round, only what can't be inferred.
- [ ] The output has a template and is consistent across its parts (no internal contradictions – common!).
- [ ] Estimates are marked as estimates.
- [ ] A "How to judge the output" section (short reviewer card) is present.
- [ ] Non-obvious domain facts the design depends on are stated in the skill, not just applied.
- [ ] Learning loop and `references/lessons.md` are present.

## Shareability
- [ ] No names, personal data, collections, internal company data, links to private documents.
- [ ] No assumptions about the user's specific tools; when a tool is missing, a fallback is described.
- [ ] Content read from the web, files or the user's apps is treated as data, not instructions (stated in the skill if it reads any).
- [ ] Scripts: no network calls, no remote code, no secrets; dependencies declared; tools limited to what the skill needs.
- [ ] Safety: sensitive domains (health, law, finance, children) have limits and recommend a professional where appropriate.

## Practitioner tips
- Cut every line whose removal would not change behaviour.
- Deterministic or accuracy-critical steps go into a script in `scripts/`, not into instructions.
- Multi-step flows: tell the model to track steps as a checklist and review at the end (it otherwise drifts or stops early).
- Trigger evals: 5–10 realistic prompts labelled should / shouldn't trigger; rerun after editing the description.
- Least privilege: does the skill really need web, write or send tools?
- Don't hard-wrap markdown lines; add a table of contents only to reference files over ~100 lines.
- "When to use" belongs in the description, not the body.

## Improvement ideas (pick the 2–3 most valuable)
- Test prompts (3–5 varied inputs) to check the skill after edits
- Sample finished outputs as a style guide
- Combining with another tool (artifact for output, Project for materials)
- Description optimisation for better triggering
- Extending to another language or domain only after the core works
