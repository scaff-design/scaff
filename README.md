# Scaff

A macOS app for designers. Download a release, move it to Applications, and start working.

This repository hosts **installers only**. Source is not published here.

## Download

Get the latest DMG from [Releases](https://github.com/scaff-design/scaff/releases/latest).

| Your Mac | File |
|----------|------|
| Apple Silicon (M1, M2, M3, M4, …) | `Scaff-…-mac-arm64.dmg` |
| Intel | `Scaff-…-mac-x64.dmg` |

Apple menu → **About This Mac** shows the chip. The wrong DMG will not run.

## Install

1. Open the DMG.
2. Drag **Scaff** into **Applications**.
3. If **Scaff.app** is in **Downloads** instead, move it to Applications (Finder, or Terminal below).
4. Eject the disk image.

```sh
mv ~/Downloads/Scaff.app /Applications/
```

### First launch (unsigned builds)

Current releases are **unsigned**. After AirDrop, Messages, email, or a browser download, macOS quarantines the app and blocks it. On Sequoia and Tahoe, Control-click → Open no longer bypasses that.

In Terminal:

```sh
xattr -cr "/Applications/Scaff.app"
open "/Applications/Scaff.app"
```

## After it opens

1. Pick a workspace folder if the welcome dialog asks.
2. Open **Settings → Models** and paste an API key.
3. Start a session.

Keys stay on this Mac.

## Updates

**Settings → Check for updates** looks at this repository’s latest release. Anyone can download; only maintainers can publish new versions.
