# DAN — Serial Communication Protocol

> A lightweight asynchronous self-clocking serial communication protocol using only two wires.

![Status](https://img.shields.io/badge/status-draft-orange)
![Version](https://img.shields.io/badge/version-v0.1-blue)
![License](https://img.shields.io/badge/license-MIT-green)

---

## Overview

DAN is a unidirectional lightweight serial communication protocol designed for embedded systems.

Unlike conventional asynchronous serial links that require transmitter and receiver to share communication parameters (e.g. UART), DAN does not rely on a predefined baud rate, predefined word size and a predefined parity enabling shared between transmitter and receiver. 

The protocol was designed to be:

- Lightweight
- Easy to implement
- Suitable for bit-banging
- Independent of dedicated hardware peripherals

---

## Specification

The complete technical specification is available here:

- **[DAN Protocol Specification v0.1 Draft](docs/specification/DAN01-v0.1.md)**

---
## Features

- Two-wire interface (`DATA` + `GND`)
- Asynchronous communication
- Self-synchronizing frames
- Payload length from 1 to 16 bits
- Optional parity checking
- Designed for microcontrollers and FPGAs

---

## Frame Format

![DAN01 Frame](docs/diagrams/frame-format.svg)

---

## Timing Diagram

Transmitting the 8-bit value `01010110` with parity enabled:

![Timing Diagram](docs/diagrams/timing-diagram.svg)

---

## Repository Structure

```
docs/
examples/
reference/
test_vectors/
tools/
```

---

## Current Status

Current specification version:

**v0.1 Draft**

This protocol is currently under development. Breaking changes may occur until version 1.0.


## License

MIT License

Copyright (c) 2026 Daniel S. Amaral

