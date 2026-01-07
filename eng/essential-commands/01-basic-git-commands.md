# Essential Git Commands

This section presents the most commonly used Git commands, with their equivalents for Windows and Linux operating systems, facilitating transition and use in different environments.

## Navigation and File Manipulation Commands

| Description             | Windows (W)             | Linux (L)                   |
| :-------------------- | :---------------------- | :-------------------------- |
| List directories      | `dir`                   | `ls`                        |
| Change directory      | `cd`                    | `cd`                        |
| Clear screen          | `cls`                   | `clear` or `Ctrl + L`       |
| Create directory      | `mkdir`                 | `mkdir`                     |
| Create file with text | `echo hello > hello.txt`| `echo hello > hello.txt`    |
| Delete files          | `del <file>`            | `rm <file>`                 |
| Remove directory      | `rmdir <directory> /S /Q`| `rm -rf <directory>`        |

## Git Commands

| Git Command                     | Description                                                                 |
| :------------------------------ | :------------------------------------------------------------------------ |
| `git init`                      | Initializes a new Git repository in the current folder. Creates the hidden `.git` folder. |
| `git config --global user.email "your@email.com"` | Configures the author's email for all local repositories.          |
| `git config --global user.name "Your Name"`     | Configures the author's name for all local repositories.            |
| `git add .` or `git add <file>` | Adds files to the *staging area* for the next commit. |
| `git commit -m "Commit message"` | Records changes from the *staging area* to the repository history with a descriptive message. |
| `git status`                    | Shows the repository status: modified, added files, etc.   |
| `git remote add origin <URL>`   | Adds a remote repository (usually on GitHub) to your local repository. |
| `git push origin master`        | Sends commits from your local repository to the `master` branch of the remote repository. |
| `git pull origin master`        | Downloads changes from the `master` branch of the remote repository to your local repository. |
| `git config --list`             | Lists all Git configurations.                                      |
| `git config --global --unset user.email` | Removes the globally configured author's email.                         |

**Note**: For administrative commands on Linux, it may be necessary to use `sudo su` to obtain superuser privileges.
