# LOGOS — Starter Core v0.3 — Lexical Cleanup Pass 1

Date: 2026-09-14
Status: RESEARCH_CANDIDATE / NOT PRODUCTION

## Core
- Learner target words: exactly 500
- Alpha-rank cutoff required after filtering: 522
- Strict bridge nodes: 10
- Total graph-visible rows: 510
- Targets in meaningful multi-target Matryoshka components: 153
- Direct fallback targets: 347

## Critical rule
Bridge nodes do NOT consume one of the 500 learner-target slots.
Frequency decides WHAT belongs to the first dictionary.
Matryoshka organizes HOW it is learned.

## Lexical filtering
Excluded/demoted before target 500:
s, mr, de, d, american, shit, b, m, t, c, john, fuck, york, e, gonna, r, fucking, non, la, april, london, french

Manual demotions in this pass:
- NON — not retained as a beginner target; still permitted in MASTER graph if structurally needed.
- FRENCH — delayed to proper-name/language/demonym handling because capitalization/entity policy is not yet implemented.

Replacement target words beyond alpha TOP500:
mother(501), near(502), period(503), process(504), art(506), former(507), heard(508), plan(510), quite(511), series(512), site(513), talking(514), west(515), behind(516), bring(517), clear(518), held(520), outside(521), phone(522)

## Morphology
Inflected/irregular forms are NOT deleted when highly frequent.
They are linked to a lemma and are prevented from masquerading as independent lemmas in later scoring.

Morphology counts:
- LEMMA_OR_INDEPENDENT: 422
- IRREGULAR_FORM: 26
- INFLECTED_FORM: 22
- REGULAR_S_FORM: 11
- FORM_AND_LEMMA: 9
- IRREGULAR_PLURAL: 3
- SUPPLETIVE_DEGREE: 2
- PARTICIPLE_DERIVED: 2
- LEXICALIZED_PLURAL: 1
- COMPARATIVE_FORM: 1
- REGULAR_ING_FORM: 1

## POS policy
No fabricated full POS tagging.
This pass records only high-confidence function classes plus lemma/morphology relations.
Full POS is deferred to Stage-1 lexical enrichment using an authoritative POS lexicon.

## Bridge layer
- hour — BRIDGE_BONUS — alpha rank 669 — our>hour>hours [LR] => hours
- hi — BRIDGE_BONUS — alpha rank 868 — i>hi>his [LR] => him
- sit — BRIDGE_BONUS — alpha rank 1321 — i>it>sit [RL] => site
- ad — BRIDGE_USEFUL_SHORT — alpha rank 1894 — a>ad>had [RL] => bad|had
- mad — BRIDGE_BONUS — alpha rank 1920 — a>ad>mad>made [RLR] => made
- don — BRIDGE_TECHNICAL — alpha rank 2458 — on>don>done [LR] => do
- sing — BRIDGE_BONUS — alpha rank 2595 — in>sin>sing>using [LRL] => using
- hat — BRIDGE_BONUS — alpha rank 2660 — a>at>hat [RL] => what|that
- sin — BRIDGE_BONUS — alpha rank 3052 — in>sin>sing>using [LRL] => using
- mall — BRIDGE_BONUS — alpha rank 4644 — all>mall>small [LL] => small

## Remaining gates before v1.0
1. Authoritative lemma/POS enrichment.
2. Proper-name/capitalization normalization.
3. Register/slang/offensive policy on the full 500.
4. Licensing-safe production frequency/lexicon source.
5. Recompute lesson ordering after morphology is prevented from inflating family scores.
