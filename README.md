# Scaff

A Mac and Windows app for designers. Download a release and start working.

This repository hosts **installers only**. Source is not published here.

## Download

Get the latest installer from [Releases](https://github.com/scaff-design/scaff/releases/latest).

| Your computer | File |
| --- | --- |
| Mac, Apple silicon (M1, M2, M3, M4, …) | `Scaff-…-mac-arm64.dmg` |
| Windows, 64-bit | `Scaff-…-win-x64.exe` |

Apple menu → **About This Mac** shows the chip. Current releases are Apple silicon and 64-bit Windows.

## Install

### Mac

1. Open the DMG.
2. Drag **Scaff** into **Applications**.
3. If **Scaff.app** is in **Downloads** instead, move it to Applications (Finder, or Terminal below).
4. Eject the disk image.

```sh
mv ~/Downloads/Scaff.app /Applications/
```

The first time you open it, macOS asks you to confirm an app downloaded from the internet. Current Mac releases are signed and notarized, so that confirmation is enough.

If macOS says Scaff is damaged, clear the download quarantine once and open it again:

```sh
xattr -dr com.apple.quarantine "/Applications/Scaff.app"
open "/Applications/Scaff.app"
```

### Windows

1. Run `Scaff-…-win-x64.exe`.
2. If SmartScreen says **Windows protected your PC**, click **More info**, then **Run anyway**.
3. Finish the installer. It installs for your account, and you can choose the folder.

## After it opens

1. Pick a project folder if the welcome dialog asks, or start fresh and add one later.
2. Open **Settings → Models**. Sign in with Claude, ChatGPT, Grok, Cursor, or Copilot, paste an API key, or connect Ollama on this computer.
3. Start a session.

Keys and sign-ins stay on this computer.

## Updates

Scaff checks this repository’s latest release on its own, and **Settings → Check for updates** checks now. Mac and Windows builds download the update and install it when you restart. Projects and settings stay in place.

Anyone can download. Only maintainers can publish new versions.

## If Scaff can't start

When some of Scaff’s files are missing, it opens a repair window, looks for a newer release, and installs that over this copy. Projects and settings stay. You can also download the installer again and install it over the app you already have.
