# golden-arch/repo

Signed pacman repository for Golden Arch Linux, served via GitHub Pages.

## Add to pacman.conf

```ini
[golden-arch]
SigLevel = Required
Server = https://golden-arch.github.io/repo/$arch
```

Then trust the key:

```bash
sudo pacman-key --recv-keys 5FB5BF0F55007959
sudo pacman-key --lsign-key 5FB5BF0F55007959
# or install golden-arch-keyring first
```

## Packages

| Package | Description |
|---------|-------------|
| `golden-arch-keyring` | GPG keyring — install this first |
| `golden-arch-theme` | KDE Everforest Dark theme + Kvantum + icons |
| `golden-arch-defaults` | sysctl hardening, pacman.conf, /etc/skel |
| `golden-arch-branding` | Wallpapers, GRUB theme, Plymouth theme, SDDM theme |
| `golden-arch-hyprland-config` | Hyprland session config |
