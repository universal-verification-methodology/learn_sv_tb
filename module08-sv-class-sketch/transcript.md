# Module 08 — Class / inheritance sketch

**Module id:** module08-sv-class-sketch
**Lab:** sv-class-sketch
**Tracks:** A (local SV TB) · B (browser lab)

## Slide 1 — Class / inheritance sketch

SystemVerilog testbenches lean on classes long before UVM. Two trees matter: objects hold transaction data you construct with new and pass by handle; components live in a hierarchy with build and run roles. Inheritance with extends shares fields and methods; children add protocol-specific members or override virtual tasks. This module is diagram literacy—Packet to UartPacket on the object side, Driver to UartDriver on the component side—so later CRV and UVM names feel familiar.

## Slide 2 — Objects versus components

On the object side, a base class carries a name; Packet adds data and kind fields; UartPacket extends Packet and adds parity. Siblings like SpiPacket share the same parent but different extras—that is specialization, not duplication. On the component side, CompBase knows parent and name; Agent, Driver, and Monitor are peers under it; UartDriver extends Driver and overrides run for baud timing. Objects are data handles you create and pass; components are structural nodes you build once and then run. Extends means the child inherits every member unless it overrides a virtual method.

## Slide 3 — Browser lab

![Browser lab starter](assets/lab-starter.png)

In the browser lab track, open the class sketch lab and load the starter with UartPacket selected on the object tree. Click classes in either tree—object or component—and read fields, methods, and the extends chain. Switch to the component tree and compare Agent, Driver, and Monitor roles. Expand the code sketch panel and note how extends shares members. Work one challenge that names which tree holds transactions versus hierarchy, then use Check.

## Slide 4 — Real SV TB track practice

In the real track, open this module's examples prompts. Restate the two trees in one sentence—objects for data, components for hierarchy. On paper, sketch Packet with two children: UartPacket and SpiPacket, each listing one extra field. Then sketch CompBase with Driver and Monitor as siblings and UartDriver extending Driver with an override note on run. Optional: find one extends in a local testbench or UVM example and label parent and child. No compile required—the goal is to read inheritance, not run a full class runtime.

## Slide 5 — Pitfalls to watch

Do not treat every class as a component—transaction objects are not in the TB hierarchy tree. Do not copy fields into every child when extends already shares them—that is what Packet is for. Do not forget virtual when you mean override—without virtual, a child method hides rather than replaces parent behavior in polymorphic calls. And remember: the browser lab is a diagram aid, not a SystemVerilog simulator executing new and phases.

## Slide 6 — Your turn

Complete the checklist for at least one track—preferably both. In the browser, select UartPacket and state what it inherits from Packet versus what it adds. On paper, draw one object tree and one component tree with extends arrows labeled. When you are ready, take the short quiz, then continue to constraint and random lite in the next module.
