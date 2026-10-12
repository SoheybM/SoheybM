# Autonomous Sap-Flow Measurement System

**Research internship | Laboratoire Ampère × CETHIL | 2025–2026**

## Overview
An existing research prototype studies tree sap flow using temperature responses to controlled heat pulses. My internship focused on improving the embedded firmware and the reliability of its acquisition–heating–logging–sleep cycle, rather than claiming to have invented the complete sensor.

## My contributions
- Reorganized much of the application-level **PIC24 firmware** while reusing existing low-level peripheral code and previous work.
- Integrated temperature acquisition (six thermistors and AD7799 ADCs), RTC wake-up, microSD / FatFs logging and BLE diagnostics.
- Developed a mobile BLE interface in **MIT App Inventor**, supporting setup, time synchronization and laboratory/field modes.
- Diagnosed SPI conflicts between the ADCs and microSD; adopted distinct acquisition and logging configurations, following a solution suggested by technical supervision.
- Corrected heating-timing variability using a dedicated timer; investigated board power-consumption and battery-sensing problems.
- Iterated a **FreeCAD** enclosure and participated in laboratory calibration and field tests.

## Results and limitations
A stable autonomous cycle was demonstrated. One field experiment on one tree showed a detectable thermal response with observed measurement noise around **0.001 °C**. Tested configurations recorded roughly **17 mA active** and **8.5 µA in sleep**. Long-duration multi-site field validation remained outstanding.

## Credits
**Supervisors:** Laurent Morel (Ampère), Frédéric Lefèvre (CETHIL); **academic tutor:** Fabien Mieyeville (Polytech Lyon). **Research collaborator:** Ilane Cherif. **Previous contributors:** Kevin Maillot and Youssouf Fofana.

## Source and publication notes
Based on Soheyb Mebarbeche, *Développement d’une carte d’acquisition et de contrôle d’un capteur de flux de sève*, fourth-year internship report (January 2026), including its manufacturer datasheet bibliography and predecessor reports. No laboratory code, schematics, data or full report are republished. Only selected personally taken tree-installation images will be considered after final review.
