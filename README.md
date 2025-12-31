# 🏠 Self-Hosted Docker Homelab Stack

## Overview

This repository documents my **self-hosted homelab infrastructure**, built and maintained using **Docker and Docker Compose**. The stack hosts a diverse set of services spanning **networking, security, media management, productivity, and system automation**, all running on a **private network without public internet exposure**.

The primary goals of this homelab are:

* Hands-on experience with **containerized infrastructure**
* **Security-first system design**
* Service orchestration, automation, and lifecycle management
* Self-hosting critical services with an emphasis on **privacy and data ownership**

> ⚠️ This repository documents the infrastructure and configuration.
> The homelab itself is intentionally **not publicly accessible**.

---

## Design Principles

* **Private-by-default**: No services are exposed directly to the public internet
* **Container isolation**: Each service runs in its own container with scoped volumes
* **Modular structure**: Each container and its persistent data live in a dedicated directory
* **Reproducibility**: Infrastructure is defined declaratively using Docker Compose
* **Security awareness**: Secrets are managed via environment variables and excluded from version control

---

## Repository Structure

Each service is contained within its **own directory**, alongside its configuration and persistent data.

```
.
├── <service-name>/
│   ├── docker-compose.yml
│   ├── config/
│   └── data/
├── README.md           # This file (stack-level documentation)
└── .gitignore
```

* Each service directory contains **only what it needs**
* No shared volumes unless explicitly required
* Individual services may include their own `README.md` with service-specific details

---

## Core Infrastructure Components

### Container Management & Automation

* **Docker / Docker Compose** – Container orchestration
* **Portainer** – Web-based container management
* **Watchtower** – Automated image updates

### Networking & Access Control

* **NGINX** – Reverse proxy for internal service routing
* **Pi-hole** – Network-wide DNS filtering
* **Unbound** – Recursive DNS resolver
* **Heimdall** – Centralized service dashboard

### Security & Privacy

* **Vaultwarden** – Self-hosted password management
* **SearXNG** – Privacy-focused metasearch engine
* **Isolated internal networking** to minimize attack surface

### Remote Access

* **RustDesk (HBBS & HBBR)** – Self-hosted remote desktop relay and synchronization servers

### Media & Automation Services

* **Jellyfin** – Media server
* **Media management and automation services** (metadata handling, workflow orchestration)
* Supporting services for background processing and API-driven automation

### Productivity & Collaboration

* **WordPress + MySQL** – Self-hosted web platform
* **OpenCloud** – File sharing and collaboration
* **FreshRSS** – RSS aggregation
* **Calibre-Web** – E-book management
* **Stirling-PDF** – Document processing
* **Draw.io** – Diagramming service

---

## Security Considerations

* No credentials or secrets are committed to this repository
* Hostnames, IP addresses, and domains are sanitized where applicable
* Services are designed to operate **entirely within a trusted local network**

---

## Why No Public Demo?

This homelab is **intentionally private** and not exposed via a public IP or port forwarding.

Instead, this repository provides:

* Full infrastructure documentation
* Declarative service definitions
* Architecture diagrams and screenshots (added separately)
* Reproducible configurations suitable for local deployment

This approach reflects **real-world security best practices** rather than demo-oriented exposure.

---

## Screenshots & Diagrams

Screenshots and architecture diagrams will be added to demonstrate:

* Running containers (Portainer)
* Service dashboards
* Network and proxy topology

All visual materials are sanitized to avoid exposing sensitive information.

---

## Disclaimer

All services are used for **legitimate self-hosting, experimentation, and infrastructure learning purposes**.
The stack itself is content-agnostic and focused on orchestration, automation, and system design.

---

## Technologies Used

Docker · Docker Compose · Linux · NGINX · DNS · Reverse Proxying · Container Networking · Self-Hosting · Infrastructure Automation · Security Hardening
