![Ubuntu Logo](https://assets.ubuntu.com/v1/29985a98-ubuntu-logo32.png)

# Install Ubuntu on your mobile using `Termux` ✅


### Install Termux on Android
Termux is a terminal emulator and Linux environment for Android that allows you to run Linux tools directly on your phone.

## Steps to Install Termux
### 1. Install from Official Sources
The Google Play version of Termux is outdated. The only official and updated sources are:
- [F-Droid (official open-source repository)](https://f-droid.org/packages/com.termux/)
- [GitHub Releases (official Termux page)](https://github.com/termux/termux-app/releases)

 ✅ It is recommended to install from F-Droid, as updates are more stable and released faster.

### 2. Enable installation from unknown sources (on Android)
  Before installation, enable the following setting on your phone:
```
 Settings → Security → Install from unknown sources 
```

### 3. Download and Install
   
- Download the Termux APK file from one of the sources above.
- Install it (tap on the file and follow the installation steps).

### 4. Run Termux

  - After installation, open the app. The first launch will give you a simple terminal environment.

### 5. Update packages
- Always update built-in packages after first launch:

```bash
pkg update && pkg upgrade -y
```


## Official Resources & Documentation:

- [Official Termux repository on GitHub](https://github.com/termux/termux-app)
- [Termux page on F-Droid](https://f-droid.org/packages/com.termux/)
- [Official Termux Wiki](https://wiki.termux.com/wiki/Main_Page)
  
---


## Install Ubuntu on Termux
After installing and preparing Termux, you can run the Ubuntu operating system inside it.

![Ubuntu Logo](assets/ubuntu-logo.png)


## Steps to Install
### 1. Update packages in Termux
- Open Termux and run:
```bash
pkg update && pkg upgrade -y
```

### 2. Install required tools
- To download and run Ubuntu, install proot-distro:
```bash
pkg install proot-distro -y
```

### 3. Download and install Ubuntu
- Now install Ubuntu:
```bash
proot-distro install ubuntu
```
🐧 This command will download and install Ubuntu inside Termux.


### 4. Create a shortcut for quick access

- Typing the full login command every time is long. You can create an alias so that typing ubuntu will enter `Ubuntu`directly.
- Run the following command to create the alias and apply it immediately:

```bash
echo "alias ubuntu='proot-distro login ubuntu'" >> ~/.bashrc && source ~/.bashrc
```

### 5. Enter Ubuntu
- From now on, simply type:
```bash
ubuntu
```

#### and you will directly enter the Ubuntu environment ✅



