# FLICC technique taxonomy

The FLICC taxonomy of science-denial techniques (Cook et al., 2015, expanded in Cook 2020), as listed in Skeptical Science's [FLICC cheat sheet](https://skepticalscience.com/docs/FLICC-Cheat-Sheet.pdf) (August 2022). Canonical reference for the `technique:` frontmatter field in myth files and for naming techniques in `myth-research` and `myth-debunk`.

Two levels: **category** (the five FLICC letters) and **sub-technique** (the specific move). When tagging or naming, use the most specific sub-technique slug; fall back to the category slug only when nothing more specific fits. The cheat sheet prints 36 rows — "fake debate" and "false equivalence" each appear twice — giving the 34 unique techniques below. Machine-readable slugs: [`flicc.yaml`](flicc.yaml).

## Fake experts (`fake-experts`)

| Sub-technique | Slug | Definition | Example |
|---|---|---|---|
| Fake experts (appeal to false authority) | `fake-experts` | Presenting an unqualified person or institution as a source of credible information. | "A retired physicist argues against the climate consensus, claiming the current weather change is just a natural occurrence." |
| Bulk fake experts | `bulk-fake-experts` | Citing large numbers of seeming experts to argue that there is no scientific consensus on a topic. | "There is no expert consensus because 31,487 Americans with a science degree signed a petition saying humans aren't disrupting climate." |
| Magnified minority | `magnified-minority` | Magnifying the significance of a handful of dissenting scientists to cast doubt on an overwhelming scientific consensus. | "Sure, there's 97% consensus but Professor Smith disagrees with the consensus position." |

## Logical fallacies (`logical-fallacies`)

| Sub-technique | Slug | Definition | Example |
|---|---|---|---|
| Logical fallacy (non sequitur) | `logical-fallacy` | Arguments where the conclusion doesn't logically follow from the premises. | "Climate has changed naturally in the past so what's happening now must be natural." |
| Fake debate (false balance) | `fake-debate` | Presenting science and pseudoscience in an adversarial format to give the false impression of an ongoing scientific debate. | "Climate deniers should get equal coverage with climate scientists, providing a more balanced presentation of views." |
| Misrepresentation | `misrepresentation` | Misrepresenting a situation or an opponent's position in such a way as to distort understanding. | "They changed the name from 'global warming' to 'climate change' because global warming stopped happening." |
| Straw man | `straw-man` | Misrepresenting or exaggerating an opponent's position to make it easier to attack. | "In the 1970s, climate scientists were predicting an ice age." |
| Ad hominem | `ad-hominem` | Attacking a person/group instead of addressing their arguments. | "Climate science can't be trusted because climate scientists are biased." |
| Ambiguity | `ambiguity` | Using ambiguous language in order to lead to a misleading conclusion. | "Thermometer readings have uncertainty which means we don't know whether global warming is happening." |
| Slippery slope | `slippery-slope` | Suggesting that taking a minor action will inevitably lead to major consequences. | "If we implement even a modest climate policy, it will start us down the slippery slope to socialism and taking away our freedom." |
| Oversimplification | `oversimplification` | Simplifying a situation in such a way as to distort understanding, leading to erroneous conclusions. | "CO2 is plant food so burning fossil fuels will be good for plants." |
| False choice | `false-choice` | Presenting two options as the only possibilities, when other possibilities exist. | "CO2 lags temperature in the ice core record, proving that temperature drives CO2, not the other way around." |
| Single cause | `single-cause` | Assuming a single cause or reason when there might be multiple causes or reasons. | "Climate has changed naturally in the past so what's happening now must be natural." |
| Red herring | `red-herring` | Deliberately diverting attention to an irrelevant point to distract from a more important point. | "CO2 is a trace gas so its warming effect is minimal." |
| Blowfish | `blowfish` | Focusing on an inconsequential aspect of scientific research, blowing it out of proportion in order to distract from or cast doubt on the main conclusions of the research. | "The hockey stick graph is invalid because it contains statistical errors." |
| False equivalence (apples vs. oranges) | `false-equivalence` | Incorrectly claiming that two things are equivalent, despite the fact that there are notable differences between them. | "Why all the fuss about COVID when thousands die from the flu every year." |
| False analogy | `false-analogy` | Assuming that because two things are alike in some ways, they are alike in some other respect. | "Climate skeptics are like Galileo who overturned the scientific consensus about geocentrism." |

