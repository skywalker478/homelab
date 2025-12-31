# RustDesk (HBBS & HBBR)

## Overview
This directory contains the Docker configuration for a self-hosted RustDesk infrastructure, including both the **HBBS (synchronization server)** and **HBBR (relay server)** components.

Both services are deployed together using a single Docker Compose configuration and operate as part of the same remote access system.

---

## Purpose
RustDesk provides a self-hosted remote desktop solution for secure, private remote access without relying on third-party relay services.

- **HBBS** handles client registration, synchronization, and session coordination
- **HBBR** relays traffic when direct peer-to-peer connections are unavailable

---

## Directory Structure

```
.
├── docker-compose.yml
├── data/
└── README.md

```

---

## Networking

- Operates entirely within a private network
- No direct public exposure via port forwarding
- Designed for controlled, authenticated access

---

## Security Considerations

- Self-hosted relay and synchronization infrastructure
- Access restricted to authorized clients
- Secrets and keys are injected via environment variables

---

## Notes

This setup enables full control over remote access infrastructure while minimizing reliance on external services.
