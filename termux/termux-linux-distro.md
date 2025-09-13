# 📖 Installing Kali Linux on Termux

## 📌 Prerequisites & Warnings

Before installing any Linux distribution (Ubuntu, Kali, Debian, Alpine, Arch) inside Termux, you should be aware of the following requirements and limitations:

### 🔹 Storage Requirements

- Minimum **4 GB free space** for lightweight distros (like Alpine).
- At least **6–8 GB free space** for larger distros (Ubuntu, Debian, Arch).
- For **Kali Linux**, it is recommended to have **10 GB free space** due to its security tools.

### 🔹 Termux Version

- Always use the **latest version of Termux** (download from [F-Droid](https://f-droid.org/packages/com.termux/)).
- The old Play Store version is outdated and no longer maintained, which may cause package errors.

### 🔹 Required Permissions

Run the following command to grant storage access:

```bash
termux-setup-storage
```

This allows Termux to access internal storage (needed for saving files and rootfs backups).

A stable internet connection is required to download rootfs or packages.

### 🔹 Security Notes & Limitations

- Inside Termux with `proot`, you **do not get real root access** to the Android kernel.
- Installing or modifying kernel modules or low-level system components is not possible.
- Installed distros act more like a **user-space environment**, not a full replacement for your phone’s OS.
- If you run network services (like SSH or VNC), be careful about security risks since your phone could be exposed.

### 📋 Check Available Distributions Before Installation
  - Before installing any Linux distribution, you can check which ones are available in **proot-distro** by running:
    ```bash
    proot-distro list
    ```

### 🔹 Installation Options

2. **Using proot-distro** ✅  
   - Easiest method to install Linux distributions.  
   - Just run:  
     ```bash
     proot-distro install <distro>
     ```  
   - Fast, stable, and recommended for most users.  

3. **Manual installation with proot + rootfs extraction** ⚙️  
   - For advanced users who want custom versions or manual setup.  
   - Requires downloading rootfs (via `wget`) and running `proot` with specific parameters.  
   - More flexible, but involves more steps and a higher chance of errors.
  
---

## Step 2: Preparing Termux

Before installing any Linux distribution, you need to prepare your Termux environment with the necessary updates and tools.

### 🔹 Update and Upgrade Packages
First, update the package lists and upgrade existing packages:
```bash
pkg update && pkg upgrade -y
```

### 🔹 Install Required Tools
Install `proot` and `proot-distro` which are needed to run Linux distributions:
```bash
pkg install proot proot-distro -y
```

### 🔹 (Optional) Grant Storage Access
If you haven’t already, allow Termux to access your device storage:
```bash
termux-setup-storage
```

This step is useful for saving files, backups, and sharing data between Termux and your Android internal storage.

---








