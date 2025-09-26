# Docker Installation Guide

This guide will walk you through the process of installing Docker on different operating systems.

---

## 📌 Prerequisites
Before installing Docker, make sure you have:
- A 64-bit operating system.
- A user account with **sudo/root** privileges.
- Internet connection for downloading packages.

---

## 🐧 Install Docker on Linux (Ubuntu/Debian)

```bash
# Update your package index
sudo apt update
```

```bash
# Install required dependencies
sudo apt install -y ca-certificates curl gnupg lsb-release
```

```bash
# Add Docker’s official GPG key
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

```bash
# Set up the Docker repository
echo \ 
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \ 
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```bash
# Install Docker Engine
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

```bash
# Verify Docker installation
docker --version
```
