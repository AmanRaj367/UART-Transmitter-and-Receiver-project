# UART-Transmitter-and-Receiver-project

This project implements a basic **UART (Universal Asynchronous Receiver/Transmitter)** protocol system using Verilog HDL. The system includes both transmitter and receiver modules, fully verified via a testbench and waveform simulation using Icarus Verilog and GTKWave.

---

##  Project Objective

To design and simulate a **UART communication system** that can:
- Transmit and receive 8-bit serial data
- Support start and stop bits
- Operate at a configurable baud rate
- Use FSMs (Finite State Machines) for TX and RX logic

---

##  Project Architecture

The UART system consists of the following components:

1. **UART Transmitter (TX)**
   - Shifts out serial bits including start and stop
   - FSM handles states: IDLE → START → DATA → STOP

2. **UART Receiver (RX)**
   - Samples serial input and reconstructs the byte
   - FSM handles states: IDLE → START → DATA → STOP

3. **Baud Rate Generator**
   - Generates timing pulses according to the desired baud rate (e.g., 9600 bps)

4. **Testbench**
   - Stimulates TX with data and connects output to RX input
   - Verifies full communication loop

---

##  File Structure

```txt
├── uart_tx.v           # UART transmitter module
├── uart_rx.v           # UART receiver module
├── baud_generator.v    # Baud rate divider
├── uart_top.v          # Top-level integration
├── uart_tb.v           # Testbench for full simulation
├── uart_wave.vcd       # Waveform output (generated)
└── README.md           # This file
```

---

## Simulation Guide
- Icarus Verilog
- GTKWave

---

## Author
- Aman Raj
- Github : AmanRaj367
