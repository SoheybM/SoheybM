# Hestia — Connected Door Sensor

**Polytech Lyon | Fourth-year Industrial Systems & Robotics project**

## Goal
A functional prototype to detect magnetic proximity at a door and transmit the interpreted state to a home-automation dashboard.

## Architecture
- **ESP32-H2 DevKitM-1** reads a reed switch on GPIO3 and drives a status LED.
- **Zigbee** transmits the ON/OFF state to **Home Assistant**, hosted on a **Raspberry Pi 3 Model B** with a Sonoff coordinator via ZHA.
- A **LiPo 1S battery**, TP/TC4056 charging module and MT3608 step-up converter support standalone power.
- An initial CAD model explores the mechanical enclosure.

## Implementation and validation
The team adapted ESP-IDF's `HA_on_off_light` sample, using a Home Assistant template entity to present an understandable state. Reading, LED response, Zigbee integration and battery operation were demonstrated. A power-supply voltage-drop problem was resolved by replacing the charging module.

## Important limitation
The reed switch senses **magnet proximity**, not whether the actual bolt has mechanically locked. The project is a **functional prototype**, not a secure locking detector.

## Credits and references
**Authors:** Soheyb Mebarbeche and Nicolas Ogliastri Alfonso. Based on the team's nine-page *Projet Hestia — Capteur de porte connecté* report and the attributed ESP-IDF / Zigbee / Home Assistant ecosystem. No supervisor credits are added, as requested.
