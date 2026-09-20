# LOGOS — PPP Audit v0.3 → v0.3.1

Date: 2026-09-14

## PASS — structural
- 500 TARGET rows.
- 10 bridge rows.
- No duplicate words.
- target_index is exactly 1..500.
- alpha_rank and source_rank independently reproduce.
- Every listed L/R edge satisfies the exact +1 edge-only predicate.
- Every edge is internal to the 510-row graph table.
- Target order exactly reproduces the current research selection rule.

## CORRECTED — morphology semantics
The old value LEMMA_OR_INDEPENDENT was logically too strong: failure to map a form does not prove that it is an independent lemma.
It is replaced by UNRESOLVED_OR_LEMMA.

Clear corrections include:
- BEING: IRREGULAR_FORM → INFLECTED_FORM.
- FOUND: FIND form + independent lexeme FOUND → FORM_AND_LEMMA.
- MEANS: MEAN form + independent noun MEANS → FORM_AND_LEMMA.
- GIVEN, BASED, UNITED, LATER, THANKS: independent lexical uses retained alongside form relation.
- HOURS, MONTHS, MINUTES, MEMBERS: explicit regular plural mapping even though the lemma may lie outside the 500-target set.

Morphology remains PARTIAL. Absence of a relation is not a negative claim.

## CORRECTED — function classes
function_class is renamed function_roles_partial.
It is explicitly non-exhaustive. Multifunctional items such as THAT, HER, HIS, WHAT, WHICH, AS, FOR, THAN are no longer represented by one misleading class.

## CORRECTED — morphology inflation of Stage 0
Old headline: 153 targets in multi-target graph components.
This includes regular/irregular form edges and optional bridges.

PPP core metric:
- 108 TARGETS are connected in the PRIMARY, non-same-lemma strict visual graph.
- 45 additional TARGETS are connected only in the broader extension graph (morphology and/or optional bridges).
- 347 TARGETS remain DIRECT_FALLBACK.

Therefore 153 is retained only as RAW/EXTENSION connectivity, not as the primary Stage-0 quality metric.

## CORRECTED — bridge classes
PRIMARY_BRIDGE (6):
HI, SIT, AD, DON, HAT, MALL

OPTIONAL_FORM_BRIDGE (4):
HOUR, MAD, SING, SIN

The optional bridges mainly improve access to already-inflected/form-related targets and must not dominate core ranking.

## FAIL — canonical lexical selection
The 500 TARGET composition is NOT yet canonical.

Current selection is:
wordfreq alpha frequency order
INTERSECT research commonWords filter
minus manual demotions NON and FRENCH
until 500 targets are obtained.

The commonWords source is unsuitable as a production/canonical gate because its own README states:
- usage is limited to non-commercial usage because of Brysbaert-derived data;
- offensive words are deliberately removed;
- manual subjective common/uncommon correction lists are used;
- final word choice is at repository-owner discretion.

Thus current TARGET 500 remains a RESEARCH SELECTION, not LOGOS Core v1.0.

## Source/provenance status
wordfreq export: useful research frequency baseline; derived list is CC BY-SA 4.0.
commonWords: research-only for this project until replaced/resolved.

## Next canonical gate
Before lesson ordering:
1. replace the commonWords admission gate with a licensing-safe lexical/POS source;
2. define explicit beginner-suitability categories instead of inheriting someone else's subjective filter;
3. enrich authoritative lemma/POS;
4. recompute Target 500;
5. recompute morphology-penalized Matryoshka families.

## v0.3.1 counts
- TARGET: 500
- PRIMARY_BRIDGE: 6
- OPTIONAL_FORM_BRIDGE: 4
- MATRYOSHKA_CORE targets: 108
- MATRYOSHKA_EXTENSION-only targets: 45
- DIRECT_FALLBACK targets: 347

Morphology-partial rows:
- UNRESOLVED_OR_LEMMA: 427
- IRREGULAR_FORM: 23
- INFLECTED_FORM: 23
- FORM_AND_LEMMA: 16
- REGULAR_S_FORM: 14
- IRREGULAR_PLURAL: 3
- SUPPLETIVE_DEGREE: 2
- LEXICALIZED_PLURAL: 1
- REGULAR_ING_FORM: 1
