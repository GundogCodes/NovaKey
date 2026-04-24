# NovaKey

NovaKey is a keyboard-first macOS productivity app that combines a hotkey launcher with a tiling window manager.

The goal is simple: make a Mac feel faster, more intentional, and more controllable from the keyboard without losing native macOS behavior. NovaKey lets you launch apps and websites instantly, rearrange windows with a single key combo, move through virtual workspaces on a laptop, and keep larger multi-display setups neatly tiled.

NovaKey ships in two editions:

| Edition | Where to get it | Focus |
| --- | --- | --- |
| **NovaKey** | [Mac App Store](https://apps.apple.com/ca/app/novakey/id6751394828?mt=12) | Hotkey launcher — sandboxed, App-Store-safe subset |
| **NovaKey Pro** | [Gumroad — $9.99](https://gunwithish.gumroad.com/l/novakeypro) | Full experience: tiling window manager, virtual workspaces, multi-display mode |

Landing page: https://gundogcodes.github.io/NovaKey/

This repository tracks the full feature set that powers both editions.

## Why NovaKey Pro (vs. yabai, Amethyst, AeroSpace, HyprMac)

The open-source macOS tilers are excellent tools — for users who enjoy editing config files. NovaKey Pro is for everyone else.

- **All in one app.** Hotkey launcher, auto-tiling, ten virtual workspaces, and cross-Mac sync in a single coherent app. No stitching together three or four tools.
- **Zero config to start.** Sensible defaults, a real Preferences window, and no `brew services` or YAML. Grant Accessibility once and you're tiling.
- **Native feel.** Fullscreen, Mission Control, minimize, and multi-display behavior are all respected. NovaKey works with macOS instead of pretending it's Linux.
- **Signed, notarized, supported.** Apple-notarized DMG, one-time $9.99, and a human to email when something breaks.

If you want a Linux-style WM on your Mac and enjoy tuning dotfiles, yabai or AeroSpace are the right fit. If you want the power-user layer without the homework, that's NovaKey Pro.

## What NovaKey Does

- Launch apps and websites from custom hotkeys.
- Provide a one-handed Caps Lock leader layer for core actions.
- Automatically tile windows across one or more displays.
- Support manual retile and layout cycling when the user wants to intervene.
- Offer single-display virtual workspaces with app-to-workspace assignment and overflow rules.
- Detect monitor changes and switch between workspace mode and multi-display tiling mode automatically.
- Give users a native Preferences window for setup, shortcuts, diagnostics, import/export, and recovery tools.

## Core Experience

### 1. Hotkey Launcher

NovaKey can launch one or more applications, open websites, and focus running apps from configurable keyboard shortcuts. This is the fast-entry side of the product and works independently from the tiling system.

### 2. Caps Lock Leader System

NovaKey turns Caps Lock into a dual-role key:

- Tap `Caps Lock` normally to toggle caps lock.
- Hold `Caps Lock` as a leader key for window-management actions.

Default leader actions:

- `Caps + Q` cycles tiled window positions.
- `Caps + A` manually tiles the current display or workspace.
- `Caps + Space` opens or closes Preferences.
- `Caps + 1..0` switches workspaces on single-display setups.
- `Caps + Shift + 1..0` moves the active window to a workspace.
- `Caps + Left` / `Caps + Right` switches adjacent workspaces on a single display.
- `Caps + Left` / `Caps + Right` moves the focused window between displays when multiple monitors are connected.
- `Caps + letter` can be assigned to user-defined hotkeys.

Legacy shortcuts are still supported for compatibility:

- `Control + Option + P` cycles windows.
- `Control + Option + L` tiles windows.
- `Control + Option + M` opens Preferences.

### 3. Auto-Tiling Window Manager

NovaKey monitors window changes and tiles them automatically.

Behavior highlights:

- Up to 4 windows are tiled cleanly on a display.
- When more than 4 windows exist on one display, the newest window stays floating on top as overflow.
- Manual tiling is always available when the user wants to reset the layout.
- Window cycling lets users rotate the tiled positions without breaking the workspace assignment.
- Multi-display tiling happens per display, not across the full desktop as one giant canvas.

### 4. Single-Display Workspaces

When only one display is connected, NovaKey can enable workspace mode.

Workspace behavior:

- 10 keyboard-addressable workspaces (`1` through `0`).
- Apps are assigned to the current workspace.
- If a workspace is full, newly opened apps overflow into the next workspace with room.
- Empty workspaces intentionally show the desktop/home screen instead of glitching between windows.
- Minimized apps free up a slot in the workspace.
- Restored apps reopen onto the current workspace, following the same overflow rules if needed.
- Cycled layouts are preserved when leaving and returning to a workspace.
- Fullscreen windows are handled as a special case so exiting fullscreen returns the user to the original workspace context cleanly.

### 5. Multi-Display Mode

When NovaKey detects more than one connected display, it disables workspaces automatically and switches to multi-display tiling rules.

Multi-display behavior:

- Each display is tiled independently.
- Moving a window from one display to another triggers a retile on both displays.
- Dragging windows across displays is supported.
- Caps-based left/right display movement is supported for the focused window.
- If a second monitor is connected, workspace mode is turned off automatically.
- If the setup returns to a single display, workspace mode can be restored automatically.

## Product Principles

- Keyboard first: the main workflows should feel faster from keys than from the mouse.
- Native feeling: the app tries to work with macOS instead of pretending macOS is Linux.
- Minimal friction: one-handed shortcuts, clear defaults, and visible setup state.
- Robust state handling: workspace assignment, minimized windows, fullscreen transitions, and monitor changes should not destroy layout state.

## Preferences and User Controls

NovaKey includes a native Preferences window for:

- hotkey management
- workspace controls
- setup and permission guidance
- usage stats
- import/export of configuration
- diagnostics and recovery tools

The app also includes a menu bar interface so core actions are always reachable even when the user forgets a shortcut.

## Permissions

NovaKey uses a few macOS permissions because it performs real window-management work:

- Accessibility: required to move, resize, hide, restore, and inspect windows.
- Screen Recording: used only for temporary transition snapshots that smooth workspace switching. NovaKey does not record, save, or upload screen content.
- Apple Events: used to focus or open apps when a configured hotkey targets them.

## Editions

NovaKey is available in two editions so users can pick what fits their setup and comfort level.

### NovaKey (Mac App Store)

- Download: [apps.apple.com/ca/app/novakey](https://apps.apple.com/ca/app/novakey/id6751394828?mt=12)
- Sandboxed, App-Store-reviewed build.
- Focused on the hotkey launcher and Caps Lock leader system.
- Best for users who want a lightweight, App-Store-safe install with no permission setup beyond standard macOS prompts.

### NovaKey Pro (Direct Download)

- Buy: [gunwithish.gumroad.com/l/novakeypro](https://gunwithish.gumroad.com/l/novakeypro) — $9.99, one-time.
- Signed and notarized DMG.
- Full experience: auto-tiling window manager, ten virtual workspaces, multi-display mode, manual retile and cycle, import/export, diagnostics.
- Requires macOS 13 Ventura or later. Apple Silicon + Intel supported.
- Unlocks features that cannot ship through the sandboxed App Store build because they rely on deeper window-management APIs.

This repository currently contains the full feature set that powers both editions.

## Tech Stack

- Swift
- SwiftUI
- AppKit
- macOS Accessibility APIs
- ScreenCaptureKit
- Carbon hotkeys where appropriate

## Development

Open the project in Xcode:

```sh
open HyperKey.xcodeproj
```

Or build from the command line:

```sh
xcodebuild -project HyperKey.xcodeproj -scheme HyperKey build
```

## Direct Distribution

For direct-download packaging, a DMG build script is included:

```sh
Scripts/build_dmg.sh
```

For local unsigned smoke testing:

```sh
Scripts/build_dmg.sh --unsigned
```

See [Docs/DirectDistribution.md](Docs/DirectDistribution.md) for the full packaging and notarization flow.
