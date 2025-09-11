<img src="https://code.visualstudio.com/assets/images/code-stable.png" alt="VS Code Logo" width="100"/>  
<img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub Logo" width="50"/>

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
- **Press Enter to accept the default path:**
  - Windows (Git Bash): `C:\Users\YourUser\.ssh\id_ed25519`
  - Linux/macOS: `/home/username/.ssh/id_ed25519`

### 2. Next, you will be prompted to enter a passphrase.
It is recommended to use a secure passphrase. You can also leave it empty by pressing `Enter` for testing purposes. 🔒

- **Result**
  - **Private Key**: The file you saved (e.g., `id_ed25519`) — keep this secret!
  - **Public Key**: The same file with .pub extension (e.g., `id_ed25519.pub`) — this will be added to GitHub.

- **Notes** 📝
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
```

```bash
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

- ### ✅ Verifying the SSH Key (Green Check)
  After adding your public key to GitHub, you can verify that the key is working correctly.

  - Run the following command to verify the connection:
  ```bash
  ssh -T git@github.com
  ```
- ✅ If successful, you should see a welcome message from GitHub.


  ---> Example output:
  ```bash
  Hi **username**! You've successfully authenticated, but GitHub does not provide shell access.
  ```
  - ✅ This message means your SSH key is correctly set up and GitHub recognizes you.
  - In GitHub, under Settings → SSH and GPG keys, a green check (✅) appears next to the key, indicating it is valid and ready to use.
  - ⚠️ If you see a "Permission denied" error, check that your key is added to `ssh-agent` and registered on GitHub.

---

## Step 3: Configuring Git and Connecting VSCode
After setting up your SSH key, the next step is to configure Git and connect VSCode to your GitHub repository.

### 🖥️ Set Git Username and Email
- To properly record your commits, configure your Git username and email:
  ```bash
  git config --global user.name "Your Name"
  ```

  ```bsah
  git config --global user.email "your.email@example.com"
  ```

  - ⚠️ This sets your information globally for all repositories on your computer.
  - ✅ You can also set repository-specific information later if needed.

