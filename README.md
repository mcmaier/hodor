# HODOR
**H**ighly flexible, **O**pen-source **D**oor **O**peration **R**egulator — HODOR holds your door!

## Overview

HODOR is a universal controller for sliding door and roller shutter motor systems. It drives brushed DC motors (12–24 V) using an ESP32-S3 as the main controller with an H-bridge motor driver. Built-in Wi-Fi makes smart home integration straightforward.

## Repository Structure

This is the main repository containing project-level documentation and release bundles. Hardware and software development happen in dedicated sub-repositories, included here as Git submodules:

| Repository | Description |
|---|---|
| [hodor-hardware](https://github.com/mcmaier/hodor-hardware) | KiCad 9 schematic & PCB design |
| [hodor-software](https://github.com/mcmaier/hodor-software) | ESP-IDF firmware (C, ESP32-S3) |

### Directory Layout

```
hodor/
├── documentation/       Project-level documentation (block diagrams, specs)
├── releases/            Matched HW/SW release bundles
│   └── v0.1.0/          Example: Gerbers + firmware binary for a release
├── hodor-hardware/      Git submodule → mcmaier/hodor-hardware
├── hodor-software/      Git submodule → mcmaier/hodor-software
└── README.md
```

## Getting Started

Clone with submodules:

```bash
git clone --recurse-submodules https://github.com/mcmaier/hodor.git
```

Or, if already cloned:

```bash
git submodule update --init --recursive
```

## Releases

The `releases/` directory contains matched hardware and software versions that are tested together. Each release folder includes the relevant Gerber files, BOM, and firmware binary.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
