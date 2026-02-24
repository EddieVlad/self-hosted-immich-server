# Self-Hosted Immich Media Server  
## Privacy-Focused Home Media Infrastructure

---

## About This Project

This repository documents the complete setup of a self-hosted Immich media server running on a repurposed Dell OptiPlex 3040 using Ubuntu Server and Docker Compose.

The goal of this project is to promote digital ownership, privacy-first infrastructure, and practical self-hosting knowledge. Instead of depending entirely on commercial cloud providers, this setup demonstrates how individuals can build and maintain their own secure media infrastructure using accessible hardware and open-source tools.

This documentation is shared to help others replicate, learn from, and improve upon the setup.

---

## Why This Matters

Modern digital life generates thousands of personal photos and videos, often stored across multiple devices and cloud platforms. While convenient, this creates:

- Fragmented storage
- Long-term subscription dependency
- Limited control over personal data
- Reduced transparency in how data is handled

This project demonstrates a privacy-conscious alternative:

- Centralized personal media storage
- Full ownership of data
- Secure remote access without exposing services publicly
- Open-source infrastructure built on transparent technologies

The intent is not only to host media, but to encourage responsible and secure self-hosting practices.

---

## Hardware Platform

- **Device:** Dell OptiPlex 3040 (repurposed enterprise desktop)
- **Processor:** Intel Core i3 (6th Gen)
- **Memory:** 8GB
- **Storage:** 256GB SSD for OS and Media storage
- **Network:** Wired Ethernet for reliability

This setup demonstrates that meaningful infrastructure can be built using affordable, reused hardware.

---

## Operating System

- **OS:** Ubuntu Server (LTS)
- Minimal installation for lightweight performance
- Managed via SSH
- Firewall configured using UFW

Ubuntu Server was selected for its stability, long-term support, and strong Docker ecosystem compatibility.

---

## Deployment Approach

Immich and its supporting services were deployed using Docker and Docker Compose.

### Containerized Services

- Immich server
- Immich microservices
- PostgreSQL database

### Infrastructure Principles

- Separation of services into containers
- Persistent volume configuration for durability
- Environment variable isolation via `.env`
- Restart policies for resilience
- Detached background execution for stability

Docker Compose ensures portability, reproducibility, and maintainability of the environment.

---

## Secure Remote Access

Remote access is implemented using **Tailscale VPN**, following a zero-trust access philosophy.

Security principles applied:

- No public port forwarding
- No direct internet exposure
- Encrypted peer-to-peer VPN connectivity
- SSH restricted to VPN network
- Firewall rules limiting unnecessary services

This approach reduces attack surface while preserving accessibility from authorized devices anywhere in the world.

---

## Monitoring & Resource Awareness

System health and performance are monitored using:

- `htop`
- `docker stats`
- `free -h`
- `df -h`

This ensures responsible resource management within hardware constraints.

---

## Data Protection Strategy

- PostgreSQL backups performed using `pg_dump`
- Media stored in persistent mounted volumes
- Backup automation possible via cron jobs
- Data separated from container lifecycle to prevent accidental loss

---

## Knowledge Shared Through This Repository

This documentation aims to help others understand:

- Linux server fundamentals
- Docker-based service orchestration
- Secure self-hosting practices
- VPN-based private access models
- Storage persistence strategies
- Infrastructure monitoring basics

Anyone interested in building a private, self-controlled media server can use this repository as a starting point.

---

## Encouraging Responsible Self-Hosting

Self-hosting is not only about running services — it is about:

- Understanding your infrastructure
- Reducing unnecessary data exposure
- Practicing responsible security configurations
- Contributing back by documenting learnings

If this project helps you build your own setup, improve your privacy posture, or learn containerized infrastructure, then it has served its purpose.

---
