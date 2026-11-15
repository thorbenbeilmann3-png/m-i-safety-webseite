# Website der M&I Safety - Solution GmbH

Öffentliche Firmenwebsite mit Admin-Bereich und Mitarbeiter-Portal (Demo-Stand). Die Struktur orientiert sich an etablierten Sicherheitsdienstleistern; alle Bewertungen, Partner, Zertifikate, Mitteilungen und Dienstplan-Daten sind Beispieldaten und werden vor dem Live-Betrieb durch echte Daten ersetzt.

## Struktur

- `index.html` – vollständige, eigenständige Website (HTML, CSS und JavaScript in einer Datei, ohne externe Abhängigkeiten, DSGVO-freundlich: keine externen Schriftarten, keine Tracker)

## Funktionen

### Öffentlicher Bereich
- Leistungen (Objektschutz, Baustellenbewachung, Betriebssanitäter, Reinigungsdienste, Servicedienstleistungen, Brandwache) mit leicht verständlichen Erklärungen und Glossar
- Kontaktformular (öffnet das lokale E-Mail-Programm) mit Kopier-Ausweichweg
- Impressum, Datenschutzerklärung und AGB als gekennzeichnete Beispieltexte

### Admin-Bereich
- Anmeldung mit Benutzername und einmalig gültigem Schlüssel; im Quellcode liegt ausschließlich ein SHA-256-Prüfhash, keine Klartextdaten
- Verwaltung: Banner, Werbepartner, Zertifikate, öffentliche Meldungen, Portal-Mitteilungen, Dienstplan (Einzel-Einträge und Excel-CSV-Import), Mitarbeiter-Konten, Lohnabrechnungen
- Mitarbeiter-Portal: standardmäßig deaktiviert; Freischaltung und Sperrung ausschließlich durch die Verwaltung an dieser Stelle (Demo: Status pro Browser-Gerät; Server-Lösung: zentral für alle Mitarbeitenden)

### Mitarbeiter-Portal (Vollbild nach der Anmeldung)
- Menü: Start, Meine Daten, Dienstplan, Lohnabrechnung, Mitteilungen, Wünsche, Beenden
- Konto-Anlage durch die Verwaltung: Name und E-Mail-Adresse erzeugen Personalnummer (1001 aufwärts) und ein einmalig gültiges Passwort (20 Zeichen, SHA-256-gehasht gespeichert); das E-Mail-Programm öffnet sich mit den Zugangsdaten, das Passwort selbst wird auf separatem Weg übermittelt
- Erstanmeldung erzwingt ein eigenes Passwort (mindestens acht Zeichen); die Verwaltung kann jederzeit ein neues Einmalpasswort ausstellen
- Dienstplan: Tabelle, Export als Excel-CSV, Druckansicht (PDF), Import einer Excel-CSV-Tabelle im Admin-Bereich
- Lohnabrechnung: Bereitstellung als PDF per Drag-and-Drop im Admin-Bereich, E-Mail-Benachrichtigung an die hinterlegte Adresse, Download im Portal ausschließlich mit der persönlichen, selbst gewählten zehnstelligen Bewachernummer (SHA-256-gehasht gespeichert); die Bewachernummer wird ausdrücklich niemals per E-Mail übermittelt

## Demo-Einschränkungen (bewusst)
- Konten, Dienstplan, Mitteilungen, Dokumente und der Portal-Status werden pro Browser (localStorage) gespeichert; ein echter Mehrbenutzer-Betrieb erfordert die geplante Server-Lösung.
- Formulare öffnen das lokale E-Mail-Programm (mailto); ein serverseitiger Versand ist Bestandteil der Server-Lösung.
- Im Demo-Betrieb wird die PDF-Datei im Browser gespeichert und über die Bewachernummer freigegeben; die verschlüsselte Zustellung per E-Mail ist Bestandteil der Server-Lösung.

## Offene Punkte vor dem Live-Betrieb
1. Domain m-safety-solution.de ist noch nicht registriert. Nach dem Kauf beim Anbieter (Paket mit E-Mail-Postfach, empfohlen: IONOS oder Strato) DNS wie folgt auf GitHub Pages umstellen: A-Einträge der Hauptdomain auf 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153; www-CNAME auf `thorbenbeilmann3-png.github.io` (siehe https://docs.github.com/de/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site). Danach die CNAME-Datei ergänzen und HTTPS erzwingen.
2. Impressum: Handelsregister-Eintrag (Amtsgericht und HRB-Nummer) ergänzen; eine USt-IdNr. ist nicht vorhanden. Rechtstexte (Impressum, Datenschutz, AGB) vor Veröffentlichung prüfen lassen.
3. Beispieldaten (Bewertungen, Partner, Zertifikate, Mitteilungen, Dienstplan) durch echte Daten ersetzen oder entfernen.
4. Server-Lösung für Admin-Bereich und Mitarbeiter-Portale (Datenbank, echte Authentifizierung, verschlüsselte Dokumentzustellung, serverseitiger Formularversand).

## Hinweis zur Erstellung
Die Website wurde KI-gestützt erstellt und im Seitenfuß sowie im Impressum entsprechend gekennzeichnet.
