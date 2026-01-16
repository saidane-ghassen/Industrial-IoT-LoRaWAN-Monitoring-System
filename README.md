# Industrial IoT Monitoring System (LoRaWAN + MQTT)

Summer internship project (June–August 2025) carried out at YUCCAINFO (Sousse, Tunisia) as part of my Embedded Systems engineering curriculum at ENISo.

## Objective

Design and prototype a long‑range, low‑power IoT node for industrial monitoring, using:

- LoRaWAN for long‑range wireless communication (EU868 band)
- MQTT for cloud integration and data visualization
- A custom 2‑layer PCB designed in Altium
- Multiple industrial sensors (vibration, current, temperature)

The node collects environmental data, sends it through a LoRaWAN gateway to the cloud, and makes it available to an IIoT platform.

## System Architecture

- MCU / Radio: RAK3172 module based on STM32WLE5 (ARM Cortex‑M4 with integrated Sub‑GHz LoRa radio)
- Sensors:
  - Vibration sensor (SW‑420)
  - AC current sensor (SCT‑013‑100)
  - NTC 10K temperature sensor
- Power stage:
  - Battery supply with charger and monitoring
  - USB‑C connector for configuration and debugging
- Communication:
  - LoRaWAN (OTAA) toward a public network server (e.g. TTN)
  - UART / USB interface for AT commands and firmware debug

A 2‑layer PCB has been designed with a continuous ground plane, impedance‑controlled USB differential pair, and RF matching for the antenna.

## Research and Design Work

This repository also contains the research and development work done during the internship:

- Study of LoRa / LoRaWAN: modulation, network architecture, device classes, security (ABP vs OTAA)
- Study of MQTT: publish/subscribe model, QoS levels, topic hierarchy for IIoT
- Component selection methodology with compliance matrix and BOM
- Complete schematic and PCB design flow in Altium, with DRC reports

The detailed internship report and slides are provided in the `docs/` and `presentation/` folders.

## Repository Structure

- `docs/` – Internship report, research notes (LoRaWAN, MQTT, RAK3172), component selection
- `hardware/` – Schematics, PCB layout (2D and 3D), BOM and DRC files
- `firmware/` – Source code and configuration examples for the LoRaWAN node
- `results/` – Photos, test logs and measurement results
- `presentation/` – `Summer-Internship-Presentation.pdf` (short project presentation)

## Main Outcomes

- Fully designed and routed custom LoRaWAN node PCB
- Validated hardware prototype with multiple sensors
- Successful LoRaWAN communication and MQTT integration
- Practical experience with IIoT architectures, embedded development and PCB design

## Technologies and Skills

- Embedded systems: STM32, C, STM32CubeIDE
- Wireless and IoT: LoRa, LoRaWAN, MQTT, TTN
- Hardware: Altium Designer, PCB layout, DRC, BOM
- Methodology: Agile/Scrum, compliance matrix, technical documentation
