# TdF 3D · desktop app releases

Installers for **TdF 3D**, a 3D route explorer for the 2026 Tour de France, for Windows and macOS.
This repository holds the release downloads only; the app checks it for updates every time it starts.

## Download

Go to the [latest release](https://github.com/magex9/cycling-releases/releases/latest) and download:

| Platform | File |
| --- | --- |
| Windows 10/11 | `TdF.3D_<version>_x64-setup.exe` |
| macOS 11+ (Apple silicon and Intel) | `TdF.3D_<version>_universal.dmg` |

## First launch

The app isn't signed with a paid certificate yet, so both systems warn the first time:

- **Windows:** "Windows protected your PC" → **More info** → **Run anyway**.
- **macOS:** drag **TdF 3D** to Applications and open it. When macOS says it can't verify the developer, open
  **System Settings → Privacy & Security**, scroll down and click **Open Anyway**.
  If macOS instead says the app "is damaged", run this once in Terminal, then open it again:

  ```sh
  xattr -dr com.apple.quarantine "/Applications/TdF 3D.app"
  ```

## Updates

Each time the app starts it checks this repository. When a newer version is available it asks before installing,
then restarts. Updates are signed, and the app refuses any update that isn't.

The app needs an internet connection for the map, terrain and fonts.
