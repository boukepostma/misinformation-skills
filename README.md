# misinformation-skills

Skills for combating misinformation, built on Skeptical Science's method. The cited evidence base lives in [`research/`](research/); credits and licenses in [`ATTRIBUTION.md`](ATTRIBUTION.md).

## Skills

- [myth-debunk](skills/myth-debunk/SKILL.md) — end-user skill: given a misinformation claim, produce an evidence-based rebuttal in chat (Fact–Myth–Fallacy plus the full picture), grounded in the bundled myth catalog when matched, researched on the fly via `myth-research` when not.
- [myth-research](skills/myth-research/SKILL.md) — investigate a new myth against primary sources and return a structured myth entry. Invoked by `myth-debunk` on catalog misses; run by repo developers when adding myths (see [`CONTRIBUTING.md`](CONTRIBUTING.md)).

## Docs

- [`GLOSSARY.md`](GLOSSARY.md) — canonical terms: Misinformation, Disinformation, Myth, Rebuttal, Technique, Prebunking, Topic
- [`CONTRIBUTING.md`](CONTRIBUTING.md) — add myths and topics as a repo developer
- [`ATTRIBUTION.md`](ATTRIBUTION.md) — credits and licenses
- [`research/`](research/) — primary-source research notes feeding the skills
- [`docs/adr/`](docs/adr/) — decision records
- [`docs/agents/`](docs/agents/) — issue tracker and label conventions used by the engineering flow
