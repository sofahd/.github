# SOFAH: Speedy Open Framework for Automated Honeypot-development
![sofah logo](https://github.com/sofahd/.github/blob/main/img/logo.png)

## Introduction

SOFAH (Speedy Open Framework for Automated Honeypot-development) is an open-source framework designed to facilitate the rapid and automated development of honeypots being specifically optimized for Internet of Things (IoT) devices, but will work for other usecases aswell. Developed as part of a project report for a Computer Science program, SOFAH aims to address the challenges in developing flexible honeypots that can adapt to the dynamic landscape of cybersecurity threats targeting IoT devices.

## Features

- **Automated Honeypot Development**: Quickly generate honeypots tailored for various IoT devices with minimal manual intervention.
- **Dockerized Components**: Leverages Docker and Docker Compose for easy deployment and isolation of honeypot services.
- **Extensible Architecture**: Modular design allows for easy extension and customization of the framework to support new types of IoT devices and services.
- **Automated Data Generation**: Supports the automatic generation and normalization of datasets for honeypot simulation.
- **Comprehensive Logging**: Integrated logging services for capturing and analyzing interactions with the deployed honeypots.

## Components

SOFAH is composed of several key components, each running in its own Docker container for isolation and scalability:

- **Recon**: Module for reconnaissance and data collection on IoT devices.
- **ENNORM (ENrichment NORMalization)**: Processes reconnaissance data to generate datasets and configurations for the honeypots.
- **Honeypot Services**: Dockerized services that simulate various IoT device functionalities.
- **Logging Services**: Captures and aggregates logs from honeypot interactions for analysis.

## Getting Started

1. **Prerequisites**
   - Docker and Docker Compose installed on your system.
   - Basic understanding of Docker, IoT device behaviors, and cybersecurity concepts.

2. **Installation**
   - Clone the main SOFAH repository: `git clone https://github.com/sofah/main.git`
   - Navigate to the cloned directory and put your variables in the `sofah_starter.py` then you can simply startup the script.

3. **Configuration**
   - Configuration happens automatically (which is the whole point).
   - The Configuration can take up 15-20 minutes per ip.
   - you should receive a number of folders containing configured honeypots.

4. **Deployment**
   - Once configured, deploy the honeypots simply with a `docker compose up` in the folder with the configured `docker-compose.yml` file.

## Notes to Deployment

**Please note:** The deployment has only been tested on Ubuntu 22.04 LTS so far. However, you will likely have success using a modern Linux system, as the containerization layer should mitigate most incompatibilities.

### Management via SSH

To manage your honeypot, you need access to the machine. If you have VNC or physical access, great! If not, and you want to use SSH, please consider the following recommendations:

- **Port Conflicts:** Ensure that your SSH service does not conflict with any ports used by SOFAH. Moving your SSH service to a high port can significantly reduce the risk of port conflicts.
- **Port Hiding:** As this honeypot aims to withstand an nmap scan, it's essential to hide the SSH port. Moving SSH to a high port is a good first step, but ideally, the SSH port should only be open when you need access and should close once you disconnect.
   - To fully hide your SSH service, consider using "port knocking."
   - Port knocking works by requiring a specific sequence of port "knocks" to open the SSH port in the firewall. After disconnecting, another sequence can close the port again.
   - Refer to the `knockd` documentation for detailed instructions on configuring port knocking.

## Contact

For questions, suggestions, or contributions, please open an issue in the GitHub repository.

Thank you for your interest in SOFAH!
