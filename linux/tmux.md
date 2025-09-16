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

## 🚀 Getting Started

To start tmux, simply type:

```bash
tmux
```

You are now inside a tmux session.  
By default, tmux uses **`Ctrl + b`** as the **prefix key**. Every command in tmux starts with this prefix.

Example:
- To split the screen horizontally → press `Ctrl + b` then `"`
- To split vertically → press `Ctrl + b` then `%`

---

## 🪟 Windows and Panes

### Windows
- Create a new window: `Ctrl + b, c`
- Switch to next window: `Ctrl + b, n`
- Switch to previous window: `Ctrl + b, p`
- List all windows: `Ctrl + b, w`
- Rename window: `Ctrl + b, ,`

### Panes
- Split horizontally: `Ctrl + b, "`
- Split vertically: `Ctrl + b, %`
- Move between panes: `Ctrl + b` + Arrow key
- Close pane: `Ctrl + b, x`
- Resize pane: `Ctrl + b` + Alt + Arrow key

---

## 📂 Sessions

Sessions are collections of windows and panes. They make it easy to organize different tasks.

- Start a new named session:
  ```bash
  tmux new -s mysession
  ```

- Detach from session (leave it running):
  ```
  Ctrl + b, d
  ```

- List all sessions:
  ```bash
  tmux ls
  ```

- Reattach to a session:
  ```bash
  tmux attach -t mysession
  ```

- Kill a session:
  ```bash
  tmux kill-session -t mysession
  ```

---

## 🛠️ Useful Commands Cheat Sheet

| Action | Command |
|--------|----------|
| New session | `tmux new -s name` |
| List sessions | `tmux ls` |
| Attach session | `tmux attach -t name` |
| Detach session | `Ctrl + b, d` |
| New window | `Ctrl + b, c` |
| Rename window | `Ctrl + b, ,` |
| Next/Prev window | `Ctrl + b, n` / `Ctrl + b, p` |
| Split pane (vertical) | `Ctrl + b, %` |
| Split pane (horizontal) | `Ctrl + b, "` |
| Switch pane | `Ctrl + b` + Arrow key |
| Close pane | `Ctrl + b, x` |
| Kill session | `tmux kill-session -t name` |

---

## 🎯 Example Workflow

Here’s how you might use tmux in real life:

1. Start tmux:
   ```bash
   tmux new -s dev
   ```

2. Split your terminal into two vertical panes:
   ```
   Ctrl + b, %
   ```

3. In the left pane, run a development server (e.g., `npm run dev`).  
   In the right pane, edit files or monitor logs.

4. Open another window for Git commands:  
   ```
   Ctrl + b, c
   ```

5. Detach from your session (leave everything running):  
   ```
   Ctrl + b, d
   ```

6. Later, reconnect to it:
   ```bash
   tmux attach -t dev
   ```

---

## ⚡ Tips and Tricks

- **Scroll in history:** Press `Ctrl + b, [` then use Arrow keys or PgUp/PgDn. Exit with `q`.
- **Rename session:**  
  ```bash
  tmux rename-session -t oldname newname
  ```
- **Persistent sessions:** Combine tmux with `byobu` or use `tmux-resurrect` plugin to save/restore sessions.

---

## 📚 Resources

- Official documentation: [https://github.com/tmux/tmux/wiki](https://github.com/tmux/tmux/wiki)
- Cheatsheet: [https://tmuxcheatsheet.com/](https://tmuxcheatsheet.com/)
- Tutorial: [https://linuxize.com/post/getting-started-with-tmux/](https://linuxize.com/post/getting-started-with-tmux/)

---

🚀 Now you are ready to supercharge your terminal with tmux!
