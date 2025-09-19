# Digital SoC Design Flow: From Concept to GDSII

This document outlines the structured workflow for designing a System-on-Chip (SoC), from high-level specification to the final manufacturing-ready file. Each stage is an essential and equal part of the complete design journey.

### **`O1` | Architecture & High-Level Modelling**

This is the conceptual stage. Before writing any hardware code, we define and verify the chip's intended behavior at a high level.

* **Input:** System Specifications.
* **Process:** Model the chip's functionality using a high-level language (`C Model`).
* **Verification:** Create a `C Testbench` to validate the model's logic and behavior.
* **Output:** A verified architectural model.

### **`O2` | RTL Design & Pre-Synthesis Verification**

Here, the architectural model is translated into a hardware description language (HDL), describing the actual digital circuits.

* **Input:** Verified architectural model.
* **Process:** Write the Register-Transfer Level (RTL) code in `Verilog`. This describes the flow of data between registers and the logic that processes it.
* **Verification:**
    * **`iverilog`:** Simulate the Verilog code to check for logical correctness.
    * **`GTKWave`:** Visualize the simulation output to debug and analyze signal behavior.
* **Output:** Functionally correct and verified RTL code.

### **`O3` | Physical Design: Synthesis to Tapeout**

This is the back-end flow, where the abstract RTL code is transformed into a physical, geometric layout. This is the `RTL2GDS` stage.

* **1. Synthesis**
    * **Tool:** `Yosys`
    * **Action:** Translates the Verilog RTL into a `Gate-Level Netlist`—a list of standard logic gates and their interconnections.
* **2. Physical Layout**
    * **Tool:** `Magic`
    * **Action:**
        * **Floorplanning:** Arranging blocks (`Processor`, `IPs`) on the silicon die.
        * **Placement:** Placing individual standard cells (logic gates).
        * **Routing:** Drawing the metal wires to connect everything.
* **3. Post-Layout Verification**
    * **Tool:** `ngspice`, DRC/LVS Checkers
    * **Action:** Analyze the final layout for timing, power, and manufacturing rule violations.
* **Final Output:** `GDSII` — The master file sent to the foundry for chip fabrication.

### **`O4` | The Final Product: Integrated SoC**

This represents the final, tangible outcome of the entire design process: a functional chip ready for real-world application.

* **Result:** A complete SoC with a central processor and integrated peripherals.
* **Performance:** Designed to operate in the `100MHz to 130MHz` frequency range.
* **Applications:** This versatile SoC can be the core of various systems, including:
    * Wearables (e.g., iWatch)
    * Prototyping platforms (e.g., Arduino boards)
    * Consumer electronics (e.g., TV panels)
    * Control systems (e.g., AC applications)

---

This principle signifies that every stage—from the initial C model to the final application—is equally critical. A flaw in any one stage invalidates the entire effort. The process is a unified whole, not just a sequence of steps.
