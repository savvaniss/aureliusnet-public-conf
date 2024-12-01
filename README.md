# Apache2 Configuration for Aurelius Chain and Nepheli Coin

Welcome to the **Aurelius Configuration Repository** for the **Aurelius Chain** and **Nepheli Coin** projects. This repository will be used as an entry point for all configuration files that needed to the project. contains optimized and secure Apache2 virtual host configurations tailored to manage HTTPS traffic, enforce security best practices, and ensure seamless operation of your blockchain and cryptocurrency services.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
  - [1. Clone the Repository](#1-clone-the-repository)
  - [2. Obtain SSL Certificates](#2-obtain-ssl-certificates)
  - [3. Deploy Configuration Files](#3-deploy-configuration-files)
  - [4. Enable Required Apache Modules](#4-enable-required-apache-modules)
  - [5. Enable Virtual Hosts and Reload Apache](#5-enable-virtual-hosts-and-reload-apache)
- [Configuration Details](#configuration-details)
  - [blockchain.aurelius.world.conf](#blockchainaureliusworldconf)
  - [project.aurelius.world.conf](#projectaureliusworldconf)
- [Security Enhancements](#security-enhancements)
- [Automatic SSL Renewal](#automatic-ssl-renewal)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

This repository provides **Apache2** virtual host configurations for two primary domains:

1. **blockchain.aurelius.world**: Handles blockchain-related services, acting as a reverse proxy to a backend application running on `localhost:3000`.
2. **project.aurelius.world**: Serves the Nepheli Coin project’s static website from `/var/www/html/aureliusnet-site/`.

Both configurations enforce HTTPS, implement robust security measures, and ensure that all HTTP traffic is seamlessly redirected to HTTPS.

## Features

- **HTTPS Enforcement**: All HTTP requests are automatically redirected to HTTPS to ensure secure communication.
- **Reverse Proxy Setup**: Efficiently proxy requests to backend services.
- **Security Headers**: Protect against common web vulnerabilities using essential HTTP security headers.
- **Rate Limiting**: Mitigate potential abuse and denial-of-service (DoS) attacks by limiting request rates.
- **Sensitive File Protection**: Prevent unauthorized access to critical configuration and environment files.
- **ModSecurity Integration**: Incorporate a Web Application Firewall (WAF) for enhanced security.
- **Automatic SSL Renewal**: Ensure SSL certificates are always up-to-date with automatic renewal via Certbot.

## Prerequisites

Before deploying these configurations, ensure you have the following:

- **Apache2 Installed**: Ensure Apache2 is installed on your server.
- **Root or Sudo Access**: Administrative privileges to modify server configurations.
- **Domain Names**: Proper DNS records pointing `blockchain.aurelius.world` and `project.aurelius.world` to your server’s IP address.
- **Certbot Installed**: For obtaining and managing SSL certificates from Let's Encrypt.

## Installation

Follow the steps below to set up the configurations on your Apache2 server.

### 1. Clone the Repository

First, clone this repository to your local machine or directly to your server.

```bash
git clone https://github.com/yourusername/aurelius-apache-configs.git
cd aurelius-apache-configs
