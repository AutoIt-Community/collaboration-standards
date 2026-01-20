## Wie arbeite ich auf GitHub (Fork + Pull Request)

### Fork

1. **Fork** das Repository auf GitHub.
   - Gehe auf die Ziel-Repository-Seite auf GitHub.
   - Klicke auf den **Fork**-Button (oben rechts).
   - Dadurch wird eine Kopie des Repositories in deinem eigenen GitHub-Account erstellt.

2. **Clone** deines Forks auf deinen lokalen Rechner.
   - Gehe in deinem geforkten Repository auf **Code** und kopiere die URL (HTTPS oder SSH).
   - Empfehlung: Nutze HTTPS der Einfachheit.
   - Im Terminal ausführen:

   ```bash
   git clone <dein-fork-url>
   ```

   - Wechsle in das geklonte Verzeichnis:

   ```bash
   cd <repository-name>
   ```

3. Füge das Original-Repository als **upstream remote** hinzu (optional, aber empfohlen).
   - So kannst du deinen Fork aktuell halten.

   ```bash
   git remote add upstream <original-repo-url>
   ```

4. Erstelle einen **neuen Branch** für deine Änderungen.
   - Arbeite niemals direkt auf dem `main`-Branch.

   ```bash
   git checkout -b <feature-branch-name>
   ```

5. **Nimm deine Änderungen** in diesem Branch vor.
   - Bearbeite, füge hinzu oder lösche Dateien nach Bedarf.

6. **Stagen und committen** deiner Änderungen.

   ```bash
   git add .
   git commit -m "<Kurze Beschreibung deiner Änderungen>"
   ```

7. **Push** deinen Branch zu deinem Fork auf GitHub.

   ```bash
   git push origin <feature-branch-name>
   ```

### Pull Request

8. Erstelle einen **Pull Request (PR)** auf GitHub.
   - Gehe zu deinem Fork auf GitHub.
   - Klicke auf **Compare & pull request** oder **New pull request**.
   - Wähle deinen Branch und den Ziel-Branch (meistens `main` des Original-Repos).
   - Gib einen klaren Titel und eine Beschreibung an und klicke auf **Create pull request**.

9. Warte auf **Review und Freigabe.**
   - Reagiere auf Feedback und nimm ggf. Änderungen vor (erneut committen und pushen, um den PR zu aktualisieren).

10. **Merge** den Pull Request (wenn du Berechtigung hast) oder warte, bis ein Maintainer merged.
   - Klicke auf **Merge pull request** und dann auf **Confirm merge**.

11. **Clean up** dein lokales Repository.
   - Wechsle zurück auf deinen lokalen `main`-Branch:

   ```bash
   git checkout main
   ```

   - Aktualisiere deinen lokalen `main`-Branch mit den neuesten Änderungen aus dem Original-Repository:

   ```bash
   git fetch upstream
   git pull upstream main
   ```

   - (Optional) Lösche deinen Feature-Branch lokal und remote:

   ```bash
   git branch -d <feature-branch-name>
   git push origin --delete <feature-branch-name>
   ```

   ==> Du bist jetzt bereit für deinen nächsten Beitrag!
