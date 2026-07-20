---
marp: true
title: Clock and reset in the TB
paginate: true
---

# Clock and reset in the TB

Most sequential DUTs need a free-running clock and a reset sequence before stimulus

---

## Assert, hold, sync release
- Starter: active-low reset rst_n starts at zero while clock toggles
- Hold reset across two posedges
- The wave panel shows half-period clock phases and where reset rises relative to edges
- Compare to async release preset where rst_n rises between edges
- Also try hold-forever and no-reset presets to see idle and stuck-in-reset behavior

---

## Browser lab
![Browser lab starter](assets/lab-starter.png)

---

## Real SV TB track practice
- In the real track, open this module's examples prompts
- Restate clock-plus-reset in one sentence
- Sketch two initial blocks on paper
- Optional: note whether your DUT expects sync or async reset from the datasheet
- No compile required yet, recognize the twin initial pattern in real testbenches

---

## Pitfalls to watch
- Do not release reset on the wrong edge if your DUT samples sync reset on posedge clk
- Do not hold reset zero forever and wonder why nothing runs
- Do not forget clock starts defined, unknown X on clk breaks edge detection in some tools
- Mixing active-high and active-low reset names without reading the DUT causes silent
- And remember

---

## Your turn
- Complete the checklist for at least one track, preferably both
- In the browser, load classic starter, count two assert posedges
- On paper, draw clk and rst_n for two cycles of assert then sync release
- When you are ready, take the short quiz, then continue to file and vector I/O

