<div align="center">

# Prathik Amte · Engineer · Chip Design & Verification

Undergrad at BITS Pilani, K K Birla Goa Campus

<a href="https://www.linkedin.com/in/prathik-amte-313367296"><img src="https://img.shields.io/badge/LinkedIn-0077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="https://github.com/Prathik28/TinyMAC"><img src="https://img.shields.io/badge/TinyMAC-000000?style=for-the-badge&logo=github&logoColor=white"/></a>
<a href="https://github.com/Prathik28/sar-adc-4bit-gf180"><img src="https://img.shields.io/badge/4--bit%20SAR%20ADC-000000?style=for-the-badge&logo=github&logoColor=white"/></a>
<a href="https://github.com/Prathik28/chip-flow-atlas"><img src="https://img.shields.io/badge/Chip%20Flow%20Atlas-000000?style=for-the-badge&logo=github&logoColor=white"/></a>

</div>

## About

I design and verify chip-level hardware, digital and mixed-signal. My digital project is TinyMAC, an open INT8 matrix-multiply accelerator with a built-in self-test, built for the Tiny Tapeout GF180MCU shuttle; my analog project is a 4-bit SAR ADC, taken from transistors through simulation, formal proofs and layout. I care about designs that are tested thoroughly, formally checked where it matters, and documented well enough for someone else to reproduce.

## Featured projects

**[TinyMAC](https://github.com/Prathik28/TinyMAC)**: 2x2 output-stationary systolic array of INT8 MACs with 20-bit accumulators, controlled over SPI.

- Built-in self-test: LFSR operands, MISR, golden signature
- 19 cocotb tests including 1000 random matrix multiplications checked against NumPy, plus BIST fault injection
- 53-bin functional coverage model; 98.3% line and 100% branch code coverage
- SymbiYosys formal proofs (bounded and unbounded) running in CI
- Hardened with the open-source GF180MCU flow; gate-level simulation in CI
- Status: verified design, not yet fabricated

**[4-bit SAR ADC (GF180MCU)](https://github.com/Prathik28/sar-adc-4bit-gf180)**: course project (EEE F376): a successive-approximation ADC with a transistor-level control path, charge-redistribution capacitor DAC with bottom-plate sampling and a StrongARM latch comparator, plus a Verilog controller for an FPGA prototype.

- Simulated in ngspice on the open GF180MCU models: ramp DNL / INL within 0.125 LSB, ENOB 3.97 on a sine test (ideal 4.02), 11 process / voltage / temperature corners, comparator-offset and mismatch Monte Carlo, MIM capacitors, input-noise sweep
- Found and fixed an error in the original FSM equations; the control logic is checked three ways: simulation, a gate-level mirror of the transistor logic, and SymbiYosys proofs (including that the converter returns the input code for every 4-bit input)
- Cross-checked in Cadence Spectre on the generic gpdk180 kit, reported separately and labelled as a different process
- Full converter laid out in a Python flow on the foundry's device generators (175 logic cells, comparator, switches, 16 unit capacitors, inter-block wiring): 0 violations in a 54-rule subset of the design manual and an extracted netlist that matches the simulated one (490 transistors)
- Status: simulated, proven and laid out; **not** signed off (no foundry DRC / LVS, no parasitic extraction), FPGA build not yet run, not fabricated

**[Chip Flow Atlas](https://github.com/Prathik28/chip-flow-atlas)** ([live site](https://chip-flow-atlas.web.app)): a beginner-friendly website that explains which chip design tool is used when, and where to learn it.

- Flowchart and map of the ASIC, FPGA and analog design flows, with free and paid tools for each step and step-by-step learning paths
- Interactive 3D FPGA board you can spin and tap, with five sample Verilog programs (blink, button logic, counter, light chaser, traffic light) and a simplified simulation showing how the board reacts
- Plain HTML, CSS and JavaScript with no build step or libraries; hosted on Firebase Hosting and GitHub Pages

## Team projects

**[Nebula-project](https://github.com/Blackflash-BITS/Nebula-project)** (Blackflash-BITS): team entry for Nebula@BITS Goa, Digital track, sponsored by Astera Labs. A closed loop that takes a static timing violation, asks a language model for an RTL fix, proves it functionally equivalent, re-synthesises the design and accepts or rejects the fix on the re-measured result. My part (per the project README): Track A, the synthesis and static timing analysis runs (Yosys, OpenSTA, OpenROAD in Docker), and Track B, the LLM-driven fix proposal and validation stage, together with teammates Nihal and Praneeth.

## Technical skillset

**Hardware design & verification**
![Verilog](https://img.shields.io/badge/Verilog-1f425f?style=for-the-badge)
![cocotb](https://img.shields.io/badge/cocotb-2b5b84?style=for-the-badge)
![Formal](https://img.shields.io/badge/Formal%20(SymbiYosys)-5a3e85?style=for-the-badge)
![Systolic arrays](https://img.shields.io/badge/Systolic%20arrays-0b6e4f?style=for-the-badge)
![SPI](https://img.shields.io/badge/SPI-8a5a00?style=for-the-badge)
![Analog / mixed-signal](https://img.shields.io/badge/Analog%20%2F%20mixed--signal-7a3b3b?style=for-the-badge)
![SAR ADC](https://img.shields.io/badge/SAR%20ADC-7a3b3b?style=for-the-badge)

**Tools & flow**
![Icarus Verilog](https://img.shields.io/badge/Icarus%20Verilog-444?style=for-the-badge)
![Verilator](https://img.shields.io/badge/Verilator-444?style=for-the-badge)
![Yosys](https://img.shields.io/badge/Yosys-444?style=for-the-badge)
![OpenROAD / LibreLane](https://img.shields.io/badge/OpenROAD%20%2F%20LibreLane-444?style=for-the-badge)
![OpenSTA](https://img.shields.io/badge/OpenSTA%20%2F%20Static%20Timing-444?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![ngspice](https://img.shields.io/badge/ngspice-444?style=for-the-badge)
![Cadence Spectre](https://img.shields.io/badge/Cadence%20Spectre-444?style=for-the-badge)
![KLayout](https://img.shields.io/badge/KLayout-444?style=for-the-badge)
![GF180MCU](https://img.shields.io/badge/GF180MCU-444?style=for-the-badge)
![Tiny Tapeout](https://img.shields.io/badge/Tiny%20Tapeout-444?style=for-the-badge)

**Languages & general**
![Python](https://img.shields.io/badge/python-316192?style=for-the-badge&logo=python&logoColor=ffdd54)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

## Currently

- Preparing TinyMAC for its first tapeout and bring-up
- Taking the SAR ADC layout toward signoff checks and parasitic extraction

## Developer Insight of the Day

<p align="left">
  <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=dark" />
</p>

<p align="center"><sub>Keep learning. Keep building. Keep shipping.</sub></p>
