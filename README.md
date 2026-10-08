# comb-releases

Comb is a Windows file search launcher that stays in the system tray and opens with a hotkey (default Alt+Space). It searches file names and contents.

This repository holds only Comb's release files: the Windows installer (`Comb-Setup-<version>.exe`) and `update.json` for each release. It does not contain source code; the source is kept in a separate repository.

## Download and install

To install Comb, download `Comb-Setup-<version>.exe` from the [Releases](https://github.com/luisdonginseo/comb-releases/releases) page of this repository and run it. It installs for the current user only and does not need administrator rights.

The installer is not code-signed yet, so Windows SmartScreen may show a warning on the first manual install. Automatic updates do not show this warning.

## Requirements

Windows 10 version 1809 or later, or Windows 11, 64-bit (x64).

## Automatic updates

An installed Comb checks this repository's latest release once, 3 minutes after it starts. If a newer version exists, it downloads it quietly and installs it the next time Comb starts (the tray menu also offers "Restart to update"). Automatic updates can be turned off in Comb's settings ("Install updates automatically"); when off, Comb does not use the network for updates at all.

`update.json` is signed (ECDSA P-256) and contains the installer's SHA-256 hash. Comb installs an update only if the signature and the hash both match. If a new version fails to start, Comb goes back to the previous version.

## Uninstall

Settings > Apps > Installed apps > Comb > Uninstall. Downloaded update files are removed with it.
