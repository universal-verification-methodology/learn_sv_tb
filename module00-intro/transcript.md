# Module 00 — Welcome to SV testbench

**Module id:** module00-intro
**Lab:** none (intro)
**Tracks:** A (local SV TB) · B (browser labs)

## Slide 1 — Welcome to SV testbench

Welcome to learn SV testbench. This course builds directed SystemVerilog testbench literacy—self-checking patterns, classes, constrained random, cover, and SVA—before you jump into UVM or formal flows. The goal is vocabulary and habits you can reuse in Icarus, Verilator, or a commercial simulator, not a full VIP in the browser.

## Slide 2 — What you'll build toward

Across eleven modules you'll map TB anatomy, write self-checks, generate clock and reset, wire file and vector I/O, sketch classes and virtual interfaces, taste CRV and cover bins, read SVA on a timeline, and compare directed TB to UVM. Browser labs teach the idea fast; local sketches keep the fidelity you need when a real compile fails.

## Slide 3 — Two tracks, one idea

Track A is your local toolchain—SystemVerilog testbench files, Make or a course script, and the HDL simulator you already use. Track B is the platform's SV TB concept labs: clickable sketches for anatomy, self-check, clock and reset, and more. You may do either track, or both. A good rhythm is browser first for the picture, then a short offline sketch for muscle memory.

## Slide 4 — Set up Track A

Install the tools named in the course two-tracks doc—Icarus, Verilator, or the browser HDL simulator sibling course if that is your entry point. Open this course folder and skim module READMEs as you go. Optional: run the course module self-check script when you want automated checklist feedback. You are not expected to run a full UVM flow here.

## Slide 5 — Set up Track B

![Tools index](assets/tools-index.png)

From the monorepo, serve the platform folder with a simple local web server, then open the tools index and scroll to the SV testbench section. Labs for TB anatomy, self-check, clock and reset, and later topics are shipped. If you prefer, use the published tools site instead. Either way, confirm you can reach the index—the next module sends you into TB anatomy.

## Slide 6 — How to move through modules

For each module, read the README for the outcome, pick a track—or both—then work the checklist. Prefer Track B when you want graded challenges on structure and timing; prefer Track A when you want compile-and-run fidelity. When you finish this intro checklist, continue to TB anatomy.
