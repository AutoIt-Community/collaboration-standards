## Globale Konfiguration von Git

1. Prüfe ob Git installiert ist.

   ``` bash
   git --version
   ```

   ==> Du solltest die installierte Git-Version sehen.

2. Setze deinen Namen (wird bei Commits angezeigt).

   ``` bash
   git config --global user.name "Vorname Nachname"
   git config --global user.email "deine.email@example.de"
   git config --global init.defaultbranch main
   ```

   ==> Dies setzt deinen Namen, deine E-Mail-Adresse und den Standard-Branch-Namen für neue Repositories.

3. Optional: Überprüfe die Konfiguration.

   ``` bash
   git config --global --list
   ```

   ==> Du solltest die gesetzten Konfigurationswerte sehen.
