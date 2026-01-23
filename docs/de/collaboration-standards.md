## Beitragsrichtlinie

### Zweck

Für Projekte/Repositories gibt es mehrere allgemeine und empfohlene Richtlinien, die zu einer stabilen und verständlichen Art der Arbeit mit Code im Team führen.

Einer der Hauptgründe für die Existenz dieser Leitlinien und Standards ist die Einheitlichkeit beim Schreiben von Code, auch beim Review des Codes. Ansonsten könnte es zu allerlei verschiedenen Stilen kommen, die Neueinsteigern verwirren könnten und den Einstieg in das Projekt erschweren würden.

<br>

### 1. Sprache

- verwende Englisch für Code, Kommentare, Branches, Tags, Commit-Nachrichten usw.
- versuche so gut es geht Deutsch und Englisch nicht zu vermischen
- allerdings übersetze auch keine deutschen Eigennamen (behalte sie wie sie sind)

<br>

### 2. Branch Benennung

**Verwendung**

- verwende [kebab-style](/docs/en/case-styles.md) für die Branch Benennung
  - alles klein geschrieben
  - alle Wörter separiert durch einen Bindestrich (Minus)

**Beispiele**

- add-database-connection
- add-login-feature
- apply-common-standards
- fix-prototype-code
- project-restructuring
- remove-obsolete-feature
- update-to-specific-version

**Warum**

- Einheitlichkeit
- verbreitete Art und Weise, dies zu tun

<br>

### 3. Konventionen für Commit-Nachrichten

**Verwendung**

- nutze den "[Keep a Changelog](https://keepachangelog.com/de/1.1.0/)" Stil
  - \<Schlagwort\>\<Doppelpunkt\>\<Leerzeichen\>\<Commit Nachricht als Satz mit schließenden Punkt.\>
- Schlagwörter und deren Zweck
  - **Added** für neue Features.
  - **Changed** für Änderungen in existierender Funktionalität.
  - **Deprecated** für Features die bald entfernt werden sollen.
  - **Documented** für Änderungen die ausschließlich mit Dokumentation zu tun haben.
  - **Fixed** für etwaige Fehlerbehebungen.
  - **Refactored** für Änderungen die weder einen Fehler beheben noch ein Feature hinzufügen.
  - **Removed** für entfernte Features.
  - **Security** im Falle von Schwachstellen.
  - **Styled** für Änderungen wie Leerzeichen, Formatierung, fehlende Semikolons usw.

**Beispiele**

``` bash
git commit -m "Added: Three-part statusbar to the main GUI."
git commit -m "Changed: Sort logic to DESC order instead of ASC."
git commit -m "Fixed: Broken label by set correct attribute."
git commit -m "Refactored: Usage of map data type instead of array."
```

**Warum**

- Einheitlichkeit
- neben "[conventional commits](https://www.conventionalcommits.org/de/v1.0.0/)" (cc) ist der "Keep a Changelog" Stil ein verbreiteter Weg (jedoch einfacher und besser lesbar als cc) damit umzugehen
- die CHANGELOG.md Datei kann beim Erstellen einer neuen Version (Release) automatisch generiert werden

<br>

### 4. Pull requests (merge requests)

- pushe nicht direkt in den main (default) branch (kein force push)
- erstellen den pull request aus deinem Feature Branch heraus in den main
- warte auf die Genehmigung der Codeüberprüfung (code review approval) und dann<br>führe deinen Code mit dem main  zusammen [^1]

<br>

### 5. Code review

Wird noch definiert.

<br>

### 6. Version hochzählen (SemVer)

Wird noch definiert.

<br>

### 7. Changelog (Änderungshistorie)

Wird noch definiert.

<br>

### 8. Releases und Tags

**Verwendung**

- benutze Git Tags für die jeweilige Release Version
- benutze einfache [SemVer](https://semver.org/lang/de/) Tag Namen wie `v0.13.2` oder `v4.1.0`
- benutze keine Prefixes oder Suffixe für die Release Tags
  - Prefixe können für alle anderen Tags genutzt werden, wie bspw. für "hotfixes" oder "MVPs"
  - wenn Prefixe oder Suffixe eingesetzt werden, dann in Kleinschreibweise und in [kebab-style](/docs/en/case-styles.md)

**Erstellungsbeispiel**

Siehe [diese](https://github.com/Sven-Seyfert/au3webdriver-boilerplate/releases) Release-Struktur als Beispiel.

| Choose a tag | Release title        | Release description |
| ---          | ---                  | ---                 |
| v0.13.2      | v0.13.2 - 2024-02-20 | Kopiere entweder den Text aus der Änderungshistorie (CHANGELOG) der neuen Version in den Abschnitt "Release description". Oder verweise auf die Datei CHANGELOG.md mit bspw. "see CHANGELOG.md file" oder ähnlichem. |

**Warum**

- Einheitlichkeit
- jedes Release stellt eine stabile Version dar

<br>

---

## 🔗 weitere Themen

### [Arbeitsabläufe und Anleitungen](/docs/de/workflows-how-tos.md)

<br>

---

Fußnoten
[^1]: Der Genehmigungsprozess muss für jedes GitHub-Repository konfiguriert werden.
