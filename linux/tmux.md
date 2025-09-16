# 🖥️ Introduction to tmux

`tmux` (Terminal MUltipleXer) is a powerful tool that allows you to manage multiple terminal sessions within a single window.  
It is especially useful when working on remote servers, running long processes, or organizing different tasks in one place.

With tmux, you can:
- Run multiple shells in one terminal.
- Split your terminal into multiple panes.
- Detach from sessions and reattach later.
- Keep your programs running even if you disconnect.

---

## 📦 Installation

### Linux
Install tmux with your package manager:

```bash
# Ubuntu/Debian
sudo apt update && sudo apt install tmux -y
```

```bash
# Fedora
sudo dnf install tmux -y
```

```bash
# Arch Linux
sudo pacman -S tmux
```

### macOS

```bash
brew install tmux
```

### Windows (via WSL)
If you are using **Windows Subsystem for Linux (WSL)**, just install tmux inside your Linux distribution as above.

Check installation:
```bash
tmux -V
```

---