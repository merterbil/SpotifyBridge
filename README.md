 # SpotifyBridge

SpotifyBridge brings live Spotify playback data and lyrics into TouchDesigner.

## Download

SpotifyBridge is free to download:

[**Download SpotifyBridge v2.6.1 (.tox)**](https://raw.githubusercontent.com/merterbil/SpotifyBridge/main/releases/SpotifyBridgeV2.6.1.tox)

Versioned builds are stored in the repository's [releases folder](https://github.com/merterbil/SpotifyBridge/tree/main/releases).

## How to Use

1. Download SpotifyBridgeV2.6.1.tox.
2. Open a fresh TouchDesigner project and drag the .tox into the network.
3. Open the component's **Spotify Setup** parameter page.
4. Enter your own Spotify **Client ID** and **Client Secret**.
5. Press **Authenticate with Spotify** and complete authorization in your browser.
6. Start Spotify playback. SpotifyBridge will expose the current playback data, lyrics, and prepared public output operators inside the component.

## What's New in v2.6.1

- Added **Lyric Offset (ms)** to **Output Control** so you can shift lyrics earlier or later to match your playback. Positive values delay the lyrics; negative values advance them.
- Added **Block Unsynced Lyrics** at the bottom of **Output Control**. When enabled, lyrics without synchronized timing are replaced with **Unsynced Lyrics Found** in the lyric outputs. Turn it off to display the unsynced lyrics again. Synchronized lyrics are unaffected.

## Authentication Cache

After successful authorization, SpotifyBridge stores its Spotify authentication cache in the TouchDesigner project's VFS so the session can refresh without requiring a new login each time.

Press **Disconnect / Clear Cache** on the **Spotify Setup** page whenever you want to disconnect and delete that stored VFS cache. Use this before sharing or exporting a project that has been authenticated.

## Compatibility

The current release was built and tested with TouchDesigner 2025.33230 on macOS.

A TouchDesigner 2025-exported .tox should not be treated as TouchDesigner 2023 compatible. A separate TD 2023 export and independent Windows/macOS testing are required before claiming broader compatibility.

## Security

Release builds must never contain Spotify access tokens, refresh tokens, client secrets, populated cache files, or user information. Users enter their own Spotify credentials locally.

## Support

Use [GitHub Issues](https://github.com/merterbil/SpotifyBridge/issues) for reproducible bugs and documentation problems. Do not post Spotify credentials, tokens, or cache files.

The downloadable .tox is free to download and use. No open-source license has been declared for its internal code unless explicitly stated.
