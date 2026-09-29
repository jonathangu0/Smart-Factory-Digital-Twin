# Smart Factory Digital Twin

A live 3D digital twin of a fischertechnik training factory, built with Python and NVIDIA Isaac Sim. The system connects physical factory telemetry to a virtual scene for machine-state monitoring, motion visualization, and production analysis.

Developed during my **Software Engineering Internship with the Infosys InStep Program in Bangalore, India, June–August 2026**.

## My Contributions

- Built a Python telemetry pipeline integrating OPC UA and MQTT data from a Siemens S7-1500 PLC to support a digital twin of a six-station training factory.
- Automated discovery of 2,510 OPC UA nodes to identify machine-state and motion signals.
- Developed a 42-tag event logger with automatic reconnection to capture timestamped production histories for replay and analysis.
- Implemented Isaac Sim station drivers that translate factory signals into robot, warehouse, processing, and sorting-line motion.
- Created offline demonstrations and a full order-cycle animation so the virtual factory can be explored without connected hardware.

## How It Works

The live integration reads factory state and axis positions over OPC UA. Python drivers update the corresponding objects in Isaac Sim, while a heads-up display and station indicator expose the current operating state.

Event logging captures production histories for subsequent analysis. Separate offline animations demonstrate station movement and the product’s journey through the factory.

## Operating Modes

| Mode | Purpose |
|---|---|
| Live digital twin | Visualize machine states and motion from a connected factory. |
| Offline demonstration | Explore station animations without physical hardware. |
| Full order cycle | Follow a simulated product through the manufacturing sequence. |

## Technology

Python · NVIDIA Isaac Sim · USD · OPC UA · MQTT · Node-RED · Siemens S7-1500

## Setup and Technical Documentation

See [Setup](docs/SETUP.md), [Running the Twin](docs/RUNNING.md), and [Architecture](docs/ARCHITECTURE.md) for installation, operating instructions, and implementation details.

Live operation requires compatible factory hardware and locally configured connection settings. Offline demonstrations do not require a factory connection.
