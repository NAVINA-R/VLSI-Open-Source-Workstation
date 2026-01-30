# OpenLane Flow Explanation

OpenLane is an open-source automated RTL-to-GDSII
digital ASIC design flow. It integrates multiple
open-source tools to convert Verilog RTL code into
a manufacturable chip layout.

---

## 1. RTL Design
The design process starts with writing Verilog
code that describes the digital logic of the circuit.

Input:
- Verilog RTL files

Output:
- Functional RTL design

---

## 2. Synthesis
RTL code is synthesized into a gate-level netlist
using Yosys. Logic optimization and technology
mapping are performed in this stage.

Tool Used:
- Yosys

Output:
- Gate-level netlist

---

## 3. Floorplanning
Floorplanning defines the chip area, pin locations,
and placement of major blocks.

Key Tasks:
- Define core area
- Set power and ground structure
- Place I/O pins

Output:
- Initial physical layout structure

---

## 4. Placement
Standard cells from the synthesized netlist are
placed within the defined floorplan while
optimizing timing and congestion.

Output:
- Placed design

---

## 5. Clock Tree Synthesis (CTS)
CTS builds a balanced clock network to ensure
minimum clock skew and reliable timing.

Output:
- Clock-distributed design

---

## 6. Routing
Interconnections between placed cells are
created using global and detailed routing.

Output:
- Fully routed design

---

## 7. DRC (Design Rule Check)
DRC ensures the layout follows fabrication
rules defined by the PDK.

Tool Used:
- Magic

Output:
- DRC-clean layout

---

## 8. LVS (Layout Versus Schematic)
LVS verifies that the layout matches the
original synthesized netlist.

Tool Used:
- Netgen

Output:
- LVS-clean design

---

## 9. GDSII Generation
The final verified layout is exported as a
GDSII file, which is used for fabrication.

Final Output:
- GDSII file

---

## Summary
OpenLane provides a complete RTL-to-GDS flow
using open-source tools, enabling students
and researchers to experience real-world
ASIC design methodologies.
