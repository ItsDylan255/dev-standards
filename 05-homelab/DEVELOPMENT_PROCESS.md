# Homelab: Development Process

Stack: Python, FastAPI, HTMX, Jinja2, SQLAlchemy, Docker Compose

Von oben nach unten abarbeiten.

## 1. Konzept
- [ ] Problem in einem Satz (`templates/CONCEPT.md`)
- [ ] Gibt es ein fertiges Tool (Self-Hosted)? Dann lieber das nutzen

## 2. Features und MVP
- [ ] 3 bis 5 MVP-Features, Rest später
- [ ] Brauche ich Web-UI, CLI/TUI oder beides?

## 3. Datenmodell und API
- [ ] Entities und Relations (`templates/DATA_MODEL.md`)
- [ ] Endpunkte auflisten (Methode, Pfad, Zweck)

## 4. Projekt-Setup
- [ ] `uv init`, Ruff, pytest einrichten
- [ ] Struktur: `app/{api,models,services,templates}`, `tests/`
- [ ] Config über Umgebungsvariablen (`.env`, nicht im Git)
- [ ] `Dockerfile` und `compose.yaml` früh anlegen

## 5. Umsetzung in Vertical Slices
- [ ] Pro Feature: Model → Service → Endpoint → Template → Test
- [ ] Datenbank-Änderungen über Alembic-Migrations
- [ ] Jede Slice lauffähig committen

## 6. Tests
- [ ] pytest für Services und Endpoints
- [ ] Einmal komplett über Docker durchstarten

## 7. Deployment
- [ ] Siehe `DEPLOYMENT_STANDARDS.md`
- [ ] Reverse Proxy, Backup und Monitoring einrichten

## 8. Betrieb
- [ ] Logs und Healthcheck prüfen
- [ ] Updates der Images regelmäßig
- [ ] Backup-Restore einmal testen
