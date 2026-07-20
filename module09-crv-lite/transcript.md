# Module 09 — Constraint / random lite

**Module id:** module09-crv-lite
**Lab:** crv-lite
**Tracks:** A (local SV TB) · B (browser lab)

## Slide 1 — Constraint / random lite

Constrained random verification picks legal values automatically instead of hand-writing every vector. You declare rand fields, write constraints that shrink the legal set, and call randomize to get a sample—or a failure when constraints conflict. A seed makes rolls reproducible so you can replay a bug. This module is dice-level literacy: data inside zero through fifteen, aligned addresses, paired relations, and one impossible preset—not a commercial solver, but the same vocabulary.

## Slide 2 — Rand, constraints, randomize

A rand field tells the tool this value may change on each randomize call. A constraint block filters the domain—inside a range, modulo alignment, or a relation like data less than len. randomize returns success when at least one legal combination exists, and failure when hard constraints have no intersection. The legal set here is small and discrete; real CRV uses a constraint solver over huge spaces, but the success-or-fail story is the same. Fix a seed before you roll so two runs with the same seed produce the same sample sequence.

## Slide 3 — Browser lab

![Browser lab starter](assets/lab-starter.png)

In the browser lab track, open the constraint random lite lab and load the starter with data inside zero through fifteen and seed forty-two. Read the legal set size versus the full eight-bit domain. Hit randomize once and watch the sample land in range. Try the aligned preset and see only multiples of four. Switch to the pair preset where data must stay below len. Open the conflict preset and confirm randomize fails with an empty legal set. Roll a few times with the same seed, then change the seed and compare histograms.

## Slide 4 — Real SV TB track practice

In the real track, open this module's examples prompts. Restate CRV lite in one sentence—rand fields, constraints, randomize, seed. On paper, write a tiny class with one rand byte and constraint data inside zero through fifteen, then list five legal values. Add a second constraint that conflicts—data inside zero through three and data inside twelve through fifteen—and predict randomize success or failure before you check. Optional: run randomize in a local simulator if you have one; the paper exercise is enough for literacy.

## Slide 5 — Pitfalls to watch

Do not assume randomize always succeeds—over-constraining is a real bug source. Do not forget the seed when you want reproducibility—without it, replaying a failure is guesswork. Do not treat inside as the only constraint form—modulo, inequalities, and cross-field relations all appear in real tests. And remember: the browser dice uses a tiny discrete set; a production solver explores much larger spaces with the same randomize interface.

## Slide 6 — Your turn

Complete the checklist for at least one track—preferably both. In the browser, roll ten samples with seed forty-two on the range preset and name one value that never appeared. On paper, write one solvable constraint and one impossible pair. When you are ready, take the short quiz, then continue to coverpoint and bins in the next module.
