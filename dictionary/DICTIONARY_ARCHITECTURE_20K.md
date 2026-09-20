LOGOS — DICTIONARY ARCHITECTURE v0.1
Date: 2026-09-14

DECISION
The LOGOS dictionary is built as a 20,000-word MASTER LEXICON from the beginning.
3,000–5,000 words are NOT a system limit. They were only benchmark ranges used to optimize and validate Stage 0.

MASTER STRUCTURE

Tier A — STARTER CORE
Target: 300–500 very frequent words.
Purpose: first learner-visible Stage 0 vocabulary.
Selection: strongest visual Matryoshka families + usefulness + recoverability.

Tier B — BASIC 1K
Target: first ~1,000 frequent words.
Purpose: basic comprehension and first phrase-building.

Tier C — CORE 3K
Target: first ~3,000 frequent words.
Purpose: broad everyday vocabulary.

Tier D — EXTENDED 5K
Target: first ~5,000 frequent words.
Purpose: mature general vocabulary and richer Stage 1–4 expansion.

Tier E — ADVANCED 10K
Target: first ~10,000 frequent words.
Purpose: advanced reading/listening, semantic and collocational coverage.

Tier F — MASTER 20K
Target: first ~20,000 ranked words.
Purpose: full LOGOS lexical backend and future Stage 1–6 expansion.

IMPORTANT
A word does NOT need to belong to a Matryoshka chain to exist in the MASTER LEXICON.
Stage 0 membership is metadata, not an admission criterion to the dictionary.

CURRENT COMPUTATIONAL SNAPSHOT
Source benchmark: wordfreq 25k export intersected with current common-word filter.
TOP 500: 482 filtered words; 141 in strict L/R graph.
TOP 1,000: 940 filtered; 279 in graph.
TOP 3,000: 2,765 filtered; 1,055 in graph.
TOP 5,000: 4,508 filtered; 1,908 in graph.
TOP 10,000: 8,515 filtered; 3,938 in graph.
TOP 20,000: 15,041 filtered; 7,029 in graph; 4,778 strict directed edges.

These numbers are research-baseline figures, not final production counts. Final production corpus requires a licensing-safe lexical/frequency source.

WORD RECORD — TARGET SCHEMA
Each word in MASTER 20K should support:

IDENTITY
- word
- lemma
- part_of_speech
- inflection/derived flag
- frequency rank
- frequency score
- source/provenance

STAGE 0
- strict Matryoshka parents
- strict Matryoshka children
- L/R edge operation
- all known L/R paths
- family depth
- graph component
- Seed Utility
- Expansion Utility
- Density
- Recoverability
- Stage0 eligibility
- learner tier

STAGE 1
- core meanings
- main parts of speech
- base translation/gloss

STAGE 2
- semantic extensions
- polysemy map
- metaphorical/derived senses

STAGE 3
- collocations
- fixed/semi-fixed phrases
- frequency/usefulness

STAGE 4
- phrasal verbs
- particle combinations
- sense separation

STAGE 5
- idioms
- fixed expressions
- compositionality flag

STAGE 6
- register
- nuance
- near-synonym contrasts
- native-like usage notes
- C1-level patterns

DESIGN PRINCIPLE
MASTER 20K = storage/research universe.
Tier A 300–500 = first learning surface.
The learner progresses through tiers; the backend does not need to be rebuilt later.

NEXT
1. Build Matryoshka Score v2.
2. Choose licensing-safe production lexical/frequency source.
3. Generate MASTER 20K records.
4. Populate Stage 0 graph for all eligible words.
5. Derive Tier A 300–500 from the master graph.
