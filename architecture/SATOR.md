# LOGOS — SATOR Functional Model

Date: 2026-09-28  
Status: CANONICAL PROJECT WORKING DEFINITION / RESEARCH HYPOTHESIS

## 1. Function

SATOR is the LOGOS function that extracts a **candidate invariant / underlying structure** from a set of deliberately or naturally varied representations.

Minimal form:

`SATOR(X1, X2, ... Xn; contexts) -> {candidate_invariant, validity_scope, unresolved_cases}`

SATOR does not declare truth. It produces the structure that VERIFY must subsequently test.

## 2. Input boundary

SATOR receives variation exposed by MATRYOSHKA. Variation may include:

- geometric or spatial transformation;
- change of form or representation;
- change of example while preserving a target relation;
- change of semantic or practical context;
- change of state or trajectory.

The key question is not merely "what changed?" but:

**What remains the same across the relevant changes?**

## 3. Output

A SATOR result should preserve at least:

- `candidate_invariant` — the hypothesized stable relation/rule/structure;
- `validity_scope` — where the invariant is currently believed to apply;
- `supporting_variants` — which variations produced it;
- `unresolved_cases` / candidate counterexamples;
- provenance references sufficient for later VERIFY.

## 4. Contextual SATOR

SATOR is not limited to geometric transformation.

`CONTEXTUAL_SATOR` asks whether the same underlying structure can be recovered across different contexts or representations.

This does **not** collapse SATOR into VERIFY.

Boundary:

- **SATOR** infers a candidate invariant from the available comparison set.
- **VERIFY** challenges that candidate on held-out/new contexts, independent evidence, and later time points.

Thus contextual extraction and contextual verification are complementary but distinct.

## 5. Relation to MATRYOSHKA

MATRYOSHKA and SATOR form a paired mechanism:

`controlled variation -> invariant extraction`

MATRYOSHKA makes discriminating differences visible. SATOR compresses those differences into a candidate rule that can generalize beyond the examples.

Without variation, an apparent rule may be accidental. Without invariant extraction, variation remains a set of examples rather than understanding.

## 6. Relation to VERIFY

A SATOR output remains provisional until VERIFY succeeds.

Typical path:

`MATRYOSHKA variants -> SATOR invariant candidate -> contextual transfer test -> delayed verification -> accepted/revised/rejected knowledge`

A failed VERIFY returns information to a new learning cycle; it does not retroactively turn the failed candidate into knowledge.

## 7. Human teaching use

For a teacher, a SATOR bottleneck means the learner can inspect examples and differences but has not yet extracted the stable relation that unifies them.

The response should therefore be to change or improve the comparison set, representation, or contextual contrast—not merely to repeat the same explanation unchanged.

## 8. Machine use

Machines do not require the circular mnemonic visualization. SATOR can be represented as an operator over evidence-linked variants with explicit outputs and timestamps.

A future implementation may record:

`input_variant_ids, context_ids, candidate_invariant_id, scope, counterexample_ids, confidence/evidence_state, created_at`

This schema is illustrative, not yet a production data contract.

## 9. Scientific status and falsifiability

SATOR is canonical inside LOGOS as the current functional definition, but its claim to universality remains testable.

The model must be reopened if controlled study finds a reproducible class of successful conscious, purposeful learning in which stable knowledge is acquired while no operation reasonably equivalent to invariant/structure extraction occurs, or if a separate irreducible function is required between MATRYOSHKA and VERIFY.

## 10. ASTRADELIA bridge

SATOR is a candidate research lens for future autonomous knowledge formation in ASTRADELIA: extracting stable structure from alternative hypotheses, contexts, trajectories, or observations before independent verification.

This is a cross-project research correspondence only. It does not alter ASTRADELIA production architecture or promote SATOR to a runtime component there.
