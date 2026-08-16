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


## Neu in v6.1.2
- Uploads behalten jetzt ihr ursprüngliches Seitenverhältnis
- Keine gestreckten Bilder mehr in Galerie oder Souvenir-Set
- Fotos werden per Center-Crop in den Rahmen eingepasst
- Square/nahezu quadratische Bildflächen auf den Park-Seiten, besonders für Animal Kingdom verbessert


## Neu in v6.1.3
- Einzelne Park-Souvenir-Seiten neu gestaltet: kompakte dunkle Karten statt großer Rahmen
- 4:3-Fotofenster mit feinem Goldrand; Bilder bleiben unverzerrt und werden nur gecroppt
- Unvollständige letzte Zeilen werden zentriert
- Links-/Rechts-Wischen zwischen allen 5 Souvenir-Seiten
- Seitenpunkte und dezente Übergangsanimation im Souvenir-Viewer


## Neu in v7
- Manueller Bildausschnitt pro Charakterfoto
- Das vollständige Foto bleibt gespeichert
- Fester 4:3-Rahmen im Editor; du verschiebst das Bild innerhalb des Rahmens
- Der gewählte Ausschnitt erscheint in Galerie-Vorschau und auf den Souvenir-Set-Seiten
- Nach jedem neuen Foto öffnet sich direkt der Ausschnitt-Editor


## Neu in v7.1
- Zoom-Funktion im Bildausschnitt-Editor
- Slider sowie + / − Buttons für den Zoom
- Der gewählte Zoom wird zusammen mit dem Ausschnitt gespeichert
- Vorschau und Souvenir-Set verwenden jetzt sowohl den manuellen Ausschnitt als auch den Zoom


## Neu in v7.2
- Pinch-to-Zoom im Bildausschnitt-Editor
- Zoomen jetzt per Zwei-Finger-Geste direkt auf dem Bild
- Slider und + / − Buttons bleiben zusätzlich erhalten


## Neu in v8
- Schnellsuche nach Charakter oder Skulptur
- Live-Treffer während der Eingabe
- Treffer öffnet automatisch den richtigen Park und springt zur passenden Zeile
- „Nur offene“ wird für einen Suchtreffer automatisch auf „Alle“ umgeschaltet
- Zielzeile wird kurz hervorgehoben
- Versionsnummer `v8` direkt in der Unterzeile des App-Headers
