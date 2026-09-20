# LOGOS — Lexical Gate v0.4 — ESDB

Date: 2026-09-16
Status: CANONICAL_RESEARCH_GATE / PRODUCTION_LICENSE_REVIEW

## Replacement
The previous commonWords admission filter is removed from the active LOGOS pipeline.
It remains only in superseded research baselines.

New admission source:
- English Speller Database (ESDB)
- exact generated American-English default wordlist en_US.txt
- tag: rel-2026.02.25
- en_US.txt blob: b4222bda8be5826fce1635230f9503234ec31e5a
- ESDB default size: 60
- metadata from generated scowl.txt at the same tag

Frequency ordering remains the wordfreq-en-25000 export for the current research phase.

## Admission rule
A word is AUTO-ADMITTED when:
1. it occurs in the exact American-English ESDB size-60 output in the correct lowercase form (I is the capitalization exception);
2. it is a single alphabetic word;
3. one-letter entries are rejected except A and I;
4. it has ESDB general-word evidence as a lemma or derived form;
5. abbreviations, affixes, non-words, multiword parts and entity-only analyses do not qualify;
6. SPECIAL_ONLY entries do not auto-enter the beginner core;
7. if a lowercase sense is ESDB-size >35 and an uppercase/proper analysis is at least as common, the token is flagged CASE_FREQ_COLLISION and does not auto-enter.

Offensive/vulgar words are not silently censored. If frequency and lexical rules admit them, they are retained as RECEPTIVE_ONLY.

## MASTER20K v0.4
- admitted: 16188
- strict graph nodes: 7925
- strict directed edges: 5452
- morphology/same-lemma strict edges: 3352

## Starter Target500
- exactly 500 learner targets
- cutoff alpha rank: 517
- MATRYOSHKA_DIRECT targets: 99
- targets connected after adding all current bridge candidates: 127
- direct fallback after candidate bridges: 373
- bridge candidates: 24

Rejected before the 500th target:
s(173:SINGLE_LETTER), mr(218:NOT_EXACT_EN_US), de(231:NOT_EXACT_EN_US), d(240:SINGLE_LETTER), american(321:NOT_EXACT_EN_US), b(353:SINGLE_LETTER), m(363:SINGLE_LETTER), t(384:SINGLE_LETTER), c(389:SINGLE_LETTER), john(410:CASE_FREQ_COLLISION), york(449:NOT_EXACT_EN_US), e(452:SINGLE_LETTER), r(458:SINGLE_LETTER), non(489:SPECIAL_ONLY), la(499:CASE_FREQ_COLLISION), april(505:NOT_EXACT_EN_US), london(509:NOT_EXACT_EN_US)

Special teaching modes:
- RECEPTIVE_ONLY: shit, fuck, fucking
- CONTRACTION_SPOKEN: gonna

## Change vs v0.3.1
Newly admitted into Target500:
shit, fuck, gonna, fucking

Moved outside Target500:
clear, held, outside, phone

This is caused by replacing the subjective/offensive-filtering commonWords gate with the ESDB lexical gate.

## Stage 0 bridge policy
Bridge candidates do not consume Target500 slots.
A v0.4 primary bridge candidate must:
- be ESDB-admitted;
- have alpha rank <=5000;
- connect directly by non-same-lemma strict edges to at least two Target500 words.

Bridge candidates are not yet final lesson items.

## Licensing/provenance
ESDB combined work uses its published permissive/MIT-like licensing terms; preserve the ESDB Copyright/attribution in production.
The current wordfreq export is CC BY-SA 4.0 and remains a research frequency source; its attribution/share-alike obligations must be addressed before production distribution.

## Next
1. PPP audit v0.4.
2. Decide production frequency source / wordfreq compliance strategy.
3. Freeze Target500 v1.0 only after that gate.
4. Then create lesson ordering.