- ### 🔗 Connect VSCode to GitHub via SSH
  1. Open VSCode.
  2. Go to Source Control (or press `Ctrl + Shift + G`.
  3. Clone an existing repository or initialize a new one:

  ```bash
  # Clone an existing repository
  git clone git@github.com:username/repo.git
  ```
  
  ```bash
  # Or initialize a new repository
  git init
  ```

    - 🐙 If you cloned the repository, VSCode will automatically recognize it.
    - 🔑 Make sure your SSH key is active and the connection to GitHub is working.

- #### 📝 Important Notes
  - After cloning or initializing a repository, you can edit files and use VSCode to stage and commit changes.
  - To push changes to GitHub, use SSH:
  ```bash
  git push origin main
  ```

  **⚠️ Make sure the branch name matches your repository’s main branch (often main or master).**

---

## Step 4: Creating Files, Committing, and Pushing to GitHub

Once your repository is set up and VSCode is connected, you can start adding files, making commits, and pushing them to GitHub.

1. 📝 **Create or Edit Files**  
   - Open your project in **VSCode**.  
   - Create a new file or edit existing files.  
   - Example: create a `README.md` file with some content:  
     ```markdown
     # My Project
     This is my first file in the repository.
     ```

2. ➕ **Stage Your Changes**  
   Add the modified or new files to the staging area:  
   ```bash
   git add .
   ```  
   - 🔑 `git add .` stages all changes.  
   - You can also stage individual files:  
     ```bash
     git add filename
     ```

3. 💾 **Commit Your Changes**  
   Create a commit with a descriptive message:  
   ```bash
   git commit -m "Add README file"
   ```  
   - 🐙 This records your changes locally in the Git repository.

4. 🚀 **Push Changes to GitHub**  
   Send your commits to the remote repository on GitHub:  
   ```bash
   git push origin main
   ```  
   - ✅ Make sure the branch name matches your repository’s main branch (`main` or `master`).  
   - 🔒 Since you set up SSH, you won’t need to enter your GitHub password.



### 🧐 Notes
- You can repeat these steps anytime you make changes.  
- Always **stage (`git add`) before committing**.  
- Use **descriptive commit messages** for better project history.

---

## Step 5: Managing SSH Keys and Additional Tips

Once your SSH key is working and you are pushing/pulling from GitHub, it’s useful to know how to manage keys and handle common issues.

### 🔑 List All SSH Keys Added to ssh-agent
Check which keys are currently added:
```bash
ssh-add -l
```
✅ You will see the fingerprint and file path of all active SSH keys.

### ❌ Remove a Key from ssh-agent
If you need to remove a key:
```bash
ssh-add -d ~/.ssh/id_ed25519
```
- 🔒 Use this when switching keys or retiring old ones.

### 🐙 Adding Multiple Keys
If you have multiple GitHub accounts or multiple keys, you can add more keys to the agent:
```bash
ssh-add ~/.ssh/another_key
```
- Use `ssh -T git@github.com` to test each key.



### 📝 Additional Tips
- Keep your private key secure — never share it. ⚠️  
- Use descriptive titles for keys on GitHub (e.g., `Work Laptop`, `Home PC`).  
- If you encounter errors like `Permission denied`, check:  
  1. The correct key is added to ssh-agent.  
  2. The public key is registered in GitHub.  
  3. You are connecting to the correct account/username.  

Optional: For advanced users, create a `~/.ssh/config` file to manage multiple keys and hosts:

```text
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519
```

⚠️ This simplifies using multiple SSH keys with different accounts or repositories.
---

## Step 6: Troubleshooting and Additional Tips

Even after setting up everything, you might encounter some issues. Here are tips and common solutions.

---

### ⚠️ Common SSH Errors

1. **Permission denied (publickey)**  
   - Make sure your private key is added to `ssh-agent`:  
     ```bash
     ssh-add ~/.ssh/id_ed25519
     ```
   - Verify the public key is registered on GitHub.
   - Ensure you are using the correct username and repository URL.

2. **Host key verification failed**  
   - This happens if GitHub’s host key changed or was never accepted.  
     Run:
     ```bash
     ssh-keyscan github.com >> ~/.ssh/known_hosts
     ```

3. **Multiple keys conflict**  
   - If you have multiple SSH keys, configure a `~/.ssh/config` file:  
     ```text
     Host github.com
       HostName github.com
       User git
       IdentityFile ~/.ssh/id_ed25519
     ```

---

###  Useful Git Tips

**Check current configuration**:
  ```bash
  git config --list
  ```

**Check SSH connection:**
  ```bash
  ssh -T git@github.com
  ```
**Switch branches safely:**
  ```bash
  git checkout branch_name
  ```
**Undo last commit (without losing changes):**
  ```bash
  git reset --soft HEAD~1
  ```
  

- ### 📝 Additional Recommendations
  - Keep your keys safe and backed up.
  - Use descriptive commit messages for clarity.
  - Regularly pull (`git pull`) to stay up-to-date with remote changes.
  - Use SSH over HTTPS for secure and password-less operations.



- ### 🔒 Security Recommendations
  - Keep your **private SSH key** safe and never share it with anyone.  
  - Use **strong and unique passphrases** for your SSH keys.  
  - Regularly **review and remove old or unused SSH keys** from GitHub.  
  - Use descriptive titles for your keys on GitHub (e.g., `Work Laptop`, `Home PC`) to easily manage them.  
  - Avoid storing private keys in public or shared folders.  
  - Always verify the SSH connection before pushing sensitive code:

```bash
ssh -T git@github.com
```

---

## Step 7: Managing Multiple GitHub Accounts with SSH

Sometimes you may want to use GitHub with more than one account (for example, **personal** and **work**).  
Here is a clean way to manage this.


### 🔑 Create SSH Key for Personal Account

```bash
# Generate SSH key for personal account
ssh-keygen -t ed25519 -C "personal.email@example.com"
```

- Add the key to the SSH agent:
  ```bash
  ssh-add ~/.ssh/id_ed25519
  ```

- Copy the public key and add it to GitHub (Settings → SSH and GPG Keys):
  ```bash
  cat ~/.ssh/id_ed25519.pub
  ```

📝 Configure SSH for Personal Account
  Edit (or create) `~/.ssh/config` file:
  ```text
  Host github-personal
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519
  ```

- Now you can clone personal repositories like this:
  ```bash
  git clone git@github-personal:username/personal-repo.git
  ```

- ### 💡 What about Work Account?
  - If you also need a work account, simply repeat the same process:
  - Generate another SSH key (`e.g., id_ed25519_work`)
  - Add it to ssh-agent
  - Add the public key to your work GitHub account
  - Add a new section in `~/.ssh/config` (e.g., `github-work`)

Then you’ll be able to manage both accounts without conflicts.


