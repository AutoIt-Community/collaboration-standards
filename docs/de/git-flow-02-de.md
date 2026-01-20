## Lokales Git-Repository erstellen

1. **Erstelle** einen Ordner.
2. **Wechsle** in diesen Ordner im Terminal (Kommandozeile).
3. **Initialisiere** ein neues Git-Repository in diesem Ordner.

   ``` bash
   git init --initial-branch=main
   ```

   ==> Dadurch wird ein versteckter `.git`-Ordner erstellt (diesen nicht verändern).

4. **Füge** Dateien dem Repository hinzu.
5. Optional: **Status anzeigen** (untracked).

   ``` bash
   git status
   ```

   ==> Du solltest **untracked files** sehen (nicht verfolgte Dateien).

6. **Stage** die Dateien für den Schritt danach - commit.

   ``` bash
   git add .
   ```

   ==> Die Dateien sind jetzt gestaged (zum Commit vorbereitet).

7. Optional: **Status anzeigen** (staged).

   ``` bash
   git status
   ```

   ==> Du solltest **changes to be committed** sehen. Git zeigt: `new file: <Dateiname>`.

8. **Commit** die gestagten Dateien ins Repository.

   ``` bash
   git commit -m "<Commit-Nachricht>"
   ```

   ==> Die Commit-Nachricht ist eine kurze Beschreibung der vorgenommenen Änderungen.
