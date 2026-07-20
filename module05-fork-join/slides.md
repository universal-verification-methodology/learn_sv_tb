---
marp: true
title: Fork / join
paginate: true
---

# Fork / join

When a testbench needs parallel activity

---

## When the parent resumes
- Picture two forked threads: A takes thirty time units, B takes ten
- Under join, the parent resumes at thirty , the maximum
- Under join_any, the parent resumes at ten , the minimum
- Under join_none, the parent resumes at zero while both children continue
- That difference drives real testbench structure

---

## Browser lab
![Browser lab starter](assets/lab-starter.png)

---

## Real SystemVerilog practice
- In the real SystemVerilog track, open this module's examples prompts
- Restate when you would pick each join flavor , all done, first done, or no wait
- Sketch the fork block below on paper and write the resume time for each keyword with A
- Optional stretch
- ```systemverilog // fork-join , parent waits for ALL children (max time) fork begin #30

---

## Pitfalls to watch
- Do not assume join_any stops the other threads
- Do not use join_none when the parent must observe child results before continuing
- Do not forget that resume time depends on the slowest or fastest child, not an average
- And remember

---

## Your turn
- Complete the checklist for at least one track , preferably both
- In the browser, load starter, step through join and join_any
- On paper, write a fork block with two delays and label where the parent prints under all
- When you are ready

