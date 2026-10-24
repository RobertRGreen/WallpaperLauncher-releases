# RGLauncher Windows Edition - releases

Downloads for **RGLauncher Windows Edition**, a desktop-style game launcher for Windows that sits on top of your
wallpaper (including live Wallpaper Engine wallpapers). It scans Steam, Epic, GOG, EA, Ubisoft, Battle.net, Riot and
Xbox, shows your games on a 3D carousel, and keeps running in the background.

Source code is private; this repo only hosts built releases. **Current beta: [0.2.0-beta.1](../../releases/tag/v0.2.0-beta.1).**

## Get the beta

1. Open the [latest release](../../releases/latest) (or the [beta](../../releases/tag/v0.2.0-beta.1)) and download
   **`WallpaperLauncher.exe`**.
2. Optional but recommended: check the download is intact. In PowerShell:
   ```powershell
   Get-FileHash .\WallpaperLauncher.exe -Algorithm SHA256
   ```
   The hash must match the `SHA256` shown next to the file on the release page (beta.1:
   `4b6777ae9677bcabea13847e7d2b5accdb676c964caeba4598562eae2f4c3a95`).
3. Double-click it and accept the install prompt. It installs for your account only; no admin rights are needed.
4. Windows SmartScreen may say "unknown publisher" because the app is not code-signed yet. Choose
   **More info > Run anyway**.

Requires Windows 10 (1809) or Windows 11, 64-bit. Nothing else to install.

Beta builds are also listed at <https://robertrgreen.online/betas>.

## Trial and license

Free for 7 days, then the launcher locks until you enter a license key in **Settings > License**. Beta testers get a
free key: email [robert@robertrgreen.online](mailto:robert@robertrgreen.online) and include the machine ID shown in
Settings > License if you want the key locked to your PC.

## Updates and channels

The app updates itself: **Settings > Updates**. Releases marked *Pre-release* are the **beta** channel; the rest are
**stable**. A version like `0.2.0-beta.1` is beta, `0.2.0` is stable. Beta users also receive stable releases that are
newer than their beta, so they are never stranded. You can switch channels in Settings > Updates.

## What is in beta 1

- Four design languages: Cyberpunk, Glass, Terminal, Minimal
- Animated backdrops (particles, aurora, digital rain, synthwave grid, stars) with mouse parallax; they pause when a
  game or maximized window covers the screen
- Settings window and tray icon; per-monitor on/off and Full/Ambient layout
- Scans Steam, Epic, GOG, EA, Ubisoft, Battle.net, Riot and Xbox libraries
- Stays put through Show Desktop (Win+D); real desktop icons stay hidden while it runs
- Watchdog: restarts itself within a minute if it ever dies
- Built-in updater on the stable or beta channel

## Known rough edges (beta 1)

- Only tested on one machine so far, and multi-monitor handling has only been tested on a single display. Please
  report anything odd.
- Not code-signed yet (see SmartScreen above).

## Reporting a problem

[Open an issue](../../issues/new) or email the address above. Helpful details: your Windows version, how many monitors,
which game stores you use, what you did, and what happened instead. If the launcher crashed, attach
`%APPDATA%\WallpaperLauncher\crash.log` (review it first; it is a plain text file).

If your desktop icons stay hidden after removing the app, run `WallpaperLauncher.exe --show-icons` once.

## Uninstall

Windows Settings > Apps > RGLauncher Windows Edition. Your settings, crash log and license are kept in
`%APPDATA%\WallpaperLauncher`; delete that folder for a completely clean removal.
