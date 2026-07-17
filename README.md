# DAN#01 — Serial Communication Protocol

> A lightweight asynchronous self-clocking serial communication protocol using only two wires.

![Status](https://img.shields.io/badge/status-draft-orange)
![Version](https://img.shields.io/badge/version-v0.1-blue)
![License](https://img.shields.io/badge/license-MIT-green)

---

## Overview

DAN#01 is a lightweight serial communication protocol designed for embedded systems.

Unlike UART, DAN#01 does not require both devices to share a predefined baud rate. Instead, every transmitted frame contains a synchronization pattern that allows the receiver to estimate the bit period before decoding the remaining data.

The protocol was designed to be:

- Lightweight
- Easy to implement
- Suitable for bit-banging
- Independent of dedicated hardware peripherals

---

## Frame Format

![DAN01 Frame](docs/diagrams/frame-format.svg)

---

## Timing Diagram

Transmitting the 8-bit value `01010110` with parity enabled:

![Timing Diagram](docs/diagrams/timing-diagram.svg)

---

## Features

- Two-wire interface (`DATA` + `GND`)
- Asynchronous communication
- Self-synchronizing frames
- Payload length from 1 to 16 bits
- Optional parity checking
- Designed for microcontrollers and FPGAs

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

---

## License

MIT License