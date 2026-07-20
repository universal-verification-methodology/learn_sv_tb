# learn_sv_tb

[![GitHub](https://img.shields.io/badge/GitHub-learn__sv__tb-181717?logo=github)](https://github.com/universal-verification-methodology/learn_sv_tb)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-green?logo=creativecommons&logoColor=white)](LICENSE)
[![Role](https://img.shields.io/badge/role-course%20scaffold-orange)](https://github.com/universal-verification-methodology/learning)
[![Parent](https://img.shields.io/badge/parent-learning%20monorepo-0A9EDC)](https://github.com/universal-verification-methodology/learning)
[![Labs](https://img.shields.io/badge/labs-GitHub%20Pages-222?logo=githubpages)](https://universal-verification-methodology.github.io/learning/tools/)
[![Domain](https://img.shields.io/badge/domain-SV%20TB%20%7C%20SVA%20%7C%20CRV-purple)](https://github.com/universal-verification-methodology/learn_sv_tb)

**learn_sv_tb** is the open learning path for *Directed TB → CRV → SVA → cover (before UVM)*.

Authors rebuild slides/audio with **module-slides** in the parent monorepo.

## Table of contents

- [Contents](#contents)
- [Browse or clone](#browse-or-clone)
- [Author: module-slides](#author-module-slides)
- [Two learning tracks](#two-learning-tracks)
- [Module landings](#module-landings)
- [Browser labs](#browser-labs)
- [License](#license)

## Contents

```text
learn_sv_tb/
├── README.md
├── LICENSE
├── docs/
│   ├── MODULES.md
│   └── TWO_TRACKS.md
├── scripts/
│   └── module.sh
├── module00-intro/
├── module01-tb-anatomy/
├── module02-self-check-tb/
├── module03-tb-clock-reset/
├── module04-file-vector-io/
├── module05-vif-wiring/
├── module06-sv-class-sketch/
├── module07-crv-lite/
├── module08-cover-bins/
├── module09-sva-timeline/
├── module10-tb-vs-uvm-map/
└── module11-wrap/
```

## Browse or clone

- **Browser labs:** [https://universal-verification-methodology.github.io/learning/tools/](https://universal-verification-methodology.github.io/learning/tools/)
- **Syllabus:** [`syllabus.md` § learn_sv_tb](https://github.com/universal-verification-methodology/learning/blob/main/syllabus.md#16-learn_sv_tb)

```bash
git clone --recurse-submodules \
  git@github.com:universal-verification-methodology/learning.git
ls courses/learn_sv_tb
./scripts/module.sh 01 --check
```

## Author: module-slides

```bash
cd ../..   # monorepo root
python .cursor/skills/module-slides/scripts/transcript_to_outline.py \
  courses/learn_sv_tb/module01-tb-anatomy
bash .cursor/skills/module-slides/scripts/narrate_clips.sh \
  courses/learn_sv_tb/module01-tb-anatomy
```

## Two learning tracks

Details: [docs/TWO_TRACKS.md](docs/TWO_TRACKS.md).

| Track | Practice surface | Start here |
|-------|------------------|------------|
| **A** | Local SV TB sketches (iverilog / Verilator / HDL Simulator) | [docs/TWO_TRACKS.md](docs/TWO_TRACKS.md) |
| **B** | Browser SV TB & assertion sketches | [tools index](https://universal-verification-methodology.github.io/learning/tools/) |

## Module landings

Full status table: **[docs/MODULES.md](docs/MODULES.md)**.

| Module | Landing |
|--------|---------|
| 00 — Welcome to SV testbench | [module00-intro](module00-intro/README.md) |
| 01 — TB anatomy | [module01-tb-anatomy](module01-tb-anatomy/README.md) |
| 02 — Self-checking TB | [module02-self-check-tb](module02-self-check-tb/README.md) |
| 03 — Clock + reset patterns | [module03-tb-clock-reset](module03-tb-clock-reset/README.md) |
| 04 — File / vector I/O | [module04-file-vector-io](module04-file-vector-io/README.md) |
| 05 — Virtual interface wiring | [module05-vif-wiring](module05-vif-wiring/README.md) |
| 06 — Class / inheritance sketch | [module06-sv-class-sketch](module06-sv-class-sketch/README.md) |
| 07 — Constraint / random lite | [module07-crv-lite](module07-crv-lite/README.md) |
| 08 — Coverpoint / bins | [module08-cover-bins](module08-cover-bins/README.md) |
| 09 — SVA implication timeline | [module09-sva-timeline](module09-sva-timeline/README.md) |
| 10 — TB vs UVM map | [module10-tb-vs-uvm-map](module10-tb-vs-uvm-map/README.md) |
| 11 — SV TB complete | [module11-wrap](module11-wrap/README.md) |

## Browser labs

**Shipped:** [tb-anatomy](https://universal-verification-methodology.github.io/learning/tools/tb-anatomy/) · [self-check-tb](https://universal-verification-methodology.github.io/learning/tools/self-check-tb/) · [tb-clock-reset](https://universal-verification-methodology.github.io/learning/tools/tb-clock-reset/) · [file-vector-io](https://universal-verification-methodology.github.io/learning/tools/file-vector-io/) · [vif-wiring](https://universal-verification-methodology.github.io/learning/tools/vif-wiring/) · [sv-class-sketch](https://universal-verification-methodology.github.io/learning/tools/sv-class-sketch/) · [crv-lite](https://universal-verification-methodology.github.io/learning/tools/crv-lite/) · [cover-bins](https://universal-verification-methodology.github.io/learning/tools/cover-bins/) · [sva-timeline](https://universal-verification-methodology.github.io/learning/tools/sva-timeline/) · [tb-vs-uvm-map](https://universal-verification-methodology.github.io/learning/tools/tb-vs-uvm-map/).

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — see [`LICENSE`](LICENSE).
