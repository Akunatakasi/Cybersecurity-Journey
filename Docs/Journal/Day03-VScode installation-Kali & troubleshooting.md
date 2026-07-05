# Day 03 - VS Code Environment Setup & Dependency Troubleshooting

## Goal
Set up Visual Studio Code as my primary development environment in Kali Linux for Python and cybersecurity labs.

## Process

1. Updated Kali Linux packages.
   ```bash
   sudo apt update
   sudo apt full-upgrade -y
   ```

2. Created my Cybersecurity workspace.
   ```bash
   mkdir ~/Cybersecurity-Journey
   cd ~/Cybersecurity-Journey
   ```

3. Installed Code OSS.
   ```bash
   sudo apt install code-oss -y
   ```

4. Attempted to launch VS Code.

5. Encountered the following error:
   ```text
   Error: libnode.so.115: cannot open shared object file
   ```

6. Verified the installed Node libraries.
   ```bash
   ldconfig -p | grep libnode
   ```

7. Reinstalled the Node runtime.
   ```bash
   sudo apt install --reinstall nodejs libnode-dev
   ```

8. Removed and reinstalled Code OSS.
   ```bash
   sudo apt purge code-oss -y
   sudo apt autoremove -y
   sudo apt install code-oss -y
   ```

9. Confirmed the issue still persisted after reinstalling.

10. Decided to switch from Code OSS to the official Microsoft Visual Studio Code package for better compatibility and long-term stability.

## Commands Used

```bash
sudo apt update
sudo apt full-upgrade -y

mkdir ~/Cybersecurity-Journey
cd ~/Cybersecurity-Journey

sudo apt install code-oss -y

ldconfig -p | grep libnode

sudo apt install --reinstall nodejs libnode-dev

sudo apt purge code-oss -y
sudo apt autoremove -y
sudo apt install code-oss -y
```

## Lesson

- Always verify the root cause before reinstalling software.
- Shared library errors often indicate dependency mismatches.
- Rolling Linux distributions can introduce package compatibility issues.
- Official vendor packages are sometimes more stable than distribution packages.
- Troubleshooting is a process of eliminating possibilities rather than guessing solutions.