# FlixBus VAT-ID Prüfer

Diese Demo-Seite nutzt die offizielle BZSt eVATR REST-API zur Prüfung ausländischer Umsatzsteuer-Identifikationsnummern im FlixBus-Design.

## Funktionen

- Import von USt-ID-Daten aus Excel (`.xlsx`, `.xls`) oder CSV (`.csv`)
- Automatische Zuordnung gängiger Spaltenbezeichnungen für USt-IdNrn, Firmenname, Ort, Straße und PLZ
- Auswahl des richtigen Blatts, wenn die Datei mehrere Sheets enthält (z. B. Stammdaten-Blatt)
- Batch-Überprüfung der importierten Datensätze über die REST-API
- Export der Prüfungsergebnisse als CSV-Datei
- Dashboard mit Gesamtanzahl, geprüften Einträgen, Erfolgen und Fehlern
- Detailtabelle mit Status für jede importierte Zeile

## Dateiformat

Die importierte Datei sollte mindestens die Spalten enthalten:

- `anfragendeUstid`
- `angefragteUstid`

Optional für qualifizierte Prüfungen:

- `firmenname`
- `ort`
- `strasse`
- `plz`

## Nutzung

1. Öffne `index.html` im Browser.
2. Importiere die Datei mit USt-ID-Daten.
3. Überprüfe die Vorschau und korrigiere ggf. die Quelldatei.
4. Klicke auf "Prüfen", um die Datensätze über die BZSt-API abzurufen.
5. Sieh dir das Dashboard und die Detailergebnisse an.

## Hinweise

- CORS wird unterstützt, ein Backend-Proxy ist für diese Demo nicht nötig.
- Der Dienst verarbeitet Einzelabfragen in Echtzeit; bei Verzögerungen bitte später erneut probieren.
- Die Seite ist als Prototyp gedacht.

## GitHub Pages Deployment

Diese Oberfläche kann als statische Seite über GitHub Pages veröffentlicht werden.

1. Erstelle ein neues GitHub-Repository unter deinem Account.
2. Füge diese Dateien hinzu und pushe sie in den `main`-Branch:
   - `index.html`
   - `README.md`
   - `sample_import.csv`
   - `.gitignore`
3. Aktiviere in den Repository-Einstellungen unter `Pages` die Quelle `main` / `/root`.
4. Warte kurz, dann ist die Seite unter `https://<dein-benutzername>.github.io/<repo-name>/` erreichbar.

Alternativ kannst du das Repo als `username.github.io` benennen, dann ist die Seite unter `https://<dein-benutzername>.github.io/` verfügbar.

> Wenn du möchtest, kann ich dir auch helfen, das Repository für dein GitHub-Konto vorzubereiten und die genauen `git`-Befehle zu liefern.
