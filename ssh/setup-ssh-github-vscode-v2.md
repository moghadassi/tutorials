<img src="https://code.visualstudio.com/assets/images/code-stable.png" alt="VS Code Logo" width="100"/>  
<img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub Logo" width="50"/>


# SSH Key Setup for GitHub and VSCode 🖥️

This guide will help you securely connect **GitHub** with **SSH keys** and configure **VSCode** for development.

---

## 🚀 Step 1: Generating an SSH Key

To connect GitHub securely, generate an SSH key:

```bash
ssh-keygen -t ed25519 -C "your.email@example.com"
```

### 📌 Key Details
- Default save path:
  - **Windows (Git Bash):** `C:\Users\YourUser\.ssh\id_ed25519`
  - **Linux/macOS:** `/home/username/.ssh/id_ed25519`
- You’ll be asked for a passphrase (recommended for security).
- Generated files:
  - **Private Key** → `id_ed25519` (keep secret!)
  - **Public Key** → `id_ed25519.pub` (add to GitHub)

⚠️ Never share your **private key**.

---

## 🔑 Step 2: Adding SSH Key to `ssh-agent` and GitHub

### Start ssh-agent
```bash
# Linux / macOS
eval "$(ssh-agent -s)"

# Windows (Git Bash)
eval $(ssh-agent -s)
```

### Add Private Key
```bash
ssh-add ~/.ssh/id_ed25519
```

### Copy Public Key
```bash
cat ~/.ssh/id_ed25519.pub
```

Example:
```bash
ssh-ed25519 AAAAC3... your.email@example.com
```

### Add Key to GitHub
1. Open **GitHub → Settings → SSH and GPG keys → New SSH key**  
2. Enter a title (e.g., *My Laptop*)  
3. Paste your public key → Save ✅  

### Verify Connection
```bash
ssh -T git@github.com
```
Expected output:
```
Hi username! You've successfully authenticated, but GitHub does not provide shell access.
```

---

## ⚙️ Step 3: Configure Git and Connect VSCode

### Set Git Identity
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Clone or Init Repo
```bash
# Clone
git clone git@github.com:username/repo.git

# Or init new repo
git init
```

Open repository in **VSCode** → it will detect Git automatically.  

To push changes:
```bash
git push origin main
```

---

## 📝 Step 4: Workflow — Files, Commit, Push

1. **Create/Edit Files**
   ```markdown
   # My Project
   This is my first file in the repository.
   ```

2. **Stage Changes**
   ```bash
   git add .
   ```

3. **Commit**
   ```bash
   git commit -m "Add README file"
   ```

4. **Push**
   ```bash
   git push origin main
   ```

---

## 🔐 Step 5: Managing SSH Keys

### List Keys
```bash
ssh-add -l
```

### Remove Key
```bash
ssh-add -d ~/.ssh/id_ed25519
```

### Add Multiple Keys
```bash
ssh-add ~/.ssh/another_key
```

Optional `~/.ssh/config`:
```text
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519
```

---

## 🛠️ Step 6: Troubleshooting

### Common Errors

**Permission denied (publickey)**  
- Ensure private key is added:
  ```bash
  ssh-add ~/.ssh/id_ed25519
  ```
- Verify public key is registered on GitHub.

**Host key verification failed**
```bash
ssh-keyscan github.com >> ~/.ssh/known_hosts
```

**Multiple keys conflict** → Use `~/.ssh/config`.

---

## 👥 Step 7: Managing Multiple GitHub Accounts

### Personal Account
```bash
ssh-keygen -t ed25519 -C "personal.email@example.com"
ssh-add ~/.ssh/id_ed25519
```

`~/.ssh/config`:
```text
Host github-personal
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519
```

Clone:
```bash
git clone git@github-personal:username/personal-repo.git
```

### Work Account
Repeat with `id_ed25519_work` and configure:
```text
Host github-work
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_work
```

---

## ✅ Best Practices

- Use SSH instead of HTTPS for GitHub.  
- Protect your **private keys**.  
- Use **descriptive commit messages**.  
- Regularly review SSH keys in GitHub settings.  
- Backup your keys securely.  

---
