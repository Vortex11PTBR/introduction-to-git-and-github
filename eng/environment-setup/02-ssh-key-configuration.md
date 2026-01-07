# SSH Key Configuration for GitHub/GitLab

SSH authentication offers a secure and convenient way to interact with remote Git repositories, eliminating the need to repeatedly type your password.

## What is an SSH Key?

An **SSH Key** is a pair of cryptographic keys (public and private) used for secure authentication. The public key is added to your GitHub/GitLab profile, while the private key remains on your computer, protected by a passphrase.

## Steps to Configure an SSH Key

1.  **Generate the SSH Key**:
    Open your terminal (Git Bash on Windows, terminal on Linux/macOS) and execute the command:
    ```bash
    ssh-keygen -t ed25519 -C "your@email.com"
    ```
    Replace `your@email.com` with your email address. Follow the prompts, pressing Enter to use the default location and, optionally, set a passphrase for your private key.

2.  **Copy the Public Key**:
    After generation, your public key will be in the `~/.ssh/id_ed25519.pub` file. Copy its content to your clipboard:
    ```bash
    cat ~/.ssh/id_ed25519.pub
    ```

3.  **Add the Public Key to GitHub/GitLab**:
    - Go to your account settings on GitHub or GitLab.
    - Navigate to the "SSH and GPG keys" (GitHub) or "SSH Keys" (GitLab) section.
    - Click on "New SSH Key" or "Add SSH Key".
    - Paste the content of your public key into the provided field and give the key a descriptive title.

4.  **Test the SSH Connection**:
    To verify that the SSH connection is working correctly, execute:
    ```bash
    ssh -T git@github.com
    ```
    You should see a success message, indicating that authentication was successful.

## SSH Agent

To avoid typing your private key passphrase every time you use it, you can start the SSH agent and add your key to it:

```bash
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_ed25519
```

This will keep your private key loaded in memory during the session, allowing for automatic authentication.

## Using SSH with Git

With the SSH key configured, you can clone repositories using the SSH protocol:

```bash
git clone git@github.com:user/repository.git
```

**Reference**: For more details, consult the official GitHub documentation: [Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
