# golden-arch/repo

The signed pacman package repository for Golden Arch, served via GitHub Pages.

## Structure

```
repo/
└── x86_64/
    ├── golden-arch.db            # pacman database (symlink to .tar.gz)
    ├── golden-arch.db.tar.gz
    ├── golden-arch.files
    ├── golden-arch.files.tar.gz
    └── *.pkg.tar.zst             # built packages + .sig files
```

## Adding a package

```bash
repo-add golden-arch.db.tar.gz golden-arch-keyring-*.pkg.tar.zst
```

Then commit and push — GitHub Pages serves the directory automatically.

## pacman.conf entry

```ini
[golden-arch]
SigLevel = Required DatabaseOptional
Server = https://golden-arch.github.io/repo/$arch
```

> Note: GitHub Pages must be enabled on this repo (Settings → Pages → Deploy from branch → main).