## Impossible expectations (`impossible-expectations`)

| Sub-technique | Slug | Definition | Example |
|---|---|---|---|
| Impossible expectations | `impossible-expectations` | Demanding unrealistic standards of certainty before acting on the science. | "Scientists can't even predict the weather next week. How can they predict the climate in 100 years?" |
| Moving goalposts | `moving-goalposts` | Demanding higher levels of evidence after receiving requested evidence. | "Sea levels may be rising but they're not accelerating." |
| Lowered expectations | `lowered-expectations` | Lowering the standard by which you grade a performance or assess evidence. | "Two snapshots of Mars show shrinking ice, so Mars is global warming." |
| Anchoring | `anchoring` | Depending too heavily on an initial piece of information when making subsequent judgments. | "2.2 million people might have died from COVID-19 so keeping it down to only 130,000 deaths is a good job." |

## Cherry picking (`cherry-picking`)

| Sub-technique | Slug | Definition | Example |
|---|---|---|---|
| Cherry picking | `cherry-picking` | Carefully selecting data that appear to confirm one position while ignoring other data that contradicts that position. | "Global warming stopped in 1998." |
| Anecdote | `anecdote` | Using personal experience or isolated examples instead of sound arguments or compelling evidence. | "The weather is cold today — whatever happened to global warming?" |
| Slothful induction | `slothful-induction` | Ignoring relevant evidence when coming to a conclusion. | "There is no empirical evidence that humans are causing global warming." |

## Conspiracy theories (`conspiracy-theories`)

| Sub-technique | Slug | Definition | Example |
|---|---|---|---|
| Conspiracy theory | `conspiracy-theory` | Proposing that a secret plan exists to implement a nefarious scheme such as hiding a truth. | "The climategate emails prove that climate scientists have engaged in a conspiracy to deceive the public." |
| Quote mining | `quote-mining` | Taking a person's words out-of-context in order to misrepresent their position. | "Mike's trick… to hide the decline." |
| Wishful thinking | `wishful-thinking` | Choosing to believe something is true because we really want it to be true, instead of relying on scientific evidence. | "Forget climate model predictions of warming, I think we're about to experience global cooling." |
| Contradictory | `contradictory` | Simultaneously believing in ideas that are mutually contradictory. | "The temperature record is fabricated by scientists… the temperature record shows cooling." |
| Overriding suspicion | `overriding-suspicion` | Having a nihilistic degree of skepticism towards the official account, preventing belief in anything that doesn't fit into the conspiracy theory. | "Show me one line of evidence for climate change… oh, that evidence is faked!" |
| Nefarious intent | `nefarious-intent` | Assuming that the motivations behind any presumed conspiracy are nefarious. | "Climate scientists promote the climate hoax because they're in it for the money." |
| Something must be wrong | `something-must-be-wrong` | Maintaining that "something must be wrong" and the official account is based on deception, even when specific parts of a conspiracy theory become untenable. | "Ok, fine, 97% of climate scientists agree that humans are causing global warming, but that's just because they're toeing the party line." |
| Persecuted victim | `persecuted-victim` | Perceiving and presenting themselves as the victim of organized persecution. | "Climate scientists are trying to take away our freedom." |
| Immune to evidence | `immune-to-evidence` | Re-interpreting any evidence that counters a conspiracy theory as originating from the conspiracy. | "Those investigations finding climate scientists aren't conspiring were part of the conspiracy." |
| Re-interpreting randomness | `reinterpreting-randomness` | Believing that nothing occurs by accident, so that random events are re-interpreted as being caused by the conspiracy. | "NASA's satellite exploded? They must be trying to hide inconvenient data!" |

## Not FLICC

`solutions-denial` is used as a `technique:` tag in myth files but comes from Skeptical Science's claim-category taxonomy, not from FLICC.

## Credits

Definitions and examples are short excerpts from the [FLICC cheat sheet](https://skepticalscience.com/docs/FLICC-Cheat-Sheet.pdf) (Bärbel Winkler, Skeptical Science, August 2022), quoted with attribution and a link per [`ATTRIBUTION.md`](../../ATTRIBUTION.md).
