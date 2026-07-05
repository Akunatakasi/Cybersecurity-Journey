# Linux Terminal Basics (ELF)

## pwd (Print Working Directory)

**Purpose:** Shows your current directory.

**Syntax**
```bash
pwd
```

**Example**
```bash
pwd
# /home/akunatakasi/Cybersecurity-Journey
```

**Used For**
- Confirm your current location
- Verify where commands will execute

---

## ls (List Directory)

**Purpose:** Lists files and folders in the current directory.

**Syntax**
```bash
ls
```

**Useful Options**
```bash
ls -l      # Detailed list
ls -a      # Show hidden files
ls -la     # Detailed + hidden files
```

**Used For**
- View files
- Check project contents
- View hidden files like `.git`

---

## cd (Change Directory)

**Purpose:** Moves between folders.

**Syntax**
```bash
cd folder_name
```

**Examples**
```bash
cd Cybersecurity-Journey
cd ..
cd ~
```

**Used For**
- Navigate projects
- Enter folders
- Return Home

---

## mkdir (Make Directory)

**Purpose:** Creates a new folder.

**Syntax**
```bash
mkdir folder_name
```

**Examples**
```bash
mkdir Labs
mkdir Notes
mkdir -p Notes/Linux/Commands
```

**Used For**
- Create project folders
- Organize notes

---

## touch

**Purpose:** Creates an empty file.

**Syntax**
```bash
touch filename
```

**Examples**
```bash
touch README.md
touch notes.md
touch script.py
```

**Used For**
- Create scripts
- Create documentation

---

## cat

**Purpose:** Displays file contents.

**Syntax**
```bash
cat filename
```

**Example**
```bash
cat README.md
```

**Used For**
- Read files
- View configuration

---

## cp (Copy)

**Purpose:** Copies files or folders.

**Syntax**
```bash
cp source destination
```

**Examples**
```bash
cp notes.md backup.md
cp -r Labs Backup
```

**Used For**
- Backups
- Duplicate files

---

## mv (Move / Rename)

**Purpose:** Moves or renames files.

**Syntax**
```bash
mv source destination
```

**Examples**
```bash
mv old.py new.py
mv script.py Scripts/
```

**Used For**
- Organize files
- Rename projects

---

## rm (Remove)

**Purpose:** Deletes files or folders.

**Examples**
```bash
rm file.txt
rm -r Folder
rm -rf Folder
```

⚠️ `rm -rf` permanently deletes files.

**Used For**
- Clean up files
- Remove folders

---

## clear

**Purpose:** Clears the terminal.

```bash
clear
```

Shortcut:

```text
Ctrl + L
```

---

## history

**Purpose:** Shows previously executed commands.

```bash
history
```

---

## whoami

**Purpose:** Displays the current logged-in user.

```bash
whoami
```

---

## man

**Purpose:** Opens the manual page for a command.

```bash
man ls
```

Exit:

```text
q
```

---

## find

**Purpose:** Searches for files or folders.

```bash
find . -name "*.py"
```

---

## grep

**Purpose:** Searches for text inside files.

```bash
grep "password" notes.txt
```

---

## sudo

**Purpose:** Executes commands with administrator privileges.

```bash
sudo apt update
```

---

## apt

**Purpose:** Installs, updates and removes software.

```bash
sudo apt update
sudo apt upgrade
sudo apt install package_name
sudo apt remove package_name
```

---

# Quick Reference

| Command | Purpose |
|---------|---------|
| `pwd` | Show current directory |
| `ls` | List files |
| `cd` | Change directory |
| `mkdir` | Create folder |
| `touch` | Create file |
| `cat` | Display file |
| `cp` | Copy |
| `mv` | Move / Rename |
| `rm` | Delete |
| `clear` | Clear terminal |
| `history` | Show command history |
| `whoami` | Current user |
| `man` | Manual pages |
| `find` | Search files |
| `grep` | Search text |
| `sudo` | Administrator privileges |
| `apt` | Package manager |