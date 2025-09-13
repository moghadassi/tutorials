<img src="https://www.kali.org/images/kali-nethunter-logo.png" alt="Kali NetHunter Logo" width="150"/>

# Kali Linux Installation on Termux (Android)

This guide will help you install Kali Linux on your Android device using Termux.

## Prerequisites

Before starting the installation process, ensure you have the following:

- **Android device** (rooting is not required)
- **Termux app** installed (You can get Termux from [F-Droid](https://f-droid.org/packages/com.termux/))
- **Stable internet connection**

## Step-by-Step Guide

### Step 1: Update Termux Packages

First, update the Termux repositories to ensure you have the latest packages:
```bash
pkg update && pkg upgrade
```

## Step 2: Install Required Packages
Install essential packages needed for Kali Linux installation:
```bash
pkg install wget proot -y
```

### Step 3: Download the Kali Linux Installer
Download the official Kali NetHunter installer from the latest source:

```bash
wget -O install-nethunter-termux https://gitlab.com/kalilinux/nethunter/build-scripts/kali-nethunter-project/-/raw/master/nethunter-rootless/install-nethunter-termux
```
--- 

```bash
curl -LO https://gitlab.com/kalilinux/nethunter/build-scripts/kali-nethunter-project/-/raw/master/nethunter-rootless/install-nethunter-termux
```

```bash
wget -O install-nethunter-termux https://offs.ec/2MceZWr
chmod +x install-nethunter-termux
./install-nethunter-termux
```

### Step 4: Give Execute Permission
Make the downloaded script executable:
```bash
chmod +x install-nethunter-termux
```

### 5. Run the installer:
```bash
./install-nethunter-termux
```

- You'll be prompted to choose the installation type. Select Full for a complete Kali setup, or Minimal if you want a lighter version.
- The script will download and extract Kali Linux files. This may take some time – please be patient.

### Step 6: Start Kali Linux in Termux
1. Once installation is complete, start Kali with:
  ```bash
  nh
  ```
  - (This is short for `nethunter`.)
2. If it's your first time, you may need to set up a password or configure additional settings as prompted.

### Step 7: (Optional) Set Up GUI with KeX
  1. To access a graphical interface:
     
  - In Kali (after starting with nh), install a desktop environment if not already included:
    ```bash
    apt update
    apt install kali-desktop-xfce -y
    ```
  - Exit Kali and return to Termux.
  - Launch the NetHunter-KeX client app.
  - Connect to localhost:1 (default settings).

  2. You should now see the Kali Linux desktop on your Android device!

### Step 8: Basic Usage and Commands
  - To update Kali packages: Run `apt update && apt upgrade` inside the Kali session.
  - To exit Kali: Type `exit`.
  -  Common tools like `nmap`, `metasploit`, etc., are available in the full installation.
  - If you need to uninstall: Run `./install-nethunter-termux` -r to remove it safely.


## Troubleshooting Tips
- **Error with downloads? Check your internet connection or try a VPN if your region has restrictions.**
- **Permission denied? Ensure Termux has storage access (Settings > Apps > Termux > Permissions).**
- **Out of space? Clear cache or use an SD card if supported.**
- **For more help, visit the official Kali NetHunter documentation or Termux GitHub issues.**


---
