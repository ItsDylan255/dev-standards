# Elektrotechnik: Development Process

Stack: KiCad, LTspice, Python (NumPy, SciPy, PyVISA)

Von oben nach unten abarbeiten.

## 1. Anforderungen
- [ ] Was soll die Schaltung tun? (`templates/CONCEPT.md`)
- [ ] Spannungen, Ströme, Bandbreite, Platzgrenzen festlegen

## 2. Blockschaltbild
- [ ] Funktionsblöcke und Signalfluss skizzieren
- [ ] Bauteile pro Block auswählen, Datenblätter lesen

## 3. Berechnung und Simulation
- [ ] Wichtige Werte per Hand oder Python berechnen
- [ ] In LTspice simulieren (DC, AC, Transient)
- [ ] Auf Breadboard prüfen, wenn möglich

## 4. Schaltplan (KiCad)
- [ ] Symbole, Footprints, Werte zuweisen
- [ ] Entkopplung, Schutzbeschaltung, Testpunkte einplanen
- [ ] ERC fehlerfrei

## 5. PCB-Layout
- [ ] Board-Umriss und Stackup festlegen
- [ ] Platzierung zuerst, dann Routing
- [ ] DRC fehlerfrei
- [ ] Regeln aus `DESIGN_RULES.md` prüfen

## 6. Review und Fertigung
- [ ] Review-Checkliste aus `DESIGN_RULES.md`
- [ ] Gerber, BOM und Pick-and-Place exportieren
- [ ] Bestellen (JLCPCB/PCBWay)

## 7. Bring-up
- [ ] Erst Sichtprüfung und Kurzschlusstest
- [ ] Spannungen einzeln hochfahren (Netzteil mit Strombegrenzung)
- [ ] Blöcke nacheinander testen

## 8. Messung und Doku
- [ ] Messen und mit Simulation vergleichen
- [ ] Fehler und Änderungen für Revision B notieren
- [ ] KiCad-Projekt und Gerber-Version taggen
