# Nginx Reverse Proxy for Resume & Club Websites

This project provides a production-ready Nginx reverse proxy configuration for hosting two Django-based websites behind a single EC2 instance.

## 🔧 Services

- **nginx**: Routes HTTP/HTTPS traffic to:
  - `resume` (personal site)
  - `club` (group site)

## 📁 Structure

```
.
├── docker-compose.yml
└── nginx/
├── nginx.conf # Main Nginx config
├── ssl/ # Let's Encrypt certificates (mounted)
├── ssl-dhparams/ # Diffie-Hellman params (mounted)
└── www/ # ACME challenge directory
```

## 🌐 Domains

Configured for:

- `codingunited.club` → Resume site
- `jmdelima.cv` → Club site

## 🔐 SSL

- Nginx serves `/.well-known/acme-challenge/` for Certbot verification.
- SSL files are expected under `./nginx/ssl` and `./nginx/ssl-dhparams`.

## 🚀 Deployment

This setup is **not intended for local development**. It's designed for use in production on an EC2 instance.

Start the stack:

```bash
docker compose up -d
```

## Extras

- Auto-restart policy (unless-stopped)

- Custom Docker label: project=reverse-proxy
