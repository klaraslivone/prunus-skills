# Prunus skills

Shareable Claude skills by Klara Slivone. Every skill lives in its own folder. Every release carries a ZIP that is ready to upload into Claude.

## Skills

| Skill | What it does | Version | Download |
|---|---|---|---|
| [research-to-skill](research-to-skill/) | Builds a new Claude skill: researches the field first, waits for your approval, then builds it, and teaches you how to judge the result. | 1.4.1 | Releases > `research-to-skill-v1.4.1` > file `research-to-skill.zip` |

## Install (Claude app, web or desktop)

1. Open **Releases** (right-hand column on this page) and pick the newest release of the skill you want. Download the file named after the skill, for example `research-to-skill.zip`.
   **Do not use "Source code (zip)" or Code > Download ZIP.** They contain the whole repository with a different folder layout, and uploading them into Claude will most likely fail.
2. In Claude: Customize > Skills > + > Create skill > Upload a skill. Upload the ZIP without unpacking it.
3. Claude needs "Create and edit files" (code execution) turned on in Settings > Capabilities.

More detail is in the README inside each skill folder.

## Known limit

research-to-skill may not start by itself when another skill-creation skill is installed. If that happens, write: "Use the skill research-to-skill and build me a skill that ...".

## License

CC BY 4.0. You may use, change and share the skills with credit to Klara Slivone / Prunus skills.
