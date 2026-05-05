---
title: Hybrid-Cloud Reverse Proxy & Monitoring
publishDate: 2026-03-15 00:00:00
img: /assets/stock-2.jpg
img_alt: Abstract representation of a cloud network
description: |
  Designed a hybrid network using a cloud VPS as a secure reverse proxy to route encrypted traffic to my on-premise homelab.
tags:
  - VPS
  - Nginx
  - Cloudflare
  - Uptime Kuma
---

Designed a hybrid network using a cloud VPS as a secure reverse proxy to route encrypted traffic to my on-premise homelab. Implemented Uptime Kuma to monitor 20+ active internal services with automated downtime alerting via webhooks.

### The Problem

Exposing on-premise services to the public internet opens the network up to vulnerabilities. A standard port-forwarding approach was too risky for a production-grade homelab.

### The Solution

I utilized a cloud VPS and Zero-Trust Networking (Tailscale) combined with Cloudflare Tunnels to act as a secure gateway. The cloud node routes encrypted traffic back to the on-premise Nginx proxy, hiding the true IP address of the homelab.

To ensure reliability, I deployed Uptime Kuma on a separate node to continuously monitor all 20+ internal services, sending automated alerts to Discord/Telegram in the event of an outage.

### Technologies Used

- **Cloud / Network:** Cloud VPS, Cloudflare Tunnels, Tailscale (Zero Trust)
- **Web Server:** Nginx Reverse Proxy
- **Monitoring:** Uptime Kuma, Portainer
