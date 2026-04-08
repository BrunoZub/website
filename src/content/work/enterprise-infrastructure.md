---
title: Self-Hosted Enterprise Infrastructure
publishDate: 2026-03-30 00:00:00
img: /assets/stock-3.jpg
img_alt: Servers in a data center
description: |
  Deployed a resilient, containerized suite of self-hosted enterprise services, backed by ZFS network storage and DNS sinkholing.
tags:
  - Docker Compose
  - ZFS & SMB
  - Nextcloud
  - AdGuard Home
---

Deployed a resilient, containerized suite of self-hosted enterprise services. This includes a ZFS-backed network storage solution for automated backups, network-wide DNS filtering, and node-based workflow automation to streamline server maintenance.

### The Problem

I wanted a cohesive "business operations" environment capable of handling file storage, credential management, ad-blocking, and automation without relying on third-party SaaS subscriptions that compromise data privacy.

### The Solution

I architected a Docker & Docker Compose stack to deploy these core services securely.

- **ZFS & SMB:** For resilient network storage and automated snapshot backups.
- **Nextcloud:** As an internal Google Drive alternative for secure cloud storage.
- **AdGuard Home:** Providing network-wide DNS sinkholing and Zero-Trust DNS filtering.
- **n8n:** Node-based workflow automation to streamline server maintenance tasks and handle data pipelines.
- **Vaultwarden:** Self-hosted credential management.

### Technologies Used

- **Compute:** Docker, Docker Compose
- **Storage:** ZFS, SMB, NFS Shares
- **Software:** Nextcloud, n8n, AdGuard Home, Vaultwarden
