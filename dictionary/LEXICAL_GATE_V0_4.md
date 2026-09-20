# LOGOS — Lexical Gate v0.4 — commonWords REMOVED

Date: 2026-09-15

## Canonical separation
1. Frequency ranking: wordfreq 25k export (research frequency baseline).
2. Lexical admission: stable American SCOWL size-60 Hunspell dictionary, version 2020.12.07.
3. POS enrichment: Princeton WordNet 3.1 direct lemma POS.
4. Beginner surface policy: SCOWL NOSUGGEST/taboo words remain in MASTER and RAW500 but are transparently deferred from BEGINNER500_NEUTRAL.

commonWords is no longer used anywhere in v0.4 admission.

## Why pinned SCOWL 2020.12.07
The current 2026 ESDB/SCOWL transition has a released dictionary, but the underlying database/API remains in architectural transition. The stable size-60 en_US dictionary is pinned for reproducibility. A future migration check against ESDB 2026+ remains OPEN.

## Gate rules
- preserve SCOWL case: only lowercase lexical headwords/derived forms admit lowercase wordfreq tokens;
- one-letter tokens are rejected except A and I;
- WordNet does NOT admit a word by itself;
- proper-name-only uppercase spellings therefore do not enter merely because wordfreq lowercased them;
- NOSUGGEST is metadata, not deletion.

## MASTER20K v0.4
- alpha-ranked entries: 20,000
- SCOWL60 admitted: 16586
- Stage-0 graph members: 8199
- strict directed L/R edges: 5853

## RAW FREQ500
- cutoff alpha rank: 514
- taboo/NOSUGGEST entries inside RAW500: shit(330), fuck(420), fucking(477)

## BEGINNER500_NEUTRAL
- exactly 500 learner targets
- cutoff alpha rank: 517
- deferred taboo/NOSUGGEST before cutoff: shit(330), fuck(420), fucking(477)
- target-only non-morph Matryoshka connected: 107
- after provisional bridges: 126
- direct fallback after bridges: 374
- bridge nodes: 18

## Bridge rule
Bridge words never consume one of 500 target slots.
Same-lemma morphological edges are excluded from bridge optimization when detected from SCOWL affix generation or conservative irregular mapping.

Bridges:
- RE rank 703 — TECHNICAL_SHORT_BRIDGE — re>are>care [LL]; component_gain=red
- HI rank 868 — TECHNICAL_SHORT_BRIDGE — i>hi>him [LR]; component_gain=him
- SIT rank 1321 — PRIMARY_BRIDGE — i>it>sit [RL]; component_gain=site
- AID rank 1628 — PRIMARY_BRIDGE — i>id>aid>said [RLL]; component_gain=said
- AD rank 1894 — TECHNICAL_SHORT_BRIDGE — a>ad>had [RL]; component_gain=bad|had
- MAD rank 1920 — PRIMARY_BRIDGE — a>ad>mad>made [RLR]; component_gain=made
- LAY rank 2073 — PRIMARY_BRIDGE — a>la>lay [LR]; component_gain=play
- MA rank 2327 — TECHNICAL_SHORT_BRIDGE — a>ma>may [LR]; component_gain=may
- DON rank 2458 — PRIMARY_BRIDGE — on>don>done [LR]; component_gain=do
- SING rank 2595 — PRIMARY_BRIDGE — in>sin>sing>using [LRL]; component_gain=using
- HAT rank 2660 — PRIMARY_BRIDGE — a>at>hat [RL]; component_gain=what|that
- ID rank 2779 — TECHNICAL_SHORT_BRIDGE — i>id>did [RL]; component_gain=did
- SIN rank 3052 — OPTIONAL_BRIDGE — in>sin>sing>using [LRL]; component_gain=using
- PA rank 3736 — TECHNICAL_SHORT_BRIDGE — a>pa>pay [LR]; component_gain=pay
- MIN rank 3865 — OPTIONAL_BRIDGE — in>min>mind [LR]; component_gain=mind
- ATE rank 4011 — OPTIONAL_BRIDGE — a>at>ate [RR]; component_gain=late
- MALL rank 4644 — OPTIONAL_BRIDGE — all>mall>small [LL]; component_gain=small
- FA rank 4784 — TECHNICAL_SHORT_BRIDGE — a>fa>far [LR]; component_gain=far

## Status
Lexical-source replacement: PASS.
Licensing/provenance separation: PASS.
Final pedagogical utility of every TARGET500 item: still PROVISIONAL.
Lesson ordering: remains gated until utility review of the new 500 is complete.
