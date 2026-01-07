# Adding and Committing Changes in Git

After making modifications to your files, Git offers a two-step process to record these changes in the repository's history: **adding** (staging) and **committing**.

## `git add` (Adding to the Staging Area)

The `git add` command is used to add modified or new files to the *staging area* (also known as the index). The *staging area* is an intermediate area where you prepare the changes you want to include in the next commit.

- **Add all modified and new files in the current directory:**
  ```bash
  git add .
  ```
  or
  ```bash
  git add *
  ```

- **Add a specific file:**
  ```bash
  git add <file_name>
  ```

## `git commit` (Recording Changes)

Once files are added to the *staging area*, the `git commit` command is used to permanently record these changes in the repository's history. Each commit represents a "snapshot" of your project at a given moment and should be accompanied by a descriptive message.

- **Perform a commit with a message:**
  ```bash
  git commit -m "Descriptive commit message"
  ```
  The commit message should be clear and concise, explaining what was changed and why.

## `git status` (Checking Repository Status)

The `git status` command is essential for tracking the state of your repository. It shows which files have been modified, which are in the *staging area*, and which have not yet been tracked by Git.

```bash
git status
```

This command is very useful for checking your changes before committing and to ensure you are adding the correct files.
