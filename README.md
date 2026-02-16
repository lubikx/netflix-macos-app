# Netflix for macOS

A lightweight floating video player for [netflix.com](https://www.netflix.com). Sits on top of your workspace like a PiP window.

> **Disclaimer:** Netflix is a trademark of [Netflix, Inc](https://www.netflix.com). This app is not affiliated with, endorsed by, or officially connected to Netflix, Inc. in any way.

## Features

- **Snap small** — video fills the window, Netflix UI hidden, window floats on top
- **Go big** — full Netflix experience, normal window behavior
- Press **⌘ Enter** (or double-click the title bar) to toggle between the two
- Auto-updates via Sparkle

**Requires macOS 14 (Sonoma) or later.**

## Install

Paste in Terminal:

```
curl -sL https://raw.githubusercontent.com/lubikx/netflix-macos-app/main/install.sh | bash
```

## Manual Installation

1. Download `Netflix.dmg` from the [Releases](https://github.com/lubikx/netflix-macos-app/releases) page
2. Open the DMG and drag **Netflix.app** to `/Applications`
3. Open Finder → Applications (⌘ Shift A)
4. **Right-click** Netflix → **Open** → click **Open** in the dialog

> **Why right-click → Open?** The app isn't signed with an Apple Developer certificate (it's a small personal tool — the $99/year fee isn't worth it). macOS blocks unsigned apps by default, but right-clicking → Open bypasses this once. After that, it launches normally. The install script handles this automatically.

## First Launch — DRM Keychain Prompt

On the first video playback, macOS will ask for permission to access **"Netflix WebCrypto Master Key"** in your keychain. This is the FairPlay DRM key that Netflix uses for video playback.

Click **Always Allow** and enter your login keychain password. This is a one-time prompt — it won't ask again.

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| ⌘ Enter | Snap / Maximize |
| ⌘ T | Toggle always on top |
| ⌘ R | Reload page |
| ⌃ ⌘ F | Full Screen |

When the window is **small** (less than half your screen), it automatically floats on top and shows just the video. When **big**, it behaves like a normal window with the full Netflix UI.

## Troubleshooting

If the app misbehaves, reset all settings by running:

```
defaults delete eu.apptory.netflix
```

Then relaunch the app. This clears saved window positions, welcome screen state, and all other preferences.

Alternatively, just re-run the install script — it resets settings automatically.

## Feedback & Support

Have a question, suggestion, or found a bug? Head over to [Discussions](https://github.com/lubikx/netflix-macos-app/discussions).
