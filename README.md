# LifeLink — SOS Safety Bracelet

**A wearable emergency alert system designed to help users request assistance and share their location during emergencies.**

## About the Project

LifeLink is a wearable safety bracelet being developed as a group engineering project for the Vishwakarma Awards Stage 2 competition under the Social Projects Club, IIT (BHU), Varanasi.

The project aims to provide a convenient way for users to trigger an emergency alert through a physical SOS button. Using a microcontroller, cellular communication, and GNSS positioning, the proposed system is designed to communicate an emergency message and the user's location to a designated recipient.

## Problem Statement

During an emergency, a person may have limited time or ability to unlock a smartphone, open an application, and contact someone for help. Personal safety solutions should make emergency activation simple and accessible.

LifeLink aims to address this challenge through a wearable device with a dedicated SOS button, location-acquisition capability, and cellular communication.

## Proposed Solution

LifeLink combines embedded electronics, location tracking, cellular connectivity, and user feedback in a compact bracelet enclosure.

Key proposed features include:

- **One-touch SOS activation:** A physical button initiates the emergency workflow.
- **Location acquisition:** GNSS positioning provides geographical coordinates when a valid satellite fix is available.
- **Cellular communication:** A cellular module and SIM provide the communication path for sending emergency alerts.
- **Visual feedback:** RGB LEDs indicate device status.
- **Haptic feedback:** A vibration motor provides tactile feedback to the user.
- **Rechargeable power system:** A Li-Po battery and charging and protection circuitry support portable operation.
- **Wearable enclosure:** A dedicated enclosure is being developed to accommodate the electronics and user-interface components.

*These are intended capabilities. End-to-end functionality depends on firmware implementation, hardware integration, network availability, and testing.*

## How It Works

1. The user presses the SOS button.
2. The ESP32-S3 processes the input and initiates the emergency workflow.
3. The GNSS subsystem attempts to obtain the user's location.
4. The cellular module establishes communication through a compatible SIM and available network.
5. The firmware is intended to send an SMS containing the emergency alert and available location information to a configured recipient.
6. LEDs and vibration provide feedback according to the implemented device states.

**Note:** SMS delivery and location availability are not guaranteed. The system must be tested under different network, power, and positioning conditions.

## Hardware Components

| Component                                   | Purpose                                       |
| ------------------------------------------- | --------------------------------------------- |
| ESP32-S3-DevKitC-1                          | Main controller                               |
| A7672S-FASE cellular/GNSS development board | Cellular communication and GNSS functionality |
| Active GNSS antenna                         | Satellite signal reception                    |
| LTE antenna                                 | Cellular communication                        |
| Nano SIM                                    | Cellular network access                       |
| BQ24074 charger board                       | Battery charging and power-path management    |
| 3.7 V, 1000 mAh Li-Po battery               | Portable power source                         |
| Battery protection board                    | Battery protection                            |
| 3.3 V buck-boost regulator                  | Voltage regulation                            |
| Tactile push buttons                        | User input, including SOS activation          |
| RGB LEDs                                    | Visual status feedback                        |
| Vibration motors                            | Haptic feedback                               |
| Resistors, capacitors, MOSFETs and diodes   | Supporting electronics and protection         |

Additional prototyping materials include breadboards and jumper wires. The final hardware configuration and compatibility will be verified during integration.

## Software and Development

The software is intended to coordinate button input, location acquisition, cellular communication, and user feedback.

Planned development tasks include:

- ESP32-S3 firmware development.
- Communication between the controller and cellular/GNSS module.
- AT-command-based modem control, where supported by the selected module firmware.
- SMS generation and delivery to a configured recipient.
- Handling unavailable GNSS fixes, network failures, and low-battery conditions.
- Testing and debugging the complete emergency workflow.

The implementation language, module interface, wiring, and tested firmware behavior will be documented as development progresses.

## CAD Design

A preliminary 3D enclosure has been developed in Autodesk Fusion 360. It includes a rounded bottom case, removable lid, SOS and LED openings, a charging-port opening, an alignment lip, and screw-post placeholders.

**CAD Model:** [https://a360.co/4jzrfRw](url)

The current enclosure is a draft. Strap attachments, internal component clearances, and final assembly tolerances may require further refinement.

## Project Roadmap

1. **System Design:** Finalize requirements, architecture, and emergency workflow.
2. **Hardware Setup:** Connect and verify the controller, cellular/GNSS module, SOS button, and power system.
3. **Firmware Development:** Implement button handling, location acquisition, SMS alerts, and status feedback.
4. **Prototype Integration:** Integrate electronics and enclosure, resolving fit and antenna-placement constraints.
5. **Testing and Validation:** Test SOS activation, location reporting, SMS delivery, charging, battery endurance, and failure scenarios.
6. **Final Refinement:** Resolve issues, document results, and prepare the prototype demonstration.

## Current Project Status

The project is in the design and development stage. A preliminary enclosure CAD model and component BOM have been prepared. Firmware implementation, hardware integration, and end-to-end validation should be documented as completed only after the corresponding work has been verified.

## Team

Developed as a collaborative engineering project under the Social Projects Club, IIT (BHU), Varanasi.

**Competition:** Vishwakarma Awards — Stage 2

## Disclaimer

LifeLink is a prototype under development. It is intended as a supplementary safety aid and is not a replacement for emergency services or other established safety measures. Communication and location functions depend on hardware, network availability, and environmental conditions.
