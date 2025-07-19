# QPSK PlutoSDR to RTL-SDR Pipeline

![WIP](https://img.shields.io/badge/status-WIP-orange)

> **Work In Progress**  
> This project is under active development. Core features are incomplete, and the implementation and interface are subject to change.  
> Contributions and issue reports are welcome, but please note that stability is not guaranteed.

This repo contains a complete QPSK digital communication pipeline implemented in C++ and designed to transmit on the [ADALM PlutoSDR](https://www.analog.com/en/resources/evaluation-hardware-and-software/evaluation-boards-kits/adalm-pluto.html) and receive on the [RTL-SDR](https://www.rtl-sdr.com/). It includes modulation, frame synchronization, timing error correction, carrier recovery, channel equalization, demodulation, and other related functionality.

## Features

- Real-time QPSK transmission and reception via PlutoSDR
- Carrier recovery using a Costas loop 
- Symbol timing recovery using Gardner TED and Farrow interpolation
- Support for variable timing loop bandwidth and damping
- Modular structure for easy swapping of synchronizers, interpolators, equalizers, etc.

## Requirements

- PlutoSDR connected and configured (USB or Ethernet)
- TODO

## Repo Structure
```text
qpsk-pluto-pipeline/   
├── include/  
│   ├── dsp/                        # Header files for core DSP logic  
│   └── gnuradio_blocks/            # Header files for GNU Radio integration  
├── src/  
│   ├── dsp/                        # DSP algorithm implementations  
│   └── gnuradio_blocks/            # GNU Radio block implementations  
├── grc/                            # GRC XML files for custom blocks  
├── apps/                           # Example pipelines or standalone demos  
├── notebooks/                      # Python notebooks for prototyping, design decisions  
├── debug/                          # Problem logs and notes  
├── cmake/                          # CMake modules  
├── CMakeLists.txt                  # Top-level CMake  
└── README.md
```

## Goals

- Use this pipeline as a learning and demonstration tool for SDR systems
- Explore trade-offs in synchronization and equalization on real hardware
- Eventually extend to support adaptive equalization and ML-based blocks

## Screenshots

TODO

## License

MIT License

