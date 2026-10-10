# Personal Homelab Architecture & Services

Bienvenue sur le dépôt de mon infrastructure personnelle hébergée sur mon serveur Homelab.

---

## 🌐 Dashboard Centralisé

L'ensemble des services de mon infrastructure est accessible et supervisé en temps réel depuis mon tableau de bord **Homepage** :
* **URL Dashboard** : `https://dashboard.ebroly.fr` (accès restreint via Nginx Proxy Manager Access Lists)

---

## 🛠️ Stack & Infrastructure

- **OS Serveur** : Ubuntu Server LTS
- **Reverse Proxy** : Nginx Proxy Manager (Certificats Let's Encrypt Wildcard `*.ebroly.fr`, HTTPS & Access Lists)
- **Conteneurisation** : Docker & Docker Compose
- **Supervision & Métriques** : Netdata & Uptime Kuma

---

## 📋 Services Hébergés

| Catégorie | Service | Description | Sous-domaine / URL | Techno |
| :--- | :--- | :--- | :--- | :--- |
| **Dashboard** | **Homepage** | Hub centralisé & métriques en direct | `dashboard.ebroly.fr` | Node.js / React |
| **Supervision** | **Netdata** | Métriques système (CPU, RAM, Disque) en temps réel | `netdata.ebroly.fr` | Netdata |
| **Supervision** | **Uptime Kuma** | Monitoring de disponibilité des services | `status.ebroly.fr` | Uptime Kuma |
| **Administration** | **Portainer** | Interface Web de gestion des conteneurs Docker | `docker.ebroly.fr` | Portainer CE |
| **Réseau & DNS** | **AdGuard Home** | Bloqueur de publicités réseau & serveur DNS local | `dns.ebroly.fr` | AdGuard Home |
| **Proxy** | **Nginx Proxy Manager** | Gestion du routage et des certificats SSL | `npm.ebroly.fr` | Nginx Proxy Manager |
| **Sécurité** | **Vaultwarden** | Gestionnaire de mots de passe chiffré | `vault.ebroly.fr` | Vaultwarden (Rust Bitwarden) |
| **Stockage** | **Nextcloud** | Cloud privé & synchronisation de fichiers | `cloud.ebroly.fr` | Nextcloud / MySQL |
| **Web** | **Landing Page** | Portail d'accueil & redirection | `ebroly.fr` | Nginx / HTML / CSS |
| **Web** | **Portfolio** | Site web personnel & backend de contact | `portfolio.ebroly.fr` | Nginx / Node.js Express |
| **Web** | **BTS TP Site** | Projet / TP BTS CIEL | `bts.ebroly.fr` | PHP 8.2 / MySQL 8.0 |
| **Web** | **Love Project** | Mini-projet web | `love.ebroly.fr` | Nginx Alpine |
| **Gaming** | **Serveur Minecraft** | Serveur de jeu multijoueur | `mc.ebroly.fr` | PaperMC 26.3 / Java |

---

## 📂 Organisation du Dépôt

Tous les fichiers de déploiement `docker-compose.yml` sont organisés par service sous le dossier `/docker` :

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
