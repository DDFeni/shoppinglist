# Einkaufsliste (PWA) – GitHub Pages

Dies ist eine kleine Progressive Web App (PWA) für die Einkaufsliste.  
Sie funktioniert offline, lässt sich auf dem Handy installieren und speichert deinen Abhak-Status lokal.

## Dateien
- `index.html` – App
- `manifest.webmanifest` – PWA Manifest
- `sw.js` – Service Worker (Offline-Funktion)
- `icons/` – App-Icons (192 & 512 px)
- `.nojekyll` – Deaktiviert Jekyll-Verarbeitung auf GitHub Pages

## Deploy auf GitHub Pages (Projektseite)
1. **Neues Repository anlegen** (z. B. `einkaufsliste`).
2. **Dateien hochladen**: Den gesamten Inhalt dieses Ordners (inkl. `.nojekyll`) ins Repo kopieren und committen.
3. **GitHub Pages aktivieren**:  
   - In deinem Repo: **Settings → Pages**  
   - **Source**: `Deploy from a branch`  
   - **Branch**: `main` und Ordner `/ (root)` → **Save**  
4. Warte kurz, bis GitHub eine URL anzeigt (z. B. `https://<username>.github.io/einkaufsliste/`).  
5. Die App öffnen → **Zum Startbildschirm hinzufügen** (im Browser-Menü).

**Hinweis**: `start_url` und alle Pfade sind relativ (`./`), deshalb funktioniert die App in einem Projekt-Unterordner.

## Daten anpassen
Die Liste befindet sich in `index.html` innerhalb der Konstanten `DATA`.  
Dort kannst du einfach Einträge ändern, hinzufügen oder entfernen.

## Troubleshooting
- Seite lädt offline nicht? → Einmal online öffnen, damit der Service Worker alles cacht.  
- Änderungen werden nicht angezeigt? → Seite neu laden, ggf. Service Worker in den Browser-Einstellungen „unregistern“ und neu öffnen.  
- iOS (Safari) zeigt „Installieren“ nicht? → Über Teilen-Menü **Zum Home-Bildschirm** wählen.
