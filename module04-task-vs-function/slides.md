---
marp: true
title: Task vs function
paginate: true
---

# Task vs function

SystemVerilog gives you several procedural shapes, and they are not interchangeable

---

## Timing, return, and synthesis
- Here is the decision table in plain language
- Tasks may use hash-delay and at-events
- Functions must finish in zero simulation time and return a value
- Always_ff and always_comb are for synthesizable RTL
- The browser lab lets you flip between modes and see timing and synthesis roles side by

---

## Browser lab
![Browser lab starter](assets/lab-starter.png)

---

## Real SystemVerilog practice
- In the real SystemVerilog track, open this module's examples prompts
- Restate the core idea in one sentence , when you need to wait, use a task
- Sketch the four shapes on paper using the patterns below
- Optional stretch: mark which lines would fail synthesis if you moved them into RTL
- ```systemverilog // task , may wait

---

## Pitfalls to watch
- Do not put hash-delay or at-events inside a function
- Do not use a task where you only need a pure calculation
- Tasks describe testbench procedures
- And remember

---

## Your turn
- Complete the checklist for at least one track , preferably both
- In the browser, load starter, compare task versus function timing
- On paper, write one task that waits two clock edges and one function that adds two bytes
- When you are ready, take the short quiz, then continue to fork and join in the next module

