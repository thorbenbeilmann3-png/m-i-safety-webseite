# Hinweise für KI-Agenten (Codex und vergleichbare Werkzeuge)

Dieses Repository enthält die statische Website der M&I Safety - Solution GmbH. `index.html` ist die einzige Quelldatei: kein Build-Schritt, keine externen Abhängigkeiten, keine Paketverwaltung.

## Regeln für Änderungen

1. Änderungen nur in kleinen, prüfbaren Schritten. Nach jedem Schritt prüfen: HTML-Tag-Balance (section, div, form, table) und JavaScript-Syntax (zum Beispiel mit `node --check` auf den extrahierten Skript-Block).
2. Keine externen Ressourcen einbinden: keine Google Fonts, keine CDNs, keine Tracker, keine Social-Plugins. Alle Schriftarten bleiben lokale Systemfonts.
3. Keine Klartext-Zugangsdaten, API-Schlüssel oder Tokens in Dateien, Commits oder Ausgaben ablegen. Der Admin-Zugang wird ausschließlich über SHA-256-Prüfhashes (`ADMIN_PRUEFWERT`) abgeglichen; Mitarbeiter-Passwörter und Bewachernummern liegen ausschließlich als SHA-256-Hashes vor (`textZuHash`).
4. Das Mitarbeiter-Portal ist standardmäßig deaktiviert und wird ausschließlich über den Admin-Bereich freigeschaltet (localStorage-Schlüssel `mi_portal_status`; Standardwert `aus` darf nicht geändert werden).
5. Die Seite ist bewusst schlank gehalten: Die Abschnitte Leistungswelten, Begriffe, Ablauf, Bewertungen sowie Partner und Zertifikate sind auf Auftrag entfernt und dürfen nur auf ausdrücklichen Auftrag wieder eingebaut werden. Keine erfundenen Bewertungen, Partner oder Zertifikate ergänzen.
6. Keine KI-Hinweise einbauen: Weder im Seitenfuß noch im Impressum oder an anderer Stelle wird auf die Erstellung mit Künstlicher Intelligenz hingewiesen.
7. Formulare versenden per `mailto` an die in `TEST_EMPFAENGER` hinterlegte Adresse; ein serverseitiger Versand ist der geplanten Server-Lösung vorbehalten.
8. Beim Erweitern des Mitarbeiter-Portals die bestehenden Speicher-Schlüssel beibehalten: `mi_ma_konten`, `mi_dienstplan`, `mi_mitteilungen`, `mi_loehne`, `mi_portal_status`.
9. Sicherheit der Lohnabrechnung nicht schwächen: Die Bewachernummer (zehn Ziffern, selbst gewählt) wird niemals per E-Mail übermittelt und nur als Hash gespeichert.
10. Vor jeder Veröffentlichung prüfen: Alle Anker-Links zeigen auf existierende Ziele, alle Schaltflächen sind verdrahtet, Impressum-Vollständigkeit, Rechtstexte, Ersetzen von Beispieldaten.
