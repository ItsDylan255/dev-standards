# Android: Development Process

Stack: Kotlin, Jetpack Compose, MVVM, Coroutines/Flow, Hilt, Room, Retrofit/Ktor

Von oben nach unten abarbeiten.

## 1. Konzept
- [ ] Problem und Zielgruppe in einem Satz (`templates/CONCEPT.md`)
- [ ] Gibt es das schon? Was mache ich anders?

## 2. Features und MVP
- [ ] Alle Ideen sammeln, dann auf 3 bis 5 MVP-Features kürzen
- [ ] Rest unter "Später"

## 3. User Flows und Wireframes
- [ ] Screens auflisten, Flow als Skizze (Papier oder Figma)
- [ ] Pro Screen: Zweck, Daten, Aktionen

## 4. Datenmodell
- [ ] Entities und Relations (`templates/DATA_MODEL.md`)
- [ ] Was liegt lokal (Room), was im Netz (API)?

## 5. Architektur und Setup
- [ ] Projekt mit Compose anlegen, Min SDK festlegen
- [ ] Version Catalog, Hilt, Navigation Compose einrichten
- [ ] Pakete pro Feature: `feature/x/{ui,domain,data}`
- [ ] Git-Repo und `.gitignore`

## 6. Umsetzung in Vertical Slices
- [ ] Pro Feature: Data → ViewModel → UI → Test
- [ ] Mit dem Kern-Feature starten
- [ ] Jede Slice lauffähig committen

## 7. Polish
- [ ] Loading, Empty und Error States
- [ ] Dark Mode, Rotation, Accessibility prüfen

## 8. Testing
- [ ] Unit Tests für ViewModel und Repository
- [ ] Compose UI Test für den Kernflow
- [ ] Auf echtem Gerät testen

## 9. Release
- [ ] Icon, Name, Privacy Policy
- [ ] Signing Key sichern, `.aab` bauen
- [ ] Play Console: Internal Testing, dann Production

## 10. Maintenance
- [ ] Crash-Reports lesen
- [ ] Dependencies und `targetSdk` jährlich updaten
