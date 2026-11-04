# Backend & Self-Hosting: Deployment Standards

## Container
- Ein Dienst = ein Container, Definition in `compose.yaml`
- Images mit festem Tag (nicht `latest`)
- `restart: unless-stopped`, Healthcheck definieren
- Daten in benannten Volumes oder festen Ordnern, nie im Container
- Läuft als Nicht-Root-User, wenn möglich

## Reverse Proxy
- Caddy vor allen Web-Diensten, HTTPS automatisch
- Dienste nur über den Proxy erreichbar, keine direkten Ports nach außen
- Subdomain pro Dienst (`dienst.home.example`)

## Secrets
- `.env` oder Docker Secrets, nie im Git
- `.env.example` ohne echte Werte ins Repo

## Backups
- restic: täglich, Ziel auf anderem Gerät oder Cloud
- Gesichert werden Volumes, Datenbank-Dumps und Configs
- Restore einmal pro Projekt testen

## Monitoring
- Prometheus + Grafana für Metriken, Healthchecks für Uptime
- Alarm nur für wirklich wichtige Dinge

## Zugriff von außen
- Kein Port-Forwarding, stattdessen Tailscale oder WireGuard
- Admin-Oberflächen nur im VPN erreichbar

## MQTT (Sensoren)
- Mosquitto mit Benutzer und Passwort
- Topic-Schema: `home/<raum>/<gerät>/<messwert>`
