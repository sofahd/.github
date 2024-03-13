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
   - Once configured, deploy the honeypots simply with a `docker-compose up` in the folder with the configured `docker-compose.yml` file.

## Contact

For questions, suggestions, or contributions, please open an issue in the GitHub repository.

Thank you for your interest in SOFAH!
