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
Now, let's download the Kali Linux installation script.
```bash
wget https://raw.githubusercontent.com/EXALAB/AnLinux-Resources/master/Scripts/Kali/Kali.sh
```

```bash
wget -O install-nethunter-termux https://offs.ec/2MceZWr
chmod +x install-nethunter-termux
./install-nethunter-termux
```
--- 
```bash
wget -O install-nethunter-termux https://offs.ec/am
```
- [This URL is from the official Kali documentation; it points to the latest installer.](https://www.kali.org/docs/nethunter/nethunter-rootless/)


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

Step 8: Basic Usage and Commands


    

