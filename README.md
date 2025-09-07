# Sequence_Detector
---

# Sequence Detector (1010) – Verilog FSM Implementation

A clean and efficient **Finite State Machine (FSM)** in Verilog that detects the binary sequence **`1010`** in a serial input stream. Ideal for showcasing core digital design principles, this project is ready for FPGA deployment and educational presentation.

---

## Project Overview

* **Goal**: Detect the `1010` bit sequence using a Moore FSM.
* **Language**: 100% Verilog ([GitHub][1])
* **Contents**:

  * `sequ_1010.v` – FSM design in Verilog
  * `sequ_1010_tb.v` – Testbench for simulation
  * `sequence Detector WF.png` – Simulation waveform illustrating detection ([GitHub][1])

---

## Key Features

* Moore FSM detecting `1010`
* Synchronous design (clocked, resettable)
* Testbench for automated validation
* Waveform output for visual verification

---

## Repository Structure

```
Sequence_Detector/
│── sequ_1010.v           # Verilog design (Moore FSM)
│── sequ_1010_tb.v        # Verilog testbench
│── sequence Detector WF.png  # Simulation waveform
│── README.md             # Project documentation
```

---

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/SivaKarthik9804/Sequence_Detector.git
cd Sequence_Detector
```

### 2. Simulate the Design

Using Xilinx Vivado :

```bash
iverilog -o seq_detector sequ_1010.v sequ_1010_tb.v
vvp seq_detector
gtkwave dump.vcd
```

Review the waveform (`sequence Detector WF.png`) to confirm detection of `1010`.

### 3. Deploy on FPGA (Optional)

* Import `sequ_1010.v` into your FPGA tool (e.g., Vivado).
* Map input/output pins and define clock/reset.
* Synthesize → Implement → Generate bitstream → Program board.

---

## How It Works (Overview)

1. **Idle State**: Waiting for input.
2. **State Transitions**: On receiving `1`, `0`, `1`, then `0` in sequence, transitions progress.
3. **Detection**: When FSM enters the final state, output asserted.
4. **Reset Behavior**: Recognizes only full, non-overlapping matches and resets cleanly.

In a Moore FSM, the output is tied to the current state, ensuring stable detection driven by state logic.

---

## Applications & Extensions

* **Applications**:

  * Communication protocol decoders
  * Pattern recognition in digital systems
  * Educational FSM prototype

* **Future Enhancements**:

  * Convert to **Mealy FSM** for optimized latency
  * Parameterized sequence length (e.g., detect `1101`, `1010`, etc.)
  * FPGA deploy with buttons/LED indicators for live input
  * Expand flow using Yosys + OpenLane for ASIC targeting

---

## Author

* **Siva Karthik**
  ECE Student | Aspiring VLSI Innovator
  GitHub: [SivaKarthik9804](https://github.com/SivaKarthik9804)

---

