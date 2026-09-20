# LOGOS — Lexicon Gate v0.4

Date: 2026-09-16
Status: RESEARCH BASELINE / COMMONWORDS REMOVED

## Decision
The non-commercial/subjective commonWords filter is no longer used for Starter Core admission.

New admission architecture:
1. Frequency order: existing wordfreq research baseline.
2. Lexical validity: SCOWL-derived en_US Hunspell level-60 dictionary surface forms.
3. Capitalization gate: lowercase lexical entries only, except explicit pronoun I.
4. Beginner policy: explicit LOGOS deferrals, not hidden source filtering.
5. Stage-0 graph: strict +1 left/right only.
6. Morphology penalty: same-lemma generated edges do not count toward primary Matryoshka connectivity.

Official ESDB/SCOWL v2 is the canonical lexical specification target. The executable v0.4 membership snapshot uses the current LibreOffice en_US Hunspell dictionary derived from SCOWL level 60 because it is directly machine-readable in the connected GitHub environment.

## Licensing
SCOWL/ESDB combined work is described by the official project as BSD-compatible / MIT-like; commercial use/distribution is permitted subject to included notices.
Princeton WordNet is also commercially usable under its license.
The remaining licensing issue is frequency provenance: the current wordfreq-derived ordering is still research baseline and must be handled separately before production distribution.

## Target result
TARGET count: 500
Alpha frequency cutoff: 522
Target composition identical to v0.3.1: true

Excluded/deferred before cutoff:
s(173:SINGLE_LETTER_OR_SYMBOL), mr(218:CAPITAL_ONLY), de(231:CAPITAL_ONLY), d(240:SINGLE_LETTER_OR_SYMBOL), american(321:CAPITAL_ONLY), shit(330:DEFER_TABOO_REGISTER), b(353:SINGLE_LETTER_OR_SYMBOL), m(363:SINGLE_LETTER_OR_SYMBOL), t(384:SINGLE_LETTER_OR_SYMBOL), c(389:SINGLE_LETTER_OR_SYMBOL), john(410:DEFER_ENTITY_DOMINATED_AMBIGUOUS), fuck(420:DEFER_TABOO_REGISTER), york(449:CAPITAL_ONLY), e(452:SINGLE_LETTER_OR_SYMBOL), gonna(454:DEFER_NONSTANDARD_CONTRACTION), r(458:SINGLE_LETTER_OR_SYMBOL), fucking(477:DEFER_TABOO_REGISTER), non(489:DEFER_PREFIX_SPECIAL), la(499:DEFER_ENTITY_FOREIGN_MUSIC_AMBIGUOUS), april(505:CAPITAL_ONLY), london(509:CAPITAL_ONLY), french(519:DEFER_ENTITY_DOMINATED_AMBIGUOUS)

## Graph result
Eligible TOP5000 lexical universe: 4593
Strict edges: 1333

Primary bridge count: 11
Optional form bridge count: 5
Primary Matryoshka-connected TARGETS: 110
Extension-connected TARGETS: 4
Raw connected TARGETS including morphology: 158
Direct fallback TARGETS after extension: 386

PRIMARY BRIDGES:
- HI rank 868 — i>hi>him [LR] => him
- SIT rank 1321 — i>it>sit [RL] => site
- AD rank 1894 — a>ad>had [RL] => bad|had
- MA rank 2327 — a>ma>may [LR] => may
- DON rank 2458 — on>don>done [LR] => do
- HAT rank 2660 — a>at>hat [RL] => what|that
- PA rank 3736 — a>pa>pay [LR] => pay
- MIN rank 3865 — in>min>mind [LR] => mind
- ATE rank 4011 — a>at>ate [RR] => late
- MALL rank 4644 — all>mall>small [LL] => small
- FA rank 4784 — a>fa>far [LR] => far

OPTIONAL FORM BRIDGES:
- AID rank 1628 — i>id>aid>said [RLL] => said
- MAD rank 1920 — a>ad>mad>made [RLR] => made
- SING rank 2595 — in>sin>sing>using [LRL] => using
- ID rank 2779 — i>id>did [RL] => did
- SIN rank 3052 — in>sin>sing>using [LRL] => using

## Comparison with v0.3.1
Target 500: unchanged.
Old primary connected target metric: 108.
New primary connected target metric: 110.
Old broad/raw metric: 153.
New broad non-morph extension metric: 114.
New raw including morphology: 158.

The graph improves because the new lexicon gate admits legitimate general English bridge candidates that commonWords had filtered out.

## Remaining production gate
Replace/resolve the wordfreq-derived frequency ordering with a redistribution-safe production frequency strategy. Until then v0.4 remains a research baseline, even though commonWords has been removed.
