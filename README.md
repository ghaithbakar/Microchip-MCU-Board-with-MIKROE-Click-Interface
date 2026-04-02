# PIC32MX MCU Board with MIKROE Click Interface

A full embedded hardware platform built around the **Microchip PIC32MX534H64H** 
32-bit microcontroller, featuring onboard power regulation, USB connectivity, 
a MIKROE MikroBUS host connector, CAN bus transceiver, and extensive I/O 
headers. Designed as part of EEE394 (Printed Circuit Design Fundamentals) 
at Arizona State University.

## Overview

This board provides everything needed to run a PIC32MX microcontroller and 
interface it with the MIKROE Click ecosystem — including the companion 
VCNL4035 proximity sensor board in this repo series. The design integrates 
power regulation, USB, CAN, crystal oscillator, debug LEDs, and a full 
MikroBUS host connector into a single compact PCB.

## Schematic Highlights

| Block | Components |
|---|---|
| Microcontroller | PIC32MX534H64H-IPT (32-bit MIPS, 80MHz) |
| Power Regulation | LD29080DT33R (3.3V LDO) + LTST-C150ERT protection diodes |
| Reverse Protection | LTST-C1506GKT Schottky diode |
| USB | USB Micro-B (MUSB-ID) — VBUS sensing + D+/D- routing |
| CAN Transceiver | AFS08ASM-1E |
| Crystal Oscillator | FC-135 32.768KHz + 12MHz crystal |
| MikroBUS Host | Full MIKROE connector (SPI, I2C, UART, PWM, INT, RST, AN) |
| Debug LEDs | 4× LTST-C150ERT status LEDs |
| Decoupling | 100nF × 4, 100µF × 2, 2.2µF, bulk caps throughout |
| Programming | ICSP header (MCLR, PGD, PGC) |
| I/O Headers | P1, P2 expansion headers + GPIO breakout |
| Supply Voltage | VCC regulated to 3.3V via LDO |
| PCB Layers | 4 |
| USB Routing      | Differential pairs (D+/D−), 90Ω     |

## How It Works

Input power is regulated down to 3.3V by the LD29080DT33R LDO, with a 
Schottky diode for reverse polarity protection and bulk capacitors for 
supply stability. The PIC32MX runs from the 3.3V rail with AVDD/AVSS 
isolated for clean ADC operation. USB D+/D- lines are routed to the 
microcontroller's USB peripheral with VBUS detection. The CAN transceiver 
connects to the PIC32's CAN peripheral and exposes a differential bus 
interface. The MikroBUS host connector breaks out SPI (SCK/MISO/MOSI/CS), 
I2C (SDA/SCL), UART (TX/RX), PWM, INT, RST, and AN — making it directly 
compatible with any MIKROE Click module including the companion VCNL4035 
proximity sensor board.

## Companion Board

This MCU board is designed to work with the 
[MIKROE Click Bus Interface Board](../mikroe-click-bus-interface-pcb) 
in this repo series — plug the VCNL4035 proximity sensor board into the 
MikroBUS connector and communicate via I2C.

## Status

✅ Designed · ✅ Manufactured · 🔄 Assembly in Progress · ⏳ Testing Pending

## Tools Used

Altium Designer · Soldering Station · ICSP Programmer

## Key Skills Demonstrated

32-bit MCU support circuit design · LDO power regulation · USB hardware 
integration · CAN bus transceiver integration · Crystal oscillator layout · 
MIKROE MikroBUS host design · Multi-peripheral I/O routing · 
ICSP programming interface · Gerber/BOM/NC drill generation · 4-layer stackup design · USB 2.0 differential pair routing (90Ω controlled impedance) · DFM
