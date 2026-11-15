# Hinweise für KI-Agenten (Codex und vergleichbare Werkzeuge)

Dieses Repository enthält die statische Website der M&I Safety - Solution GmbH. `index.html` ist die einzige Quelldatei: kein Build-Schritt, keine externen Abhängigkeiten, keine Paketverwaltung.

## Regeln für Änderungen

1. Änderungen nur in kleinen, prüfbaren Schritten. Nach jedem Schritt prüfen: HTML-Tag-Balance (section, div, form, table) und JavaScript-Syntax (zum Beispiel mit `node --check` auf den extrahierten Skript-Block).
2. Keine externen Ressourcen einbinden: keine Google Fonts, keine CDNs, keine Tracker, keine Social-Plugins. Alle Schriftarten bleiben lokale Systemfonts.
3. Keine Klartext-Zugangsdaten, API-Schlüssel oder Tokens in Dateien, Commits oder Ausgaben ablegen. Der Admin-Zugang wird ausschließlich über SHA-256-Prüfhashes (`ADMIN_PRUEFWERT`) abgeglichen; Mitarbeiter-Passwörter und Bewachernummern liegen ausschließlich als SHA-256-Hashes vor (`textZuHash`).
4. Beispieldaten im sichtbaren Text als Beispiel kennzeichnen (Bewertungen, Partner, Zertifikate, Mitteilungen, Dienstplan, Schulungen).
5. Formulare versenden per `mailto` an die in `TEST_EMPFAENGER` hinterlegte Adresse; ein serverseitiger Versand ist der geplanten Server-Lösung vorbehalten.
6. Beim Erweitern des Mitarbeiter-Portals die bestehenden Speicher-Schlüssel beibehalten: `mi_ma_konten`, `mi_dienstplan`, `mi_mitteilungen`, `mi_loehne`.
7. Sicherheit der Lohnabrechnung nicht schwächen: Die Bewachernummer (zehn Ziffern, selbst gewählt) wird niemals per E-Mail übermittelt und nur als Hash gespeichert.
8. Vor jeder Veröffentlichung prüfen: Impressum-Vollständigkeit, Rechtstexte, Ersetzen von Beispieldaten, Funktionsfähigkeit der Anmeldung.
