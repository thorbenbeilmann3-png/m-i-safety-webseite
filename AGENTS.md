# AGENTS.md – Projektanweisung: Firmenwebsite M&I Safety - Solution GmbH

## Projekt
Statische, einseitige Firmenwebsite in `index.html` (HTML, CSS und JavaScript in einer Datei, kein Build-Schritt).
GitHub Pages ist aktiviert; das Repository ist privat, die veröffentlichte Seite bleibt öffentlich erreichbar.
Geplante eigene Domain: `m-safety-solution.de` (DNS noch nicht gesetzt).

## Abgeschlossene Schritte
1. Repository angelegt (privat), Code übertragen; GitHub Pages aktiviert (Branch `main`).
2. Formular-Empfänger: `m.eroglu@m-safety-solution.de`.
3. Admin-Bereich: Anmeldung über 10-stelligen Benutzernamen und einen Einmalschlüssel (mindestens 20 Zeichen). Der Schlüssel ist nach erster Nutzung ungültig; ein neuer Schlüssel wird durch Ändern der Konstanten `ADMIN_KONTO` in `index.html` angelegt. Wichtiger Hinweis: Bei einer statischen Seite erfolgt die Prüfung im Browser; der Verbrauch des Schlüssels wird pro Gerät (localStorage) gespeichert. Ein geräteübergreifender Schutz erfordert einen Server.

## Offene Aufgaben
1. DNS beim Domain-Anbieter setzen (Anbieter noch zu erfragen):
   - A-Records der Hauptdomain auf: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - CNAME für `www` auf: `thorbenbeilmann3-png.github.io`
   - Danach CNAME-Datei mit `m-safety-solution.de` ins Repository übertragen, Domain in den Pages-Einstellungen hinterlegen und HTTPS erzwingen.
2. Impressum ergänzen: USt-IdNr. und Handelsregisterdaten; Rechtstexte (Datenschutz, AGB) sind Beispieltexte und rechtlich prüfen zu lassen.
3. Beispieldaten ersetzen oder entfernen: Bewertungen, Werbepartner, Zertifikate, News, Dienstpläne, Schulungen.
4. Mitarbeiter-Portal: Demo-Zugang (Personalnummer 1001) entfernen oder durch echte Anmeldung ersetzen; keine Klartext-Passwörter im Quellcode belassen.
5. Empfehlung: Formularversand serverseitig lösen (Formspree, Netlify Forms oder PHP beim Hoster); der mailto-Versand verliert auf Geräten ohne E-Mail-Programm Daten.

## Regeln
- Keine Zugangsdaten oder Schlüssel in Dokumentationen oder Berichte übernehmen.
- Änderungen nur über Commits mit aussagekräftigen Nachrichten.
- Nach jeder Änderung: Links, Formulare, Anmeldung und mobile Ansicht testen.
