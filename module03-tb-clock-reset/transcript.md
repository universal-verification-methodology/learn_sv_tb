# Module 03 — Clock + reset patterns

**Module id:** module03-tb-clock-reset
**Lab:** tb-clock-reset
**Tracks:** A (local SV TB) · B (browser lab)

## Slide 1 — Clock and reset in the TB

Most sequential DUTs need a free-running clock and a reset sequence before stimulus. Classic pattern: initialize clock low, forever toggle with half-period delays; assert reset active-low, hold for N posedges, then deassert. The TB generates both— the DUT does not supply your clock. Reset length and release timing matter: too short and flops never leave reset; async release mid-cycle can surprise flops that sample on posedge. This module is literacy for those TB generators.

## Slide 2 — Assert, hold, sync release

Starter: active-low reset rst_n starts at zero while clock toggles. Hold reset across two posedges—count rising clock edges while rst_n stays low—then drive rst_n high on a posedge for sync-style release. The wave panel shows half-period clock phases and where reset rises relative to edges. Compare to async release preset where rst_n rises between edges—legal sometimes, risky for posedge flops. Also try hold-forever and no-reset presets to see idle and stuck-in-reset behavior.

## Slide 3 — Browser lab

![Browser lab starter](assets/lab-starter.png)

In the browser lab track, open the clock and reset lab and load the classic starter. Step the cursor through half-cycles; watch posedge markers and when rst_n deasserts. Switch presets—async mid-cycle release, long assert, idle with no reset—and read the note panel. Challenges ask how many posedges reset stayed asserted and whether release was sync or async. Use the source sketch to connect the animation to forever clock toggle and repeat posedge hold loops.

## Slide 4 — Real SV TB track practice

In the real track, open this module's examples prompts. Restate clock-plus-reset in one sentence—free-running clk, assert reset N cycles, deassert. Sketch two initial blocks on paper: one forever toggling clock with hash delays, one asserting rst_n, repeating posedge wait, then releasing. Optional: note whether your DUT expects sync or async reset from the datasheet. No compile required yet—recognize the twin initial pattern in real testbenches.

## Slide 5 — Pitfalls to watch

Do not release reset on the wrong edge if your DUT samples sync reset on posedge clk—async release mid-cycle can violate assumptions. Do not hold reset zero forever and wonder why nothing runs—the hold-forever preset shows that trap. Do not forget clock starts defined—unknown X on clk breaks edge detection in some tools. Mixing active-high and active-low reset names without reading the DUT causes silent mismatches. And remember: the browser uses a fixed half-period grid; real TBs still need timescale and period math.

## Slide 6 — Your turn

Complete the checklist for at least one track—preferably both. In the browser, load classic starter, count two assert posedges, and try async versus sync release presets. On paper, draw clk and rst_n for two cycles of assert then sync release. When you are ready, take the short quiz, then continue to file and vector I/O.
