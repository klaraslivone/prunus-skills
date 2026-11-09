# Learning loop

Skill files are read-only at runtime. A skill therefore "learns" by proposing a lesson after use and releasing a new version the user reinstalls. Be transparent about this with the user.

## When to learn
- After the real test (always).
- When the user corrects an output or says something doesn't work.
- When the same question or correction appears a second time.

## How
1. At the end of a use, ask max. 3 questions: What was most useful? What did you have to fix? What was missing? Also ask which reviewer-card checks failed — they point to the rule to change.
2. From the answers and your own observations, write 1–3 **general** lessons (valid for other users too; nothing personal).
3. A lesson goes either to `references/lessons.md` (experience) or straight into the skill's rules (when it's a flaw in the workflow).
4. Copy the skill to a working folder, edit, bump the version in the Changes section, package as `.skill` and offer it for reinstalling.
5. When `lessons.md` exceeds ~30 entries, merge recurring ones into rules in SKILL.md and shorten the file.

## Block to insert into every newly built skill (in SKILL.md)
```
## Learning
At the start, read `references/lessons.md` and follow it.
At the end of a use, offer a short tune-up (max. 3 questions: what helped, what needed fixing, what was missing).
Turn the answers into 1–3 general lessons without personal data and offer to release a new version of the skill
(copy → edit `lessons.md` or the rules → bump version → package .skill).
```

## Template for `references/lessons.md`
```
# Lessons from use
Format: what happened · lesson · where recorded (lessons / rule)

## Changes
- v1.0 – first version
```
