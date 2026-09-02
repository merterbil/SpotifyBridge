 # SpotifyBridge

SpotifyBridge brings live Spotify playback data and lyrics into TouchDesigner.

## Download

SpotifyBridge is free to download:

[**Download SpotifyBridge v2.6.0 (.tox)**](https://raw.githubusercontent.com/merterbil/SpotifyBridge/main/releases/SpotifyBridgeV2.6.0.tox)

Versioned builds are stored in the repository's [releases folder](https://github.com/merterbil/SpotifyBridge/tree/main/releases).

## How to Use

1. Download SpotifyBridgeV2.6.0.tox.
2. Open a fresh TouchDesigner project and drag the .tox into the network.
3. Open the component's **Spotify Setup** parameter page.
4. Enter your own Spotify **Client ID** and **Client Secret**.
5. Press **Authenticate with Spotify** and complete authorization in your browser.
6. Start Spotify playback. SpotifyBridge will expose the current playback data, lyrics, and prepared public output operators inside the component.

## What's New in v2.6.0

- Added an optional **Three-Line Lyrics View** that keeps the previous, current, and next lyric lines visible together.
- Added smooth animated line transitions for a more polished Spotify-style lyric display.
- Added karaoke highlighting for the active line using the synchronized lyric timing data.
- Fixed Spotify OAuth refresh caching so authentication data remains inside the TouchDesigner VFS instead of creating a .cache file beside the project.

## Authentication Cache

After successful authorization, SpotifyBridge stores its Spotify authentication cache in the TouchDesigner project's VFS so the session can refresh without requiring a new login each time.

Press **Disconnect / Clear Cache** on the **Spotify Setup** page whenever you want to disconnect and delete that stored VFS cache. Use this before sharing or exporting a project that has been authenticated.

## Compatibility

The current release was built and tested with TouchDesigner 2025.33070 on macOS.

A TouchDesigner 2025-exported .tox should not be treated as TouchDesigner 2023 compatible. A separate TD 2023 export and independent Windows/macOS testing are required before claiming broader compatibility.

## Security

Release builds must never contain Spotify access tokens, refresh tokens, client secrets, populated cache files, or user information. Users enter their own Spotify credentials locally.

## Support

Use [GitHub Issues](https://github.com/merterbil/SpotifyBridge/issues) for reproducible bugs and documentation problems. Do not post Spotify credentials, tokens, or cache files.

You can also follow and support my TouchDesigner work on [Patreon — merderbil](https://www.patreon.com/merderbil).

The downloadable .tox is free to download and use. No open-source license has been declared for its internal code unless explicitly stated.

