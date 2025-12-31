# NGINX

## Overview
This container provides a reverse proxy for internal services running within the homelab.

## Purpose
NGINX is used to route incoming requests to appropriate backend services, enabling centralized access control, clean internal URLs, and simplified service management.

## Networking
- Operates on a private Docker network
- Acts as a gateway for internal services
- No direct public internet exposure

## Notes
This service forms a core part of the homelab’s internal networking architecture.
