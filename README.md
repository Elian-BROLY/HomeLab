# Personal Homelab Architecture & Services

Bienvenue sur la documentation de mon infrastructure personnelle hébergée à la maison.

## Vue d'ensemble Architecture

- **OS Serveur** : Ubuntu Server LTS
- **Reverse Proxy** : Nginx Proxy Manager (Gestion SSL Let's Encrypt + routage sous-domaines)
- **Conteneurisation** : Docker & Docker Compose
- **Monitoring** : Uptime Kuma (exposé sur `status.ebroly.fr`)

---

## Services hébergés

| Service | Description | Sous-domaine / URL | Techno |
| :--- | :--- | :--- | :--- |
| **Landing Page** | Portail principal & hub de liens | `ebroly.fr` | HTML / CSS / Nginx |
| **Portfolio** | Parcours, projets & contact | `portfolio.ebroly.fr` | Web Stack |
| **Status Page** | Monitoring et métriques d'uptime | `status.ebroly.fr` | Uptime Kuma v2 |

---

## ⚙️ Stack & Docker Composes

Tous les fichiers `docker-compose.yml` utilisés pour déployer les services sont disponibles dans le dossier `/docker`.
