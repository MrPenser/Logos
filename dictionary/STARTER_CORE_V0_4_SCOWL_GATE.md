# LOGOS — Starter Core v0.4 — SCOWL Admission Gate

Date: 2026-09-15
Status: SOURCE-GATE REPLACED / CANDIDATE FOR STARTER REVIEW

## What changed
The previous commonWords admission filter is removed from the active pipeline.
Lexical admission now uses the official English Speller Database / SCOWL generated American English size-60 wordlist.

Pinned source:
- repository: en-wl/wordlist-diff
- tag: rel-2026.02.25
- en_US.txt blob SHA: b4222bda8be5826fce1635230f9503234ec31e5a
- upstream tag commit: 71d7dd07676edb60ade43552e10b41314b7e9287

SCOWL/ESDB permission explicitly allows use, copy, modify, distribute, and sell the database or word lists created from it, subject to retaining the copyright/permission notice.

## Admission rule
1. Frequency order remains the existing wordfreq-en-25000 research ranking.
2. A and I are accepted single-letter English words.
3. Other single-letter tokens are excluded from the word inventory.
4. Generic lexical targets require an exact lowercase entry in SCOWL en_US size 60.
5. CAPITALIZED_ONLY entries are not admitted to the generic Starter lexical core.
6. No offensive/slang/commonness blacklist is applied at admission.
7. Beginner suitability is a separate visible field and never silently changes lexical validity.

## Lexical-500 result
- lexical targets: 500
- alpha-rank cutoff: 514
- admitted TOP5000 universe: 4599
- strict +1 edge-only edges in universe: 1341

Excluded before cutoff by formal admission rule:
- s(173:LOWERCASE_WITH_CASE_COLLISION)
- mr(218:CAPITALIZED_ONLY)
- de(231:CAPITALIZED_ONLY)
- d(240:LOWERCASE_WITH_CASE_COLLISION)
- american(321:CAPITALIZED_ONLY)
- b(353:LOWERCASE_WITH_CASE_COLLISION)
- m(363:LOWERCASE_WITH_CASE_COLLISION)
- t(384:LOWERCASE_WITH_CASE_COLLISION)
- c(389:LOWERCASE_WITH_CASE_COLLISION)
- york(449:CAPITALIZED_ONLY)
- e(452:LOWERCASE_WITH_CASE_COLLISION)
- r(458:LOWERCASE_WITH_CASE_COLLISION)
- april(505:CAPITALIZED_ONLY)
- london(509:CAPITALIZED_ONLY)

Explicit suitability-review targets retained in Lexical-500:
- shit — REVIEW_VULGAR
- fuck — REVIEW_VULGAR
- fucking — REVIEW_VULGAR
- gonna — REVIEW_INFORMAL_NONSTANDARD
- john — REVIEW_CASE_COLLISION_SENSE
- la — REVIEW_SPECIALIZED_SENSE
- non — REVIEW_RARE_SENSE

These entries remain in Lexical-500. Any future pedagogical deferral must be explicit and versioned.

## Difference vs v0.3.1
Removed from target set (7):
west, behind, bring, clear, held, outside, phone

Added to target set (7):
shit(330), john(410), fuck(420), gonna(454), fucking(477), non(489), la(499)

## Matryoshka graph
- structural bridges: 18
- raw connected TARGETS (morphology allowed): 164
- morphology-penalized core connected TARGETS: 121
- extension-only TARGETS: 43
- direct fallback TARGETS: 336

Bridges:
- re (703) — re>are>care [LL] => red
- hi (868) — i>hi>his [LR] => him
- sit (1321) — i>it>sit [RL] => site
- aid (1628) — i>id>aid>said [RLL] => said
- ad (1894) — a>ad>had [RL] => bad|had
- mad (1920) — a>ad>mad>made [RLR] => made
- lay (2073) — a>la>lay [LR] => play
- ma (2327) — a>ma>may [LR] => may
- don (2458) — on>don>done [LR] => do
- sing (2595) — in>sin>sing>using [LRL] => using
- hat (2660) — a>at>hat [RL] => what|that
- id (2779) — i>id>did [RL] => did
- sin (3052) — in>sin>sing>using [LRL] => using
- pa (3736) — a>pa>pay [LR] => pay
- min (3865) — in>min>mind [LR] => mind
- ate (4011) — a>at>ate [RR] => late
- mall (4644) — all>mall>small [LL] => small
- fa (4784) — a>fa>far [LR] => far

## Interpretation
Frequency decides which lexical items enter the 500.
SCOWL decides whether an item is a real admitted American-English lexical form.
Matryoshka decides how admitted items can be organized visually.
Morphological edges are retained for teaching but are excluded from the primary structural-value metric.

## Remaining gates before v1.0
1. Resolve the seven explicit Starter-suitability review items without altering Lexical-500.
2. Complete authoritative POS/lemma enrichment.
3. Decide licensing/attribution handling for the frequency-ranking source (wordfreq export is still a separate provenance layer).
4. Freeze Starter-500, then build lesson order.
