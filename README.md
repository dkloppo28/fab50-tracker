# Fab 50 Tracker v4

Installierbare Progressive Web App für die Disney Fab 50 Character Collection in Walt Disney World.

## Was ist neu in v4
- 36 physische Skulpturen statt 50 separater Listenzeilen
- weiterhin Fortschritt über alle 50 Charaktere
- eigener 36-Skulpturen-Zähler
- Park-Kacheln mit Fortschritt
- aufklappbare Parkbereiche
- „Wo ist sie?“-Hinweis pro Skulptur mit präzisen Landmarken
- optimale Laufroute pro Park ab Haupteingang
- Route-Modus mit nummerierten Stopps und automatisch markiertem „Nächster Stopp“
- automatischer Fund-Zeitstempel
- "Nur offene"-Filter
- Backup und Wiederherstellung per JSON
- Offline-Nutzung
- installierbar als PWA

## Lokal testen
    python -m http.server 8000

Dann `http://localhost:8000` öffnen.

## Auf Android installieren
Die Seite muss über HTTPS bereitgestellt werden, z.B. über GitHub Pages, Netlify oder Cloudflare Pages.
Danach in Chrome öffnen und "App installieren" auswählen.
