---
name: myth-response
description: "Given any input text containing misinformation claims — an email, chat message or article; the source does not matter — extract its claims and produce a ready-to-send response that names each reasoning error. Ground each claim by invoking the myth-debunk skill (myth-research on a catalog miss). Use when asked to reply to or rebut someone's message, e.g. 'use the myth-response skill to answer Postma's latest email in my Outlook'."
---

# Respond to a message containing myths

Works on any agent harness. Answers in chat only — never writes files. Source-agnostic: the caller supplies the input text (pasted, or read via whatever tools the harness provides, e.g. Outlook); this skill works only on the text it receives.

## Steps

1. **Take the input.** Whatever text the caller provides, in full — not a summary. Record its metadata (sender, date, per-message timestamps, subject) for the intro. Done when the complete input text is in hand.
2. **Extract the claims.** Split the input into individual checkable claims; keep each claim verbatim with its location/timestamp. Done when every substantive claim is captured, one per item.
3. **Ground each claim by invoking `myth-debunk`.** Run the `myth-debunk` skill on each extracted claim — it matches the claim on substance (not exact wording) to the bundled catalog `../myth-debunk/topics/*/myths/` and falls back to `myth-research` on a catalog miss. Do not re-implement the catalog matching here. Done when each claim has Fact, Technique (FLICC), Full picture and Sources in hand.
4. **Compose the response** in this fixed format:
   1. Short intro: which inputs (sender, date, timestamps, subject)
   2. **Reasoning errors, grouped per claim** — per claim: the verbatim quote + timestamp, then the named reasoning error (FLICC technique) and a concrete factual explanation (figures, analogy, source)
   3. **In short** — the core errors in a few bullets plus the factual counterpoint
   4. **Sources** — IPCC AR6 (section/table/figure) where possible, else the peer-reviewed papers cited in the matched myth files; if the rebuttal derives from the bundled catalog, include the Skeptical Science credit link (see `ATTRIBUTION.md`)
5. **Style rules** (always):
   - Output language = input language (Dutch input → Dutch output)
   - If the input is an email: body only, no salutation or sign-off; address the author in the second person ("je" in Dutch)
   - Factual, neutral tone; no sarcasm
   - No visible references to skills, myth numbers or the catalog — the catalog is a source, not a label in the output
   - Every technical assertion gets a concrete number, analogy or source; no bare labels without explanation
   - Scan the output for stray words in other languages before returning

Done when the response is ready to paste as a reply to the input.

## Credits

Rebuttals grounded in the bundled catalog derive from [Skeptical Science](https://skepticalscience.com) (CC BY 3.0) — see `ATTRIBUTION.md`.
