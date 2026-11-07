# Nachtlichtland Homepage

7. November 2026. Niki hat Upload und Veröffentlichung im Chat ausdrücklich freigegeben.

Repository: https://github.com/nikolalammer/nachtlichtland

Homepage: https://nikolalammer.github.io/nachtlichtland/

Die eigene Domain `nachtlichtland.at` ist registriert, öffentlich sind aber noch keine passenden DNS-Einträge erreichbar. Bis die Domain verbunden wird, dient die GitHub-Adresse als öffentliche Adresse.

## Was veröffentlicht wird

Reines HTML und CSS. Startseite mit fünf Geschichtenwelten, CSS-Nachtlicht als Platzhalter, Link zum bestätigten YouTube-Kanal, Platzhalter für die neueste Geschichte. Impressum und Datenschutz enthalten Nikis mitgeteilte Anschrift und Kontakt-E-Mail. Keine Werbung, Cookies, Analysewerkzeuge, externen Schriften oder eingebetteten Videos.

GitHub Pages ist mit **GitHub Actions** als Quelle aktiviert. Der Workflow `.github/workflows/pages.yml` veröffentlicht bei jedem Push auf `main` ausschließlich `index.html`, `impressum.html`, `datenschutz.html`, `stil.css`, `CNAME` und `.nojekyll`. Kein Framework und kein Build-System nötig.

Nur der Homepage-Code gehört ins öffentliche Repository. Die übrigen Nebeneinkommen-Dateien und die Archive werden nicht hochgeladen. Die älteren lokalen Dateien `README.md` und `PRUEFUNG.md` beschreiben den Stand vor Nikis Veröffentlichungserlaubnis und werden nicht hochgeladen. Diese neue Anleitung gilt für die Live-Fassung.

## Lokal ansehen

`index.html` doppelklicken. Alternativ aus diesem Ordner:

```powershell
python -B -m http.server 8765 --bind 127.0.0.1
```

Danach http://127.0.0.1:8765/ öffnen. Mit Strg+C beenden.

## Die Domain verbinden

1. GitHub-Konto **Settings → Pages → Add a domain**: `nachtlichtland.at` verifizieren. Den von GitHub angezeigten individuellen TXT-Eintrag bei INWX ergänzen.
2. Repository **Settings → Pages**: Quelle bleibt **GitHub Actions**. Unter **Custom domain** `nachtlichtland.at` speichern. Direkt danach die DNS-Einträge bei INWX einrichten, damit die Weiterleitung bald funktioniert.
3. INWX-DNS:

| Typ | Name | Ziel |
| --- | --- | --- |
| A | Hauptdomain, je nach Ansicht leer oder `@` | `185.199.108.153` |
| A | Hauptdomain | `185.199.109.153` |
| A | Hauptdomain | `185.199.110.153` |
| A | Hauptdomain | `185.199.111.153` |
| CNAME | `www` | `nikolalammer.github.io` |

Kein `https://` und kein Repository-Pfad im CNAME-Ziel. Falls INWX einen abschließenden Punkt verlangt: `nikolalammer.github.io.`. Widersprechende Parking-Einträge prüfen, Mail-Einträge erhalten.

4. DNS und Zertifikat können bis zu 24 Stunden brauchen. Sobald verfügbar, **Enforce HTTPS** aktivieren. https://nachtlichtland.at und https://www.nachtlichtland.at testen.

Die Datei `CNAME` enthält die gewünschte Domain. Bei Workflow-Deployments schaltet die Datei allein keine Weiterleitung ein, dafür ist die Custom-domain-Einstellung nötig. So bleibt bis zur DNS-Verbindung die GitHub-Adresse erreichbar.

## Spätere Änderungen

* Das bestätigte Nachtlicht-Referenzbild als lokale Datei ergänzen, sobald es fertig ist.
* Beim ersten Video den Abschnitt `VIDEO-PLATZHALTER` in `index.html` aktualisieren. Ein normaler YouTube-Link genügt. Keine externen Vorschaubilder laden.
* Jeder Push auf `main` veröffentlicht automatisch. Weitere Pushes nur nach Nikis Freigabe.
* Git-Commits verwenden die GitHub-noreply-Adresse.

Zeit für Niki: Seite ansehen, etwa 5 Minuten. INWX-DNS und Domain verbinden, etwa 10 Minuten plus Wartezeit.

Quellen, geprüft am 7.11.2026:

* [GitHub: eigene Domain und DNS](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)
* [GitHub: Pages-Workflows](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)
* [GitHub: Datenschutz](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)
