# STATUS — 2026-09-14

## CLOSED / fixed
- Project name: LOGOS.
- "Matryoshka" = Stage 0 mechanism, not whole-project name.
- Stage 0 visual priority fixed.
- Strict +1 letter edge-only rule fixed.
- L/R signature fixed as structural metadata.
- Dictionary represented as DAG, not a list.
- Full learning chain Stage 0 → Stage 6 restored and fixed.

## CURRENT
- Matryoshka Score v1 exists.
- v1 prioritizes frequency utility after visual validity.
- Strong provisional seeds include A, I, HE, AN, AT, NO, ON, ALL, EAR, ILL.
- Depth 3 is current working family limit.

## OPEN
- Matryoshka Score v2: Seed Utility vs Expansion Utility.
- Commercial-safe lexical/frequency source.
- Dictionary Core 300–500.
- Experimental lesson-load validation.
- Stage 1–6 data schema.
- Research branches integration tests.

## UPDATE — 2026-09-16 — LEXICAL GATE v0.4 ESDB
- commonWords removed from active admission logic; retained only in superseded research baselines.
- canonical research lexical gate = ESDB generated American-English default dictionary, ref `rel-2026.02.25`.
- pinned `en_US.txt` blob = `b4222bda8be5826fce1635230f9503234ec31e5a`.
- exact lowercase admission is required; `I` is the capitalization exception.
- one-letter tokens rejected except A/I.
- ESDB lemma and derived-form evidence are both accepted.
- entity-only / abbreviation / affix / non-word / multiword-part analyses do not auto-admit.
- case-frequency collision rule active (e.g. JOHN/LA type collisions).
- SPECIAL_ONLY entries do not auto-enter Target500.
- offensive/vulgar words are not silently removed; admitted items are tagged `RECEPTIVE_ONLY`.
- MASTER20K v0.4: 16,188 admitted.
- MASTER20K Stage-0 strict graph: 7,925 graph members; 5,452 strict directed edges; 3,352 same-lemma/morphology edges flagged separately.
- Target500: exactly 500; cutoff alpha rank 517.
- Target-only non-morph Matryoshka connectivity: 99 targets.
- 24 provisional direct bridge candidates (each touches at least 2 Target500 words); with all candidates present, 127 targets are in multi-target components.
- bridge candidates do not consume Target500 slots and are NOT frozen lesson items.
- v0.3.1 and all commonWords-based cores are superseded for current work.
- current frequency ordering still uses the wordfreq-en-25000 research export; production licensing/compliance remains OPEN.
- next gate: PPP audit of v0.4, then production frequency-source decision, then freeze Target500 v1.0 and lesson ordering.
