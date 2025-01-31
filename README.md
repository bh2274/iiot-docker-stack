# IIoT Docker Stack

This project provides a Docker stack for Industrial Internet of Things (IIoT) applications. It includes the following services:

- **Mosquitto MQTT Broker**: A lightweight MQTT broker for messaging.
- **MQTT Explorer**: A tool for visualizing and debugging MQTT messages.
- **InfluxDB**: A time-series database for storing sensor data.
- **Node-RED**: A flow-based development tool for wiring together IoT devices.
- **Grafana**: A visualization tool for creating dashboards.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Deployment](#deployment)
- [Python Scripts](#python-scripts)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites
- Docker and Docker Compose installed.
- Portainer (optional, for deployment).

## Installation
1. Install Docker: [Docker Installation Guide](https://docs.docker.com/get-docker/)
2. Install Docker Compose: [Docker Compose Installation Guide](https://docs.docker.com/compose/install/)

## Configuration
Configure environment variables in `.env` file (create if it doesn't exist). Example:
```dotenv
MQTT_EXPLORER_USER=admin
MQTT_EXPLORER_PASSWORD=admin
DOCKER_INFLUXDB_INIT_USERNAME=admin
DOCKER_INFLUXDB_INIT_PASSWORD=admin
GF_SECURITY_ADMIN_USER=admin
GF_SECURITY_ADMIN_PASSWORD=admin

## Deployment
1. Clone this repository: git clone https://github.com/yourusername/iiot-docker-stack.git
cd iiot-docker-stack
2. Start the Docker Compose stack: docker-compose up -d

## Python Scripts
The python-scripts service runs Python scripts to interact with MQTT, InfluxDB, and other services. It includes:

   - MQTT subscription and message processing.
   - Writing data to InfluxDB.
   - Internet access for external APIs or data fetching.
## Running Python Scripts
1. Place your Python scripts in the python-scrips directory.
2. Add dependencies to requirements.txt.
3. The service will automatically install dependencies and run main.py on startup.

## Contributing
Contributions are welcome! Please fork this repository and submit pull requests.

