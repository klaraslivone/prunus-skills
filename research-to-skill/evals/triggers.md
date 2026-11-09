# Trigger evals

Purpose: check that the description makes the skill start when it should and stay out of the way when it shouldn't. Machine-readable copy: `triggers.json`.

## Should trigger
1. "I write the same weekly status report every Friday and it always follows the same steps. Can you turn this workflow into a skill so I can reuse it?"
2. "Udělej skill, který z přepisu schůzky vytáhne úkoly a rozdělí je podle jednotlivých lidí."
3. "Build a skill for reviewing supplier contracts against our standard checklist."
4. "My onboarding-checklist skill triggers too rarely and its output is thin. Can you improve this skill? The folder is ./skills/onboarding with SKILL.md and a references folder."
5. "Postav skill na přípravu podkladů pro obchodní schůzky. Nejdřív zjisti, jak to dělají profesionálové."
6. "I want to design a skill that helps parents simplify the rules of board games for small kids. Where do we start?"

## Should not trigger
1. "Use the pdf skill to merge these two PDF files into one."
2. "Which of my installed skills should I use for editing a Word document?"
3. "Write a Python script that renames all files in a folder by their creation date."
4. "Summarize this research paper on spaced repetition and tell me the three main findings."
5. "Napiš mi prompt, který mi pomůže psát příspěvky na LinkedIn v mém stylu."
6. "My script that syncs the skills folder to a backup drive throws a KeyError on line 42. Can you fix the bug?"

## Result (run before release of 1.4)
Method: `claude -p` per prompt, 2 runs each, using the skill-creator trigger-eval script, in an environment where other skills were installed, including a generic skill-creation skill.

| Description | Passed | Should-trigger prompts that triggered | False triggers |
|---|---|---|---|
| Version 1.3 (long "ALWAYS use when…") | 6/12 | 0 of 6 | 0 of 6 |
| Version 1.4 (shipped) | 7/12 | 1 of 6 (one run of two) | 0 of 6 |

Reading: the skill does not interfere with unrelated requests, but it **rarely starts on its own** in this setup. In a sampled run of prompt 3, the assistant chose a generic skill-creation skill instead. A control skill with a deliberately obvious description did trigger, so the measuring tool works. The difference between the two descriptions is within noise (2 runs per prompt).

Not known: how it behaves on a clean installation without a competing skill-creation skill. If it does not start, name it directly ("use research-to-skill") or ask for it by name.

To re-run: use the trigger-eval script from the skill-creator skill with `triggers.json`.
