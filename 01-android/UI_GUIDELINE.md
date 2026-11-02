# Android: UI Guideline

Basis: Material 3

## Layout und Spacing
- 8dp-Raster (4dp für feine Abstände), Seitenrand 16dp
- Touch Targets mindestens 48dp
- Wichtigste Aktion unten erreichbar (FAB oder Bottom Bar)
- Responsive: Compact, Medium, Expanded (WindowSizeClass) bedenken

## Typography
- Nur Material-3-Typescale nutzen (`titleLarge`, `bodyMedium`, ...)
- Max. 2 Schriftgrößen-Stufen pro Screen-Bereich
- Text in `sp`, nie in `dp`

## Color
- Theme mit Material Theme Builder erzeugen, Dynamic Color optional
- Nur Farb-Rollen verwenden (`primary`, `surface`, `error`), keine festen Hex-Werte im UI-Code
- Dark Mode von Anfang an testen
- Kontrast mindestens 4.5:1

## Navigation
- 3 bis 5 Hauptziele: Bottom Navigation Bar
- Mehr: Navigation Drawer
- Zurück-Geste muss immer sinnvoll funktionieren

## Feedback
- Jeder Screen hat 3 Zustände: Loading, Empty, Error
- Aktionen bestätigen mit Snackbar, Fehler mit Retry-Option
- Destruktive Aktionen: Bestätigung oder Undo

## Accessibility
- `contentDescription` für Icons und Bilder
- Schrift bis 200 % skalieren testen
- Nicht nur Farbe als Information nutzen
