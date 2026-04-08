# 8051 Event Counter using Timer

A simple **8051 microcontroller project written in Assembly language** that counts input pulses and displays the result on a **3-digit multiplexed 7-segment display**.

The system detects pulses from an input pin and increments a counter value. The count is then split into digits and shown on the display using multiplexing.

---

## Project Overview

This project demonstrates:

* Timer usage in 8051
* Event / pulse counting
* Assembly programming for embedded systems
* Multiplexing technique for multi-digit 7-segment displays
* Simulation using Proteus

---

## Hardware Requirements

* AT89C51 / 8051 Microcontroller
* 3 × Common Cathode 7-Segment Displays
* Push Button or Sensor (pulse input)
* Resistors (220Ω for segments)
* 5V Power Supply

---

## Pin Configuration

| Microcontroller Pin | Function             |
| ------------------- | -------------------- |
| P0                  | 7-Segment Data Lines |
| P1.0                | Digit 1 Enable       |
| P1.1                | Digit 2 Enable       |
| P1.2                | Digit 3 Enable       |
| P3.1                | Pulse Input          |
| P3.0                | Control Signal       |

---

## Folder Structure

```
8051-event-counter/
│
├── src/
│   └── event_counter.asm
│
├── hex/
│   └── event_counter.hex
│
├── proteus/
│   └── simulation.pdsprj
│
├── docs/
│   └── circuit_diagram.png
│
├── images/
│   └── simulation_output.png
│
└── README.md
```

---

## How It Works

1. The system waits for an input pulse on **P3.1**.
2. When a pulse is detected, the counter value increments.
3. The number is divided into **hundreds, tens, and units**.
4. Each digit is displayed using **multiplexing** across three 7-segment displays.
5. Timer1 helps maintain stable counting and display timing.

---

## Running the Simulation (Proteus)

1. Open the project inside the **proteus** folder.
2. Load the HEX file:

```
/hex/event_counter.hex
```

3. Run the simulation.
4. Press the input button to simulate pulses.
5. The display will increment accordingly.

---

## Building the Code

You can compile the assembly program using:

* Keil µVision
* ASM51 assembler
* Any 8051 compatible assembler

The compiled output will generate the **HEX file** required for hardware or Proteus simulation.

---

## Possible Improvements

* Add reset button
* Convert into digital stopwatch
* Add LCD display version
* Use interrupt based counting instead of polling

---

## Author

Mallikarjun Jigalur

---

## License

This project is open source and available under the MIT License.
