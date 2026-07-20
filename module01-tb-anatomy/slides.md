---
marp: true
title: TB anatomy
paginate: true
---

# TB anatomy

A SystemVerilog testbench is a simulation-only wrapper around a design under test

---

## Classic AND testbench sketch
- Starter picture: a tiny AND gate DUT with inputs a and b and output y
- In the TB, a and b are regs, you procedural-assign them in initial
- Y is a wire, the DUT drives it; the TB reads it but does not assign it
- The instance wires ports: dut dot a to a, dut dot b to b, dut dot y to y
- An initial block applies vectors with hash delays, display the result, then finish
- Step the timeline and you see stimulus, propagation, print, and end-of-sim in order

---

## Browser lab
![Browser lab starter](assets/lab-starter.png)

---

## Real SV TB track practice
- In the real track, open this module's examples prompts
- Restate TB anatomy in one sentence, wrapper, stimulus, DUT, observe, finish
- Sketch the AND testbench on paper
- Optional: map the same regions to a cocotb or Verilator test you already have
- No full compile required yet, the goal is to recognize the skeleton in real code

---

## Pitfalls to watch
- Do not procedural-assign a wire in initial, that is a classic compile or runtime mistake
- Do not drive a DUT output from the TB
- Do not confuse the DUT module with the TB module, only the wrapper is simulation-only
- And remember

---

## Your turn
- Complete the checklist for at least one track, preferably both
- In the browser, load starter, step through display and finish
- On paper, draw one TB block diagram with stimulus, DUT, and observe labeled
- When you are ready, take the short quiz, then continue to self-checking testbenches

