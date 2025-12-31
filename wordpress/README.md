# WordPress (Application & Database)

## Overview
This directory contains the Docker configuration for a self-hosted **WordPress deployment**, including its dedicated **MySQL database backend**.

Both containers are deployed together using a single Docker Compose file and are tightly coupled as part of the same application stack.

---

## Purpose
WordPress is used as a content management system for hosting blogs, documentation, or internal web content within the homelab.

- The **WordPress container** handles application logic and web serving
- The **MySQL container** provides persistent relational storage for WordPress data

---

## Directory Structure

```
.
├── docker-compose.yml
├── wordpress/
├── mysql/
└── README.md

```


---

## Networking

- Database is not exposed directly
- WordPress communicates with MySQL over an internal Docker network
- Access to WordPress is routed internally via reverse proxy

---

## Security Considerations

- Database credentials are managed via environment variables
- MySQL service is isolated and accessible only to WordPress
- No credentials are committed to version control

---

## Notes

The database container exists solely to support the WordPress application and is not intended for general-purpose use.