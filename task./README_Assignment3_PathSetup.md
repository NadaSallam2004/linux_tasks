![Track](https://img.shields.io/badge/Track-ITI%20Shell%20Scripting-1f6feb) ![Language](https://img.shields.io/badge/Language-Bash-f4a261) ![Status](https://img.shields.io/badge/Status-Completed-2a9d8f)

# 🧭 Assignment 3 — Build Your Own Linux Shell Environment (Custom PATH)

Turning a personal `mybin` folder into a source of "built-in" commands, available from anywhere in the terminal.

<sub>📎 Part of the ITI Linux & Shell Scripting series — reviewed and documented command-by-command, not just copy-pasted output.</sub>

---

### 🧭 At a Glance

| | |
|---|---|
| **Goal** | Add a personal `~/mybin` directory to `PATH`, permanently |
| **Where it lives** | `~/.bashrc` |
| **Status** | ✅ Completed & verified |

---

### 🛠️ Walkthrough

| Step | Command | Result |
|---|---|---|
| 1. Check current directory | `pwd` | `/home/rahma11` |
| 2. Create the personal bin folder | `mkdir ~/mybin` | Folder ready to hold custom scripts |
| 3. Add it to `PATH` permanently | `echo 'export PATH=$PATH:$HOME/mybin' >> ~/.bashrc` | Line appended to `.bashrc` |
| 4. Reload the shell config | `source ~/.bashrc` | Change applied immediately |
| 5. Verify `PATH` | `echo $PATH` | Includes `:/home/rahma11/mybin` |
| 6. Create a test script | `nano ~/mybin/hello.sh` → `echo "Hello ITI"` | Script written |
| 7. Make it executable | `chmod +x ~/mybin/hello.sh` | Ready to run |
| 8. Run it from anywhere | `hello.sh` | `Hello ITI` |

---

### 🧪 Proof It Works

**PATH setup and verification**
![PATH setup](screenshots/assignment3-path.png)

**Script creation and execution**
![Script running](screenshots/assignment3-script.png)

---

### 🏁 Verdict

> ✅ Any script dropped into `~/mybin` now runs as a plain command from anywhere, in every new terminal session — no `./` and no full path needed.

---

<sub>✍️ Part of a personal ITI Linux & Shell Scripting portfolio.</sub>
