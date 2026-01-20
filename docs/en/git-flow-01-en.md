## Global configuration of Git

1. Check if Git is installed.

   ``` bash
   git --version
   ```

   ==> You should see the installed Git version.

2. Set your name (will be shown in commits).

   ``` bash
   git config --global user.name "First Last"
   git config --global user.email "your.email@example.com"
   git config --global init.defaultbranch main
   ```

   ==> This sets your name, email address, and the default branch name for new repositories.

3. Optional: Check your configuration.

   ``` bash
   git config --global --list
   ```

   ==> You should see the configured values.
