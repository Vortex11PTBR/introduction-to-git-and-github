# Git Initialization and Basic Configuration

Before starting to work with a Git repository, it is essential to initialize it and configure your user information.

## Initializing a Repository (`git init`)

To turn a regular directory into a Git repository, use the `git init` command:

```bash
git init
```

This command creates a hidden subdirectory named `.git` inside your working directory. This folder contains all the metadata and history of your repository. To view hidden files and folders, you can use `ls -a` on Linux/macOS or configure your file explorer on Windows.

## Configuring the Author (`git config`)

It is crucial to configure your username and email so that your commits are properly attributed. This information is recorded in every commit you make.

### Global Configuration

To configure your name and email globally (for all your repositories on the system):

```bash
git config --global user.email "your@email.com"
git config --global user.name "Your Name"
```

Replace `"your@email.com"` and `"Your Name"` with your information.

### Verifying Configurations

To list all Git configurations (global and local):

```bash
git config --list
```

### Changing or Removing Configurations

To change an already registered email:

```bash
git config --global user.email "new@email.com"
```

To remove a global configuration (for example, the email):

```bash
git config --global --unset user.email
```

The same principle applies to `user.name` or other configurations. Remember to use the exact configuration name as it appears in `git config --list`.
