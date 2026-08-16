# Fab 50 Navigator v9.2

Persönliche Progressive Web App (PWA) zum Finden, Abhaken, Fotografieren und Dokumentieren der **Disney Fab 50 Character Collection** in den vier Walt-Disney-World-Parks.

## Umfang

- **50 Charaktere**
- **36 physische Skulpturen**
- **4 Parks**
  - Magic Kingdom
  - EPCOT
  - Disney's Hollywood Studios
  - Disney's Animal Kingdom

## Checkliste & Fortschritt

- eine Zeile pro physischer Skulptur
- Mehrfach-Skulpturen zählen automatisch für mehrere Charaktere
- Gesamtfortschritt für Charaktere und Skulpturen
- Fortschritt pro Park
- Fund-Zeitstempel
- Anzeige der heute gefundenen Skulpturen
- Filter **Alle / Nur offene**
- lokale Speicherung auf dem Gerät

## Suche

Über die Schnellsuche **„Figur oder Skulptur suchen …“** kann nach Charakter oder Skulptur gesucht werden.

Ein Treffer:

- öffnet automatisch den richtigen Park,
- wechselt bei Bedarf von **Nur offene** auf **Alle**,
- scrollt direkt zur passenden Skulptur,
- hebt die Zielzeile kurz hervor.

## Standort & Navigation

### GPS

GPS ist optional und wird erst nach ausdrücklicher Aktivierung verwendet.

Die App zeigt:

- die geschätzte GPS-Genauigkeit,
- den wahrscheinlich aktuellen Park,
- die Luftlinien-Entfernung zu Skulpturen,
- die nächstgelegene noch offene Skulptur.

### Karte

- interaktive Leaflet-/OpenStreetMap-Karte
- alle 36 Skulpturen als Pins
- Status für offen / gefunden / nächstes Ziel
- eigener Standort als Marker
- Filter nach Park

Die gespeicherten Skulptur-Koordinaten sind Näherungspunkte anhand bekannter Landmarken und keine offiziell vermessenen Disney-Koordinaten. Entfernungen sind **Luftlinie**, keine Fußweg-Navigation.

### Park-Routen

Jeder Park enthält eine feste, sinnvoll sortierte Laufreihenfolge als Alternative oder Ergänzung zu GPS.

Zusätzlich gibt es pro Skulptur **„Wo ist sie?“** mit Landmarken und konkreteren Suchhinweisen.

## Galerie & eigene Fotos

Für jeden der 50 Charaktere kann ein eigenes Foto gespeichert werden.

- Fotoaufnahme oder Auswahl aus der Galerie
- vollständiges Originalfoto bleibt lokal gespeichert
- automatische Größenreduzierung ohne Verzerrung
- Speicherung in IndexedDB
- eigener Fotoeintrag pro Charakter
- vorhandene Fotos können ersetzt oder gelöscht werden
- Galerie zeigt den Fortschritt `x / 50`

### Manueller Bildausschnitt

Für jedes Foto kann der spätere **4:3-Ausschnitt** selbst festgelegt werden.

Im Editor kann das Foto:

- horizontal und vertikal verschoben,
- über Slider gezoomt,
- mit `+ / −` gezoomt,
- per **Pinch-to-Zoom** mit zwei Fingern gezoomt werden.

Das komplette Foto bleibt gespeichert. Gespeichert werden zusätzlich nur Ausschnittposition und Zoom.

## Erinnerungs-Export

Unter **Galerie → Souvenir-Set** stehen vier Exportdesigns zur Verfügung.

### Classic Collection

- 1 Seite
- alle 50 Charaktere
- klares, strukturiertes Raster
- minimale Dekoration
- Fokus auf vollständige Dokumentation

### Fab 50 Souvenir

- 5 Seiten
- 1 Gesamtübersicht + 4 Parkseiten
- Dunkelblau, Gold, Feuerwerk und Schloss-Silhouette
- Gesamtübersicht bewusst strukturiert
- Parkseiten mit leicht gedrehten Fotoprints

### Park Memories

- 7 Seiten
- Album-/Scrapbook-Look
- größere Fotos
- leichte Drehungen
- kontrollierte Überlappungen
- Schatten und Tape-Details
- Magic Kingdom auf mehrere Seiten verteilt, damit die Fotos größer bleiben

### Celebration Poster

- 1 Abschluss-Poster
- bis zu **8 frei auswählbare eigene Fotos**
- automatische Vorauswahl möglich
- ein Foto wird mit **★ als Hauptfoto** festgelegt
- großes Hero-Foto plus kleinere Highlights
- dynamischer Fototisch-/Scrapbook-Look
- Feuerwerk, Schloss und 50/50-Abschlussdarstellung

## Crop-Konsistenz in v9.2

Der Export verwendet dieselbe geometrische Berechnung wie der manuelle 4:3-Crop-Editor.

Damit werden:

- horizontaler Versatz,
- vertikaler Versatz,
- manueller Zoom

beim Export korrekt übernommen.

Alle relevanten Export-Fotoflächen basieren auf 4:3, damit der gespeicherte Ausschnitt reproduzierbar bleibt.

## Abschluss bei 50 / 50

Nach dem letzten Fund erscheint ein Abschlussbildschirm mit:

- Feuerwerk-Animation
- **50 / 50**
- **36 / 36 Skulpturen**
- **4 / 4 Parks**
- Zeitpunkt des ersten und letzten Fundes
- erneut abspielbarem Feuerwerk
- direktem Zugang zum Erinnerungs-Export

## Backup

Das JSON-Backup enthält derzeit:

- gefundene Skulpturen
- Fund-Zeitstempel

**Fotos, Crops und Zoomwerte sind nicht Bestandteil des JSON-Backups.**

Diese Daten liegen lokal in IndexedDB. Werden die Website-/App-Daten vollständig gelöscht, gehen die dort gespeicherten Fotos ebenfalls verloren.

## Offline-Nutzung

Nach erfolgreicher Installation arbeitet die PWA weitgehend offline:

- Checkliste
- Fortschritt
- Suchfunktion
- Park-Routen
- gespeicherte Fotos
- Crop-Editor
- Erinnerungs-Export

Die OpenStreetMap-Kartenkacheln benötigen normalerweise eine Datenverbindung, sofern sie nicht bereits gecacht wurden.

## Lokale Datenspeicherung

- Checkliste / Zeitstempel: `localStorage`
- Fotos / Crop / Zoom: IndexedDB `fab50-photo-db-v1`

Der bestehende Storage-Key bleibt erhalten, damit Updates innerhalb desselben GitHub-Pages-Projekts die bisherigen Funde nicht löschen.

## Update über GitHub Pages

Für ein Update:

1. ZIP entpacken.
2. Den **kompletten Inhalt** in das bestehende GitHub-Repository hochladen.
3. Gleichnamige Dateien überschreiben.
4. Änderungen committen.
5. GitHub Pages kurz neu deployen lassen.
6. Die PWA auf dem Smartphone vollständig schließen und erneut öffnen.

Der Service-Worker-Cache dieser Version lautet **fab50-v9-2**.

## Dateien

- `index.html`
- `manifest.webmanifest`
- `sw.js`
- `README.md`
- `icons/icon-192.png`
- `icons/icon-512.png`
- `icons/icon-maskable-512.png`
