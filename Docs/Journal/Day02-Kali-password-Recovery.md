# Day 02 - Kali Password Recovery

## Problem
Forgot my Kali login password after reinstalling.

## Recovery
1. Booted to GRUB (Esc/Shift).
2. Pressed `e` on the Kali boot entry.
3. add to:
 quiet splash
   with:
   rw init=/bin/bash
    ```
4. Booted with `Ctrl + X`.
5. Ran:
   ```bash
   mount -o remount,rw /
   passwd akunatakasi
   reboot -f
   ```

## Lesson
- GRUB can be used to recover a Linux password.
- The root filesystem must be mounted as read-write.
- Physical access to an unencrypted machine is enough to reset passwords.