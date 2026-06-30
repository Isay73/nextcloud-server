# Nextcloud Server

## Overview

This repository documents my self-hosted Nextcloud server running on Ubuntu Server with Docker.

The deployment uses PostgreSQL as the database, Redis for caching and Nginx as a reverse proxy with HTTPS provided by Let's Encrypt.

The server is used as a private cloud storage platform with automatic file synchronization and secure remote access.

---

## Architecture

```text
                 Internet
                      │
               DuckDNS Domain
                      │
            Let's Encrypt SSL
                      │
                  Nginx
                      │
              127.0.0.1:8080
                      │
                 Nextcloud
                  │       │
             PostgreSQL  Redis
```

---

## Technology Stack

- Ubuntu Server 24.04 LTS
- Docker
- Docker Compose
- Nextcloud
- PostgreSQL 16
- Redis 7
- Nginx
- Let's Encrypt
- DuckDNS

---

## Repository Structure

```text
nextcloud-server/
├── docker-compose.yml
├── docs/
│   ├── architecture.md
│   ├── backup.md
│   └── troubleshooting.md
├── nginx/
│   └── nextcloud.conf
├── screenshots/
│   ├── nextcloud-dashboard-redacted.png
│   ├── server-services.png
│   └── server-overview.png
└── README.md
```

---

## Key Features

- Self-hosted private cloud
- Docker deployment
- PostgreSQL database
- Redis caching
- HTTPS with Let's Encrypt
- Nginx reverse proxy
- Local-only container exposure
- Automatic file upload workflow
- Secure remote access

---

## What I Built

I deployed and configured a complete self-hosted Nextcloud environment on Ubuntu Server.

The application runs inside Docker containers with PostgreSQL and Redis.

Nginx acts as a reverse proxy while HTTPS is handled using Let's Encrypt certificates.

I also implemented an automatic file upload workflow to synchronize recordings without using the official Nextcloud desktop client.

---

## What I Learned

- Docker Compose
- Nextcloud deployment
- PostgreSQL configuration
- Redis integration
- Reverse proxy configuration
- SSL certificates
- Linux server administration
- Troubleshooting Docker networking

---

## Security

Sensitive information has been removed.

The repository does not contain:

- Passwords
- Tokens
- Private keys
- Public IP addresses
- Real domain names

---

## Future Improvements

- Automated backups
- Monitoring
- CI/CD deployment
- Object storage support
