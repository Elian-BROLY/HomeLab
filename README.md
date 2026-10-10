# Personal Homelab Architecture & Services

Welcome to the repository of my personal infrastructure hosted on my Homelab server.

---

## 🌐 Centralized Dashboard

All services across my infrastructure are accessible and monitored in real time from my **Homepage** dashboard:
* **Dashboard URL**: `https://dashboard.ebroly.fr` (access restricted via Nginx Proxy Manager Access Lists)

---

## 🛠️ Stack & Infrastructure

- **Server OS**: Ubuntu Server LTS
- **Reverse Proxy**: Nginx Proxy Manager (Let's Encrypt Wildcard Certificates `*.ebroly.fr`, HTTPS & Access Lists)
- **Containerization**: Docker & Docker Compose
- **Monitoring & Metrics**: Netdata & Uptime Kuma

---

## 📋 Hosted Services

| Category | Service | Description | Subdomain / URL | Tech Stack |
| :--- | :--- | :--- | :--- | :--- |
| **Dashboard** | **Homepage** | Central hub & real-time metrics | `dashboard.ebroly.fr` | Node.js / React |
| **Monitoring** | **Netdata** | Real-time system metrics (CPU, RAM, Disk) | `netdata.ebroly.fr` | Netdata |
| **Monitoring** | **Uptime Kuma** | Service uptime & availability monitoring | `status.ebroly.fr` | Uptime Kuma |
| **Administration** | **Portainer** | Web UI for Docker container management | `docker.ebroly.fr` | Portainer CE |
| **Network & DNS** | **AdGuard Home** | Network-wide ad blocker & local DNS server | `dns.ebroly.fr` | AdGuard Home |
| **Proxy** | **Nginx Proxy Manager** | Traffic routing & SSL certificate management | `npm.ebroly.fr` | Nginx Proxy Manager |
| **Security** | **Vaultwarden** | Lightweight encrypted password manager | `vault.ebroly.fr` | Vaultwarden (Rust Bitwarden) |
| **Storage** | **Nextcloud** | Private cloud & file synchronization | `cloud.ebroly.fr` | Nextcloud / MySQL |
| **Web** | **Landing Page** | Main portal & links hub | `ebroly.fr` | Nginx / HTML / CSS |
| **Web** | **Portfolio** | Personal showcase website & contact backend | `portfolio.ebroly.fr` | Nginx / Node.js Express |
| **Web** | **BTS TP Site** | Academic project / BTS CIEL coursework | `bts.ebroly.fr` | PHP 8.2 / MySQL 8.0 |
| **Web** | **Love Project** | Web mini-project | `love.ebroly.fr` | Nginx Alpine |
| **Gaming** | **Minecraft Server** | Multiplayer game server | `mc.ebroly.fr` | PaperMC 26.3 / Java |

---

## 📂 Repository Structure

All `docker-compose.yml` deployment files are organized by service under the `/docker` directory:

```text
homelab/
├── docker/
│   ├── adguard/
│   ├── bts_tp_site/
│   ├── homepage/
│   ├── landing-page/
│   ├── love/
│   ├── mc-server/
│   ├── netdata/
│   ├── nextcloud/
│   ├── nginx-proxy-manager/
│   ├── portainer/
│   ├── portfolio/
│   ├── uptime-kuma/
│   └── vaultwarden/
├── homepage/
│   └── config/
└── README.md
