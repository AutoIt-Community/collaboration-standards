## How do I work on GitHub (Fork + Pull Request)

### Fork

1. **Fork** the repository on GitHub.
   - Go to the target repository on GitHub.
   - Click the **Fork** button (top right).
   - This creates a copy of the repository under your own GitHub account.

2. **Clone** your fork to your local machine.
   - On your forked repository, click **Code** and copy the URL (HTTPS or SSH).
   - Recommended: Use HTTPS for simplicity.
   - In your terminal, run:

   ```bash
   git clone <your-fork-url>
   ```

   - Change into the cloned directory:

   ```bash
   cd <repository-name>
   ```

3. Add the original repository as an **upstream remote** (optional but recommended).
   - This allows you to keep your fork up to date.

   ```bash
   git remote add upstream <original-repo-url>
   ```

4. Create a **new branch** for your changes.
   - Never work directly on the `main` branch.

   ```bash
   git checkout -b <feature-branch-name>
   ```

5. **Make your changes** in this branch.
   - Edit, add, or delete files as needed.

6. **Stage and commit** your changes.

   ```bash
   git add .
   git commit -m "<Short description of your changes>"
   ```

7. **Push** your branch to your fork on GitHub.

   ```bash
   git push origin <feature-branch-name>
   ```

### Pull Request

8. Create a **Pull Request (PR)** on GitHub.
   - Go to your fork on GitHub.
   - Click **Compare & pull request** or **New pull request**.
   - Select your branch and the target branch (usually `main` of the original repository).
   - Add a clear title and description, then click **Create pull request**.

9. Wait for **review and approval.**
   - Respond to feedback and make changes if requested (commit and push again to update the PR).

10. **Merge** the Pull Request (if you have permission) or wait for a maintainer to merge it.
   - Click **Merge pull request** and then **Confirm merge**.

11. **Clean up** your local repository.
   - Switch back to your local `main` branch:

   ```bash
   git checkout main
   ```

   - Update your local `main` branch with the latest changes from the original repository:

   ```bash
   git fetch upstream
   git pull upstream main
   ```

   - (Optional) Delete your feature branch locally and remotely:

   ```bash
   git branch -d <feature-branch-name>
   git push origin --delete <feature-branch-name>
   ```

   ==> Done, now you are ready for your next PR.<br>
   ==> Create a new branch and repeat the relevant steps.
