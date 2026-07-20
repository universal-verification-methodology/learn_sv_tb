# Module 02 — Self-checking TB

**Module id:** module02-self-check-tb
**Lab:** self-check-tb
**Tracks:** A (local SV TB) · B (browser lab)

## Slide 1 — Self-checking TB

A self-checking testbench compares what the DUT produced against an expected value you computed separately—then reports pass or fail without you staring at every wave. The flow is stimulus, sample outputs after a delay, compute expect with a golden model or reference function, compare got to expect, and tally errors. Display pass on match; error on mismatch; finish when done. This is pre-UVM directed checking—you own the reference, not the wave viewer.

## Slide 2 — Golden expect, not copied output

Starter: AND gate with a equals one and b equals one—expect y equals one. The expect comes from a model—bitwise AND—not from reading y first and calling that the answer. After hash one, if y does not equal expect, error with a message; else display pass. Swap to an adder or mux preset to see wider buses and intentional fail when expect is wrong. The point: checking means an independent reference, even if it is just a one-line function in initial.

## Slide 3 — Browser lab

![Browser lab starter](assets/lab-starter.png)

In the browser lab track, open the self-check TB lab and load the AND starter—inputs one and one, expect one, verdict pass. Toggle stimulus, edit expect, and run check to see pass flip to fail. Try the adder and mux presets to practice wider expect and the error path. Read the TB sketch panel—it shows if-not-equal error else display pass. Challenges quiz you on where expect must come from and what error means versus only watching waves.

## Slide 4 — Real SV TB track practice

In the real track, open this module's examples prompts. Restate self-checking in one sentence—stimulus, golden expect, compare, pass or fail. Sketch a tiny initial block on paper: drive inputs, wait one time unit, compute expect in a variable, compare to DUT output, branch to error or pass display. Optional: name one check you would add to an existing testbench file. No simulator required yet—recognize the pattern when you see it in code.

## Slide 5 — Pitfalls to watch

Do not set expect equal to the DUT output you just sampled—that checks nothing. Do not rely on waves alone for sign-off—automation needs explicit compare and error tally. Do not forget the delay before sample—combinational paths need time to settle; sequential paths need a clock edge. Wrong expect on purpose is good practice—you should see fail and error, not a silent pass. And remember: the browser model is a stand-in; real TBs may use tasks, classes, or scoreboards later.

## Slide 6 — Your turn

Complete the checklist for at least one track—preferably both. In the browser, load starter, run pass, then force a wrong expect and see fail. On paper, write one if-not-equal error else display pass block with inputs and expect labeled. When you are ready, take the short quiz, then continue to clock and reset patterns.
