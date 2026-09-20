# Scaff

A macOS app for designers. Download a release, drag it to Applications, and start working.

This repository hosts **installers only**. Source is not published here.

## Download

Get the latest DMG from [Releases](https://github.com/scaff-design/scaff/releases/latest).

| Your Mac | File |
|----------|------|
| Apple Silicon (M1, M2, M3, M4, …) | `Scaff-…-mac-arm64.dmg` |
| Intel | `Scaff-…-mac-x64.dmg`

Apple menu → **About This Mac** shows the chip. The wrong DMG will not run.

## Install

1. Open the DMG.
2. Drag **Scaff** into **Applications**.
3. Eject the disk image.

### First launch (unsigned builds)

Current releases are **unsigned**. After AirDrop, Messages, email, or a browser download, macOS quarantines the app and blocks it. On Sequoia and Tahoe, Control-click → Open no longer bypasses that.

In Terminal:

```sh
xattr -cr "/Applications/Scaff.app"
open "/Applications/Scaff.app"
```

That only clears the “downloaded file” flag. Use it for a build you trust. Testers have to run this themselves; it is not a shipping path.

Without an [Apple Developer](https://developer.apple.com/programs/) account ($99/year) you do **not** get:

- A DMG that opens after drag-to-Applications with no Terminal step
- [Notarization](https://developer.apple.com/documentation/security/notarizing-macos-software-before-distribution)
- Auto-update that replaces the app in place on the Mac

Unsigned apps can still *offer* a newer DMG from this Releases page. Installing it is a manual replace, then the `xattr` step again.

## After it opens

1. Pick a workspace folder if the welcome dialog asks.
2. Open **Settings → Models** and paste an API key.
3. Start a session.

Keys stay on this Mac.

## Updates

**Settings → Check for updates** looks at this repository’s latest release. Anyone can download; only maintainers can publish new versions.
