# Module 11 — SVA implication timeline

**Module id:** module11-sva-timeline
**Lab:** sva-timeline
**Tracks:** A (local / offline) · B (browser lab)

## Slide 1 — SVA implication timeline

You have built directed testbenches, classes, constraints, and coverpoints. Assertions are the next piece: they state what must stay true across clock cycles, not just what one test vector checked. An implication reads as when the antecedent is true, the consequent must hold on a chosen cycle. Overlapping pipe checks the consequent in the same cycle; non-overlapping double arrow checks the next cycle. This module is timeline literacy—pass, fail, and vacuous on a short wave—so you can read SVA in a testbench or a formal sketch without getting lost in syntax.

## Slide 2 — Overlap, next cycle, and vacuous

Here is the starter picture. Antecedent a and consequent b both high at cycle two under overlapping implication—that is a pass. Shift b one cycle later and overlapping fails while non-overlapping can pass. If a never goes high, no attempt fires and the property is vacuously satisfied—technically green, but it proved nothing about b. The lab presets walk overlap pass, overlap fail, next-cycle pass, next-cycle fail, and the all-zero-a vacuous case. Rebuild after you change operator or waves so the verdict panel updates before you trust the color.

## Slide 3 — Browser lab

![Browser lab starter](assets/lab-starter.png)

In the browser lab track, open the SVA timeline sketch and load the starter example. You will see short waves for a and b, a cursor on the evaluation cycle, and a verdict naming pass, fail, or vacuous. Try presets to compare overlapping versus next-cycle behavior, then use the challenge panel to quiz yourself on which operator matches which cycle rule. Step the cursor and rebuild until you can predict the verdict before you press Check.

## Slide 4 — Real shell practice

In the real shell track, open this module's examples prompts. Restate the timeline idea in one sentence—when a is true, b must hold on the cycle the operator chooses. Sketch one worked example on paper: draw eight cycles, mark a and b, and label pass or fail for both overlapping and non-overlapping implication at the cycle where a first rises. Optional stretch: write a property block you would drop into a self-checking testbench later. No full simulator run required yet—the goal is to read SVA timing in your head.

## Slide 5 — Pitfalls to watch

Do not treat overlapping and next-cycle operators as interchangeable—they differ by exactly one cycle. Do not celebrate vacuous green as a design win; if the antecedent never fires, you learned nothing about the consequent. Do not confuse this sketch with full SVA sequences and repetitions—that comes in formal and advanced TB courses. And remember: the browser animator is conceptual; a real testbench still needs clocking, reset, and sensible sampling behind the scenes.

## Slide 6 — Your turn

Complete the checklist for at least one track—preferably both. In the browser, load starter, run the overlap pass and vacuous presets, and clear a couple of challenges on bar arrow versus double arrow. On paper, draw one eight-cycle wave and mark where each operator would pass or fail. When you are ready, take the short quiz, then continue to the testbench versus UVM map.
