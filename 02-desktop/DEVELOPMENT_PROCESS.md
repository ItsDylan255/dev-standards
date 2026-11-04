# Desktop: Development Process

## 1. Konzept
- [ ] Problem und Zielgruppe in einem Satz (`templates/CONCEPT.md`)
- [ ] Windows only oder auch Linux? Früh festlegen

## 2. Features und MVP
- [ ] Ideen sammeln, auf 3 bis 5 MVP-Features kürzen

## 3. User Flows und Wireframes
- [ ] Fenster und Dialoge auflisten
- [ ] Hauptfenster-Layout skizzieren (Menü, Navigation, Inhalt)
- [ ] Keyboard-Workflow mitdenken

## 4. Datenmodell
- [ ] Entities und Relations (`templates/DATA_MODEL.md`)
- [ ] Speicherort: SQLite (EF Core) oder JSON-Datei

## 5. Architektur und Setup
- [ ] `dotnet new` mit Avalonia-Template, Solution in Projekte trennen (`App`, `Core`, `Tests`)
- [ ] MVVM mit CommunityToolkit.Mvvm, DI einrichten
- [ ] Git-Repo und `.gitignore`

## 6. Umsetzung in Vertical Slices
- [ ] Pro Feature: Model → Service → ViewModel → View → Test
- [ ] Logik gehört in `Core`, nicht in die Views
- [ ] Jede Slice lauffähig committen

## 7. Polish
- [ ] Settings speichern, Fenstergröße merken
- [ ] Fehlerdialoge, Logging in Datei
- [ ] Auf Windows und Linux starten

## 8. Testing
- [ ] xUnit für Core und ViewModels
- [ ] Manueller Durchlauf des Kernflows

## 9. Release
- [ ] `dotnet publish` (self-contained, single file)
- [ ] Installer (Velopack/MSI), Linux: AppImage oder `.deb`
- [ ] Versionsnummer und Icon setzen

## 10. Maintenance
- [ ] .NET-LTS-Updates und NuGet-Updates regelmäßig
