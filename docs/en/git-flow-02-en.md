## Create a local Git repository

1. **Create** a folder.
2. **Navigate** to the folder in a terminal (command line).
3. **Initialize** a new Git repository in the folder.

   ``` bash
   git init --initial-branch=main
   ```

   ==> This creates a hidden `.git` folder (don't touch them).

4. **Add** files to the repository.
5. Optional: See the **status** (untracked).

    ``` bash
    git status
    ```

   ==> You should see **untracked files**.

6. **Stage** the files for the step afterwards - commit.

   ``` bash
   git add .
   ```

   ==> The files are staged (prepared to be committed).

7. Optional: See the **status** (staged).

   ``` bash
   git status
   ```

   ==> You should see **changes to be committed**. Git says: `new file: <filename>`.

8.  **Commit** the staged files to the repository.

   ``` bash
   git commit -m "<Commit message>"
   ```

   ==> The commit message is a short description of the changes you made.
