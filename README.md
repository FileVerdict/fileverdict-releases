<p align="center">
  <a href="https://fileverdict.com">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset=".github/assets/fileverdict-logo-violet-white-text.svg">
      <img src=".github/assets/fileverdict-logo-colour.svg" alt="FileVerdict" width="360">
    </picture>
  </a>
</p>

<p align="center">
  Review and clean up the audio and subtitle tracks in your video files,<br>
  rename them the way Plex and Jellyfin expect, and compress them, all in one desktop app.
</p>

<p align="center">
  <a href="https://github.com/FileVerdict/fileverdict-releases/releases/latest"><img src="https://img.shields.io/github/v/release/FileVerdict/fileverdict-releases?label=latest&color=5B5BD6&style=flat-square" alt="Latest release"></a>
  <img src="https://img.shields.io/badge/Windows-10%20%7C%2011-5B5BD6?style=flat-square" alt="Windows 10 and 11">
  <img src="https://img.shields.io/badge/Linux-AppImage-5B5BD6?style=flat-square" alt="Linux AppImage">
  <img src="https://img.shields.io/badge/price-free%20%2B%20Pro-5B5BD6?style=flat-square" alt="Free, with an optional Pro plan">
</p>

<p align="center">
  <a href="https://fileverdict.com"><b>Website</b></a> ·
  <a href="https://fileverdict.com/docs/"><b>Docs</b></a> ·
  <a href="https://github.com/FileVerdict/fileverdict-releases/releases"><b>All releases</b></a> ·
  <a href="https://fileverdict.com/support/"><b>Support</b></a>
</p>

---

## Download

Get the newest version from the **[latest release](https://github.com/FileVerdict/fileverdict-releases/releases/latest)**.

| Platform | File to download | Notes |
|---|---|---|
| **Windows** 10 or 11, 64-bit | `File.Verdict_<version>_x64-setup.exe` | Run the installer. |
| **Linux**, 64-bit Intel or AMD | `FileVerdict_<version>_amd64.AppImage` | Make it executable, then open it. Ubuntu 22.04, Debian 12, Fedora 36 or newer. |
| macOS | | Planned. |
| Headless / Docker | | Planned. |

Once installed, FileVerdict checks this page for updates shortly after launch and installs them
for you. Updates are signed, and the app refuses one that isn't.
Step-by-step setup is in the [installation guide](https://fileverdict.com/docs/getting-started/installation/).

## What it does

- **Track review.** Reads every audio and subtitle track and suggests which to keep and which to
  remove, using language, caption density, forced and hearing-impaired flags and commentary
  detection. You check each suggestion before anything is changed.
- **Renaming.** Builds Plex and Jellyfin style names, such as `Some Movie (2015).mkv`, from the
  file's own name, or matched automatically against a metadata database with Pro.
- **Compress.** Re-encodes with presets, and lets you test a short sample before a full encode.
- **Queue.** Runs the jobs one after another while you get on with something else.
- **Tools.** Subtitle sync, converting image subtitles to text, and a library health check.

ffmpeg, MKVToolNix and Tesseract ship inside the download, so there is nothing else to install.

## Free and Pro

FileVerdict is free. Everything you do with your own files is in the free version, with no key
and no account. [Pro](https://fileverdict.com/pricing/) adds automatic name matching from online
metadata and cast-based commentary detection, as a one-time purchase.

## What's in each release

Besides the installer and the AppImage, each release carries:

| File | What it is |
|---|---|
| `*.sig`, `latest.json` | Update signatures and the update manifest the app reads. |
| `SHA256SUMS.txt`, `SHA256SUMS-linux.txt` | SHA-256 checksums of the Windows installer and the Linux AppImage. |
| `*-source.tar.*`, `*-library-sources.tar` | Source code of the bundled open-source tools (ffmpeg, MKVToolNix and their libraries), as their GPL and LGPL licences require. |

To check a download on Linux:

```bash
sha256sum --ignore-missing -c SHA256SUMS-linux.txt
```

On Windows, in PowerShell, compare the result with the hash in `SHA256SUMS.txt`:

```powershell
Get-FileHash .\File.Verdict_*_x64-setup.exe
```

## About this repository

This repository holds release builds only; FileVerdict's source code is not published here.
Please don't open issues for help: email [support@fileverdict.com](mailto:support@fileverdict.com)
or see the [support page](https://fileverdict.com/support/). To report a security problem, email
the same address.

<p align="center">
  <sub><a href="https://fileverdict.com/privacy-policy/">Privacy</a> · <a href="https://fileverdict.com/terms/">Terms</a></sub>
</p>
