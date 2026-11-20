<div align="center">

# Prathik Amte · Chip Design & Verification

Undergrad at BITS Pilani, K K Birla Goa Campus

<a href="https://www.linkedin.com/in/prathik-amte-313367296"><img src="https://img.shields.io/badge/LinkedIn-0077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="https://github.com/Prathik28/TinyMAC"><img src="https://img.shields.io/badge/TinyMAC-000000?style=for-the-badge&logo=github&logoColor=white"/></a>

</div>

## About

I design and verify digital hardware. My current project is TinyMAC, an open INT8 matrix-multiply accelerator with a built-in self-test, built for the Tiny Tapeout GF180MCU shuttle. I care about designs that are tested thoroughly, formally checked where it matters, and documented well enough for someone else to bring up on a bench.

## Featured project

**[TinyMAC](https://github.com/Prathik28/TinyMAC)**: 2x2 output-stationary systolic array of INT8 MACs with 20-bit accumulators, controlled over SPI.

- Built-in self-test: LFSR operands, MISR, golden signature
- 19 cocotb tests including 1000 random matrix multiplications checked against NumPy, plus BIST fault injection
- 53-bin functional coverage model; 98.3% line and 100% branch code coverage
- SymbiYosys formal proofs (bounded and unbounded) running in CI
- Hardened with the open-source GF180MCU flow; gate-level simulation in CI
- Status: verified design, not yet fabricated

## Team projects

**[Nebula-project](https://github.com/Blackflash-BITS/Nebula-project)** (Blackflash-BITS): team entry for Nebula@BITS Goa, Digital track, sponsored by Astera Labs. A closed loop that takes a static timing violation, asks a language model for an RTL fix, proves it functionally equivalent, re-synthesises the design and accepts or rejects the fix on the re-measured result. My part (per the project README): Track A, the synthesis and static timing analysis runs (Yosys, OpenSTA, OpenROAD in Docker), and Track B, the LLM-driven fix proposal and validation stage, together with teammates Nihal and Praneeth.

## Technical skillset

**Hardware design & verification**
![Verilog](https://img.shields.io/badge/Verilog-1f425f?style=for-the-badge)
![cocotb](https://img.shields.io/badge/cocotb-2b5b84?style=for-the-badge)
![Formal](https://img.shields.io/badge/Formal%20(SymbiYosys)-5a3e85?style=for-the-badge)
![Systolic arrays](https://img.shields.io/badge/Systolic%20arrays-0b6e4f?style=for-the-badge)
![SPI](https://img.shields.io/badge/SPI-8a5a00?style=for-the-badge)

**Tools & flow**
![Icarus Verilog](https://img.shields.io/badge/Icarus%20Verilog-444?style=for-the-badge)
![Verilator](https://img.shields.io/badge/Verilator-444?style=for-the-badge)
![Yosys](https://img.shields.io/badge/Yosys-444?style=for-the-badge)
![OpenROAD / LibreLane](https://img.shields.io/badge/OpenROAD%20%2F%20LibreLane-444?style=for-the-badge)
![OpenSTA](https://img.shields.io/badge/OpenSTA%20%2F%20Static%20Timing-444?style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GF180MCU](https://img.shields.io/badge/GF180MCU-444?style=for-the-badge)
![Tiny Tapeout](https://img.shields.io/badge/Tiny%20Tapeout-444?style=for-the-badge)

**Languages & general**
![Python](https://img.shields.io/badge/python-316192?style=for-the-badge&logo=python&logoColor=ffdd54)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

## Currently

- Preparing TinyMAC for its first tapeout and bring-up

<p align="center"><sub>Keep learning. Keep building. Keep shipping.</sub></p>
