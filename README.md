# Fab 50 Navigator v6

## Funktionen
- 36 physische Fab-50-Skulpturen / 50 Charaktere
- Fortschritt gesamt und pro Park
- Fund-Zeitstempel und lokale Speicherung
- „Wo ist sie?“-Hinweise
- optimierte feste Laufreihenfolge pro Park
- GPS-Ortung (freiwillig)
- Luftlinien-Entfernung zu allen Skulpturen
- automatische „nächste offene Statue“ im aktuellen Park
- interaktive Leaflet/OpenStreetMap-Karte mit Status-Pins
- **eigenes Foto pro Charakter (50 separate Fotoplätze)**
- Fotos aus Kamera/Galerie, automatisch quadratisch zugeschnitten und komprimiert
- lokale Bildspeicherung per IndexedDB; App-Updates behalten die Fotos
- Fotoübersicht mit 0–50 Fortschritt
- **automatische 50er-Abschluss-Collage als JPG**
- Collage teilen oder als Bild speichern
- Backup / Wiederherstellung für Häkchen und Zeitstempel
- Offline-PWA für Checkliste, Routen und gespeicherte Fotos; Kartenkacheln benötigen Datenverbindung
- 50/50-Abschlussbildschirm mit Feuerwerk-Animation und Statistik

## Update von v5
Die App verwendet weiterhin den Storage-Key `fab50-tracker-v2`. Bestehende Häkchen und Zeitstempel bleiben erhalten, wenn du die Dateien im selben GitHub-Pages-Projekt ersetzt. Fotos verwenden zusätzlich die IndexedDB `fab50-photo-db-v1`.

## Foto-Hinweis
Die Bilder bleiben ausschließlich lokal im Browser-/PWA-Speicher dieses Geräts. Der JSON-Backup-Button sichert derzeit nur Häkchen und Zeitstempel, nicht die Fotos. Wenn App-/Website-Daten vollständig gelöscht werden, gehen auch die lokalen Fotos verloren.

## GPS-Hinweis
Die Pins sind Näherungspunkte auf Basis der bekannten Standort-Landmarken. Angezeigte Entfernungen sind Luftlinie, keine Fußweg-Navigation.


## Neu in v6.1
- Souvenir-artiger Collage-Export
- 5 Seiten: 1 Gesamtübersicht + 4 einzelne Park-Seiten
- Vor-/Zurück-Navigation im Collage-Dialog
- Download der aktuellen Seite oder aller 5 Seiten
- Teilen der aktuell sichtbaren Seite


## v6.1.1 Hotfix
- Behebt einen JavaScript-Syntaxfehler aus v6.1, durch den die Park-/POI-Listen nicht gerendert wurden.
- Vollständiges PWA-Paket mit Manifest, Service Worker und Icons.
- Service Worker nutzt eine neue Cache-Version und Network-First für lokale Dateien, damit Updates zuverlässiger geladen werden.
