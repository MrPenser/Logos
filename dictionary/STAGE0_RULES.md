# Stage 0 — Strict Matryoshka Rules

## Edge predicate
u → v iff:
- len(v) = len(u) + 1
- v = c + u OR v = u + c
- c is one letter
- v is a valid English word

Operations:
- L+1
- R+1

Forbidden:
- internal insertion
- substitution
- transposition
- rearrangement
- +2 or more letters in one step

## Ranking priority
1. Visual validity / closeness
2. Frequency / usefulness
3. Chain length / graph density
4. Bidirectional visual recoverability
5. Semantic coherence only as bonus

## Graph
Directed acyclic graph.
Branches and merges are allowed.
Cycles are impossible under pure growth.

## L/R signature
Example:
I → IN → PIN → PINE → SPINE
R L R L
