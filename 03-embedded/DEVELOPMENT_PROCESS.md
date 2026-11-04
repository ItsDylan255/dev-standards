# Embedded: Development Process

## 1. Anforderungen
- [ ] Was soll das Gerät tun? (`templates/CONCEPT.md`)
- [ ] Messgrößen, Abtastrate, Stromversorgung (Netz oder Batterie)?
- [ ] ESP32 (Konnektivität) oder STM32 (Echtzeit)?

## 2. Hardware-Auswahl
- [ ] Controller, Sensoren und Bauteile wählen, Datenblätter lesen
- [ ] Spannungspegel prüfen (3,3 V vs. 5 V)
- [ ] Bus-Adressen und Pin-Konflikte prüfen

## 3. Pinout und Aufbau
- [ ] Pinout-Tabelle anlegen (Pin, Funktion, Bauteil)
- [ ] Breadboard-Aufbau, Multimeter-Check vor dem ersten Einschalten

## 4. Architektur
- [ ] Blockdiagramm: Treiber, Tasks, Kommunikation
- [ ] Tasks und Queues festlegen (FreeRTOS)
- [ ] Hardware-Zugriff in Treiber kapseln

## 5. Umsetzung
- [ ] Erst Treiber einzeln testen (ein Sensor, ein Bus)
- [ ] Dann Tasks zusammensetzen
- [ ] Dann Konnektivität (WiFi, MQTT, BLE)
- [ ] Jeden Schritt committen, wenn er läuft

## 6. Testing und Debugging
- [ ] Logik auf dem PC testen (Unity)
- [ ] Logic Analyzer oder Oszilloskop bei Bus-Problemen
- [ ] GDB/OpenOCD bei Abstürzen
- [ ] Langzeittest (mind. 24 h) auf Speicherlecks und Resets

## 7. Härten
- [ ] Watchdog, Reconnect-Logik, Fehlerbehandlung
- [ ] Power Management (Deep Sleep) bei Batteriebetrieb

## 8. Release
- [ ] Config in NVS, keine Secrets im Code
- [ ] OTA-Update einrichten (ESP32)
- [ ] Firmware-Version und Pinout im README
