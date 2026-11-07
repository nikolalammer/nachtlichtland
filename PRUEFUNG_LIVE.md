# Prüfung der Live-Fassung

7. November 2026, Codex. Deployment und öffentlich erreichbare Adresse werden nach Abschluss im Projektstatus festgehalten.

## Tatsächlich geprüft

* Vor der Kontakt-Ergänzung: alle drei Seiten im Browser geladen. Startseite am Desktop mit 1280 Pixeln und im Handyformat mit 390 Pixeln angesehen. Bis 320 Pixeln kein seitlicher Überlauf, auch auf Impressum und Datenschutz.
* Anschließend: Nikis mitgeteilte Anschrift und E-Mail in beiden Rechtsseiten eingesetzt. Bestätigten Kanal-Link eingefügt. Keine Kontakt-Platzhalter oder internen Entwurfshinweise in den HTML-Dateien.
* Lokale Links und Seitendateien geprüft. Keine Frameworks, Scripts, Frames oder extern geladenen Ressourcen. CNAME enthält `nachtlichtland.at`.
* Der Deployment-Workflow überträgt nur die sechs ausdrücklich ausgewählten Seitendateien. Keine übrigen Projektdateien oder Archive.
* GitHub Pages wurde mit GitHub Actions und HTTPS aktiviert. DNS-Abfragen nach A für die Hauptdomain und CNAME für www lieferten noch keine Einträge.

## Offen

* Eigene Domain: INWX-DNS und Pages-Domaineinstellung noch verbinden, danach HTTPS-Zertifikat und beide Domainvarianten prüfen.
* Die endgültige Nachtlicht-Illustration und das erste Video fehlen noch. Die Website zeigt dafür Platzhalter.
* Nikis finale Sichtprüfung. Keine abschließende rechtliche Begutachtung von Impressum und Datenschutz.
* Keine Audio- oder Videoprüfung Bestandteil dieser Arbeit.
