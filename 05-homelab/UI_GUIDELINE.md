# Homelab: UI Guideline

## Web-UI (HTMX + Tailwind)
- Mobile first, ein Layout für alle Größen
- Ein Container, max. Breite begrenzen, Abstände im 4px-Raster (Tailwind-Skala)
- Eine Akzentfarbe, Rest neutral, Dark Mode via `dark:`
- Server rendert HTML, HTMX tauscht nur Teile aus (`hx-get`, `hx-swap`)
- Feedback: Ladeindikator (`htmx-indicator`), Erfolg und Fehler als kurze Meldung
- Formulare mit Validierung am Server, Fehler direkt am Feld
- Destruktive Aktionen mit Bestätigung (`hx-confirm`)
- Kontrast mindestens 4.5:1, Labels an allen Inputs

## CLI (Typer)
- Befehlsstruktur: `tool <nomen> <verb>` (z. B. `tool sensor list`)
- `--help` bei jedem Befehl, sinnvolle Defaults
- Normale Ausgabe auf stdout, Fehler auf stderr
- Maschinenlesbar optional: `--json`
- Exit-Code `0` bei Erfolg, sonst ungleich `0`
- Farbe sparsam, nie als einzige Information

## TUI (Textual)
- Alle Aktionen per Tastatur, Footer mit Keybindings anzeigen
- `q` beenden, `?` Hilfe, `/` Suche, Pfeile oder `j/k` navigieren
- Klare Bereiche: Liste, Detail, Statuszeile
- Lange Aufgaben asynchron, UI bleibt reaktiv
