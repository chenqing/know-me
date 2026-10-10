# Know me

An agent skill that interviews you one question at a time until it has a
durable, multi-layer picture of who you are, then saves **confirmed** facts
to shared memory.

Inspired by Matt Pocock’s [grill-me](https://github.com/mattpocock/skills)
interview loop, applied to a person instead of a plan.

## Install

```bash
npx skills add chenqing/know-me-skill --skill know-me
```

Or copy `skills/know-me/SKILL.md` into your agent’s skills folder.

## What it covers

Identity, life narrative, values, decision style, goals, work system,
relationships, energy rhythms, tools, communication prefs, money/time
tradeoffs, Jobs-to-be-Done help jobs, taboos, and a final check of the
agent’s mental model.

## Design notes

- One question per turn; plain language only to the user
- Full first pass in one session by default
- Confirmed semantic facts → profile; dated scenes → log
- Not therapy, not a personality test

See the skill file for theory anchors and probe shapes.

## License

MIT
