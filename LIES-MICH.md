# Pony-Hof der Zahlen – Dateien für GitHub Pages / PWABuilder

Alle fünf Dateien gehören zusammen in den Hauptordner des GitHub-Repositorys:

| Datei | Zweck |
|---|---|
| `index.html` | Die komplette App (HTML, CSS und JavaScript in einer Datei, keine externen Abhängigkeiten) |
| `manifest.json` | App-Steckbrief (Name, Farben, Icons) – nötig für die APK |
| `service-worker.js` | Offline-Cache – die App startet auch ohne Internet |
| `icon-192.png`, `icon-512.png` | App-Symbol |

## Weiter geht es mit dem PDF-Plan
Phase 1 (GitHub Pages) → Phase 2 kann übersprungen werden (manifest & Service Worker sind schon dabei) → Phase 3 (PWABuilder) → Phase 4 (Installieren).

## Bedienung
- Eltern-Bereich: Zahnrad oben rechts im Menü, Standard-PIN **1234** (dort änderbar).
- Zeitlimit, Zahlenraum (bis 10 / bis 20), Sprachausgabe, Sound, Tagesfreischaltung, Namen ändern, Zurücksetzen – alles im Eltern-Bereich.
- Die automatische Schwierigkeit startet bei „bis 10", geht nach 5 richtigen Antworten in Folge eine Stufe hoch (max. so hoch wie im Eltern-Bereich erlaubt) und nach 3 Fehlern in Folge eine Stufe runter.

## App am Verlassen hindern (Android „Bildschirm anheften")
Der Home-Button kann von keiner App gesperrt werden – das verhindert Android grundsätzlich. Nutze stattdessen die eingebaute Funktion:
1. Einstellungen → Sicherheit → **Bildschirm anheften** (bei Samsung: Sicherheit und Datenschutz → Weitere Sicherheitseinstellungen → App anheften) einschalten.
2. Zusätzlich **Vor dem Loslassen PIN abfragen** aktivieren.
3. Pony-Hof öffnen, Übersichtstaste antippen, auf das App-Symbol tippen, **Anheften** wählen.
4. Zum Beenden Zurück + Übersicht gleichzeitig gedrückt halten und PIN eingeben.

Ergänzend gibt es im Eltern-Bereich den **Fokus-Modus**: Vollbild während der Übung, ein Begrüßungs-Bildschirm beim Zurückkommen und ein Zähler, wie oft die App während einer Übung verlassen wurde.

## Änderungen später
Wenn du Texte oder Grafiken anpassen möchtest, kannst du `index.html` an Gemini geben. Wichtig für alle Änderungen: Die App darf keine React-/Babel-/Tailwind-Skripte aus dem Internet laden – sie ist absichtlich ohne solche Abhängigkeiten gebaut.
