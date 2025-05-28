# Simple-Vending-Machine-FPGA-logic-FSM
# VHDL Vending Machine FSM

This project implements a **finite state machine (FSM)** for a digital vending machine using **VHDL**. The vending machine accepts coins—nickels (5¢), dimes (10¢), and quarters (25¢)—and processes purchases once at least 20¢ has been inserted. If 25¢ is inserted, the system returns 5¢ as change.

>  **Project Date**: May 2025  
>  **Course**: ECEN 474 – Digital System Design  
>  **Author**: Gael Oswaldo Perez Alvarez  

---

## Features

- Written in **VHDL** (VHSIC Hardware Description Language)
- FSM with 7 defined states based on accumulated coin value
- Accepts multiple coin inputs:
  - `00`: No coin
  - `01`: Quarter (25¢)
  - `10`: Nickel (5¢)
  - `11`: Dime (10¢)
- Activates a **purchase signal (A)** at ≥ 20¢
- Returns **change (C)** when applicable
- **Reset functionality** to clear state
- Fully simulated using **Intel Quartus Prime** and the **University Waveform tool**

---
## FSM Design Summary

The state machine is designed around these core ideas:

- **States** represent total inserted value (`S0`, `S5`, `S10`, ..., `S30`)
- **Transitions** depend on binary-encoded coin input (`inputOne`, `inputTwo`)
- **Output Conditions**:
  - `A = '1'` → Purchase valid (≥ 20¢)
  - `C = '1'` → Change due (when more than 20¢ is inserted)
- The machine **resets to `S0`** after a valid transaction or when `R = '1'`


---

##  Getting Started

###  Requirements

- [Intel Quartus Prime](https://www.intel.com/content/www/us/en/software-kit/752917/intel-quartus-prime-lite-edition-design-software.html) (Lite Edition recommended)
- Basic knowledge of FSMs and VHDL


## Resources and References
IEEE Std 1076™-2008: VHDL Language Reference Manual

Intel Quartus Prime Documentation

FSM Design Techniques

VHDL Coin Vending FSM Example


Let me know if you'd like this bundled into a downloadable file or want me to help build the GitHub repo structure locally or online.

