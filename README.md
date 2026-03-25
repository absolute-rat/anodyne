# Scytale-ASM Bridge for Havoc

A stealthy, modular (C2) extension for the Havoc Framework. This project implements a custom, low-signal communication channel using custom Scytale encoding to bridge a raw Assembly implant with a Havoc Teamserver.


## Core Architecture & Technical Highlights
This project was designed to minimize the forensic footprint of an implant while maintaining the robust tasking capabilities of Havoc.

Custom ASM Agent: A position-independent, 100% assembly-based beacon. By avoiding the Go/C++ runtimes of standard implants, it maintains a sub-5KB memory footprint.

Scytale Encoding Layer: Implements a custom encoding transport protocol. This transforms traffic into high-entropy "noise" that mimics legitimate configuration data or fragmented registry keys.

Havoc External C2 Bridge: A Python-based service that utilizes the havoc-py API to translate between the Scytale protocol and Havoc’s internal tasking engine.


## License
This project is licensed under the Apache License 2.0. See the LICENSE file for details.

## Disclaimer
This tool is for educational purposes and authorized Red Team engagements only.
