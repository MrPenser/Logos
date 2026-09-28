# LOGOS — Conscious Learning Cycle

Date: 2026-09-28  
Status: CANONICAL PROJECT WORKING MODEL / RESEARCH HYPOTHESIS  
Scope: conscious, purposeful education and deliberate knowledge acquisition

## 1. Canonical four-function cycle

LOGOS currently models deliberate learning as four fundamental functional classes:

`INTENT -> MATRYOSHKA -> SATOR -> VERIFY -> next cycle if required`

### INTENT
Defines the explicit learning target: what must be understood, mastered, distinguished, remembered, or performed.

### MATRYOSHKA
Creates or presents controlled variation. The learner compares forms, examples, states, contexts, or representations so that relevant differences become observable.

### SATOR
Extracts a **candidate invariant / underlying structure** from those variations. SATOR includes structural, spatial, representational, and contextual invariant extraction.

### VERIFY
Tests whether the candidate knowledge is correct and stable. Verification includes direct correctness, transfer to unseen contexts, and delayed verification through time.

## 2. Boundary of the model

This model is intentionally scoped to **conscious, goal-directed learning / education**. Latent, incidental, unconscious, and spontaneous biological learning are outside the current claim.

The four-function model is canonical inside LOGOS as the current working architecture of deliberate learning. Its universality is **not claimed as scientifically proven**. A genuinely independent fifth function, if found, reopens the model.

## 3. Time is a parameter, not a fifth function

The cycle is executed in time, but time is not currently treated as another cognitive function.

For a learning object or learner, LOGOS may record:

- `t_I` — time required for INTENT;
- `t_M` — time required for MATRYOSHKA;
- `t_S` — time required for SATOR;
- `t_V` — time required for VERIFY;
- `N` — number of complete or partial passes needed for stable success;
- interval/density schedule for repeated verification.

Time and repetition affect convergence speed, retention, and stability. They do not change the four functional classes.

## 4. Transition rule

A learner does **not** move to the next function merely because a fixed amount of time has elapsed.

Transition is criterion-gated:

`function criterion satisfied -> move to next function`

Elapsed time is measured and retained as part of the learner profile.

This allows two learners to traverse the same functional cycle with very different timing distributions.

## 5. Human mnemonic representation — the learning dial

For human teachers and learners, the preferred mnemonic representation is a circular dial:

`INTENT -> MATRYOSHKA -> SATOR -> VERIFY -> INTENT...`

Movement is clockwise. The angular/arc distance assigned to a stage may be drawn proportionally to the time or repeated effort required by a specific learner.

Therefore two learners can share the same topology but have different dial geometry.

The dial is a **human visualization layer**, not a required machine representation.

## 6. Machine representation

A machine may store the same process compactly as state and timing data, for example:

`cycle_id, learner_id, object_id, current_function, stage_start, stage_end, criterion_state, pass_count, context_set, verify_schedule, outcome`

No circular geometry is required for machine execution.

## 7. Individual learning profile

A first minimal profile is:

`P = (t_I, t_M, t_S, t_V, N)`

This replaces coarse labels such as "weak / average / strong" with a functional timing profile.

A learner may be fast in MATRYOSHKA but slow in SATOR, or fast in SATOR but require longer delayed VERIFY. The profile is therefore stage-specific rather than a single scalar ability score.

## 8. Relation to the Stage 0 -> Stage 6 content chain

The four-function cycle and the existing LOGOS learning chain describe different axes:

- `Stage 0 -> Stage 6` describes **what content layer is being opened**;
- `INTENT -> MATRYOSHKA -> SATOR -> VERIFY` describes **how deliberate learning of an object is functionally completed**.

The cycle can therefore operate inside any Stage 0–6 lesson or subtask.

## 9. Cross-project ASTRADELIA bridge

LOGOS may be used as a research lens for future autonomous knowledge formation in ASTRADELIA:

`INTENT -> variation -> invariant extraction -> verification through context/time`

This is **not** a production-runtime change to ASTRADELIA and does not create a new ASTRADELIA block. The bridge remains a research hypothesis until independently validated.
