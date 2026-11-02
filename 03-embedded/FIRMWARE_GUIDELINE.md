# Embedded: Firmware Guideline

## Projektstruktur
- `main/` nur Startup und Task-Erzeugung
- `components/<name>/` pro Treiber oder Modul (eigene Header und Source)
- Hardware-Zugriff nur in Treibern, Logik hardwareunabhängig
- `docs/PINOUT.md` mit Pin-Tabelle

## Naming
- Dateien und Funktionen: `snake_case`, Präfix pro Modul (`bme280_read()`)
- Konstanten und Makros: `UPPER_CASE`
- Pin-Namen als Konstanten, keine Magic Numbers

## Error Handling
- Jede Funktion mit möglichem Fehler gibt einen Status zurück (`esp_err_t`)
- Rückgabewerte immer prüfen
- Bei Fehlern: loggen, wiederholen oder in sicheren Zustand gehen

## Logging
- Log-Level nutzen (Error, Warn, Info, Debug)
- Ein Log-Tag pro Modul
- Keine Logs in Interrupts

## Tasks und Interrupts (FreeRTOS)
- ISR kurz halten, Arbeit an Task übergeben (Queue oder Semaphore)
- Gemeinsame Daten schützen (Mutex)
- Stack-Größen prüfen (High Water Mark)

## Power
- Peripherie abschalten, wenn nicht genutzt
- Deep Sleep für Batteriebetrieb, Wake-up-Quelle dokumentieren

## Tests
- Reine Logik auf dem PC testen (Unity)
- Hardware-Teile mit einfachem Testprogramm je Treiber

## Sicherheit
- WiFi-Daten und Tokens in NVS oder `sdkconfig`, nie im Git
