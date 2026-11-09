# Choosing the tool: skill, Project, artifact, app, or prompt?

Give a verdict based on the dominant signals. Combinations are common.

| Tool | Best when | Signals | Not when |
|---|---|---|---|
| **Prompt** (saved text) | the task is rare or changes every time; the workflow isn't settled yet | "let me try", first attempt, 1–2 uses | it repeats and needs the same steps and checkpoints |
| **Skill** | a repeated workflow with stable steps, knowledge and output format; must work in any chat; will be shared | "every time I…", output template, checklist, domain know-how | it's mainly the standing context of one project or large documents |
| **Project** | long-running work over the same materials (documents, team/client context), many related conversations | "everything for project X", uploaded materials, shared memory | the workflow must also work outside this context |
| **Artifact** (published page, tool, dashboard) | the result is used repeatedly and interactively – calculator, tracker, form, generator; or shared by link | "click", "fill in", "display", "share a link" | AI judgement is needed on a new input every time |
| **App** (custom build, vibe-coding) | accounts, database, integrations, many users, mobile access, or running without Claude | "users log in", "payments", "runs on its own" | an artifact or skill would do – an app is an order of magnitude more work |

## Deciding questions
1. Will AI apply judgement (→ skill/prompt), or will a person click through it (→ artifact/app)?
2. Is the context stable and large (→ Project), or does it arrive with each request (→ skill)?
3. Does it repeat at least 3× with stable steps (→ skill), or is it a first attempt (→ prompt, convert after 2–3 uses)?
4. Must it work without Claude or for many people at once (→ app)?

Common combinations: skill + Project (skill carries the workflow, Project the materials); a skill whose output is an artifact; a prompt as the prototype of a skill.
State in the verdict what the user would gain and lose by choosing a different tool.
