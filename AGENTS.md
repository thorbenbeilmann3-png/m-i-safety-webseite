# AGENTS.md – Projektanweisung: Firmenwebsite M&I Safety - Solution GmbH

## Projekt
Statische, einseitige Firmenwebsite in `index.html` (HTML, CSS und JavaScript in einer Datei, kein Build-Schritt).
GitHub Pages ist aktiviert; die eigene Domain `m-safety-solution.de` ist als CNAME hinterlegt.

## Abgeschlossene Schritte
1. Repository angelegt, Code übertragen.
2. GitHub Pages aktiviert (Branch `main`, Ordner `/`).
3. CNAME-Datei mit `m-safety-solution.de` hinterlegt; Formular-Empfänger ist `m.eroglu@m-safety-solution.de`.

## Offene Aufgaben
1. DNS beim Domain-Anbieter setzen (sofern noch nicht geschehen):
   - A-Records der Hauptdomain auf: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - CNAME für `www` auf: `thorbenbeilmann3-png.github.io`
   - Danach in den Repository-Einstellungen unter Pages die Domain-Prüfung und HTTPS erzwingen.
2. Impressum ergänzen: USt-IdNr. und Handelsregisterdaten; Rechtstexte (Datenschutz, AGB) sind Beispieltexte und rechtlich prüfen zu lassen.
3. Beispieldaten ersetzen oder entfernen: Bewertungen, Werbepartner, Zertifikate, News, Dienstpläne, Schulungen.
4. Demo-Zugänge entfernen: Admin-Bereich (`demo1234`) und Mitarbeiter-Portal (`1001`/`demo1234`) sind rein clientseitig und dürfen nicht produktiv bleiben.
5. Empfehlung: Formularversand serverseitig lösen (Formspree, Netlify Forms oder PHP beim Hoster); der mailto-Versand verliert auf Geräten ohne E-Mail-Programm Daten.

## Regeln
- Keine Klartext-Passwörter im Quellcode belassen.
- Änderungen nur über Commits mit aussagekräftigen Nachrichten.
- Nach jeder Änderung: Links, Formulare und mobile Ansicht testen.
