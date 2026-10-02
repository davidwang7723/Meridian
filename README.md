# Meridian

A schedule app for macOS: a week planner, month calendar and timeline, reminders and alarms, a Pomodoro timer, tasks and homework, desktop widgets, a screen saver, and Sol, an AI assistant that can edit your schedule by text or voice. Available in English, 简体中文, हिन्दी, Español, العربية, Français and বাংলা.

For a full tour of what it does, see [whatismeridian.md](whatismeridian.md). For every version's changes, see [CHANGELOG.md](CHANGELOG.md).

This repository holds releases and documentation only. The source code is not public.

## Download

Get the latest DMG from [Releases](../../releases/latest).

## Install

1. Open the DMG and drag Meridian onto the Applications folder.
2. The first time you open it, macOS says the developer cannot be verified. Meridian is signed, but not notarised by Apple, so this is expected. Open System Settings, go to Privacy & Security, scroll to the bottom and click **Open Anyway** next to Meridian.
3. If that button does not appear, run this in Terminal, then open Meridian again:

   ```
   xattr -dr com.apple.quarantine /Applications/Meridian.app
   ```

## Requirements

- macOS 15 Sequoia or newer
- Apple Silicon (M1 or later) from v1.20.0 on. Older releases are Universal and also run on Intel Macs.
