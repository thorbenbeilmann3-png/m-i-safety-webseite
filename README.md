# Website der M&I Safety - Solution GmbH

Öffentliche Firmenwebsite mit Admin-Bereich und Mitarbeiter-Portal (Demo-Stand). Die Seite ist bewusst schlank gehalten: keine Beispiel-Bewertungen, keine fiktiven Werbepartner oder Zertifikate, keine KI-Hinweise. Mitteilungen und Dienstplan-Daten sind Beispieldaten und werden vor dem Live-Betrieb durch echte Daten ersetzt.

## Struktur

- `index.html` – vollständige, eigenständige Website (HTML, CSS und JavaScript in einer Datei, ohne externe Abhängigkeiten, DSGVO-freundlich: keine externen Schriftarten, keine Tracker)

## Funktionen

### Öffentlicher Bereich
- Leistungen (Objektschutz, Baustellenbewachung, Betriebssanitäter, Reinigungsdienste, Servicedienstleistungen, Brandwache)
- Aktuelles, Branchen, Über uns, Karriere (Bewerbungsformular), Kontaktformular – Formulare öffnen das lokale E-Mail-Programm
- Impressum, Datenschutzerklärung und AGB als gekennzeichnete Beispieltexte

### Admin-Bereich
- Anmeldung mit Benutzername und einmalig gültigem Schlüssel; im Quellcode liegt ausschließlich ein SHA-256-Prüfhash, keine Klartextdaten
- Verwaltung: Banner, öffentliche Meldungen, Portal-Mitteilungen, Dienstplan (Einzel-Einträge und Excel-CSV-Import), Mitarbeiter-Konten, Lohnabrechnungen
- Mitarbeiter-Portal: standardmäßig deaktiviert; Freischaltung und Sperrung ausschließlich durch die Verwaltung (Demo: Status pro Browser-Gerät; Server-Lösung: zentral)

### Mitarbeiter-Portal (Vollbild nach der Anmeldung)
- Menü: Start, Meine Daten, Dienstplan, Lohnabrechnung, Mitteilungen, Wünsche, Beenden
- Konto-Anlage durch die Verwaltung: Name und E-Mail-Adresse erzeugen Personalnummer (1001 aufwärts) und ein einmalig gültiges Passwort (20 Zeichen, SHA-256-gehasht gespeichert); das Passwort wird auf separatem Weg übermittelt
- Erstanmeldung erzwingt ein eigenes Passwort (mindestens acht Zeichen); die Verwaltung kann jederzeit ein neues Einmalpasswort ausstellen
- Dienstplan: Tabelle, Export als Excel-CSV, Druckansicht (PDF), Import einer Excel-CSV-Tabelle
- Lohnabrechnung: Bereitstellung als PDF per Drag-and-Drop, E-Mail-Benachrichtigung, Download ausschließlich mit der persönlichen zehnstelligen Bewachernummer (SHA-256-gehasht); die Bewachernummer wird niemals per E-Mail übermittelt

## Bewusst entfernt (Auftrag vom 15.11.2026)
Die Abschnitte Leistungswelten, Begriffe, Ablauf, Bewertungen sowie Partner und Zertifikate sind auf Wunsch entfernt; damit entfallen auch die zugehörigen Admin-Felder. Bei echten Daten können die Abschnitte wieder ergänzt werden. KI-Hinweise sind vollständig entfernt.

## Demo-Einschränkungen (bewusst)
- Konten, Dienstplan, Mitteilungen, Dokumente und der Portal-Status werden pro Browser (localStorage) gespeichert; ein echter Mehrbenutzer-Betrieb erfordert die geplante Server-Lösung.
- Formulare öffnen das lokale E-Mail-Programm (mailto); ein serverseitiger Versand ist Bestandteil der Server-Lösung.

## Offene Punkte vor dem Live-Betrieb
1. Domain m-safety-solution.de ist noch nicht registriert. Nach dem Kauf (Paket mit E-Mail-Postfach, empfohlen: IONOS oder Strato) DNS auf GitHub Pages umstellen: A-Einträge auf 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153; www-CNAME auf `thorbenbeilmann3-png.github.io` (siehe https://docs.github.com/de/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site). Danach die CNAME-Datei ergänzen und HTTPS erzwingen.
2. Impressum: Handelsregister-Eintrag (Amtsgericht und HRB-Nummer) ergänzen; eine USt-IdNr. ist nicht vorhanden. Rechtstexte vor Veröffentlichung prüfen lassen.
3. Beispieldaten (Mitteilungen, Dienstplan) durch echte Daten ersetzen.
4. Server-Lösung für Admin-Bereich und Mitarbeiter-Portale (Datenbank, echte Authentifizierung, verschlüsselte Dokumentzustellung, serverseitiger Formularversand).
