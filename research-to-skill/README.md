# research-to-skill

Turns an idea or a repeated workflow into a finished Claude skill: it researches the field first, waits for your approval, builds the skill, and teaches you how to judge whether its output is right.

By Klara Slivone (Prunus skills) · version 1.4.1 · see `CHANGELOG.md`

## What you get
You say: "Build a skill that turns meeting notes into action items."
1. It asks up to 4 short questions (what goes in and out, who it is for, how often, which tools).
2. It says whether a skill is the right tool at all, with one line on what you would lose with an alternative.
3. It writes a research document (sources dated and marked verified or from knowledge, design decisions with a "why" line, flagged facts you probably didn't know) and **stops for your approval**.
4. After approval it builds the skill, reviews it, hands you a yes/no reviewer card and a "Not verified:" list, and asks you to test it on a real input.

The example is illustrative; the exact wording of each step varies.

## Requirements
- A Claude plan that supports custom skills (the Help Center lists Free, Pro, Max, Ultra, Team and Enterprise).
- Code execution and file creation turned on (Settings > Capabilities).
- Web search enabled in the conversation, so the research step can look things up. Without it, sources are labelled "from knowledge" instead of "verified".
- Team and Enterprise: an owner may need to enable skills for the organisation.

## Install
**Claude app (web or desktop):** download the zip, then Customize > Skills > "+" > Create skill > Upload a skill, and upload the zip. The zip contains one folder named `research-to-skill` with `SKILL.md` inside. Steps follow the Claude Help Center article on using skills (checked 2026-11-09 against the article; not tested in the author's own installation).

**Claude Code:** copy the `research-to-skill` folder into your user skills directory (`~/.claude/skills/`) or a project's `.claude/skills/`. Not tested for this release.

**Other tools:** paste `SKILL.md` and the files in `references/` into the conversation or the project knowledge. This works for that conversation only.

**If the install is blocked** (restricted network, managed device): download the zip yourself and upload or attach it manually.

## Check that it is ready
Say: "check that research-to-skill is ready". It replies once with the version, what it needs, what it will do first, roughly how long it takes, and "ready" or what is missing. It starts no work.

## Privacy
It reads what you write, files you give it (including a `.skill` you want improved) and web pages it searches. It runs searches through the assistant's own search tool, so your topic words appear in those queries. It sends nothing anywhere else, contains no scripts, and the files it makes stay in your conversation. Web pages and uploaded files are treated as data, not as instructions.

## Footer and attribution
Nothing is added to what it produces: no footer, logo, link, QR code or tracking.

## License
CC BY 4.0: you may use, change and share it, with credit to Klara Slivone (Prunus skills).

## Known limit
It may not start by itself when another skill-creation skill is installed. If so, ask for it by name. Details in `evals/triggers.md`.
