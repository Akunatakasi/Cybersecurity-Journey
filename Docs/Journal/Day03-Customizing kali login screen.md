# Day 03 - Customizing the Kali Login Screen

## Goal
Replace Kali Linux's default LightDM login screen background with a custom cybersecurity wallpaper.

## Process
1. Identified that the desktop wallpaper and login screen wallpaper are managed separately.
2. Opened the LightDM greeter configuration file.
3. Copied the custom wallpaper (k.jpg) into `/usr/share/backgrounds/`.
4. Corrected file ownership and permissions so the greeter could access the image.
5. Updated the `background` path in `lightdm-gtk-greeter.conf`.
6. Discovered that the default `Kali-Light` theme ignores custom background images.
7. Changed the greeter theme from `Kali-Light` to `Adwaita`.
8. Saved the configuration and rebooted the system.
9. Verified that the custom Kaiju wallpaper successfully appeared on the login screen.

## Commands Learned
```bash
sudo cp ~/Pictures/k.jpg /usr/share/backgrounds/
sudo chmod 644 /usr/share/backgrounds/k.jpg
sudo mousepad /etc/lightdm/lightdm-gtk-greeter.conf
sudo reboot
```

Configuration changed:

```ini
background = /usr/share/backgrounds/k.jpg
theme-name = Adwaita
```

## Lessons
- The login screen wallpaper is controlled by LightDM, not the desktop environment.
- Image permissions must allow the greeter to read the wallpaper.
- The `Kali-Light` greeter theme overrides custom backgrounds.
- Switching to the `Adwaita` theme allows the `background` setting to work correctly.
- Troubleshooting Linux often involves verifying file paths, permissions, and configuration files step by step.

## Outcome
Successfully replaced the default Kali login screen with a custom cybersecurity wallpaper and gained a practical understanding of LightDM greeter customization, Linux permissions, and theme configuration.