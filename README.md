# IIoT Docker Stack

This project provides a Docker stack for Industrial Internet of Things (IIoT) applications. It includes the following services:

- **Mosquitto MQTT Broker**: A lightweight MQTT broker for messaging.
- **MQTT Explorer**: A tool for visualizing and debugging MQTT messages.
- **InfluxDB**: A time-series database for storing sensor data.
- **Node-RED**: A flow-based development tool for wiring together IoT devices.
- **Grafana**: A visualization tool for creating dashboards.

## Prerequisites
- Docker and Docker Compose installed.
- Portainer (optional, for deployment).

## Deployment
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/iiot-docker-stack.git
   cd iiot-docker-stack

## Python Scripts
The `python-scripts` service runs Python scripts to interact with MQTT, InfluxDB, and other services. It includes:
- MQTT subscription and message processing.
- Writing data to InfluxDB.
- Internet access for external APIs or data fetching.

### Running Python Scripts
1. Place your Python scripts in the `python-scripts` directory.
2. Add dependencies to `requirements.txt`.
3. The service will automatically install dependencies and run `main.py` on startup.
