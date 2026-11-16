# Contributing

Developer guide for this repo. End users: use the `myth-debunk` skill, not this file.

## Adding a myth

Run the **`myth-research`** skill on the claim — it investigates primary sources and returns a structured entry. Save the output as `skills/myth-debunk/topics/<topic>/myths/NNN-slug.md` (NNN = zero-padded fixed number when vendoring from Skeptical Science), following `myths/TEMPLATE.md` in that topic.

## Adding a topic

Copy the skeleton `skills/myth-debunk/topics/climate/` (`overview.md` + `myths/TEMPLATE.md`) to `skills/myth-debunk/topics/<new-topic>/`, then fill `overview.md` (scope, sources, myth count, sync date).

## Vendoring Skeptical Science arguments

Source list: [the SkS argument list](https://skepticalscience.com/argument.php), fixed numbers via its [print view](https://skepticalscience.com/print.php). For each argument, fetch the actual argument page, extract Claim / Fact / Technique / Full picture / Prebunking / Sources, and write one myth file per `TEMPLATE.md`. Work in batches; each myth file's `sks_url` is the argument page itself, and `last_synced` records the fetch date.

License rule (see `ATTRIBUTION.md`): site content is CC BY 3.0 (quote short phrases with a link); the 2010 Guide PDF is CC BY-NC 3.0 — cite and link only, never copy its text.

## Update detection (planned, not built)

A future GitHub Action will diff the SkS argument list (fixed numbers + titles) against the vendored catalog and open an issue when arguments are added, removed, or retitled. The `sks_number`, `sks_url`, and `last_synced` fields exist for this.

## ADRs

Write an ADR in `docs/adr/` only when a decision is hard to reverse, surprising without context, and the result of a real trade-off. Format: 1–3 sentences — context, decision, why. See `docs/adr/0001-skill-repo-layout.md`.
