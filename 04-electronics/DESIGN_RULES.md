# Elektrotechnik: Design Rules

## Schaltplan
- Signalfluss von links nach rechts, Versorgung oben, Masse unten
- Ein Block pro Bereich oder Hierarchisches Sheet
- Aussagekräftige Netznamen (`I2C_SDA`, `3V3`, nicht `Net-(R1-Pad1)`)
- Werte und Bauteilnummern (MPN) am Symbol pflegen
- Pull-ups, Entkopplung und Schutz im Plan sichtbar
- Testpunkte für Versorgung, Masse und wichtige Signale

## PCB-Layout
- Zuerst platzieren (Stecker, Controller, Quarz), dann routen
- Entkopplungskondensatoren direkt an den Versorgungspins
- Durchgehende Massefläche, möglichst nicht zerschneiden
- Leiterbahnbreite nach Strom (Power breiter, Signal 0,2 bis 0,3 mm)
- Schnelle oder analoge Signale kurz halten, von Schaltreglern trennen
- Keine 90°-Ecken, Via-Zahl niedrig halten
- Beschriftung: Pin 1, Polarität, Version, Testpunkte

## Review vor Bestellung
- [ ] ERC und DRC ohne Fehler
- [ ] Footprints gegen Datenblatt geprüft (1:1 ausgedruckt testen)
- [ ] Pinbelegung der Stecker doppelt geprüft
- [ ] Polarität: Dioden, Elkos, ICs
- [ ] Versorgung: Spannung und Strom jedes Reglers ausreichend
- [ ] Pull-ups, Reset, Boot-Pins korrekt
- [ ] Programmier-Anschluss erreichbar
- [ ] BOM: alle Teile verfügbar
- [ ] Gerber im Viewer kontrolliert

## Nach Bring-up
- [ ] Fehler und Verbesserungen für nächste Revision notieren
