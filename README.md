# Misumi-PLC-programming

### Connection Summary
- Misumi C-DR86A driver connected to Siemens S7-1200 PLC.
- Misumi stepper motor C-86STM03 connected to C-DR86A.
- PTO block used in TIA Portal to generate pulses.
- Connections:
  - PLC %Q0.0 → PUL+
  - PLC %Q0.1 → DIR+
  - PLC %Q0.2 → ENA+
  - All negative terminals (PUL−, DIR−, ENA−) connected to PLC GND.

### First Test Configuration
For more information about the DIP switch settings, refer to [Switches Settings](Switches-settings.md).
| Setting            | Value              |
|-------------------|--------------------|
| Output Current    | 2.00 A (Default)   |
| Hold Mode         | Half Current       |
| Microstepping     | 400 pulse/rev      |
| Pulse Edge        | Rising Edge        |
| Pulse Filter      | 4 ms               |
| Control Mode      | Internal I/O Mode  |

#### Observation:
- With PTO frequency set at **100 Hz**, the motor turned **very slowly**.
- At frequencies greater than **100 Hz**, the motor did not rotate.
- At lower frequencies (under 50 Hz), the motor took **longer steps**, appearing faster visually.

### Adjusted Configuration
For more information about the DIP switch settings, refer to [Switches Settings](Switches-settings.md).

| Setting            | Value              |
|-------------------|--------------------|
| Output Current    | 2.00 A (Default)   |
| Hold Mode         | Half Current       |
| Microstepping     | 400 pulse/rev      |
| Pulse Edge        | Falling Edge       |
| Pulse Filter      | 4 ms               |
| Control Mode      | Pulse + Direction  |

#### Observation:
- After switching to **Falling Edge** and **Pulse + Direction Mode**, the motor responded correctly.
- Motor rotated smoothly up to **2.5 kHz** PTO frequency.
- Beyond **2.5 kHz**, the motor initially stopped responding.
- After further testing, we observed that the motor is capable of rotating at higher frequencies, but requires a gradual increase of frequency to operate correctly.  
- Directly applying high frequencies from standstill did not produce rotation.

### Conclusion
- Misumi C-DR86A with Siemens S7-1200 requires:
  - Falling Edge trigger.
  - Pulse + Direction mode.
  - PTO frequency range: up to **2.5 kHz** stable without acceleration control.
  - With controlled acceleration, higher frequencies are achievable.
- Internal I/O mode is not compatible with PLC PTO signals.
- Configuration changes require power cycling the driver for reliable results.
table.
- Internal I/O mode is not compatible with PLC PTO signals.
- Configuration changes require power cycling the driver for reliable results.

