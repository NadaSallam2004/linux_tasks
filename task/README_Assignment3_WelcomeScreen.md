![Track](https://img.shields.io/badge/Track-ITI%20Shell%20Scripting-1f6feb) ![Language](https://img.shields.io/badge/Language-Bash-f4a261) ![Status](https://img.shields.io/badge/Status-Completed-2a9d8f)

# 👋 Assignment 3 — Build Your Own Linux Shell Environment (Welcome Screen)

Giving every new terminal session a personalized welcome banner, so it feels like a proper dev environment from the first keystroke.

<sub>📎 Part of the ITI Linux & Shell Scripting series — reviewed and documented command-by-command, not just copy-pasted output.</sub>

---

### 🧭 At a Glance

| | |
|---|---|
| **Scenario** | Every developer gets the same productive terminal on login |
| **Where it lives** | `~/.bashrc` |
| **Status** | ✅ Completed & verified |

---

### 🛠️ Walkthrough

**1. Open the shell configuration file**
```bash
nano ~/.bashrc
```

**2. Add the welcome block at the end of the file**
```bash
clear
echo "=========================================="
echo "      Welcome to ITI Linux Environment"
echo "=========================================="
echo "User      : $USER"
echo "Hostname  : $(hostname)"
echo "Date      : $(date)"
echo "Shell     : $SHELL"
echo "Current Dir : $(pwd)"
echo ""
echo "Have a productive day!"
echo "=========================================="
```

**3. Save and exit** — `Ctrl+O` → Enter → `Ctrl+X`

**4. Reload the configuration**
```bash
source ~/.bashrc
```

---

### 🧪 Expected Output

```
==========================================
      Welcome to ITI Linux Environment
==========================================
User      : rahma11
Hostname  : DESKTOP-RU9D2C8
Date      : Sun Aug  2 09:56:53 PDT 2026
Shell     : /bin/bash
Current Dir : /home/rahma11

Have a productive day!
==========================================
```

![Welcome screen in action](screenshots/assignment3-welcome.png)

---

### 🏁 Verdict

> ✅ The welcome block now runs automatically on every new terminal, with values that update dynamically via shell variables and command substitution — no hard-coded text.

---

<sub>✍️ Part of a personal ITI Linux & Shell Scripting portfolio.</sub>
