# 🔑 SSH Guide

This file provides a short explanation of **SSH (Secure Shell)** and how to use it for connecting to servers or services like GitHub.  

---

## ✨ What is SSH?
**SSH** (*Secure Shell*) is an encryption protocol that allows secure access to a remote server or system.  
With SSH you can:
- Log in to servers
- Execute commands
- Transfer files (`scp` or `sftp`)
- Connect securely to services like **GitHub**

---

## ⚙️ Generate an SSH Key
To create an SSH key on your system, run:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
