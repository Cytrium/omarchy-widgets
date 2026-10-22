# OmaLauncher Locket Widget (`60-locket.owl`)

A native [OmaLauncher](https://github.com/SimonSchubert/omarchy-widgets) home-screen widget and full-screen feed view for **Locket**, written in OWL.

## Features

- **Live Home-Screen Tile**: Displays the latest photo moment from your friends with sender avatar, relative timestamp, quick moment cycling (`1/N ›`), and Locket-style frosted caption pill.
- **Instant Notification Sync**: Automatically detects incoming notifications from the official Locket Android app (`com.locket.Locket`) and syncs new moments immediately.
- **Multi-Friend Feed**: Chains `getLatestMomentV2` with `excluded_users` to gather the latest moments across your friends list and resolves author profiles (`fetchUserV2`).
- **Emoji Reactions & Direct Chat Replies**: React with `💛 ❤️ 🔥 😍 😂 💕` (`reactToMoment`) or send text replies directly to Locket chat (`sendChatMessageV2`).
- **Flexible Sign-In**: Supports signing in on-device via Email & Password, Phone & Password, or Firebase `refreshToken`, with automatic token renewal.
- **Privacy First**: No credentials, tokens, emails, or user IDs are hardcoded in the widget source. Runtime session state is managed locally by OmaLauncher.

## Installation

1. Copy [`60-locket.owl`](./60-locket.owl) into your OmaLauncher widgets directory:
   ```bash
   cp 60-locket.owl ~/.config/omalauncher/widgets/60-locket.owl
   ```
2. Verify the widget with `owl-check`:
   ```bash
   owl-check ~/.config/omalauncher/widgets/60-locket.owl
   ```
3. Tap the **Locket** tile on your home screen to open the full-screen view and sign in under the **sign in / account** tab.

## License

MIT
