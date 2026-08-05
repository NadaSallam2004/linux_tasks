![Track](https://img.shields.io/badge/Track-ITI%20Shell%20Scripting-1f6feb) ![Language](https://img.shields.io/badge/Language-Bash-f4a261) ![Status](https://img.shields.io/badge/Status-Completed-2a9d8f)

# 🧬 Assignment 2 — Environment Variable Mystery

Making a custom environment variable survive past the current shell session — and proving it actually does.

<sub>📎 Part of the ITI Linux & Shell Scripting series — reviewed and documented command-by-command, not just copy-pasted output.</sub>

---

### 🧭 At a Glance

| | |
|---|---|
| **Goal** | Make `COMPANY=ITI` persistent across all terminal sessions |
| **Where it lives** | `~/.bashrc` |
| **Status** | ✅ Completed & verified |

---

### 🛠️ Walkthrough

| Step | Command | Result | Why |
|---|---|---|---|
| Create variable | `export COMPANY=ITI` | Temporary variable created | Only visible in the current shell |
| Verify it | `echo $COMPANY` | `ITI` | Confirms the variable exists |
| Test inheritance | `bash` → `echo $COMPANY` | `ITI` | Exported variables pass down to child shells |
| Make it permanent | `nano ~/.bashrc` | Added `export COMPANY=ITI` | Loads automatically on every future session |
| Apply immediately | `source ~/.bashrc` | Reloaded | No need to close/reopen the terminal |
| Confirm persistence | New terminal → `echo $COMPANY` | `ITI` | Survives across brand-new sessions |

---

### 🧪 Proof It Works

![Environment variable verified across sessions](screenshots/assignment2.png)

---

### 🏁 Verdict

> ✅ `COMPANY=ITI` is now permanent — it loads automatically in every new terminal without re-exporting it.

---

<sub>✍️ Part of a personal ITI Linux & Shell Scripting portfolio.</sub>
