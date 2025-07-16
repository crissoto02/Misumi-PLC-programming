## Misumi C-DR86A Switch Configuration Tables

### Table 1: SW1–SW3 — Peak Current Setting

| Peak Current       | RMS Current | SW1  | SW2  | SW3  |
|-------------------|-------------|------|------|------|
| 2.00 A (Default)  | 1.43 A      | ON   | ON   | ON   |
| 3.60 A            | 2.57 A      | OFF  | ON   | ON   |
| 4.40 A            | 3.14 A      | ON   | OFF  | ON   |
| 5.20 A            | 3.71 A      | OFF  | OFF  | ON   |
| 6.00 A            | 4.28 A      | ON   | ON   | OFF  |
| 6.80 A            | 4.86 A      | OFF  | ON   | OFF  |
| 7.60 A            | 5.43 A      | ON   | OFF  | OFF  |
| 8.40 A            | 6.00 A      | OFF  | OFF  | OFF  |

### Table 2: SW4 — Current Hold Mode

| Mode                | SW4  |
|--------------------|------|
| Half Current Hold  | OFF  |
| Full Current Hold  | ON   |

### Table 3: SW5–SW8 — Microstepping (Pulse/rev)

| Pulses/rev | SW5  | SW6  | SW7  | SW8  |
|------------|------|------|------|------|
| 400 (Default) | ON   | ON   | ON   | ON   |
| 800        | OFF  | ON   | ON   | ON   |
| 1600       | ON   | OFF  | ON   | ON   |
| 3200       | OFF  | OFF  | ON   | ON   |
| 6400       | ON   | ON   | OFF  | ON   |
| 12800      | OFF  | ON   | OFF  | ON   |
| 25600      | ON   | OFF  | OFF  | ON   |
| 51200      | OFF  | OFF  | OFF  | ON   |
| 100        | ON   | ON   | ON   | OFF  |
| 200        | OFF  | ON   | ON   | OFF  |
| 1000       | ON   | OFF  | ON   | OFF  |
| 2000       | OFF  | OFF  | ON   | OFF  |
| 5000       | ON   | ON   | OFF  | OFF  |
| 8000       | OFF  | ON   | OFF  | OFF  |
| 10000      | ON   | OFF  | OFF  | OFF  |
| 20000      | OFF  | OFF  | OFF  | OFF  |

### Table 4: SW9 — Pulse Edge Trigger

| Pulse Edge                | SW9  |
|--------------------------|------|
| Falling Edge (Recommended for PLC) | OFF  |
| Rising Edge              | ON   |

### Table 5: SW10 — Pulse Filter Time

| Filter Time | SW10 |
|-------------|------|
| 4 ms (Fast) | OFF  |
| 10 ms (More stable) | ON   |

### Table 6: SW11–SW12 — Control Mode

| Control Mode          | SW11 | SW12 |
|----------------------|-------|-------|
| Pulse + Direction    | OFF   | OFF   |
| Double Pulse         | ON    | OFF   |
| Auto Detection       | OFF   | ON    |
| Internal I/O Mode    | ON    | ON    |
