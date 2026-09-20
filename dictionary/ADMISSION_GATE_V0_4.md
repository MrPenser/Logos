# LOGOS — Admission Gate v0.4

Date: 2026-09-16
Status: RESEARCH CANDIDATE / commonWords REMOVED FROM ADMISSION

## Decision
The old `commonWords` admission filter is no longer used.

New two-layer gate:

1. **LEXICAL_VALIDITY** — CMU Pronouncing Dictionary (CMUdict) membership.
2. **BEGINNER_SUITABILITY** — explicit LOGOS policy categories.

CMUdict is used only to answer whether a token is an attested pronounceable dictionary entry. It does **not** decide whether a token belongs in the first 500.

## Beginner policy v1

Deferred categories in reconstructed TOP-522:
- LETTER_SYMBOL: B, C, D, E, M, R, S, T
- TITLE_ABBREVIATION: MR
- FOREIGN_OR_NAME_PARTICLE: DE, LA
- PREFIX_OR_SPECIAL_USE: NON
- PROPER_NAME: JOHN, YORK, LONDON
- CALENDAR_PROPER_NAME: APRIL
- DEMONYM_LANGUAGE_OR_PROPER_ADJECTIVE: AMERICAN, FRENCH
- TABOO_REGISTER: SHIT, FUCK, FUCKING
- COLLOQUIAL_REDUCTION: GONNA

Single-letter lexical words A and I are explicitly admitted.

## Result
- Reconstructed frequency window: TOP-522 alpha entries.
- CMUdict lexical validation: 522 / 522.
- Deferred by explicit beginner policy: 22.
- Admitted targets required to obtain 500: exactly 500.
- Final 500 TARGET composition compared with v0.3.1: **UNCHANGED**.

This is a stability result: replacing `commonWords` did not alter the first 500 under the explicit policy; it changed provenance and the reason for admission/rejection.

## Licensing/provenance
- CMUdict data permits unrestricted research/commercial use with origin acknowledgement requested.
- `commonWords` is no longer part of the admission decision.
- Current frequency ordering still comes from the existing wordfreq research baseline and retains its own attribution/share-alike obligations.

## Limitation
CMUdict is a pronunciation dictionary, not a pedagogical lexicon, so it is never used alone. Beginner exclusions are explicit, versioned and reviewable.

## Next
1. Apply lexical-validity gate to MASTER20K.
2. Add Open English Wordnet / authoritative POS-lemma layer.
3. Recompute Stage-0 graph with morphology penalties.
4. Freeze Starter Core v1.0 only after these gates pass.
