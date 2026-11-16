---
name: myth-debunk
description: "Given a misinformation claim, produce an evidence-based rebuttal in chat: match it to the bundled myth catalog (topics/*/myths/), or research it on the fly via myth-research, then answer Fact–Myth–Fallacy with the full picture. Use when the user wants to debunk, refute, or fact-check a claim."
---

# Debunk a myth

Works on any agent harness. Answers in chat only — never writes files.

## Steps

1. **Match the claim.** Search the bundled catalog `topics/*/myths/` for the myth whose core assertion matches the claim (match on substance, not exact wording). Done when the best-matching myth file is found, or none is.
2. **Ground the rebuttal.** Match found → use that myth file's Fact, Sources, Technique, Full picture, Prebunking. No match → invoke `myth-research` and use its output. Done when the raw material for the rebuttal is in hand.
3. **Answer, Fact–Myth–Fallacy, in this order:**
   1. **Warn** the reader a myth is coming (puts them on guard)
   2. State the **Fact** — a sticky replacement that fills the causal gap the myth leaves
   3. Name the **Myth**
   4. Expose the **Technique** it uses (FLICC: fake experts, logical fallacies, impossible expectations, cherry picking, conspiracy theories)
   5. Present the **Full picture** — multiple independent lines of evidence, not one counter-study

   Done when all five elements appear in that order.
4. **Prebunk.** List the likely variants of this myth and the one-line inoculation for each. Done when the top variants are covered.

## Credits

Rebuttals grounded in the bundled catalog derive from [Skeptical Science](https://skepticalscience.com) (CC BY 3.0) — end with a credit link (see `ATTRIBUTION.md`).
