# Jarvis aufs Handy bringen

Jarvis ist eine Web-App (PWA). Sie braucht eine HTTPS-Adresse, damit Mikrofon und Installation funktionieren. Am einfachsten und gratis geht das mit GitHub Pages.

## 1. Online stellen (GitHub Pages)
1. Auf github.com einloggen und ein neues Repository anlegen, z. B. `jarvis` (Public).
2. "uploading an existing file" wählen und **alle Dateien aus diesem Ordner** hochladen (index.html, manifest.webmanifest, sw.js und alle .png). Commit.
3. Settings → Pages → Source: "Deploy from a branch", Branch `main`, Ordner `/ (root)` → Save.
4. Nach ca. einer Minute ist die App erreichbar unter `https://<dein-name>.github.io/jarvis/`.

## 2. API-Schlüssel
Ausserhalb von Claude braucht Jarvis einen Anthropic API-Schlüssel:
1. Auf console.anthropic.com einen Schlüssel erstellen und Guthaben aufladen.
2. In Jarvis: Einstellungen → "Anthropic API-Schlüssel" einfügen → Fertig.

Der Schlüssel wird nur im Browser deines Handys gespeichert und nur an api.anthropic.com gesendet. **Schreib ihn nie in die Dateien im Repository**, sonst ist er öffentlich.

## 3. Auf dem Handy installieren
- **Android (Chrome):** Seite öffnen → Menü ⋮ → "App installieren" bzw. "Zum Startbildschirm hinzufügen".
- **iPhone (Safari):** Seite öffnen → Teilen-Symbol → "Zum Home-Bildschirm".

Beim ersten Tippen auf den Reaktor fragt das Handy nach dem Mikrofon → erlauben.

## Hinweise
- Spracherkennung läuft über den Dienst des Browsers und braucht Internet.
- iPhone: Falls das Mikrofon in der installierten App nicht reagiert, Jarvis direkt in Safari öffnen; dort funktioniert die Spracherkennung zuverlässiger.
- Timer laufen nur, solange die App offen ist.
- Updates: Dateien im Repository ersetzen; die App lädt beim nächsten Öffnen die neue Version.
