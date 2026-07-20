---
marp: true
title: Coverpoint / bins
paginate: true
---

# Coverpoint / bins

Functional coverage asks whether you exercised interesting values, not just whether the test passed

---

## Coverpoints, bins, holes
- A covergroup wraps one or more coverpoints
- Each coverpoint names a signal or slice, here data three colon zero, the low four bits
- Bins group values: low covers zero through three, mid covers four through seven, and so on
- When you sample a value, every bin that contains it gets a hit
- A hole is a defined bin with zero hits after your tests
- This lab stays with single coverpoints

---

## Browser lab
![Browser lab starter](assets/lab-starter.png)

---

## Real SV TB track practice
- In the real track, open this module's examples prompts
- Restate coverpoint literacy in one sentence
- On paper, write a coverpoint on a two-bit opcode with idle, read, write
- List three sample sequences and mark which bins each sequence hits
- Sketch one hole you would close by adding a directed test
- Map the same bin names to a coverage section in a verification plan you have seen

---

## Pitfalls to watch
- Do not confuse a hole with an ignorable value
- Do not assume one hundred percent bin hit means done
- Do not sample randomly without a plan
- And remember

---

## Your turn
- Complete the checklist for at least one track, preferably both
- In the browser
- On paper, write one coverpoint with four bins and mark which bin value seven hits
- When you are ready

