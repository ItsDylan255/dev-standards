# dev-standards

Meine Development Standards: pro Tech-Stack ein Playbook für den Projektstart, mit festem Ablauf von Konzept bis Release und Guidelines für gutes Design. Bewusst kurz gehalten, damit ich es bei jedem neuen Projekt wirklich benutze.

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

### 1. Android

**Kotlin + Jetpack Compose**

| Bereich | Wahl |
|---|---|
| Sprache / UI | Kotlin, Jetpack Compose, Material 3 |
| Design System | Material 3 |
| Architektur | MVVM, Unidirectional Data Flow, ViewModel + StateFlow |
| Async | Coroutines + Flow |
| Dependency Injection | Hilt |
| Daten | Room (SQLite), DataStore |
| Netzwerk | Retrofit + OkHttp oder Ktor, kotlinx.serialization |
| Navigation | Navigation Compose |
| Tests | JUnit, MockK, Compose UI Tests |
| Tooling / Release | Android Studio, Gradle (Kotlin DSL), Play Console, `.aab` |

**Warum:** Der offizielle Google-Weg mit der besten Doku und den meisten Tutorials. Kotlin lernst du als eigene Sprache.

### 2. Desktop (Windows, evtl. Linux)

**C# + Avalonia UI**

| Bereich | Wahl |
|---|---|
| Sprache / UI | C# (.NET LTS), Avalonia UI mit XAML |
| Design System | Avalonia Fluent-Theme |
| Architektur | MVVM mit CommunityToolkit.Mvvm |
| Dependency Injection | Microsoft.Extensions.DependencyInjection |
| Daten | EF Core + SQLite, Settings als JSON |
| Async / Netzwerk | async/await, HttpClient, System.Text.Json |
| Tests | xUnit, NSubstitute, Avalonia Headless Testing |
| Tooling / Release | Rider oder VS Code, `dotnet` CLI, `dotnet publish`, Velopack, AppImage / `.deb` |

**Warum:** Eine Sprache, ein Ökosystem. Läuft auf Windows und Linux ohne Anpassungen.

### 3. Embedded

**ESP32 (ESP-IDF) + STM32, beides in C/C++**

| Bereich | ESP32 | STM32 |
|---|---|---|
| Hardware | ESP32-S3 oder -C3 | Nucleo-Board (z. B. F446RE) |
| Framework | ESP-IDF + FreeRTOS | HAL / LL, CubeMX, später Register |
| Tooling | VS Code + ESP-IDF, `idf.py`, GDB / OpenOCD | STM32CubeIDE, OpenOCD, SWD |
| Schnittstellen | GPIO, ADC, I2C, SPI, UART, PWM | gleiche, dazu Timer, DMA, NVIC |
| Fokus | WiFi, BLE, MQTT, OTA, Deep Sleep | Echtzeit, Timing, Bootloader, Linker Script |
| Tests | Unity (auf dem PC), Wokwi | Logic Analyzer |

**Warum:** ESP32 für Sensoren und Konnektivität, STM32 für Echtzeit und tiefes Hardware-Verständnis. C/C++ ist der Industriestandard.

### 4. Elektrotechnik

**KiCad + LTspice + Python**

| Bereich | Wahl |
|---|---|
| Schaltplan / PCB | KiCad |
| Simulation | LTspice (alternativ ngspice) |
| Auswertung | Python: NumPy, SciPy, Matplotlib, Jupyter |
| Messtechnik | Multimeter, Oszilloskop, Logic Analyzer, Python + PyVISA (SCPI) |
| Fertigung | JLCPCB / PCBWay, SMD-Bestückung |
| Gehäuse | FreeCAD oder Fusion 360 |

**Warum:** Der ganze Weg von Simulation über Platine bis Messung, alles kostenlos. Zwei Tracks: Grundlagen und Messen, dann Design.

### 5. Backend & Self-Hosting

**Python + FastAPI + Docker**

| Bereich | Backend (Programmieren) | Self-Hosting (Betrieb) |
|---|---|---|
| Kern | FastAPI, Pydantic, SQLAlchemy + Alembic | Docker Compose, Caddy |
| Web-UI | HTMX + Jinja2 + Tailwind | — |
| Design System | Tailwind | — |
| Terminal | Typer (CLI), Textual (TUI) | — |
| Daten / Messaging | SQLite, später PostgreSQL | Mosquitto (MQTT) |
| Betrieb | uv, Ruff, pytest | restic (Backups), Prometheus + Grafana |
| Zugriff | — | Tailscale oder WireGuard |
| Hosting | — | Mini-PC oder Raspberry Pi mit Debian, optional Proxmox |
