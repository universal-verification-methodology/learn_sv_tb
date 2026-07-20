# Module 00: Welcome to SV testbench

**Kind:** `intro`

← Start · [Course README](../README.md) · [TB anatomy →](../module01-tb-anatomy/README.md)

## What this course is

**learn_sv_tb** — Directed SystemVerilog testbench literacy — self-check, classes, CRV, cover, SVA — before UVM.

| Track | Where you practice | Best for |
|-------|--------------------|----------|
| **A** | Local SV TB sketches (iverilog / Verilator / HDL Simulator) | Muscle memory you keep |
| **B** | Browser SV TB & assertion sketches | Fast intuition |

Next after this course: **learn_uvm2017**, **learn_formal**.

## Setup (Track A)

1. Install the local tools named in [docs/TWO_TRACKS.md](../docs/TWO_TRACKS.md).
2. Open this repo at `courses/learn_sv_tb`.

## Setup (Track B)

1. Serve the platform: `python -m http.server 8080 --directory platform` (from monorepo root).
2. Open http://127.0.0.1:8080/tools/index.html
3. Live: [learning/tools](https://universal-verification-methodology.github.io/learning/tools/).

## How to move through modules

1. Read the module **README** (outcomes).
2. Pick Track A, Track B, or both.
3. Check off **CHECKLIST.md**.
4. Optional: expand `transcript.md` / `outline.yaml` with **module-slides** in the parent monorepo.

## Media

| Artifact | Path |
|----------|------|
| Transcript | [transcript.md](transcript.md) |
| Outline | [outline.yaml](outline.yaml) |
| Slides | [slides.pptx](slides.pptx) · [slides.pdf](slides.pdf) |
| Video | [video.mp4](video.mp4) |
| Quiz | [quiz.json](quiz.json) |

## Files

```
module00-intro/
├── README.md
├── CHECKLIST.md
├── EXAMPLES.md
├── outline.yaml
├── transcript.md
└── quiz.json
```

## Next

→ [TB anatomy →](../module01-tb-anatomy/README.md)
