---
marp: true
title: Virtual interface wiring
paginate: true
---

# Virtual interface wiring

Class-based testbenches need a bridge to the DUT pins

---

## The wiring checklist
- Six steps, in order
- Declare the interface with clock and bus signals
- Instantiate it in the testbench module with clock connected
- Connect DUT ports to interface signals or a modport
- Declare a virtual interface handle inside the driver or monitor class
- Assign the handle , drv dot vif equals bif, or later a config database set and get

---

## Browser lab
![Browser lab starter](assets/lab-starter.png)

---

## Real SystemVerilog practice
- In the real SystemVerilog track, open this module's examples prompts
- Restate the wiring chain in one sentence
- Sketch the UART pattern below on paper and number the six checklist steps next to each
- Optional stretch
- ```systemverilog // 1–2

---

## Pitfalls to watch
- Do not drive DUT ports directly from a class when an interface is the intended boundary
- Do not forget to assign the virtual handle before calling drive tasks
- Do not mix up virtual interface with a plain interface instance
- And remember

---

## Your turn
- Complete the checklist for at least one track , preferably both
- In the browser, load the UART starter, check all six wiring steps
- On paper, draw the signal path from class through virtual handle to DUT pin
- When you are ready

