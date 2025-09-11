# SSH Key Setup for GitHub and VSCode 🖥️

## Step 1: Generating an SSH Key

To securely connect to GitHub, you first need to generate an SSH key.

### Command to Generate SSH Key

Open your terminal (Linux / macOS / Git Bash on Windows) and run:

```bash
ssh-keygen -t ed25519 -C "your.email@example.com"
```

## Steps Explained
### 1. After running the command, you will be asked for a location to save the key.
**Press Enter to accept the default path:**
- Windows (Git Bash): `C:\Users\YourUser\.ssh\id_ed25519`
- Linux/macOS: `/home/username/.ssh/id_ed25519`

### 2. Next, you will be prompted to enter a passphrase.
- It is recommended to use a secure passphrase. You can also leave it empty by pressing `Enter` for testing purposes. 🔒

**Result**
- **Private Key**: The file you saved (e.g., `id_ed25519`) — keep this secret!
- **Public Key**: The same file with .pub extension (e.g., `id_ed25519.pub`) — this will be added to GitHub.

**Notes** 🧐
- Keep your ***private key*** secure — never share it. ⚠️
- You can generate multiple keys if you need separate ones for different accounts or machines.
---

