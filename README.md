# dev-standards

Meine persönlichen Development Standards: pro Tech-Stack ein Playbook, das ich bei jedem neuen Projekt abarbeite.

## Struktur

| Ordner | Inhalt |
|---|---|
| `general/` | Stackübergreifend: Git-Workflow, Definition of Done, Dokumentation |
| `templates/` | Kopiervorlagen für den Projektstart |
| `01-android/` | Development Process, UI Guideline |
| `02-desktop/` | Development Process, UI Guideline |
| `03-embedded/` | Development Process, Firmware Guideline |
| `04-electronics/` | Development Process, Design Rules |
| `05-homelab/` | Development Process, UI Guideline, Deployment Standards |

## Die 5 Tech-Stacks

### 1. Android: Kotlin + Jetpack Compose
- **Mit was:** Kotlin, Jetpack Compose, MVVM, Coroutines/Flow, Hilt, Room, Retrofit/Ktor
- **Warum:** Offizieller Google-Weg mit der besten Doku. Kotlin ist als Java-Kenner schnell gelernt.

### 2. Desktop: C# + Avalonia UI
- **Mit was:** C# (.NET), Avalonia UI, MVVM (CommunityToolkit.Mvvm), EF Core + SQLite
- **Warum:** Eine Sprache, ein Ökosystem. Läuft auf Windows und Linux ohne Anpassungen.

### 3. Embedded: ESP32 + STM32 in C/C++
- **Mit was:** ESP-IDF + FreeRTOS (ESP32), HAL/LL + CubeMX (STM32), I2C/SPI/UART, MQTT
- **Warum:** ESP32 für Sensoren und Konnektivität, STM32 für Echtzeit und Hardware-Verständnis. C/C++ ist der Industriestandard.

### 4. Elektrotechnik: KiCad + LTspice + Python
- **Mit was:** KiCad (Schaltplan/PCB), LTspice (Simulation), Python mit NumPy/SciPy/PyVISA (Auswertung, Messautomatisierung)
- **Warum:** Kompletter Weg von Simulation über Platine bis Messung, alles kostenlos. Python kenne ich schon.

### 5. Homelab: Python + FastAPI + HTMX + Docker
- **Mit was:** FastAPI, HTMX + Jinja2 + Tailwind, Typer/Textual (CLI/TUI), Docker Compose, Caddy, Mosquitto (MQTT)
- **Warum:** Schnell zu Ergebnissen, Python ist bekannt. Passt direkt zu den ESP32-Sensoren über MQTT.

## Benutzung bei Projektstart

1. Stack-Ordner öffnen, `DEVELOPMENT_PROCESS.md` von oben nach unten durchgehen.
2. Passende Vorlagen aus `templates/` ins Projekt kopieren.
3. Vor dem Release `general/DEFINITION_OF_DONE.md` abhaken.

## Konventionen

- Fachbegriffe auf Englisch, Erklärungen auf Deutsch.
- `DEVELOPMENT_PROCESS.md`: Ablauf eines Projekts in fester Reihenfolge (Konzept bis Release).
- `UI_GUIDELINE.md`: wie ich ein gutes, passendes UI gestalte.
- Lernthemen und Konzepte stehen nicht hier, sondern im Projektmanager.

## Status

Erste Version komplett. Bewusst kurz gehalten, wird beim Benutzen angepasst.
