# Installing VMware Tools on Ubuntu
---

This guide explains how to install **VMware Tools** on an **Ubuntu** virtual machine. Installing VMware Tools provides:

- Enhanced graphics and display resolution
- Drag & Drop support between host and VM
- Improved mouse and keyboard functionality
- Time synchronization with the host system

---

## Prerequisites

1. A virtual machine running **Ubuntu**
2. VMware Workstation, VMware Player, or VMware ESXi
3. User with **sudo** or **root** privileges

---

### 1. Update your system

Always start by updating your packages:

```bash
sudo apt update
sudo apt upgrade -y
```

2. Install required packages

VMware Tools requires build tools and Linux headers:

```bash
sudo apt install -y open-vm-tools open-vm-tools-desktop build-essential linux-headers-$(uname -r)








