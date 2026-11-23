---
name: myth-research
description: "Investigate a misinformation claim against primary sources and return a structured myth entry (Claim, Fact, Technique, Full picture, Prebunking, Sources). Use when a claim has no match in a bundled myth catalog (myth-debunk invokes this on a catalog miss), or when adding/vendoring a myth to a topic catalog as a repo developer."
---

# Research a new myth

Turn one misinformation claim into a structured, sourced myth entry. Two callers: `myth-debunk` (on a catalog miss, result used in chat only) and a repo developer (result saved as a myth file — see `CONTRIBUTING.md`).

## Steps

1. **Restate the claim.** What is asserted, by whom, where seen. Done when the claim is one sentence a stranger could repeat.
2. **Investigate against primary sources.** Peer-reviewed literature, official data, source documents — follow every factual assertion back to the source that owns it. Delegate heavy reading to whatever research skill your harness provides (e.g. `mp-research`); never ask the user for facts you can look up. Done when every assertion in the entry traces to a primary source.
3. **Name the Technique.** Pick the most specific FLICC sub-technique from [`docs/techniques/flicc.md`](../../../docs/techniques/flicc.md) (34 sub-techniques in 5 categories; valid slugs in [`flicc.yaml`](../../../docs/techniques/flicc.yaml)); fall back to the category slug when no sub-technique fits. Done when the `technique:` slug records the specific move the claim makes.
4. **Write the myth entry** in the schema (template: `topics/<topic>/myths/TEMPLATE.md`):
   - frontmatter: `sks_number` (Skeptical Science fixed number when vendoring, else empty), `sks_url` (originating argument page when vendoring), `technique` (FLICC slug from `docs/techniques/flicc.yaml`), `last_synced` (YYYY-MM-DD)
   - `## Fact` — one line: what the evidence says
   - `## Full picture` — multiple independent lines of evidence, not a single counter-study
   - `## Prebunking` — likely variants of the myth and the inoculation for each
   - `## Sources` — peer-reviewed references plus the originating pages (including the SkS argument page when vendoring)

   Done when all four frontmatter fields and all four sections are present.
5. **Hand back the entry.** End-user callers use it in chat only; developer callers save it as `topics/<topic>/myths/NNN-slug.md` (NNN = zero-padded fixed number). Done when the caller has the complete entry.

## Credits

Where the claim or its rebuttal originates from Skeptical Science, attribute it with a link (see `ATTRIBUTION.md`). Never copy text from the CC BY-NC 2010 Guide — cite and link only.
