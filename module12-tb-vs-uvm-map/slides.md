---
marp: true
title: TB vs UVM map
paginate: true
---

# TB vs UVM map

You have written flat directed testbenches, clock and reset, tasks, fork-join, classes, constraints, cover

---

## Six pairs to connect
- The lab lines up six classic roles with UVM counterparts
- Pin drive maps to driver plus virtual interface
- Fixed stimulus lists map to sequence plus sequencer
- Wire peeks with display map to monitor plus analysis port
- Inline expect maps to scoreboard
- One flat testbench module maps to environment plus agent hierarchy

---

## Browser lab
![Browser lab starter](assets/lab-starter.png)

---

## Real shell practice
- In the real shell track, open this module's examples prompts
- What you do today in directed style, and which UVM role would absorb that job
- Optional stretch
- No UVM compile required, the exercise is naming and boundaries

---

## Pitfalls to watch
- Do not assume UVM replaces thinking, it replaces ad-hoc structure with reusable components
- Do not map buzzwords without behavior
- Do not skip directed TB fluency
- And do not treat this sketch as a production testbench generator, it is a concept map
- Real UVM still needs phases, objections, config database, and offline sim discipline

---

## Your turn
- Complete the checklist for at least one track
- In the browser
- Take one habit from your own directed TB and write the UVM role that would own it
- Take the short quiz

