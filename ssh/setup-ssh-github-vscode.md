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

## Step 2: Adding Your SSH Key to ssh-agent and GitHub

- Before you can use your SSH key with GitHub, you need to add it to the **`ssh-agent`** and register it on your GitHub account.

### 🖥️ Start the ssh-agent

Run the following command to start the ssh-agent in the background:

```bash
# Linux / macOS
eval "$(ssh-agent -s)"

# Windows (Git Bash)
eval $(ssh-agent -s)
```

### 🔑 Add Your Private Key to ssh-agent
- Add your private SSH key to the agent:
```bash
ssh-add ~/.ssh/id_ed25519
```
- 🔒 Make sure to use the path where your private key is saved.

### 🔑 Copy Your Public Key
- Display your public key so you can copy it to GitHub:
```bash
cat ~/.ssh/id_ed25519.pub
```

---> Sample output of a public key:
```bash
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIBX8gN0X+X3G5sYhW0u2PzB+4c3zM2yG3zqM1t1a2XyZ your.email@example.com
```
### **⚠️ The above line is your public key. Never share your private key (id_ed25519)!**

#### 🐙 Add the Key to GitHub
1. Log in to your GitHub account.
2. Go to Settings → SSH and GPG keys → New SSH key.
3. Enter a title for the key (e.g., My Laptop) and paste your public key into the Key field.
4. Click Add SSH key.

### Click Add SSH key.
- Run the following command to verify the connection:
```bash
ssh -T git@github.com
```
✅ If successful, you should see a welcome message from GitHub.


 Example output:
```bash
---> Hi **username**! You've successfully authenticated, but GitHub does not provide shell access.
```
- ✅ This message means your SSH key is correctly set up and GitHub recognizes you.
- ⚠️ If you see a "Permission denied" error, check that your key is added to ssh-agent and registered on GitHub.




