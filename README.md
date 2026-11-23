# misinformation-skills

Skills for combating misinformation, built on Skeptical Science's method. The cited evidence base lives in [`research/`](research/); credits and licenses in [`ATTRIBUTION.md`](ATTRIBUTION.md).

## Install

The skills follow the open [Agent Skills](https://agentskills.io) standard, and this public repo is a skill repo: anyone can install them with the [skills](https://skills.sh) CLI into 75+ coding agents, and the repo is indexed on [skills.sh](https://skills.sh).

```bash
npx skills add boukepostma/misinformation-skills                 # both skills
npx skills add boukepostma/misinformation-skills --skill myth-debunk
```

`myth-debunk` ships with the bundled myth catalog (`topics/`), so each install is self-contained.

## Skills

- [myth-debunk](skills/myth-debunk/SKILL.md) — end-user skill: given a misinformation claim, produce an evidence-based rebuttal in chat (Fact–Myth–Fallacy plus the full picture), grounded in the bundled myth catalog when matched, researched on the fly via `myth-research` when not.
- [myth-research](skills/myth-research/SKILL.md) — investigate a new myth against primary sources and return a structured myth entry. Invoked by `myth-debunk` on catalog misses; run by repo developers when adding myths (see [`CONTRIBUTING.md`](CONTRIBUTING.md)).
- [myth-response](skills/myth-response/SKILL.md) — end-user skill: given any input text containing misinformation claims (e.g. an email), produce a ready-to-send response that names each reasoning error per claim, grounded in the bundled myth catalog via `myth-debunk` / `myth-research`.

## Docs

- [`GLOSSARY.md`](GLOSSARY.md) — canonical terms: Misinformation, Disinformation, Myth, Rebuttal, Technique, Prebunking, Topic
- [`CONTRIBUTING.md`](CONTRIBUTING.md) — add myths and topics as a repo developer
- [`ATTRIBUTION.md`](ATTRIBUTION.md) — credits and licenses
- [`research/`](research/) — primary-source research notes feeding the skills
- [`docs/techniques/`](docs/techniques/) — FLICC taxonomy: all 34 sub-techniques with definitions and examples (`flicc.md`) plus machine-readable slugs for myth-file frontmatter (`flicc.yaml`)
- [`docs/adr/`](docs/adr/) — decision records
- [`docs/agents/`](docs/agents/) — issue tracker and label conventions used by the engineering flow
