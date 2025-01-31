# IIoT Docker Stack

This project provides a Docker stack for Industrial Internet of Things (IIoT) applications. It includes the following services:

- **Mosquitto MQTT Broker**: A lightweight MQTT broker for messaging.
- **MQTT Explorer**: A tool for visualizing and debugging MQTT messages.
- **InfluxDB**: A time-series database for storing sensor data.
- **Node-RED**: A flow-based development tool for wiring together IoT devices.
- **Grafana**: A visualization tool for creating dashboards.
- **Python Scripts**: Custom Python scripts for data processing, integration, and automation.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Deployment](#deployment)
- [Services](#services)
- [Persistent Data](#persistent-data)
- [Automatic Login](#automatic-login)
- [Contributing](#contributing)
- [License](#license)

---

## Prerequisites

Before deploying the stack, ensure you have the following installed on your system:

1. **Docker**: Install Docker by following the official [Docker installation guide](https://docs.docker.com/get-docker/).
2. **Docker Compose**: Install Docker Compose by following the official [Docker Compose installation guide](https://docs.docker.com/compose/install/).
3. **Portainer (optional)**: If you want to deploy the stack using Portainer, install it by running:
   ```bash
   docker run -d -p 9000:9000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest

## Installation
1. Clone this repository: git clone https://github.com/yourusername/iiot-docker-stack.git
cd iiot-docker-stack
2. Configure environment variables(optional):
   - Edit the docker-compose.yaml file to customize service configurations (e.g., passwords, ports).
   - For Python scripts, update the environment variables in the python-scripts service section.
3. Build and deploy the stack: docker-compose up -d


## Deployment
Using Docker Compose
1. Navigate to the project directory: cd iiot-docker-stack
2. Start the stack: docker-compose up -d
3. Stop the stack: docker-compose down
Using Portainer
1. Access Portainer at http://localhost:9000
2. Go to Stacks > Add Stack
3. Paste the contents of docker-compose.yaml into the web editor.
4. Deploy the stack.

## Services
Service         URL                        Description
-Mosquitto       mqtt://localhost:1883      MQTT broker for messaging.
-MQTT Explorer   http://localhost:4000      Web-based MQTT client for debugging and visualization.
-InfluxDB        http://localhost:8086      Time-series database for storing sensor data.
-Node-RED        http://localhost:1880      Flow-based development tool for IoT automation.
-Grafana         http://localhost:3000      Visualization tool for creating dashboards.
-Python Scripts  N/A                        Custom Python scripts for data processing and integration.

## Persistent Data 
All data is stored persistently in the following directories:
- Mosquitto: ./mosquitto/config, ./mosquitto/data, ./mosquitto/log
- InfluxDB: ./influxdb/data, ./influxdb/config
- Node-RED: ./node-red/data
- Grafana: ./grafana/data
- Python Scripts: ./python-scripts

## Automatic Login
Default credentials for the services:
Service            Username      Password
MQTT Explorer      admin         admin
InfluxDB           admin         admin
Grafana            admin         admin
For InfluxDB:
- Organization: iiot
- Bucket: iiot_data

## Contributing
Contribuitons are welcome! If you'd like to contribute to this project, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bugfix: git checkout -b feature/your-feature-name
3. Commit your changes: git commit -m "Add your commit message"
4. Push you branch: git push origin feature/your-feature-name
5. Open a pull request and describe your changes.
Please ensure your code follows best practices and includes relevant documentation.

## License
This project is licensed under the MIT License. see the LICENSE file for details.
