![Track](https://img.shields.io/badge/Track-ITI%20Shell%20Scripting-1f6feb) ![Language](https://img.shields.io/badge/Language-Bash-f4a261) ![Status](https://img.shields.io/badge/Status-Completed-2a9d8f)

# 🕵️ Task 1 — Shell & Environment Detective

A command-by-command investigation into what the shell already knows about itself — the running shell, the current user, the machine, and the environment around it — each claim backed by a real terminal screenshot.

<sub>📎 Part of the ITI Linux & Shell Scripting series — reviewed and documented command-by-command, not just copy-pasted output.</sub>

---

### 🧭 At a Glance

| | |
|---|---|
| **Focus** | Shell, process, user, and environment introspection |
| **Commands covered** | 9 |
| **Status** | ✅ Completed & verified |

---

### 🔍 The Investigation

**1. Current Shell**
```bash
echo $SHELL
```
Result: `/bin/bash` — the type of shell currently running.

![Current Shell](screenshots/01-shell.jpg)

---

**2. Parent PID**
```bash
echo $PPID
```
Result: `8` — the process ID of the parent that started this shell.

![Parent PID](screenshots/02-ppid.jpg)

---

**3. Current User**
```bash
whoami
```
Result: `rahma11` — the username of the currently logged-in user.

![Current User](screenshots/03-whoami.jpg)

---

**4. Current Working Directory**
```bash
pwd
```
Result: `/mnt/c/Windows/system32` — where the shell is currently located.

![Current Working Directory](screenshots/04-pwd.jpg)

---

**5. Hostname**
```bash
hostname
```
Result: `DESKTOP-RU9D2C8` — the name of the machine.

![Hostname](screenshots/05-hostname.jpg)

---

**6. Login Shell Entry (from `/etc/passwd`)**
```bash
grep "^$USER" /etc/passwd
```
Result: `rahma11:x:1000:1000::/home/rahma11:/bin/bash` — the user's home directory and login shell as recorded in `/etc/passwd`.

![Login Shell Entry](screenshots/06-passwd-entry.jpg)

---

**7. PATH**
```bash
echo $PATH
```
Result: a long list of directories the shell searches for executables (e.g. `/home/rahma11/miniconda3/bin`, `/usr/local/sbin`, `/usr/bin`, `/mnt/c/Windows/system32`, …).

![PATH](screenshots/07-path.jpg)

---

**8. First Attempt: Counting Environment Variables (typo)**
```bash
printwnv | wc -l
```
Result: `Command 'printwnv' not found, did you mean: command 'printenv'...` → output `0`. A typo causes the shell to fail and suggest the correct command.

![printenv typo](screenshots/08-printenv-typo.jpg)

---

**9. Number of Environment Variables (corrected)**
```bash
printenv | wc -l
```
Result: `26` — the corrected command, counting the environment variables currently set.

![printenv count](screenshots/09-printenv-count.jpg)

---

### 📋 Coverage Note

Two items from the original task list — **Shell PID** (`echo $$`) and **Home Directory** (`echo $HOME`) — aren't included above because no matching screenshots were available. Add them in the same format once the screenshots are ready, to keep the investigation complete.

---

### 🏁 Verdict

> ✅ 9 out of 11 detective checks are documented and verified against real terminal output. The remaining two only need their screenshots.

---

<sub>✍️ Part of a personal ITI Linux & Shell Scripting portfolio.</sub>
