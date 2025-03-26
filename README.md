# Pubkeys
This repository contains public keys to be downloaded for lab machines on boot.

## How to Add Your Key
To add your SSH key:
1. **Request to be added as a collaborator** on this repository.
2. **Pull the `master` branch** (i recommended to authenticate via GitHub SSH keys).
3. **Create a new branch** to add your user and ssh key
4. **Edit the `users` file**:
   - Add your username to a new line.
5. **Edit the `authorized_keys` file**:
   - Add your public SSH key to the same line number as your username in the `users` file.
   
   **Important:** Always add your username and SSH key to the nth line of both the `users` and `authorized_keys` files. If the line counts of the files differ, the user creation process will be rejected via CI and locally if it somehow bypasses the CI check.

## Detailed Steps

### 1. Adding SSH Key to Your GitHub Account
Follow this [GitHub guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) to add an SSH key to your GitHub account.

### 2. Clone the Repository
On the GitHub page for this repository:
- Click the **green "Code" button**.
- Choose **SSH** and copy the repository URL:  
  `git@github.com:nicholasentinel/pubkeys.git`

### 3. Locally, on your machine, run:

```bash
git clone git@github.com:nicholasentinel/pubkeys.git
git checkout -b <your-branch-name>

```

Add your username to the users file on a new line
Add your key to the authorized_keys file on a new line

```bash
git add --all          # Add all changes to the commit
git commit -m "some commit message"  # Commit your changes
git push -u origin <your-branch-name>  # Push your commit
```
### 4. Request merge
Ping me once you have pushed your branch and I will merge it to master where it will be pulled to the lab.