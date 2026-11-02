# Desktop: UI Guideline

Basis: Fluent-Prinzipien, angepasst für Avalonia

## Layout und Spacing
- 8px-Raster, Inhalt nicht an den Fensterrand kleben (mind. 16px)
- Hauptbereich dominiert, Nebenfunktionen in Sidebar oder Toolbar
- Mindestfenstergröße setzen, Layout muss skalieren

## Typography
- Systemschrift verwenden (Segoe UI Variable, Fallback Inter)
- 3 Stufen reichen: Titel, Text, Hinweis

## Color
- Avalonia FluentTheme nutzen, Light und Dark unterstützen
- Eine Akzentfarbe, Rest neutral
- Farben als Ressourcen, nicht fest im XAML

## Navigation und Fenster
- Wenige Hauptbereiche: Sidebar (NavigationView-Stil)
- Einstellungen in eigenem Bereich oder Dialog
- Modale Dialoge nur für Entscheidungen, sonst Inline

## Keyboard
- Alle Hauptaktionen per Tastatur erreichbar
- Standard-Shortcuts: `Ctrl+S`, `Ctrl+N`, `Ctrl+Z`, `F5`, `Esc` schließt Dialoge
- Tab-Reihenfolge logisch

## Feedback
- Lange Aufgaben: Progress-Anzeige, UI bleibt bedienbar (async)
- Fehler im Klartext, mit nächstem Schritt
- Destruktive Aktionen: Bestätigung oder Undo

## Accessibility
- Kontrast mindestens 4.5:1
- `AutomationProperties.Name` für wichtige Controls
- Fokus-Markierung sichtbar lassen
