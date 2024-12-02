To remove `node_modules` from your GitHub repository, follow these steps:

### 1. Remove `node_modules` Folder from the Repository
- First, delete the `node_modules` folder from your local project directory:
  ```bash
  rm -rf node_modules
  ```

### 2. Add `node_modules` to `.gitignore`
- Open your `.gitignore` file in the root of your project (create one if it doesn't exist) and add `node_modules/` to it. This will ensure that `node_modules` is ignored by Git in the future.
  ```
  node_modules/
  ```

### 3. Remove `node_modules` from Git's Tracking
- Even after deleting the folder locally and adding it to `.gitignore`, Git might still track it. To remove it from Git’s history, run:
  ```bash
  git rm -r --cached node_modules
  ```

### 4. Commit the Changes
- Now, commit the changes to remove `node_modules` from Git:
  ```bash
  git commit -m "Remove node_modules from the repository"
  ```

### 5. Push the Changes to GitHub
- Push the commit to your GitHub repository:
  ```bash
  git push origin main
  ```

### 6. Verify on GitHub
- After pushing the changes, check your GitHub repository to make sure the `node_modules` folder is no longer present.

### Summary of Commands:
```bash
rm -rf node_modules              # Delete the node_modules folder locally
echo "node_modules/" >> .gitignore # Add node_modules to .gitignore
git rm -r --cached node_modules   # Remove node_modules from Git tracking
git commit -m "Remove node_modules from the repository"
git push origin main             # Push changes to GitHub
```

This will clean up your repository and prevent the `node_modules` folder from being included in future commits.
